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

