# Minimal Docker PHP container.

- Runs php-fpm on port 9000
- Logs to stdout instead of a file
- Easy to link to from Nginx, container named php
    include fastcgi_params;
    fastcgi_param SCRIPT_FILENAME $document_root$script;
    fastcgi_intercept_errors on;
    fastcgi_pass php:9000;
