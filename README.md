Download Link: https://assignmentchef.com/product/solved-icsi410-homework-2
<br>
<u>Problem 1. </u> Consider the relational database defined below:

create table passenger (

passenger_ID varchar (10) , passenger_name varchar (30) , passenger_city varchar (30) , primary key (passenger_ID ));

create table seat (

train_number varchar (10) , seat_number varchar (10) , primary key (train_number , seat_number ));

create table reservation ( reservation_number varchar (10) , passenger_ID varchar (10) , train_number varchar (10) , seat_number varchar (10) , departure_station varchar (10) , departure_time timestamp , arrival_station varchar (10) , arrival_time timestamp , fare numeric(8 , 2) , primary key (reservation_number ) , foreign key (passenger_ID) references passenger , foreign key (train_number , seat_number) references seat ); Express in SQL each of the following queries:

(a) Shows the number of passengers living in (i.e., whose passenger_city is) ’Albany’. (b) (10 points) Show the train number of each train that has more than 1000 seats.

<ul>

 <li>(10 points) Find the ID of every passenger who lives in (i.e., whose passenger_city is) ’Albany’ and has never reserved a trip arriving at ’ALB’. For this query, use either an in clause or a not in clause.</li>

 <li>(10 points) Find the ID of every passenger who lives in (i.e., whose passenger_city is) ’Albany’ and has never reserved a trip arriving at ’ALB’. For this query, use a set operation.</li>

 <li>(10 points) Find the ID of every passenger who lives in (i.e., whose passenger_city is) ’Albany’ and has never reserved any trip. For this query, use a left outer join.</li>

 <li>(10 points) For each reservation whose departure time is between ’2020-04-01 00:00:00’ and’2020-04-02 23:59:59’ (inclusive), update the fare as follows: If the current fare is greater than $100, decrease the fare by 5 percent. Otherwise, decrease the fare by 3 percent.</li>

 <li>(10 points) Find the train(s) with the largest number of seats (i.e., trains with more seats orthe same number of seats compared to every other train). For each of these trains, show the train number.</li>

 <li>(10 points) Find all of the trains whose seats were all reserved at least once on ’2019-04-01’.For each of these trains, show the train number.</li>

</ul>

<u>Problem 2. </u>(20 points) Consider the relational database defined in Problem 1. Express in rela-

tional algebra each of the following queries:

<ul>

 <li>(10 points) Show the train number of each train that has more than 1000 seats.</li>

 <li>(10 points) Find the train(s) with the largest number of seats (i.e., trains with more seats orthe same number of seats compared to every other train). For each of these trains, show the train number.</li>

</ul>

After solving the above problems, please state the amount of time spent for this assignment. Feel free to add comments or suggestions if any.

<h1>Appendix A. Installing and Running PostgreSQL</h1>

<ol>

 <li>Visit:</li>

</ol>

https://www.enterprisedb.com/downloads/postgres-postgresql-downloads

<ol start="2">

 <li>On the EnterpriseDB webpage, download an installer for your computer (installers for Linux, Windows and Mac OS X are available). This instruction is based on version 10.16.</li>

 <li>Run the PostgreSQL installer. An installation guide is available at:</li>

</ol>

https://www.postgresql.org/docs/10/static/index.html.

You don’t have to include “Stack Builder”.

<ol start="4">

 <li>Start “pgAdmin 4”. Then, double click the “PostgreSQL 10” icon (Figure 1) and type the password (for the user postgres) to connect to the PostgreSQL server.</li>

</ol>

Figure 1: Connecting to the PostgresSQL server

<ol start="5">

 <li>As in Figure 2, choose the “postgres” database in the “Browser”. In the menu bar, choose “Tools” and then “Query Tool”. You can now type SQL commands in the SQL editor and run them.</li>

</ol>

Figure 2: Selecting the “postgres” database

<ol start="6">

 <li>After creating tables, you can see these tables in pgAdmin 4 using the “Browser” (Figure 3).</li>

</ol>

Figure 3: Created Tables

<h1>Appendix B. Using the EXPLAIN command in Postgres</h1>

You can see the execution plan that Postgres constructs for each submitted SQL statement. Further details of this feature can be found at:

https://www.postgresql.org/docs/10/static/sql-explain.html