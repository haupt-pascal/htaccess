## Compress Text Files with Gzip/Deflate
This is used to compress text files like HTML, CSS, JavaScript, XML, JSON, and SVG files. This is done to reduce the size of the files and speed up the loading time of the website.

``` bash
<IfModule mod_deflate.c>
    <IfModule mod_setenvif.c>
        <IfModule mod_headers.c>
            SetEnvIfNoCase Request_URI \.(?:gif|jpe?g|png)$ no-gzip dont-vary
            SetEnvIfNoCase Request_URI \.(?:exe|t?gz|zip|bz2|sit|rar)$ no-gzip dont-vary
            SetEnvIfNoCase Request_URI \.pdf$ no-gzip dont-vary
        </IfModule>

        <IfModule mod_filter.c>
            AddOutputFilterByType DEFLATE application/atom+xml \
                                        application/javascript \
                                        application/json \
                                        application/ld+json \
                                        application/manifest+json \
                                        application/rdf+xml \
                                        application/rss+xml \
                                        application/schema+json \
                                        application/vnd.geo+json \
                                        application/vnd.ms-fontobject \
                                        application/x-font-ttf \
                                        application/x-javascript \
                                        application/x-web-app-manifest+json \
                                        application/xhtml+xml \
                                        application/xml \
                                        font/eot \
                                        font/opentype \
                                        image/bmp \
                                        image/svg+xml \
                                        image/vnd.microsoft.icon \
                                        image/x-icon \
                                        text/cache-manifest \
                                        text/css \
                                        text/html \
                                        text/javascript \
                                        text/plain \
                                        text/vcard \
                                        text/vnd.rim.location.xloc \
                                        text/vtt \
                                        text/x-component \
                                        text/x-cross-domain-policy \
                                        text/xml
    </IfModule>
</IfModule>
```
