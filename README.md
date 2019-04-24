# Ejercicios-scripts-Linux
#### Ejercicio 1:
````
#! /bin/bash

# Elimina un archivo o directorio pasado como parámetro, y le pregunte si está seguro de llevar a cabo la acción.

clear
if [ -e $1 ]
then
	if [ -d $1 ]
	then
		read -p "¿Esta seguro?(Y/N) " opcion
		if [ $opcion == "Y" -o $opcion == "y" ]
		then
			rm -r $1
			exit 0
		fi
		exit 1
	else
		read -p "¿Esta seguro?(Y/N) " opcion
		if [ $opcion == "Y" -o $opcion == "y" ]
		then
			rm $1
			exit 0
		fi
		exit 1
	fi
else
	echo "No existe el fichero o directorio introducido."
fi
exit -1
````

#### Ejercicio 2:
````
#! /bin/bash

# Muestra la información de un comando al ejecutar dicho script y pasar como parámetro el comando.

clear
$1 --help
````

#### Ejercicio 3:
````
#! /bin/bash

# Comprueba si el usuario actual del sistema es blas, si es así visualiza su nombre 5 veces, sino te despides de él amigablemente.

clear
usuario=`whoami`
if [ $usuario == 'blas' ]
then
	echo $usuario
	echo $usuario
	echo $usuario
	echo $usuario
	echo $usuario
else
	echo "Nos vemos"
fi
````

#### Ejercicio 4:
````
#/!bin/bash

# Muestra si la palabra clave de un archivo es el parámetro pasado o no.

clear
clave=`cat /home/usuario/Documents/fichero.sh`
if [ $clave == $1 ]
then
	echo "Si"
else
	echo "No"
fi
````

#### Ejercicio 5:
````
#! /bin/bash

# Suma, resta o multiplica según le indiquemos en el menú.

clear
while [ true ]
do
	read -p "Introduce (1/Suma) (2/Resta) (3/Multiplicación) (4/Salir) " opcion
	case $opcion in
		1)
			read -p "Primer número " n1
			read -p "Segundo número " n2
			su=`expr $n1 + $n2`
			echo $n1" + " $n2 " = "$su
		;;
		2)
			read -p "Primer número " n1
			read -p "Segundo número " n2
			re=`expr $n1 - $n2`
			echo $n1" - " $n2 " = "$re
		;;
		3)
			read -p "Primer número " n1
			read -p "Segundo número " n2
			mu=`expr $n1 \* $n2`
			echo $n1" * " $n2 " = "$mu
		;;
		*)
			exit 0
		;;
	esac
done
````

#### Ejercicio 6:
````
#! /bin/bash

# Pide la edad y nos dice si es mayor de edad o menor.

clear
read -p "Introduce tu edad: " edad
if [ $edad -lt 18 ]
then
	echo "Eres menor de edad "
else
	echo "Eres mayor de edad"
fi
````

#### Ejercicio 7:
````

````

#### Ejercicio 8:
````
#/!bin/bash

# Nos dice al pulsar una tecla si es una letra, numero o caracter especial.


read -p "Introduce el carácter " caracter
case $caracter in
	[a-z,A-Z])
		echo "Ha introducido una letra"
	;;
	[0-9])
		echo "Ha introducido un número"
	;;
	*)
		echo "Ha introducido un caracter especial"
	;;
esac
````

#### Ejercicio 9:
````

````

#### Ejercicio 10:
````

````

#### Ejercicio 11:
````
#/!bin/bash

# Nos pide introducir la ruta de un directorio por teclado y nos dice cuantos archivos y cuantos directorios
# hay dentro de ese directorio.

clear
read -p "Introduzca la ruta de un directorio :" directorio
until [ -d $directorio ]
do
	read -p "Introduzca la ruta de un directorio :" directorio
done
contador=0
contadorFicheros=0
	for indice in `ls $directorio`
	do
		if [ -d $indice ]
		then
			contador=`expr $contador + 1`
			elif [ -f $indice ]
			then
				contadorFicheros=`expr $contadorFicheros + 1`
			fi
done
echo "Ha introducido $contador directorios y $contadorFicheros ficheros."
````

#### Ejercicio 12:
````
#/!bin/bash

# Introduce un número por parámetro y muestra su tabla de multiplicar

clear
echo "La tabla de multiplicar de $1 es: "
for (( indice=0; indice<11; indice++ ))
do
   resultado=`expr $1 \* $indice`
   echo "$1 x $indice = $resultado"
done
````

#### Ejercicio 13:
````
#/!bin/bash

# Limpia todas las reglas, y da permiso a todas las conexiones.

clear
iptables -F
iptables -A INPUT -j ACCEPT
iptables -A OUTPUT -j ACCEPT
iptables -A FORWARD -j ACCEPT
````

#### Ejercicio 14:
````
#/!bin/bash

# Limpia todas las reglas, y prohíbe cualquier conexión.

clear
iptables -F
iptables -A INPUT -j DROP
iptables -A OUTPUT -j DROP
iptables -A FORWARD -j DROP
````

#### Ejercicio 15:
````

````
