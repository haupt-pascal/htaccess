## Deactivate eTags
This is used to deactivate eTags in the Apache server. This is useful to avoid the browser from caching the files. This is useful when the files are updated frequently and the browser is caching the old files.

``` bash
<IfModule mod_headers.c>
    Header unset ETag
</IfModule>
FileETag None
```
