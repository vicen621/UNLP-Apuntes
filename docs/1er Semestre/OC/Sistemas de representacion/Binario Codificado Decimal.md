---
isSystem: true
negativos: Si puede
abreviatura: BCD
---
# Binario Codificado Decimal

## Desempaquetado

Se usa para comunicaciones entre periféricos
Cada dígito ocupa un byte, se escribe `1111`~2~ adelante de cada dígito, el dígito se escribe en [[Binario Sin Signo]]

### Sin Signo

834~10~ = 11111000 11110011 11110100~2~
            =       F8              F3              F4~16~

75~10~ = 11110111 11110101~2~
         =       F7             F5~16~

### Con Signo

Al ultimo dígito se le agrega el símbolo adelante.
\+ -> C = 1100
\- -> D = 1101

-834~10~ = 11111000 11110011 11010100~2~
               =       F8              F3              D4~16~

+69~10~ = 11110110 11001001~2~
            =      F6               C9~16~

## Empaquetado

Se utiliza para hacer cálculos
Cada dígito ocupa solo 4 bits, se escribe sin el relleno

El signo se agrega despues del ultimo numero, no pueden quedar bytes incompletos

+834~10~ = 1000 0011 0100 1100~2~
            =       8         3        4         C~16~

+75~10~ = 0000 0111 0101 1100~2~
         =     0         7       5         C~16~

-834~10~ = 1000 0011 0100 1101~2~
               =    8         3        4        D~16~

-69~10~ = 0000 0110 1001 1101~2~
            =     0         6        9       D~16~

### Suma de BCD

Como en BCD solo se usan los dígitos del 0 al 9, nos quedan 6 combinaciones de bits sin usar. Es por esto que si la suma de 2 números en BCD da un numero mayor a 9~10~ se le tiene que sumar 6~10~ (0110~2~)

Ejemplos:
   15~10~  |     0001  0101~2~
\+ 27~10~  | + 0010   0111~2~
\= 42~10~  | = 0011    1100~2~
                       3~10~       12~10~ -> Se le suma 6~10~ (0110~2~)

\     0011  1100~2~
\+  0000 0110~2~
\= 0100   0010~2~
      4~10~       2~10~
