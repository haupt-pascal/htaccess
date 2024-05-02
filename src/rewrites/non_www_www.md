## Redirect non-www to www
This is used to redirect all non-www requests to www. This is useful for SEO and to avoid duplicate content.

```bash
RewriteEngine On
RewriteCond %{HTTP_HOST} !^www\. [NC]
RewriteRule ^(.*)$ https://www.%{HTTP_HOST}/$1 [R=301,L]
```
