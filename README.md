## Instructions
* Get connected to the database using PSQL command(Postgres-client)
* Create a table in the database which we created
```
create table employee(
id SERIAL,
name varchar(50),
job varchar(40),
department varchar(40),
salary int,
hire_date date,
PRIMARY KEY (id));
```
* Exit out of that database
    * \q
* Now we are back on the VM, let's install NodeJs and NPM
    * apt-get install nodejs npm
* Let's clone the code from repository
    * git clone https://gitlab.com/synechron-aws-batch-april/postgressql-crud-nodejs
    * cd postgressql-crud-nodejs
* We need to update the connection string in the employee.js
    * vi routes/employees.js
* Install the node libraries
    * npm install
* You need to allow the traffic on port 4000 of this VM, as this application runs on that port only.
* Let's run the application
    * node app.js
* Now, browse your application in browser at http://vm_ip:4000