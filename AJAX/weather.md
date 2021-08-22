## Weather
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/snippets-template.md) 
```php
// Class & methods
class weather {
  // Register scripts and pass data to them
  static function setup_data() {
    wp_register_script(
      'weather',
      get_theme_file_uri('/assets/js/weather.js'),
      array('jquery')
    );

    wp_enqueue_script('weather');

    wp_localize_script(
      'weather',
      'Weather',
      array('ajaxurl' =>  admin_url('admin-ajax.php'))
    );
  }

  // Get data from API
  static function get_data() {
    // Request data
    $url = 'https://api.weatherbit.io/v2.0/current';
    $api_key = 'YOUR_API_KEY';
    $lat = 'YOUR_LAT';
    $lon = 'YOUR_LON';

    // Set up the transient
    $transient = get_transient('current_weather');
    if(!empty($transient)) {
      // Return transient 
      wp_send_json_success($transient);
    } else {
      // Get data from API
      $req_url = $url . '?lat=' . $lat . '&lon=' . $lon . '&key=' . $api_key;
      $data = wp_remote_get($req_url);

      // Set new transient for 1 hour
      set_transient('current_weather', $data, HOUR_IN_SECONDS);

      // Return data
      wp_send_json_success($data);
    }
  }
}
```
```php
// Hook into Wordpress
add_action('init', 'Weather::setup_data');
add_action('wp_ajax_weather', 'Weather::get_data');
add_action('wp_ajax_nopriv_weather', 'Weather::get_data');
```

```js
//Javascript
!function($) {
  $(document).ready(function() {
    var forecastContainer;
    forecastContainer = $('.forecast');

    if(Weather && forecastContainer.length > 0) {
      $.ajax({
        url: Weather.ajaxurl,
        data: {
          action: 'weather'
        }
      })
      .done(function(resp) {
        var data, icon, weather, temp, iconContainer, iconSrc, tempContainer;

        data = JSON.parse(resp.data.body);
        iconContainer = $('.forecast__icon img');
        iconSrc = iconContainer.attr('src');
        tempContainer = $('.forecast__temp-container');

        if(data) {
          // Get values
          icon = data.data[0].weather.icon;
          weather = data.data[0].weather.description;
          temp = data.data[0].temp;

          // Generate content
          iconContainer.attr('src', iconSrc + icon + '.png');
          iconContainer.attr('alt', weather);
          tempContainer.html(temp + ' &deg;C');

        }
      })
      .fail(function(err) {
        console.error('Failed to fetch data: ' + err);
      });
    }

  }); // .ready
}
```