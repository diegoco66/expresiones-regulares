\w - caracteres de palabras
\d - dígitos
\s - Espacios invisibles

[0-9] ~ \d
[a-z0-9_] ~ \w

* => 0 o todo
+ => 1 o más
? => 0 o 1

(número => cualquier expresión de números seguidos)
(dígito => Unidad de número)
\d*[a-z]?s\d* - Puede o no haber un número seguido o no de una letra seguido de una "s" seguido o no de un número
\d?[a-z]?s\d* - Puede o no haber un dígito seguido o no de una letra seguido de una "s" seguido o no de un número
\d?[a-z]?s\d? - Puede o no haber un dígito seguido o no de una letra seguido de una "s" seguido o no de un dígito
\d?[a-z]?s\d+ - Puede o no haber un dígito seguido o no de una letra seguido de una "s" seguido de un número
\d+[a-z]?s\d? - Debe ir un número seguido o no de una letra seguido de una "s" seguido o no de un dígito
\d+[a-z]+s\d? - Debe ir un número seguido de letras seguido de una "s" seguido o no de un dígito

*Contadores*

(\d{2,2}[\-\.]?){5,5} - Busca parejas de dos dígitos seguidas o no de un - o un . y esto repetido 5 veces

*? como delimitador*

.+?, - Busca grupos de expresiones que terminen en , si se dejara sin el ? una expresión del tipo (kilo,peso,taco,tira) sería: kilo,peso,taco, pero con el ? nos da 3 distintas: kilo, peso, y taco,

*Negar*

\D - Busca todo lo que no es un dígito
\W - Busca todo lo que no es una palabra.
\S - Busca todo lo que no es White Spaces
[^0-5a-c\s] - Busca todo lo que no es un dígito del 0 al 5, que no sea una letra de la a a la c y que no sea un White Space

*Inicio y final de línea*

^ - Inicio de línea
$ - Final de línea

^\w+,\w+,\w+$ - Busca las líneas que tienen una o + palabras seguido de , por 3 sin , al final

^\+?\d{2,3}[^\da-z]?\d{2,3}[^\da-z]?\d{2,3}[#pe]?\d*$ - Busca números telefónicos formados por 3 parejas de números de 2 o 3 dígitos seguido de un carácter o no que no sea un dígito o letra y puede o no finalizar con un #, p o e seguido de otro número.
