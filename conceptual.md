### Conceptual Exercise

Answer the following questions below:

- What is PostgreSQL?
  PostgreSQL is an object-relational database management system (ORDBMS)

- What is the difference between SQL and PostgreSQL?
  PostgreSQL is an advanced version of SQL which provides support to different functions of SQL

- In `psql`, how do you connect to a database?
  `psql database_name`
- What is the difference between `HAVING` and `WHERE`?
  `HAVING` is an colum operation and required `GROUP BY`
  `WHERE` is an row operation

- What is the difference between an `INNER` and `OUTER` join?
    `INNER` join will keep only the information from both tables that's related to each other (in the resulting table). An `OUTER` Join, on the other hand, will also keep information that is not related to the other table in the resulting table.

- What is the difference between a `LEFT OUTER` and `RIGHT OUTER` join?
  Left Outer Join returns all the rows from the table on the left and columns of the table on the right is null padded. Other hand, Right Outer Join returns all the rows from the table on the right and columns of the table on the left is null padded.

- What is an ORM? What do they do?
  Object Relational Mapping (ORM) is a technique used in creating a "bridge" between object-oriented programs and relational databases.

- What are some differences between making HTTP requests using AJAX 
  and from the server side using a library like `requests`?
  When API calls performed on client-side, Client-side does not need interaction with the server, runs on user@s computer and reduce load on the server. On server-side API call reqiures interaction with server, allows the server to provide dynamic websites tailored to the user. Also, increases load on server.

- What is CSRF? What is the purpose of the CSRF token?
  Cross-Site Request Forgery (CSRF) is an attack that forces authenticated users to submit a request to a Web application against which they are currently authenticated. The CSRF token is used to authenticate the HTTP request to prevent this attack.

- What is the purpose of `form.hidden_tag()`?
  The form. hidden_tag() template argument generates a hidden field that includes a token that is used to protect the form against CSRF attacks.