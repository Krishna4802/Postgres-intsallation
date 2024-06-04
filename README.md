# Postgres-intsallation

    sudo apt update
    sudo apt install postgresql postgresql-contrib -y
    sudo service postgresql start

### Switching Over to the postgres Account
    sudo -i -u postgres
    psql
    \q

### Accessing a Postgres Prompt Without Switching Accounts
    sudo -u postgres psql
    \q

### user creation
    sudo -u postgres createuser --interactive \n psql  
    
                    (or)  
    
    sudo -u postgres psql
    CREATE USER <user_name> WITH PASSWORD '<password>';

    vi /etc/postgresql/14/main/pg_hba.conf 
    
### change like this 
    # "local" is for Unix domain socket connections only
    # Change "peer" to "md5" for password authentication
    local   all             all                                     md5

### Setting password for postgres root user

    ALTER USER postgres PASSWORD 'postgres';
