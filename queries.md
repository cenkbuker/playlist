Make sure you download the starter code and run the following:

```sh
  psql < movies.sql
  psql movies_db
```

In markdown, you can place a code block inside of three backticks (```) followed by the syntax highlighting you want, for example

\```sql

SELECT \* FROM users;

\```

Using the `movies_db` database, write the correct SQL queries for each of these tasks:

1.  The title of every movie.
    `SELECT title FROM movies`

2.  All information on the G-rated movies.
    `SELECT * FROM movies WHERE rating = 'G'`

3.  The title and release year of every movie, ordered with the
    oldest movie first.
    `SELECT title, release_year FROM movies ORDER BY release_year ASC`

4.  All information on the 5 longest movies.
    `SELECT * FROM movies ORDER BY runtime DESC LIMIT 5`

5.  A query that returns the columns of `rating` and `total`, tabulating the
    total number of G, PG, PG-13, and R-rated movies.
    `SELECT rating, COUNT(*) FROM movies GROUP BY rating`

6.  A table with columns of `release_year` and `average_runtime`,
    tabulating the average runtime by year for every movie in the database. The data should be in reverse chronological order (i.e. the most recent year should be first).
    `SELECT release_year, AVG(release_year) AS average_runtime FROM movies GROUP BY release_year ORDER BY release_year DESC`

7.  The movie title and studio name for every movie in the
    database.
    `SELECT title, name FROM movies JOIN studios ON movies.studio_id = studios.id; `

8.  The star first name, star last name, and movie title for every
    matching movie and star pair in the database.
    `SELECT s.first_name, s.last_name, m.title FROM movies m JOIN roles r ON m.id = r.movie_id JOIN stars s ON r.star_id = s.id `

9.  The first and last names of every star who has been in a G-rated movie. The first and last name should appear only once for each star, even if they are in several G-rated movies. *IMPORTANT NOTE*: it's possible that there can be two *different* actors with the same name, so make sure your solution accounts for that.
    `SELECT DISTINCT s.first_name, s.last_name FROM movies m JOIN roles r ON m.id = r.movie_id JOIN stars s ON r.star_id = s.id WHERE m.rating = 'G' `

10. The first and last names of every star along with the number
    of movies they have been in, in descending order by the number of movies. (Similar to #9, make sure
    that two different actors with the same name are considered separately).
    `SELECT DISTINCT s.first_name, s.last_name, COUNT(m.title) FROM movies m JOIN roles r ON m.id = r.movie_id JOIN stars s ON r.star_id = s.id GROUP BY s.first_name, s.last_name;`