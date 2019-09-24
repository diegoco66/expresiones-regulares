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
