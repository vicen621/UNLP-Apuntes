# Representar e interpretar entre los diferentes sistemas

## Indice

1. [Tabla de equivalencias](#tabla-de-equivalencias)
2. [Binario a Decimal](#binario-a-decimal)
3. [Hexadecimal a Decimal](#hexadecimal-a-decimal)
4. [Decimal a Binario](#decimal-a-binario)
    1. [Parte Entera](#parte-entera)
        1. [Dividiendo](#dividiendo)
        2. [Restando potencias de 2](#restando-potencias-de-2)
    2. [Parte Decimal](#parte-decimal)
5. [Decimal a Hexadecimal](#decimal-a-hexadecimal)
6. [Binario a Hexadecimal](#binario-a-hexadecimal)
7. [Hexadecimal a Binario](#hexadecimal-a-binario)

## Tabla de equivalencias

| Decimal | Binario | Hexadecimal |
|:-------:|:-------:|:-----------:|
|  0~10~  | 0000~2~ |    0~16~    |
|  1~10~  | 0001~2~ |    1~16~    |
|  2~10~  | 0010~2~ |    2~16~    |
|  3~10~  | 0011~2~ |    3~16~    |
|  4~10~  | 0100~2~ |    4~16~    |
|  5~10~  | 0101~2~ |    5~16~    |
|  6~10~  | 0110~2~ |    6~16~    |
|  7~10~  | 0111~2~ |    7~16~    |
|  8~10~  | 1000~2~ |    8~16~    |
|  9~10~  | 1001~2~ |    9~16~    |
|  10~10~ | 1010~2~ |    A~16~    |
|  11~10~ | 1011~2~ |    B~16~    |
|  12~10~ | 1100~2~ |    C~16~    |
|  13~10~ | 1101~2~ |    D~16~    |
|  14~10~ | 1110~2~ |    E~16~    |
|  15~10~ | 1111~2~ |    F~16~    |

---

## Binario a Decimal

En este caso hay que usar el Teorema fundamental de la numeración
\[
N=\sum_{i=-d}^nX_i*B^i
\]

Por ejemplo: $10100101_2=1*2^7+0*2^6+1*2^5+0*2^4+0*2^3+1*2^2+0*2^1+1*2^0=165_{10}$
$1011.011_2=1*2^3+0*2^2+1*2^1+1*2^0+0*2^{-1}+1*2^{-2}+1*2^{-3}=11.375_{10}$

## Hexadecimal a Decimal

En este caso hay que usar el Teorema fundamental de la numeración
$$
N=\sum_{i=-d}^nX_i*B^i
$$
Por ejemplo: $9F7_{16}=9*16^2+15*16^1+7*16^0=2551_{10}$
$10.2_{16}=1*16^1+0*16^0+2*16^{-1}=16.125_{10}$

## Decimal a Binario

Para pasar un numero de decimal a binario la parte entera y la decimal se pasan de maneras diferentes

### Parte Entera

Hay 2 maneras de pasar la parte entera

#### Dividiendo

En esta manera lo que tenés que hacer es dividir la parte entera entre 2 hasta que el cociente sea 0 y se escriben los restos de atrás para adelante.

Ejemplo:
![[_assets/DecimalToBinaryEx.png]]

#### Restando potencias de 2

Esta forma es mas simple, tenés que restarle la potencia de 2 mas alta posible, el bit que de esa potencia va a ser 1.

Ejemplo: $210_{10}=128+64+16+2=11010010_2$

### Parte decimal

Para pasar la parte decimal es simple, tenés que multiplicar la parte decimal por 2 hasta que la misma sea 0 o se empiece a repetir. Tenes que anotar la parte entera del resultado, una vez lo anotes volves a multiplicar la **parte decimal** por 2 otra vez.

Ejemplo:
$0.375_2=0.375*2=0.75*2=1.5*2=1.0$
$0.375_{10}=0.011_2$

%% TODO %%
## Decimal a Hexadecimal

## Binario a Hexadecimal

En este caso hay que usar la tabla de Binario Codificado Hexadecimal que es la siguiente:

Lo que hay que hacer es dividir el numero en binario en bloques de 4 dígitos, empezando de derecha a izquierda, si el ultimo bloque tiene menos de 4 dígitos se le suman 0 adelante. Una vez tenés todos los bloques, lo buscas en la tabla y le pones el simbolo correspondiente.

Ejemplo: 10100101~2~ = A5~16~

%% TODO %%
## Hexadecimal a Binario
