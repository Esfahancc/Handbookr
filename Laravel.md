# Composer
```
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php composer-setup.php
rm -rf composer-setup.php
mv composer.phar /usr/local/bin/composer
```

# Redis
```
yum install -y redis
systemctl restart redis
systemctl enable redis
```

# Alias
```
printf "\n alias nr='npm run'" >> ~/.bashrc
printf "\n alias pa='php artisan'" >> ~/.bashrc
printf "\n alias pa-deploy='pa optimize:clear; pa optimize'" >> ~/.bashrc
```

# Create
```
composer create-project --prefer-dist laravel/laravel blog
```

# Deploy
```
composer install --optimize-autoloader --no-dev
composer run-script "post-root-package-install"
composer run-script "post-create-project-cmd"
composer run-script "post-autoload-dump"
npm install --production
npm audit fix
npm run prod
php artisan storage:link
chmod -R 755 storage
mkdir storage/app/ssr
chmod -R 777 storage/app/ssr
```

```
vim .env
```

```
php artisan migrate:fresh --seed
```

# Cron
```
yum install -y crontab
```

```
crontab -e
```

```
@reboot   cd <dir> && nohup php artisan queue:work --sleep=3 >> /dev/null 2>&1 &
* * * * *   cd <dir> && nohup php artisan schedule:run >> /dev/null 2>&1
```