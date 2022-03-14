Create docker network for mysql container:
<br><code>docker network create mysql-net</code>

Single line command to create mysql container with network:
<code>docker run -d --name mysql --network mysql-net -p 3306:3306 -v $PWD/db_data:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=root -e MYSQL_USER=admin -e MYSQL_PASSWORD=admin mysql:5.7</code>
