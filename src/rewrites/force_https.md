## Force HTTPS secure connection
This is used to force the server to use HTTPS secure connection. This is useful when you want to make sure that all the connections to your server are secure.

```bash
RewriteEngine on
RewriteCond %{HTTPS} !on
RewriteRule (.*) https://%{HTTP_HOST}%{REQUEST_URI}
```
