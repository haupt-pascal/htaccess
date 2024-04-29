## Deactivate eTags
``` bash
<IfModule mod_headers.c>
    Header unset ETag
</IfModule>
FileETag None
```
