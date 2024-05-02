## Deny all access to a directory
This is used to deny all access to a directory. This is useful when you want to deny access to a directory and its contents. This can be done by adding a `.htaccess` file in the directory with the following content.

```apache

``` bash
# For Apache 2.2
Order Deny,Allow
Deny from all

# For Apache 2.4
Require all denied
```
