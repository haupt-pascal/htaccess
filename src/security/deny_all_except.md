``` bash
# Apache 2.2
Order Deny,Allow
Deny from all
Allow from X.X.X.X

# Apache 2.4
Require all denied
Require ip X.X.X.X
```
