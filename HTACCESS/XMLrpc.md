## XMLrpc
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/HTACCESS/XMLrpc.md) 
```
# Block WordPress xmlrpc.php requests
<Files xmlrpc.php>

order deny,allow

deny from all

</Files>
```