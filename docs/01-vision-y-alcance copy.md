# Visión y alcance del WMS
Documentación de un Sistema WMS
## Contexto
A continuación se documentará el alcance del Sistema WMS a desarrollar, esto como parte de un proyecto de iniciativa personal, orientado a aplicar las buenas practicas y conocimientos adquiridos en la Ingeniería de Software
## Propósito
Desarrollar un sistema que permita controlar la entrada, ubicación, inventario y despachos de mercancía, manteniendo la trazabilidad desde la entrada y todos los procesos siguientes en su ciclo hasta el despacho (qué ocurrió, cuándo ocurrió y quién lo realizó)
## Problemas que se quieren resolver.
1. No se conoce con precisión dónde está cada producto.
2. El saldo registrado puede no coincidir con la existencia física.
3. Los operarios eligen ubicaciones arbitrariamente.
4. No existe una buena trazabilidad de los movimientos.
5. Dos operaciones simultáneas pueden intentar reservar o retirar el mismo inventario, causando sobreasignación, saldos incorrectos o movimientos duplicados.
6. Las diferencias se detectan demasiado tarde.
7. ***En las vistas y reportes de cara al cliente se detectan diferencias***.
8. No hay una forma de calcular las tarifas por espacio ocupado, esto porque no hay una gestión eficiente del cubicaje.
9. No hay una gestión eficiente sobre estados del producto. (Averiado, Contaminado, Restringido)
## Alcance
La primera versión será utilizada por una única empresa operadora logística. La empresa podrá administrar mercancía perteneciente a varios clientes, pero cada existencia pertenecerá exclusivamente a un cliente.

* Configuración
  * Catálogos operativos: ej: *Tipos de ubicación, estados de inventario, unidades de medida*
  * Clientes: Empresas que almacenarán su mercancía en las bodegas donde operará el software.
  * Bodegas: Instalaciones físicas donde se almacenará la mercancía.
  * Zonas: Divisiones virtuales de la bodega, ej: *Zona de Picking, Zona Despacho*
  * Productos: Mercancía del cliente


* Almacenamiento
  * Ubicaciones: Posición de estiba en estantería o piso según el tipo de almacenamiento ofrecido.
* Entradas
  * Crear Recepción
  * Registrar cantidades recibidas
  * Almacenar mercancía
* Inventario
  * Consultar existencias
  * Consultar movimientos
  * Realizar ajustes controlados
* Salida
  * Crear orden de salida
  * Reservar inventario
  * Ejecutar picking
  * Confirmar despacho

##  Fuera del Alcance

* Compras.
* Ventas.
* Facturación.
* Contabilidad.
* Gestión de transporte.
* Nómina.
* Integraciones externas.

## Evolución futura

- Gestión de lotes y fechas de vencimiento.
- Estrategias FIFO y FEFO.
- Estados y bloqueos de inventario.
- Cubicaje y capacidad de ubicaciones.
- Cálculo de tarifas de almacenamiento.
- Reportes especializados para clientes.
- Integraciones con sistemas externos.

## Supuestos iniciales

* Todos los productos se manejan por unidades enteras.
* Una ubicación puede contener varios productos.
* El inventario no puede quedar negativo.
* Toda modificación del inventario debe generar un movimiento.
* Las órdenes pueden ejecutarse parcialmente.
* Una operación confirmada no se elimina.
* Los errores confirmados se corrigen con operaciones compensatorias.
* Los usuarios deben identificarse para ejecutar operaciones.

## Criterios de éxito

La primera versión se considerará exitosa cuando:

- El usuario pueda configurar clientes, productos, bodegas, zonas y
  ubicaciones necesarias para la operación.

- El usuario pueda registrar una recepción total o parcial y almacenar
  la mercancía recibida en ubicaciones válidas.

- El usuario pueda consultar el inventario físico, reservado y
  disponible por cliente, producto y ubicación.

- El usuario pueda crear una orden de salida, reservar inventario,
  ejecutar el picking y confirmar el despacho total o parcialmente.

- El sistema impida mover, reservar o despachar una cantidad superior
  a la permitida.

- El sistema impida que una operación deje inventario físico o
  disponible negativo.

- Todo cambio físico de inventario genere un movimiento que permita
  identificar qué ocurrió, cuándo ocurrió y quién lo realizó.

- Una operación repetida accidentalmente no genere movimientos ni
  afectaciones duplicadas.

- Las operaciones confirmadas no puedan eliminarse o modificarse sin
  dejar evidencia auditable.