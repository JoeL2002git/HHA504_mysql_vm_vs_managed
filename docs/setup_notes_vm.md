## VM Set Up
### Creating VM
1. Select instance to create
2. Select E2 for affordability
3. Select e2-micro of memory
4. Select Ubuntu OS system
5. Leave everything as default and create

### Firewall Configs
1. Create a firewall rule
2. Name your firewall + description
3. Set IP to 0.0.0.0/0 (allows all IP)
4. Set protocol tcp to '3306'
5. Save and create

### SSH setup
1. Update OS system using `sudo apt-get update`
2. Install mysql using `sudo apt install mysql-server mysql-client`
3. Login to mysql by inputting `sudo mysql`
4. Input `CREATE USER 'xxx'@'%' IDENTIFIED BY 'xxx';` to add user to database
5. Give priviledge to the created user by inputting `GRANT ALL PRIVILEGES ON *.* TO 'xxx'@'%' WITH GRANT OPTION;`
6. Change network connections in mysqld.cnf file to `0.0.0.0/0`
7. Restart SSH to save the change
8. Input `mysql -u dba -p` to login

Secrets can be stored in an .env file

### Trouble
1. Did not give `dba` power, fixed it by following step 5 in SSH setup
2. Forgot to change network connection to 0.0.0.0/0

### Time to set up
Roughly an hour due to the various trouble faced along the way and lack of experience.