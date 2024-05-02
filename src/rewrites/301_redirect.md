## 301 Redirect to specific website
This is used to redirect a website to another website. This is useful when you have a website that is no longer in use and you want to redirect the traffic to another website.

```bash
RewriteEngine On
RewriteRule ^(.*)$ https://DOMAIN.OVER.HERE/$1 [L,R=301]
```
