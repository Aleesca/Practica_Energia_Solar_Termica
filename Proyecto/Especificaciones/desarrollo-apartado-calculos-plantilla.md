# Desarrollo del apartado de calculos de `plantilla.tex`

Este documento especifica el flujo de trabajo para desarrollar el apartado de calculos de `Practica_Solar-LaTeX/plantilla.tex`. El resultado esperado es una redaccion ordenada que introduzca primero, en un breve parrafo en prosa, el conjunto de comprobaciones y dimensionamientos realizados; despues debe desarrollar los calculos de los circuitos de la instalacion solar termica en una secuencia tecnica coherente y cerrar con la seleccion de las bombas, incorporando las figuras disponibles cuando correspondan.

## Objetivo

Definir como debe construirse el apartado de calculos de `Practica_Solar-LaTeX/plantilla.tex` a partir de las anotaciones tecnicas existentes en `Proyecto/Anotaciones/` y de las imagenes de apoyo disponibles en `Practica_Solar-LaTeX/Figuras/`.

El documento final en LaTeX debe mantener una progresion clara:

1. Presentacion general del trabajo realizado en el apartado de calculos.
2. Desarrollo del circuito primario solar.
3. Desarrollo del circuito secundario solar.
4. Desarrollo del circuito de distribucion de ACS.
5. Seleccion de bombas e integracion de figuras.

## Flujo de trabajo

### 1. Parrafo inicial en prosa

Antes de iniciar cualquier subseccion del apartado de calculos, se debe redactar un parrafo breve que resuma que se ha hecho en el conjunto del apartado.

Este parrafo debe:

- Estar escrito en prosa continua.
- No estar precedido por ninguna `\subsection`, `\subsubsection` ni encabezado equivalente.
- Explicar que se han calculado o justificado los circuitos hidraulicos principales de la instalacion solar termica.
- Anticipar que el apartado culmina con la seleccion de las bombas necesarias.
- Servir como transicion entre los datos de partida y el desarrollo tecnico de los calculos.

### 2. Circuito primario solar

La primera parte desarrollada despues del parrafo introductorio debe corresponder al circuito primario solar.

Fuente de trabajo:

- `Proyecto/Anotaciones/explicacion-circuito-primario-solar.md`

El desarrollo en `plantilla.tex` debe usar esta anotacion como referencia para explicar el circuito que conecta el campo de captadores solares con el intercambio o acumulacion correspondiente. La redaccion debe presentar el objetivo del circuito, los criterios de calculo aplicados y la justificacion de los parametros principales que se incorporen al documento.

Al final de este apartado se debe incluir una tabla en formato A4 horizontal. Esta pagina debe conservar los encabezados y pies de pagina del resto del documento e integrar exclusivamente la tabla de perdidas de carga por tramo del circuito primario solar.

### 3. Circuito secundario solar

Tras el circuito primario, se debe desarrollar el circuito secundario solar.

Fuente de trabajo:

- `Proyecto/Anotaciones/explicacion-circuito-secundario-solar.md`

Esta parte debe continuar el razonamiento iniciado en el circuito primario y explicar el papel del circuito secundario dentro de la transferencia de energia hacia el sistema de acumulacion o consumo. La redaccion debe mantener continuidad tecnica con el apartado anterior, evitando repetir informacion general ya introducida.

Al final de este apartado se debe incluir una tabla en formato A4 horizontal. Esta pagina debe conservar los encabezados y pies de pagina del resto del documento e integrar exclusivamente la tabla de perdidas de carga por tramo del circuito secundario solar.

### 4. Circuito de distribucion de ACS

Despues del circuito secundario, se debe desarrollar el circuito de distribucion de agua caliente sanitaria.

Fuente de trabajo:

- `Proyecto/Anotaciones/explicacion-circuito-distribucion-acs.md`

Esta seccion debe explicar como se plantea la distribucion de ACS desde el sistema de produccion o acumulacion hasta los puntos de consumo. Debe cerrar la parte dedicada a circuitos hidraulicos antes de pasar a la seleccion de equipos de impulsion.

Al final de este apartado se debe incluir una tabla en formato A4 horizontal. Esta pagina debe conservar los encabezados y pies de pagina del resto del documento e integrar exclusivamente la tabla de tramos en la impulsion de la bajante del circuito de distribucion de ACS.

### 5. Seleccion de bombas

El ultimo apartado del bloque de calculos debe estar dedicado a la seleccion de bombas.

Fuente de trabajo:

- `Proyecto/Anotaciones/seleccion-bomba-circuito-solar-termico.md`

Directorio de figuras:

- `Practica_Solar-LaTeX/Figuras/`

Esta parte debe justificar la seleccion de las bombas necesarias para los circuitos tratados previamente. La redaccion debe integrar las imagenes de bombas disponibles en `Practica_Solar-LaTeX/Figuras/`, usando las figuras como apoyo visual para documentar los modelos, curvas, caracteristicas tecnicas o criterios de seleccion que se incluyan en `plantilla.tex`.

La integracion de imagenes debe hacerse en el punto donde aporten valor a la explicacion, preferiblemente junto a la justificacion de la bomba correspondiente.

## Criterios de aceptacion

- El apartado de calculos de `Practica_Solar-LaTeX/plantilla.tex` comienza con un parrafo introductorio en prosa, sin subseccion previa.
- El circuito primario solar se desarrolla antes que el circuito secundario.
- El circuito secundario solar se desarrolla antes que el circuito de distribucion de ACS.
- El circuito de distribucion de ACS aparece antes de la seleccion de bombas.
- La seleccion de bombas queda como ultimo apartado del bloque.
- Las fuentes de `Proyecto/Anotaciones/` se usan respetando el orden indicado en este documento.
- Las imagenes de bombas de `Practica_Solar-LaTeX/Figuras/` se incorporan en el apartado de seleccion de bombas cuando sean pertinentes.
- Cada apartado de circuito termina con una tabla en formato A4 horizontal, manteniendo los encabezados y pies de pagina del resto del documento.
- Las tablas horizontales de los circuitos primario y secundario contienen exclusivamente la tabla de perdidas de carga por tramo correspondiente.
- La tabla horizontal del circuito de distribucion de ACS contiene exclusivamente la tabla de tramos en la impulsion de la bajante.
- No se mezclan los calculos de circuitos con la seleccion de bombas fuera del orden definido.

## Archivos implicados

Archivo de destino para la redaccion final:

- `Practica_Solar-LaTeX/plantilla.tex`

Fuentes tecnicas:

- `Proyecto/Anotaciones/explicacion-circuito-primario-solar.md`
- `Proyecto/Anotaciones/explicacion-circuito-secundario-solar.md`
- `Proyecto/Anotaciones/explicacion-circuito-distribucion-acs.md`
- `Proyecto/Anotaciones/seleccion-bomba-circuito-solar-termico.md`

Recursos graficos:

- `Practica_Solar-LaTeX/Figuras/`
