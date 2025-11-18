## Managed Cloud SQL
### Creating Cloud SQL
1. Create a sandbox MySQL instance
2. Name instance and set a password
3. Select a region and create

### Network Configs
1. Add 0.0.0.0/0 to allow all network
2. Disable SSL only connection
3. Create a new user and set a passowrd

Secrets can be stored in an .env file

### Trouble
1. Keep on getting an error message on python saying cannot connect. Fixed it by adding 0.0.0.0/0 in network config.

### Time to set up
It took about 30 minutes to set up due to lack of experience, but now it should take me faster. 
