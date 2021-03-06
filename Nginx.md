# Install
```
yum install -y nginx

systemctl start nginx
systemctl enable nginx
```

# Disable default
```
vim /etc/nginx/nginx.conf
```

```
# listen       80 default_server;
# listen       [::]:80 default_server;
```

# Laravel config
```
mkdir -p /var/www/laravel
```

```
vim /etc/nginx/conf.d/laravel.conf
```

```
server {
        listen       80 default_server;
        listen       [::]:80 default_server;
    # Log files for debugging
        access_log /var/log/nginx/laravel-access.log;
        error_log /var/log/nginx/laravel-error.log;
    # Webroot directory
        root /var/www/laravel/public;
        index index.php index.html index.htm;
    # Domain name
        server_name  _;
    # Laravel config
        location / {
                try_files $uri $uri/ /index.php?$query_string;
        }
    # PHP-FPM config
        location ~ \.php$ {
                try_files $uri =404;
                fastcgi_split_path_info ^(.+\.php)(/.+)$;
                fastcgi_pass unix:/run/php-fpm/php-fpm.sock;
                fastcgi_index index.php;
                fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
                include fastcgi_params;
        }
}
```

```
nginx -t
systemctl reload nginx
systemctl restart nginx
```
