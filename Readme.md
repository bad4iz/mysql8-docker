docker run -ti --rm --name mysql-server -v $(pwd)/data/:/var/lib/mysql -d -p 3308:3306 -e MYSQL_ROOT_PASSWORD=pass mysql:8

## phpadminer
docker run -d -ti --rm --name my-adminer --link mysql-server:db -p 9999:8080 adminer


## phpmyadmin
docker run --name myadmin -d -ti --rm --link mysql-server:db -p 9080:80 phpmyadmin/phpmyadmin


/var/lib/mysql

mysql -u root -p pass geo < /var/lib/mysql/geo.sql


узнать ip
ip addr show

> елси не работает удалить содержимое папки data
