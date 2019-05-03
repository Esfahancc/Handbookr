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