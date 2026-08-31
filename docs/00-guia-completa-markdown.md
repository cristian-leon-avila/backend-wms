# Guía Completa de Markdown: Sintaxis Básica y Avanzada

Markdown es un lenguaje de marcado ligero que permite aplicar formato a un texto plano de forma rápida, limpia y legible. Esta guía recopila todas las reglas esenciales desde el nivel básico hasta el avanzado.

---

## 1. Sintaxis Básica

### Títulos y Encabezados
Se crean utilizando el símbolo de número (`#`). El número de almohadillas determina el nivel del encabezado (del 1 al 6).
* `# Encabezado 1` (Título principal)
* `## Encabezado 2` (Secciones)
* `### Encabezado 3` (Subsecciones)
* `#### Encabezado 4`
* `##### Encabezado 5`
* `###### Encabezado 6`

### Énfasis en Texto
Aplica estilos visuales al texto plano mediante asteriscos (`*`) o guiones bajos (`_`):
* **Negrita**: Coloca dos símbolos antes y después del texto. Ejemplo: `**texto en negrita**` o `__texto en negrita__`.
* *Cursiva*: Coloca un símbolo antes y después del texto. Ejemplo: `*texto en cursiva*` o `_texto en cursiva_`.
* ***Negrita y Cursiva***: Combina tres símbolos. Ejemplo: `***texto combinado***`.
* ~~Tachado~~: Coloca dos virgulillas antes y después. Ejemplo: `~~texto tachado~~`.

### Listas
Organiza la información de forma estructurada y jerárquica:
* **Listas No Ordenadas**: Usa asteriscos (`*`), guiones (`-`) o signos de suma (`+`) seguidos de un espacio.
  ```markdown
  * Elemento A
  * Elemento B
    * Subelemento B1
  ```
* **Listas Ordenadas**: Usa números seguidos de un punto (`1.`, `2.`). El orden numérico real no importa en el archivo plano; el procesador lo ordenará automáticamente.
  ```markdown
  1. Primero
  2. Segundo
  ```

### Enlaces e Imágenes
* **Enlaces**: `[Texto visible del enlace](https://url-del-sitio.com)`
* **Imágenes**: `![Texto alternativo de la imagen](ruta-o-url-de-la-imagen.jpg)`

### Citas
Para destacar bloques de texto o frases de otros autores, utiliza el signo mayor que (`>`) al inicio de cada línea:
> "Esta es una cita en bloque de ejemplo. Puede ocupar varias líneas si continúas agregando el símbolo al inicio."

### Código y Resaltado
* **Código en línea**: Para mencionar variables, funciones o comandos dentro de una oración, encuérralos en acentos graves individuales (`` ` ``). Ejemplo: ``Usa el comando `git status` para revisar cambios.``
* **Bloques de código**: Para fragmentos extensos o scripts, encierra el código entre tres acentos graves (```) arriba y abajo. Puedes especificar el lenguaje para activar el resaltado de sintaxis:
  ```python
  def saludar():
      print("Hola Mundo")
  ```

---

## 2. Sintaxis Avanzada (Markdown Extendido / GFM)

### Tablas
Las tablas se crean utilizando barras verticales (`|`) para separar las columnas y guiones (`-`) para definir la fila de encabezado. Utiliza dos puntos (`:`) para alinear el contenido.
* `| Alinear a la izquierda | Alinear al centro | Alinear a la derecha |`
* `| :--- | :---: | ---: |`
* `| Celda 1 | Celda 2 | Celda 3 |`

### Listas de Tareas (Task Lists)
Ideales para el seguimiento de proyectos o pendientes. Usa corchetes con un espacio `[ ]` para tareas pendientes y una equis `[x]` para completadas:
* [x] Diseñar la estructura del documento
* [ ] Escribir el contenido del bloque avanzado
* [ ] Revisar ortografía y enlaces

### Notas al Pie (Footnotes)
Permiten añadir referencias o aclaraciones al final del documento sin interrumpir el flujo de lectura.
* **Referencia en el texto**: `Aquí hay una afirmación que requiere una nota al pie[^1].`
* **Definición de la nota**: Podrá colocarse en cualquier parte inferior del archivo:
  `[^1]: Esta es la explicación o fuente de la afirmación anterior.`

### Bloques de Alerta (Admonitions / Callouts)
Soportados nativamente en plataformas modernas como GitHub para destacar advertencias o notas importantes:
```markdown
> [!NOTE]
> Información útil que los usuarios deben tener en cuenta.

> [!WARNING]
> Contenido crítico que requiere la atención inmediata del lector.
```

---

## 3. Atajos y Buenas Prácticas
1. **Líneas divisorias**: Crea una separación horizontal usando tres o más asteriscos (`***`), guiones (`---`) o guiones bajos (`___`) en una línea sola.
2. **Saltos de línea**: Markdown ignora los saltos de línea simples. Para forzar un salto de línea dentro de un párrafo, añade dos espacios en blanco al final de la línea antes de pulsar Enter.
3. **Escapar caracteres**: Si necesitas mostrar un carácter especial de Markdown (como un asterisco o una almohadilla) como texto literal, anteponle una barra invertida (`\`). Ejemplo: `*Esto no será cursiva*`.
