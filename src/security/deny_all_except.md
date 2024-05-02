## Deny all except
This is used to deny all access to a directory except for a specific IP address. This is useful for restricting access to a directory to a specific IP address.

``` bash
# Apache 2.2
Order Deny,Allow
Deny from all
Allow from X.X.X.X

# Apache 2.4
Require all denied
Require ip X.X.X.X
```
