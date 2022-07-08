### Automate ETL for i2b2 using gitlab containers

  1. git clone …
  2. cd i2b2-cdi/postgres/
  3. sudo docker-compose up -d i2b2-etl gitlab-runner i2b2-mssql

#### Wait for 2-5 minutes for containers to start

  4. verify that webclient is working on http://localhost/webclient (username: demo ,pass: Etl@2021)
  5. Verify that gitlab is available on http://localhost:8090/  (username:root and password: adminadmin
