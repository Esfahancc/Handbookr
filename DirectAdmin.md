# DirectAdmin
```
wget http://www.directadmin.com/setup.sh
chmod 755 setup.sh
./setup.sh
```

# Ports
```
firewall-cmd --permanent --zone=public  --add-port=2222/tcp
firewall-cmd --reload
```

# DirectAdmin config
```
vim /usr/local/directadmin/conf/directadmin.conf
```

```
systemctl restart directadmin
```

# PHP config
```
vim /usr/local/lib/php.ini
```

```
# disable_functions = proc_close,proc_open
```