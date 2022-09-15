# i2b2-etl-docker
Quick Start for i2B2-etl using docker-compose

## Prerequisite 
    
[docker-compose on linux machine](prerequisites.md) 

## install steps
    1. git clone https://github.com/i2b2/i2b2-etl-docker
    2. cd i2b2-etl-docker/postgres
    3. export I2B2_ROOT_PASSWORD=$(openssl rand -base64 14) && docker-compose up -d i2b2-etl;  
    Note the password by:
    4. echo "I2B2_ROOT_PASSWORD: $I2B2_ROOT_PASSWORD" 
    5. verify that webclient is working on http://localhost/webclient (username: demo ,pass: from step 4 )
    
## to connect to diffirent data sources for the i2b2 cells
    5. docker-compose down
    6. modify .env file
    7. repeat steps 1 and 2 
    
## to use mssql container
    8. in step 2 cd to mssql folder

## to modify default password
    change I2B2_ROOT_PASSWORD in .env file, and run 'docker volume rm -f i2b2-mssql-vol i2b2pg-vol' before step 3

For assistance email: support@i2b2clinical.org
