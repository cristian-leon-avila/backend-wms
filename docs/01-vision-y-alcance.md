# Visión General del Producto
## Objetivo del Proyecto
Diseñar y desarrollar un Sistema de Gestión de Almacenes (WMS) modular enfocado en la trazabilidad, control transaccional y optimización de flujos operativos de entrada, almacenamiento e inventario interno dentro de un centro de distribución.
## Declaración del Problema
Los sistemas tradicionales de gestión de inventarios suelen limitar su alcance a la actualización de saldos globales por bodega, sin ofrecer visibilidad precisa en tiempo real a nivel de posición física, contenedor (LPN) o historial de trazabilidad (lote/vencimiento). Esto genera diferencias de stock, errores en el reabastecimiento e ineficiencias en los movimientos internos.
# Alcance del Proyecto (Scope)
Para asegurar la viabilidad técnica y mantener un estándar profesional, la versión inicial (MVP v1.0) se enfoca en tres ejes operativos principales: Maestros/Ubicaciones, Recepciones (Inbound) e Inventario Core. Las funcionalidades avanzadas quedan postergadas para iteraciones posteriores.
## Incluído en el MVP (v1.0)
* Gestión de Productos
* Gestión de Jerarquía de Ubicaciones
* Control de Lotes y Vencimientos
* Control por LPN
* Control de Estados
* Recepción de Ordenes (Inbound)
* Generación e Identificación LPN
* Trazabilidad por Kardex Inmutable
## Funcionalidades incluídas (In-Scope)

### Modulo 1: Configuración de Layout y Ubicaciones
Jerarquía del Almacén: Definición de Zonas, Pasillos, Racks, Niveles y Posiciones.

Tipos de Ubicación: Clasificación en Recepción/Staging, Almacenamiento (Rack), Picking (Suelo) y Cuarentena/Bloqueado.

Restricciones Operativas: Control de capacidad por volumen, peso máximo y compatibilidad de estado.

### Módulo 2: Recepción de Mercancía (Inbound)
Órdenes de Recepción (Inbound Orders): Registro de mercancía esperada contra proveedor o documento origen.

Proceso de Conteo y Asignación de LPN: Captura de cantidad recibida, número de lote, fecha de fabricación y fecha de vencimiento.

Generación de Contenedor (LPN): Agrupación de mercancía contada bajo una etiqueta de identificación única.

Puesta en Stock (Putaway Básico): Regla de asignación de ubicación de destino para sugerir o confirmar la posición final del LPN.

### Módulo 3: Gestión e Inventario Interno (Core Inventory)
Kardex / Ledger Inmutable: Registro auditable de cada evento de inventario (quién, cuándo, qué SKU, qué cantidad, origen y destino).

Ajustes de Inventario: Modificación de cantidades (incrementos/decrementos) justificadas por causa operativa.

Traslados Internos: Movimiento de LPNs o SKUs individuales entre ubicaciones físicas dentro del almacén.

Control de Estados: Bloqueo/Desbloqueo de lotes o LPNs por calidad o cuarentena.

## Funcionalidades Excluidas de la Versión 1.0 (Out-of-Scope)
* Salida de Mercancía y Picking (Outbound): Creación de olas de despacho, rutas óptimas de extracción y empaque (Packing).

* Integración EDI/ERP: Conectores preconstruidos para SAP, Oracle u otros ERPs (se deja expuesta únicamente la API REST).

* Facturación Logística (3PL Billing): Cálculo de costos por almacenamiento o manipulación.

* Sistemas de Automatización: Conexión con clasificadores automáticos (sorters), transelevadores o bandas transportadoras.