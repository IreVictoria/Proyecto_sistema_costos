[![banner-udd.png](https://i.postimg.cc/N09x03s9/banner-udd.png)](https://postimg.cc/R3mtsbn4)
# Proyecto N°1: Sistema de costos.
<p>
	
En este proyecto se dará a conocer la realización de forma detalla de la construcción de un algoritmo en pseudocodigo que simule un `Sistema de costo` realizado en el programa Pseint. A continuación, se mostrarán los requisitos del proyecto, planteamiento del problema y la resolución del algoritmo paso a paso. 

</p>

------------

## Requisitos para construir el proyecto.

------------


<p>
	
Para construir este algoritmo en `pseudocodigo` deberá cumplir con los siguientes requisitos:

</p>

- Lea el precio original del producto.
- Aplicar un descuento al producto si es aplicable (ejemplo, si el cliente tiene un cupón de descuento).
- Aplicar impuestos al producto (ejemplo, el IVA u otros impuestos).
- Si el cliente compra más de un artículo, se aplicará un descuento por cantidad.
- Calcular el costo de envío basado en el destino y el peso del paquete.
- Calcular el costo final del producto sumando el precio con descuento, impuestos, descuento por cantidad y costo del envío.
- Mostrar el costo final del producto, desglosando los diferentes componentes (descuentos, impuestos, descuento por cantidad y costo de envío).

------------



## Planteamiento del problema.

------------


<p>
Un cliente desea comprar un par de zapatos deportivos en línea. A continuación, se presentan los detalles del producto y la información del cliente:
</p>

- Precio original: $100.
- Cupón descuento: 10% de descuento.
- IVA (impuesto al valor agregado): 12%
- Cantidad: 2 pares de zapatos deportivos.
- Peso paquete: 3kg
- Destino del envío: Nueva York.

------------


## Construcción del algoritmo paso a paso.

------------


<p>
Primero debemos declarar las variables de nuestro algoritmo:
</p>

- `precioOriginal,descuentoCupon,precioIVA,descuentoxCantidad,costoEnvio,precioFinal1,precioFinal2`. Estas variables almacenarán los distintos valores del producto solicitados en el algoritmo que serán declarados como Reales.
  
- `i,pedidos,descuento,pedidofinal`, estas variables serán declaradas como  enteros ya que estas serán utilizadas para controlar los bucles y las estructuras condicionales para realizar cálculos.

```
Definir precioOriginal, descuentoCupon, precioIVA, descuentoxCantidad, costoEnvio, precioFinal1, precioFinal2 como real

	Definir i, pedidos, descuento, pedidofinal Como Entero
```

<p>
Se realiza asignación de valores según los datos entregados en el proyecto.
</p>

```
	//Asignación de valores

	precioOriginal<-100
	descuentocupon<-0.1
	iva<-1.12
	descuentoporcantidad<-0.05
	costoenvio<-16
	pesopaquete<-3
```
<p>
Luego tendremos las operaciones aritméticas realizadas en el programa Pseint que serán utilizadas para realizar el cálculo de cada requerimiento en el algoritmo 
</p>
		
```
//Realizar cálculo para cupón de descuento 
	descuentoCupon<-precioOriginal-(precioOriginal*0.1)

	//Realizar cálculo para aplicar el IVA al producto con descuento
	precioIVA<-descuentoCupon*1.12

	//Realizar cálculo de descuento por cantidad de producto
	descuentoxCantidad<-precioIVA-(precioIVA*0.05)

	//Realizar cálculo de costo de envio 
	costoEnvio<-10+(2*3)

	//Realizar cálculo del producto final más el envío de un par
	precioFinal1<-(precioIVA*1)+costoEnvio

	//Realizar cálculo del producto final más el envío de dos pares
	precioFinal2<-(descuentoxCantidad*2)+costoEnvio
		
```
A continuación, se creará un `arreglo unidimensional` para leer el número de pedidos ingresados por el usuario.
		
```
//Crear un array para realizar lista de pedidos de los productos

	Dimension pedidos[1]	
	//Realizar ingreso de pedidos
	Para i<-1 Hasta 1 Con Paso 1 Hacer
		Escribir "Pedido cliente" i, ":"
		Leer pedidos[i]
	Fin Para

	//Cantidad de pedidos
	Escribir "La cantidad de pedidos ingresados son:"
	Para i<-1 Hasta 1 Con Paso 1 Hacer
		Si pedidos[i]>=1 Entonces
			Escribir pedidos[i]
		FinSi
	Fin Para
```


Aquí se crea el `arreglo unidimensional` se le pide al usuario que ingrese la cantidad de pedido realizado por el cliente, para luego utilizar el bucle `para ` que se ejecutara solo una vez (i=1 hasta i=1) el cual nos dará a conocer el número de pedido ingresado que se almacenara en el arreglo `pedidos [i]`.



Una vez realizado esta parte del algoritmo se hará una estructura de control condicional el cual utilizaremos el `si...entonces`, donde ingresaremos las condiciones en las sentencias de bloque, si la sentencia es verdadera, se ejecuta el bloque de sentencia uno; de lo contrario, se ejecuta el bloque de sentencia dos. En este caso será según lo requerido por el usuario el cual se pide que ingrese la cantidad de pedidos por el cliente, dependiendo si es 1 pedido o 2 pedidos se realizaran los cálculos aritméticos adecuados para cada sentencia y se obtendrá el valor del producto con descuento respectivamente según lo solicitado. 
</p>


```
//Agregar precio y cantidad del producto pedido por el cliente

	Escribir "Ingrese cantidad de producto solicitado por el cliente:"
	leer cantidad

	Si cantidad>=2 Entonces
		Escribir "Si lleva 2 pares se aplica descuento del 5% donde cada producto queda en un valor de $",descuentoxCantidad
	SiNo
		Escribir "Si lleva 1 par se aplica descuento cupón del 10% y el producto queda en un valor de $",precioIVA 
	Fin Si
```


<p>
	
Ahora realizaremos nuevamente otra estructura de control condicional `si... Entonces` para que se pueda obtener el resultado final de producto que es el descuento correspondiente más el valor del envío. Aquí le solicitaremos al usuario que indique la cantidad final del producto requerido dependiendo si es 1 o 2 y de esta manera el control de flujo ejecutara cada sentencia según la cantidad final del articulo solicitado. 

</p>


```
// Calculo final del producto más el envío

	Escribir "Ingrese cantidad final del pedido:"
	Leer pedidoFinal

	Si pedidoFinal>=2 Entonces
		Escribir "El precio total de 2 pares más el costo de envío es de $", precioFinal2
	SiNo
		Escribir "El precio total de 1 par más el costo de envío es de $", precioFinal1
	Fin Si
```

<p>
	
Y para concluir el algoritmo se nos pide en el proyecto detallar cada producto con su respectivo valor en este caso en el `programa Pseint` se utiliza el comando `Escribir` y entre "comillas" ingresaremos el texto con la indicación dada para cada valor que queremos dar a conocer se cierran las comillas y al lado del texto escribiremos el nombre de la variable ya declaradas en el inicio que almacenan cada valor aritmético según lo explicado anteriormente. A continuación, se muestra el desglose de cada valor con descuento cupón, impuesto, descuento por cantidad y costo envió:

</p>

```
//Mostrar valores desglosados

	Escribir "Los valores deglosados de los productos son:"
	Escribir "El precio original del producto es de = $", precioOriginal
	Escribir "El precio del producto con cupón de descuento es de = $", descuentoCupon
	Escribir "El precio del producto con descuento más el IVA agregado es de = $", precioIVA
	Escribir "El precio del producto si llevas dos pares, cada producto tiene un valor de = $", descuentoxCantidad
	Escribir "El costo de envío tiene un valor de = $", costoEnvio
	Escribir "El precio final de un producto más el envío es de = $", precioFinal1
	Escribir "El precio final de dos productos más el envío es de = $", precioFinal2
	
```

------------


<p>
La solución en conjunto final del algoritmo sería de esta forma:
</p>


```

Algoritmo Proyecto_sistema_de_costos

	//Declarar variables del sistema de costo
	Definir precioOriginal,descuentoCupon,precioIVA,descuentoxCantidad,costoEnvio,precioFinal1,precioFinal2 como real
	Definir i,pedidos,cantidad,pedidofinal Como Entero

	//Asignación de valores 
	precioOriginal<-100
	descuentocupon<-0.1
	iva<-1.12
	descuentoporcantidad<-0.05
	costoenvio<-16
	pesopaquete<-3

	//Realizar cálculo para cupón de descuento 
	descuentoCupon<-precioOriginal-(precioOriginal*0.1)
	//Realizar cálculo para aplicar el IVA al producto con descuento
	precioIVA<-descuentoCupon*1.12
	//Realizar cálculo de descuento por cantidad de producto
	descuentoxCantidad<-precioIVA-(precioIVA*0.05)
	//Realizar cálculo de costo de envio 
	costoEnvio<-10+(2*3)
	//Realizar cálculo del producto final más el envío de un par
	precioFinal1<-(precioIVA*1)+costoEnvio
	//Realizar cálculo del producto final más el envío de dos pares
	precioFinal2<-(descuentoxCantidad*2)+costoEnvio

	//Crear un array para realizar lista de pedidos de los productos
	Dimension pedidos[1]	
	//Realizar ingreso de pedidos 
	Para i<-1 Hasta 1 Con Paso 1 Hacer
		Escribir "Pedido cliente" i, ":"
		Leer pedidos[i]
	Fin Para
	//Cantidad de pedidos 
	Escribir "La cantidad de pedidos ingresados son:"
	Para i<-1 Hasta 1 Con Paso 1 Hacer
		Si pedidos[i]>=1 Entonces
			Escribir pedidos[i]
		FinSi
	Fin Para

	//Agregar precio y cantidad del producto pedido por el cliente
	Escribir "Ingrese cantidad de producto solicitado por el cliente:"
	leer cantidad
	Si cantidad>=2 Entonces
		Escribir "Si lleva 2 pares se aplica descuento del 5% donde cada producto queda en un valor de $",descuentoxCantidad
	SiNo
		Escribir "Si lleva 1 par se aplica descuento cupón del 10% y el producto queda en un valor de $",precioIVA 
	Fin Si

	// Calculo final del producto más el envío 
	Escribir "Ingrese cantidad final del pedido:"
	Leer pedidoFinal
	Si pedidoFinal>=2 Entonces
		Escribir "El precio total de 2 pares más el costo de envío es de $", precioFinal2
	SiNo
		Escribir "El precio total de 1 par más el costo de envío es de $", precioFinal1
	Fin Si

	//Mostrar valores desglosados 
	Escribir "Los valores deglosados de los productos son:"
	Escribir "El precio original del producto es de = $", precioOriginal
	Escribir "El precio del producto con cupón de descuento es de = $", descuentoCupon
	Escribir "El precio del producto con descuento más el IVA agregado es de = $", precioIVA
	Escribir "El precio del producto si llevas dos pares, cada producto tiene un valor de = $", descuentoxCantidad
	Escribir "El costo de envío tiene un valor de = $", costoEnvio
	Escribir "El precio final de un producto más el envío es de = $", precioFinal1
	Escribir "El precio final de dos productos más el envío es de = $", precioFinal2
	
	
FinAlgoritmo

```
