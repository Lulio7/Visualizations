## Limpieza de la base de datos:

- Chequeamos que el tipo de dato para cada columna sea el correcto.
- Vemos en los casos que tengamos informacion en blanco o null si podemos completar esa informacion desde otra
base de datos o en el caso de ser necesario eliminaremos esas filas.

- Utilizamos dividir columna por ":" o personalizado con "(" para limpiar un poco la cantidad de opciones que
tenemos en cada una de las siguientes columnas y eliminaremos las columnas adicionales que se creen.
y borramos la columna que se creo secundaria.
Por ultimo limpiamos los titulos para que no tengan extra caracteres.

Columnas a procesar:
	Q1 - Which Title Best Fits your Current Role?
	Q11 - Which Country do you live in?
	Q4 - What Industry do you work in?
	Q5 - Favorite Programming Language
	Q13 - Ethnicity.

- Q3 - Current Yearly Salary (in USD): 
	Duplicamos columna.
	Dividimos de digito a no digito.
	Borramos la ultima con solo k y reemplazamos la k en la segunda creada. Ahora solo tenemos valores numericos.
	Reemplazamos con nada el signo "-" y "+" con 225.
	Pasamos a numero entero las columnas.

Agregamos una columna peronalizada: Average Salary =
([#"Q3 - Current Yearly Salary (in USD) - Copia.1"] + [#"Q3 - Current Yearly Salary (in USD) - Copia.2"]) /2
