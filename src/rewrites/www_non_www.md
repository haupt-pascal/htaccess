## Redirecting www to non-www
This is used to redirect all requests from www to non-www. This is useful for SEO purposes.

```bash
RewriteEngine On
RewriteBase /
RewriteCond %{HTTP_HOST} ^www\.(.*)$ [NC]
RewriteRule ^(.*)$ https://%1/$1 [R=301,L]
```
