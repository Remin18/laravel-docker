docker-compose exec php chown -R www-data:www-data /var/www
docker-compose exec php chmod -R 755 /var/www/storage
docker-compose exec php php artisan migrate