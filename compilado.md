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
