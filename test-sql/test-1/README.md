
<h1>Table: Person</h1>
<pre>
+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| PersonId    | int     |
| FirstName   | varchar |
| LastName    | varchar |
+-------------+---------+
</pre>
PersonId es la clave primaria de esta tabla.

<h1>Table: Address</h1>
<pre>
+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| AddressId   | int     |
| PersonId    | int     |
| City        | varchar |
| State       | varchar |
+-------------+---------+
</pre>
AddressId es la clave primaria de esta tabla.

<ul>
<li>Escriba en (SQL query) para generar un report con la información de cada persona con el siguiente formato</li>
</ul>
<h2>Resultado</h2>

FirstName, LastName, City, State

<h2>Solucion</h2>
<ul>
<li>
  SELECT p.FirstName,p.LastName,a.City,a.State
FROM person as p
INNER JOIN address as a
ON a.PersonId = p.PersonId;

  </li>
</ul>
