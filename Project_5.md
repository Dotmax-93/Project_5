The first thing is to create 2 different servers on AWS namely; mysql server and mysql client

`sudo apt install mysql-server` [^3]
[^3]: This command is done to install mysql for our server

`sudo apt install mysql-client` [^6]
[^6]:  This command is done to install mysql for our client

The next step is to creat a new security group(inbound rules) to port 3306 on our server that allows connection only from the client

The next step is to configure our mysql server to accept connection from remote host

`sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf`

[^13]: Change the binding address to 0.0.0.0

`sudo mysql`[^17]
[^17]:This command is run on the server to create 

The next step is to creat a database on our server

`sudo systemctl restart mysql`

On mysql-client

`sudo mysql -u root_user -h private IP address of the server -p`

Create Database on mysql-client

Our database created on the server will be replicated on the client for successful connection
