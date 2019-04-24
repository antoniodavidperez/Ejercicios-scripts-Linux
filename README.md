# Ejercicios-scripts-Linux
#### Ejercicio 1:
`#! /bin/bash`

`# Elimina un archivo o directorio pasado como parámetro, y le pregunte si está seguro de llevar a cabo la acción.`

`clear`
`if [ -e $1 ]`
`then`
`	if [ -d $1 ]`
`	then`
`		read -p "¿Esta seguro?(Y/N) " opcion`
`		if [ $opcion == "Y" -o $opcion == "y" ]`
`		then`
`			rm -r $1`
`			exit 0`
`		fi`
`		exit 1`
`	else`
`		read -p "¿Esta seguro?(Y/N) " opcion`
`		if [ $opcion == "Y" -o $opcion == "y" ]`
`		then`
`			rm $1`
`			exit 0`
`		fi`
`		exit 1`
`	fi`
`else`
`	echo "No existe el fichero o directorio introducido."`
`fi`
`exit -1`

#### Ejercicio 1:
`hola`

#### Ejercicio 2:
`hola`

#### Ejercicio 3:
`hola`

#### Ejercicio 4:
`hola`

#### Ejercicio 5:
`hola`

#### Ejercicio 6:
`hola`

#### Ejercicio 7:
`hola`

#### Ejercicio 8:
`hola`

#### Ejercicio 9:
`hola`

#### Ejercicio 10:
`hola`

#### Ejercicio 11:
`hola`

#### Ejercicio 12:
`hola`

#### Ejercicio 13:
`hola`

#### Ejercicio 14:
`hola`

#### Ejercicio 15:
`hola`
