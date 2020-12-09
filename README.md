# TECHNICAL CHALLENGE - Backend Dev

## 1. CODING  _
### A.	Design
Given the following code, which represents an Argentinian Bank account, please answer the following question:

1. Do you think the class is properly designed? If not, but it works, would you change it or will you add new classes?

		I think this class works, but I would change it by adding the classes "Cuenta Corriente" and 
		"Caja de ahorros" that will re-implement some methods applying the correct functionality to each class.

2. If you would change the design, please explain what you would change using an UML class diagram. If you think a method should be changed, please write it down as well.

    ![](https://raw.githubusercontent.com/matiasm2/atixChallenge/main/atix.png)

3. Are these changes riskless? Why? How would you introduce them?



4. Would you add any getters and setters? Which ones? Why?

		I would add the getters for "numeroCuenta", "Titular", "Saldo" and 
		(on "Cuenta corriente" class) "descubiertoAcordado".
		I would not recommend the setters because those values only would be changed by their
		respective methods.

5. Does your solution apply any design pattern? Which one?

		I am not an expert on design pattern implementations, but I think that the design I have introduced
		follows the Template Method pattern.

------------

## 3. SQL and DBS
Given the following tables (linked by idUsuario field):


| Usuario |   |
| :------------: | :------------: |
| id  | integer  |
| username  | varchar(255)  |
| password  | varchar(255)  |

| Persona |   |
| :------------: | :------------: |
| id  | integer  |
| idUsuario  | integer  |
| nombre  | varchar(255)  |
|apellido|varchar(255)|
|fechaNac|date|


Write a standard SQL query such that:

a.	Returns the users whose name starts with “Jorg”

~~~mysql
SELECT * FROM Usuario u
INNER JOIN Persona p ON u.id = p.idUsuario
WHERE p.nombre LIKE 'Jorg%';
~~~

b.	Return the months of the year where the amount of users who were born is bigger than 10.
* you can assume that there is a function called MONTH that returns the month of the year for a given date.
~~~mysql
SELECT MONTH(p.fechaNac) FROM Usuario u
INNER JOIN Persona p ON u.id = p.idUsuario
GROUP BY MONTH(p.fechaNac) 
HAVING count(MONTH(p.fechaNac) ) > 10;
~~~
