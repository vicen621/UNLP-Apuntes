# Registros

Los registros se usan para almacenar informacion bajo una misma variable, algo asi como una clase.

## Definición

Se definen de la siguiente manera:
```pascal
program example;
type
	nombre = record
		campo1: type;
		campo2: type;
	end;

var
	registro: nombre;
```

## Uso

Los registros solo tienen una accion, y es la asignacion total entre registros. Por fuera de eso el registro como tal no puede hacer nada, pero para ello podemos llamar a sus variables internas.

Para llamar a una variable dentro del registro se utiliza la siguiente sintaxis `registro.campo1`
Y eso es una variable como cualquier otra.