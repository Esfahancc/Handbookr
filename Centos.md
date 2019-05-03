# Repositories
```
yum install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
yum install -y http://rpms.remirepo.net/enterprise/remi-release-7.rpm
yum install -y yum-utils
yum-config-manager --enable remi-php72
yum update
```

# Packages
```
yum install -y wget vim htop
```

# Ports
```
firewall-cmd --permanent --zone=public --add-service=http
firewall-cmd --permanent --zone=public --add-service=https
firewall-cmd --reload
```

# SSH config
```
vim /etc/ssh/sshd_config
```

```
systemctl restart sshd
```

# PHP config
```
vim /etc/php.ini
```

```
cgi.fix_pathinfo=0
```

# PHP-FPM config
```
vim /etc/php-fpm.d/www.conf
```

```
user = nginx
group = nginx

listen = /run/php-fpm/php-fpm.sock

listen.owner = nginx
listen.group = nginx
listen.mode  = 0660

env[HOSTNAME] = $HOSTNAME
env[PATH] = /usr/local/bin:/usr/bin:/bin
env[TMP] = /tmp
env[TMPDIR] = /tmp
env[TEMP] = /tmp
```

```
systemctl restart php-fpm
```