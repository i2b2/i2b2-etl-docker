# i2b2-etl-docker
Quick Start for i2B2-etl using docker-compose

## Prerequisite 
    
[docker-compose on linux machine](prerequisites.sh)

## install steps
    1. git clone https://github.com/i2b2/i2b2-etl-docker
    2. cd i2b2-etl-docker/postgres
    3. export I2B2_ROOT_PASSWORD=$(openssl rand -base64 14) && docker-compose up -d i2b2-etl;  
    Note the password by:
    4. echo "I2B2_ROOT_PASSWORD: $I2B2_ROOT_PASSWORD" 
    5. verify that webclient is working on http://localhost/webclient (username: demo ,password: from step 4 )
    
## to connect to diffirent data sources for the i2b2 cells
    5. docker-compose down
    6. modify .env file
    7. repeat steps 1 and 2 
    
## to use mssql container
    8. in step 2 cd to mssql folder

## to modify default password
    change I2B2_ROOT_PASSWORD in .env file, and run 'docker volume rm -f i2b2-mssql-vol i2b2pg-vol' before step 3

For assistance email: support@i2b2clinical.org

##  How to Cite
Wagholikar KB, Ainsworth L, Zelle D, et.al. I2b2-etl: Python application for importing electronic health data into the informatics for integrating biology and the bedside platform. **Bioinformatics**. 2022 Oct 14;38(20):4833-4836. 

Wagholikar KB, Dessai P, Sanz J, Mendis ME, Bell DS, Murphy SN. Implementation of informatics for integrating biology and the bedside (i2b2) platform as Docker containers. **BMC Med Inform Decis Mak**. 2018 Jul 16;18(1):66. 
