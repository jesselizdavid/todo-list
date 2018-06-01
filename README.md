#### Technologies Used
```
React + 
Redux + 
React-router 4 + 
Redux-Form 6 + 
SCSS + 
Webpack 2 +
NodeJS +
ExpressJS +
KnexJS + 
PostgreSQL
```

##### FYI

* The use of the $ character symbolizes that the following text needs to be entered in the terminal/powershell

#### Setup Notes

* Install PostgreSQL on your machine if you don't already have it

* Attempt running the command $ psql in your terminal/powershell
 
```
If you try to access psql locally and get an error like this:

psql: could not connect to server: No such file or directory
	Is the server running locally and accepting
	connections on Unix domain socket "/tmp/.s.PGSQL.5432"?
```

```
Run this command to start your postgres server:   
$ pg_ctl -D /usr/local/var/postgres -l /usr/local/var/postgres/server.log start
```

* Then to make sure you have a database for yourself run this command:

```
$ createdb
```

* Then attempt to run this command:

```
$ psql
```

* If you see something like this you're good:

```
psql (9.6.3)
Type "help" for help.

Adam=#
```
* Exit from the psql repl with this command:

```
$ \q
```

* Then create a database locally by running this command:

```
$ createdb todos
```

* Now you should be able to re-enter into psql directly to your new databse:

```
$ psql todos
```

* If you see something like this you're good:

```
psql (9.6.3)
Type "help" for help.

todos=#
```

* Now as long as you have a version of node at least 6.9.5 and npm version at least 5.0.0 you can install the project dependencies in the root directory of this project:

```
$ yarn
```

* You'll also have to install the knex module globally on your machine:

```
$ yarn global add knex
```

* Now you can update the schema of your local database to be compliant with this project:

```
$ knex migrate:latest
```

* You should now be able to run the app. In one terminal/powershell tab or window run this command:

```
$ yarn run client
```

* In another terminal/powershell tab or window run this command:

```
$ yarn run server
```

* The client side of the application should now be available in the browser at:

```
localhost:8081
```