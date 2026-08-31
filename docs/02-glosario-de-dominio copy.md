# Glosario de Dominio (Ubiquitous Language)
Este lenguaje unificado define las entidades y conceptos que se utilizarán estrictamente en la documentación, base de datos y código fuente:

* SKU (Stock Keeping Unit): Identificador único del producto en el catálogo. Define atributos base como código, descripción, peso, dimensiones y unidad de medida base.

* UOM (Unit of Measure): Unidad en la que se cuantifica el producto (ej. UN - Unidad, CJ - Caja, PL - Paleta).

* Ubicación (Location): Coordenada física única en el almacén representada mediante la nomenclatura Zona-Pasillo-Rack-Nivel-Posición (Ej: Z01-A-03-2-B).

* LPN (License Plate Number): Identificador único asignado a un contenedor físico (estiba, estibador, caja contenedora o pallet). Permite mover múltiples unidades o lotes de un SKU en una sola transacción mediante un único código.

* Lote (Lot / Batch): Código de identificación atribuido por el fabricante que agrupa unidades producidas bajo las mismas condiciones. Asociado obligatoriamente a una Fecha de Vencimiento (Expiration Date).

* Kardex / Audit Trail: Registro de auditoría transaccional de solo escritura (append-only) que documenta la causa, origen, destino y saldo resultante de cualquier variación física de inventario.

* Inbound Order: Documento maestro que especifica los productos y cantidades que un proveedor entregará en el almacén.

* Putaway: Proceso logístico de trasladar la mercancía desde el área de recepción (Staging) hasta su ubicación de almacenamiento definitivo.

* Stock Disponible vs. Stock Reservado:

  * Disponible: Cantidad física en posición operativa apta para ser transferida o despachada.

  * Reservado: Cantidad física asignada a una orden en proceso que no puede disponerse para otra operación.

  * Bloqueado/Cuarentena: Cantidad física no disponible por control de calidad o daño.