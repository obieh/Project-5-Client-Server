# Client-Server refers to an architecture in which two or more computers are connected together over a network to send and receive requests between one another.
## In their communication, each machine has its own role: the machine sending requests is usually referred as *Client* and the machine responding (serving) is called *Server*.
![project5 diagram](https://user-images.githubusercontent.com/51024695/126328613-5aed0077-e8d6-4bcb-86ec-ef29e31d4480.PNG)
### To begin Sin up two ec2 machines - Server A `mysql server` Server B `mysql client`
* sudo apt-get update 
![update](https://user-images.githubusercontent.com/51024695/126330975-91ef42c2-8322-41e9-8ea3-7aacfb039865.PNG)
### Install mysql server
* Sudo apt install mysql
![server install](https://user-images.githubusercontent.com/51024695/126334606-6821b6a5-c5e2-468e-b04e-8b51caed3579.PNG)
![sql-server-installed](https://user-images.githubusercontent.com/51024695/126334867-229f6f32-5705-4ddc-87cd-fb9f5b258bee.PNG)
### Run mysql secure installation.
* sudo mysql_secure_installation
![Server_secure_install](https://user-images.githubusercontent.com/51024695/126358057-3fec7401-d07a-4716-995e-88d3ffd4bde6.PNG)
![Server_secure_install_others](https://user-images.githubusercontent.com/51024695/126358067-9a67f4e6-a7b9-4786-bd6f-76930dbb355b.PNG)
### Enable mysql
![mysql-server enable](https://user-images.githubusercontent.com/51024695/126345045-2455d251-7b9d-45e0-b58b-6a6aab0c334e.PNG)
### check mysql status on server
* sudo systemctl mysql status
![confirming sql-server](https://user-images.githubusercontent.com/51024695/126348880-7d59280f-59d6-4007-b1ad-6dfa3a66be5f.PNG)
### Edit the bind address in the conf file in the /etc to allow connection to Database
* sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf 
![bind address change](https://user-images.githubusercontent.com/51024695/126355886-10e6a6a9-bb36-460e-8d81-8f082a42aecb.PNG)
### After editing a config file its of best practice to restart the service
* sudo systemctl restart mysql
![restart mysql](https://user-images.githubusercontent.com/51024695/126356107-1fc1e24f-0326-43b1-b638-c2ebf8edb2cf.PNG)
### Login to mysql on the server to create a dadbase
* sudo mysql
![Server_sql_login](https://user-images.githubusercontent.com/51024695/126359210-2a4c4acd-d2be-49c0-a771-bc9cbcfb7fb3.PNG)
### Use creat database command 
* CREATE DATABSE(DB_NAME);
![create db](https://user-images.githubusercontent.com/51024695/126359513-a318c006-3665-4953-8f20-6d44a7a4e210.PNG)
### Create mysql user
![sql_create_user](https://user-images.githubusercontent.com/51024695/126359632-9e703bb7-7ecb-45d6-96e5-668ac14987a7.PNG)
### Grant mysql user permission to database
![sql user permission](https://user-images.githubusercontent.com/51024695/126360008-8cbff397-8cc5-42bb-bf76-3d5ebdd6e630.PNG)

### On the client system
### update 
* sudo apt-get update
![client update](https://user-images.githubusercontent.com/51024695/126346944-2be8ec61-6e1a-4980-bf30-4c7ac363f5e8.PNG)
### install mysql client
* sudo apt install mysql -y
![client install](https://user-images.githubusercontent.com/51024695/126346979-13984828-7c47-4c58-b824-222aaae021ff.PNG)
### Connect to mysql server from the client machine
![connect from client](https://user-images.githubusercontent.com/51024695/126360210-78d1a028-8255-497a-a54f-06ddb228f347.PNG)
### use the show databases to see database created in the server machine
![show database](https://user-images.githubusercontent.com/51024695/126361193-fd558330-dc51-4bf7-8d51-253eab9263ef.PNG)



