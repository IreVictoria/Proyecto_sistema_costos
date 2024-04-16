[![banner-udd.png](https://i.postimg.cc/N09x03s9/banner-udd.png)](https://postimg.cc/R3mtsbn4)
# Proyecto N°1: Sistema de costos.
<p>
En este proyecto se dará a conocer la realización de forma detalla de la construcción de un algoritmo en pseudocodigo que simule un `Sistema de costo` realizado en el programa Pseint. A continuación, se mostrarán los requisitos del proyecto, planteamiento del problema y la resolución del algoritmo paso a paso 
</p>

------------

### Requisitos para construir el proyecto.

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


### Planteamiento del problema.

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

### Construcción del algoritmo paso a paso.

------------


<p>
Primero debemos declarar las variables de nuestro algoritmo:
</p>
- `precioOriginal,descuentoCupon,precioIVA,descuentoxCantidad,costoEnvio,precioFinal1,precioFinal2`. Estas variables almacenarán los distintos valores del producto solicitados en el algoritmo que serán declarados como Reales. 
- `i,pedidos,descuento,pedidofinal`, estas variables serán declaradas como  enteros ya que estas serán utilizadas para controlar los bucles y las estructuras condicionales para realizar cálculos.
```
Definir precioOriginal,descuentoCupon,precioIVA,descuentoxCantidad,costoEnvio,precioFinal1,precioFinal2 como real
	Definir i,pedidos,descuento,pedidofinal Como Entero
```
<p>
