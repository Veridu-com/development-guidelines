# Oracle SQL Developer
- If you want a nice GUI for accessing PostgreSQL you may use the Oracle SQL developer free tool.
- You should first download the PostgreSQL jdbc driver [here](https://jdbc.postgresql.org/download/postgresql-9.4.1208.jar).
- Download SQL Developer [here](http://www.oracle.com/technetwork/developer-tools/sql-developer/overview/index-097090.html).
- You need to enable the jdbc driver in the SQL Developer by going to `Tools > Preferences > Database > Third Party JDBC Driver` and adding the path to the jar you downloaded earlier.
- We need to connect to PostgreSQL through an ssh tunnel. Since Oracle does not support that by default to PostgreSQL, we will create the ssh tunnel manually and then add the server to our local port.
- Run: `ssh -fNg -L 5432:localhost:5432 user@host` to create the ssh tunnel, replacing `user` and `host` with your configurations. This will create the tunnel in the background.
- To configure the connection in SQL Developer, right click in the `Connections` button and select a PostgreSQL connection. As hostname enter `localhost` and for port `5432`. You can then choose your database and set the username and password.
- Enjoy a nice GUI secured through ssh.
- After you disconnect from SQL Developer, you can stop the ssh tunnel by doing `ps aux | grep ssh` and then just killing the ssh process that has the tunnel.