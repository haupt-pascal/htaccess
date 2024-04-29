## Password protect a directory

At first you need to create a `.htpasswd` file. This file will store the username and password. You can create this file in the root directory of your website.

``` bash
htpasswd -c .htpasswd <username>

```

You will be prompted to enter and confirm the password for the user. If you want to add more users to the file, you can omit the `-c` flag.

``` bash
htpasswd .htpasswd <username>
```

``` bash 
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /path/to/.htpasswd
Require valid-user
```
