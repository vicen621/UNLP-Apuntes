# Arrays: Vectores

Los Vectores o arrays de una dimension se utilizan para poder almacenar informacion, siempre y cuando sepas la cantidad de informacion que necesitas almacenar.

## Definición

Los vectores se definen de la siguiente manera:

```pascal
program vectores;
const
	N = 100;
type
	vector = array [1..N] of type;
var
	vec: vector;
```

## Uso
Los vectores, al igual que los [[Registros]] solo tienen una accion directa y es la asignacion entre si `vec := vec1;`. Para poder hacer operacion con sus valores hay que llamarlos, y se hace de la siguiente manera `vec[i]` siendo `i` el indice donde se encuentra la variable que queremos llamar.

## Algoritmos utiles para vectores

### CargarVector

```pascal
procedure cargarVector(var v: vector; var dimL: integer);
var
	entrada: integer;
begin
	dimL := 0;
	readln(entrada);
	while((entrada <> -1) and (dimL < N)) do begin
		dimL := dimL + 1;
		v[dimL] := entrada;
		readln(entrada);
	end;
end;
```

### 