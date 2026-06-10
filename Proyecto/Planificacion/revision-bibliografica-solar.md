# Plan: Revision bibliografica y normalizacion de citas en `plantilla.tex`

> Documento objetivo: `Practica_Solar-LaTeX/plantilla.tex`  
> Fuentes principales: NotebookLM `Energia_Solar_Termica`, NotebookLM `Catalogos_solar`, y web de bombas localizada mediante Exa MCP.

## Resumen

El objetivo es revisar el documento LaTeX, integrar solo citas realmente usadas en el texto, completar fuentes de figuras y tablas, y depurar la bibliografia para que no incluya entradas no citadas.

No se debe implementar durante esta fase de planificacion. La lectura de `plantilla.tex`, `refs.bib`, figuras, tablas y archivos adjuntos queda reservada para la fase de implementacion.

## Decisiones de implementacion

- Usar NotebookLM MCP para extraer citas verificables de:
  - `Energia_Solar_Termica` (`62b2af52-7df4-455e-9334-8b10ebd8118d`)
  - `Catalogos_solar` (`7d1bf88b-463a-4291-9201-1959144a5921`)
- Usar Exa MCP obligatoriamente para localizar/verificar la web seleccionada de bombas. Si Exa MCP no esta disponible en el entorno de implementacion, bloquear esa parte hasta habilitarlo.
- No anadir al archivo `.bib` ninguna referencia que no aparezca citada mediante `\cite`, `\parencite`, `\textcite` o el comando equivalente ya usado por el documento.
- Para normativa, crear referencias sin URL y sin fecha de acceso; incluir solo datos bibliograficos/normativos estables: organismo, titulo, codigo, edicion/ano y publicacion oficial si aplica.
- Para figuras y tablas:
  - Si son originales: `Fuente: Elaboracion grupal.`
  - Si derivan de una fuente: `Fuente: Adaptado de ... \cite{clave}.`
  - Si reproducen datos o especificaciones de catalogo: citar el catalogo o ficha tecnica correspondiente.

## Fases tracer bullet

### Fase 1: Inventario controlado del documento

Leer `plantilla.tex`, `refs.bib`, preambulo y estructura de figuras/tablas solo durante la implementacion. Crear una matriz de auditoria con secciones, figuras, tablas, citas existentes, referencias bibliograficas existentes y huecos de fuente.

**Criterios de aceptacion**

- Existe una lista completa de figuras y tablas con estado: original, adaptada, catalogo, normativa o pendiente.
- Existe una lista de todas las claves bibliograficas usadas en el `.tex`.
- Existe una lista separada de entradas en `.bib` no citadas, marcadas para eliminar o no integrar.

### Fase 2: Obtencion de citas desde NotebookLM y Exa

Consultar NotebookLM para obtener referencias y justificacion bibliografica de energia solar termica, catalogos de captadores/acumuladores/equipos, criterios de instalacion y normativa. Usar Exa MCP para localizar la fuente web de bombas y extraer los datos necesarios para citarla.

**Criterios de aceptacion**

- Cada afirmacion tecnica anadida o corregida tiene una fuente asignada.
- Cada figura/tabla adaptada tiene una cita concreta.
- La fuente de bombas procede de Exa MCP y queda registrada con URL solo si no es normativa.
- Las normas quedan referenciadas sin URL ni fecha de acceso.

### Fase 3: Integracion bibliografica en la redaccion

Editar el texto para insertar citas donde correspondan, especialmente en fundamentos, criterios de diseno, seleccion de componentes, catalogos comerciales, normativa y justificacion tecnica. Mantener el estilo LaTeX existente.

**Criterios de aceptacion**

- No hay parrafos tecnicos relevantes sin cita cuando dependen de manuales, normativa, catalogos o bibliografia externa.
- Las citas estan integradas de forma natural en la redaccion.
- No se anaden referencias decorativas o no usadas.

### Fase 4: Fuentes en figuras y tablas

Actualizar captions, notas o pies de tabla/figura para indicar fuente en todos los elementos visuales y tabulares.

**Criterios de aceptacion**

- Todas las figuras indican `Elaboracion grupal` o `Adaptado de ... \cite{...}`.
- Todas las tablas indican `Elaboracion grupal`, `Adaptado de ... \cite{...}` o fuente de catalogo/normativa.
- Toda cita usada en una fuente de figura/tabla existe en `refs.bib`.

### Fase 5: Depuracion de `refs.bib` y compilacion

Actualizar `refs.bib` con las referencias citadas y eliminar o excluir toda referencia no citada. Compilar el documento con la herramienta LaTeX ya usada por el proyecto.

**Criterios de aceptacion**

- El PDF compila sin errores de citas indefinidas.
- No aparecen referencias no citadas en la bibliografia final.
- No quedan claves bibliograficas huerfanas en `refs.bib`.
- La bibliografia final coincide con las citas reales del documento.

## Agentes/herramientas a invocar

- NotebookLM MCP: extraccion y validacion de fuentes de los cuadernos indicados.
- Exa MCP: busqueda/verificacion de la web seleccionada de bombas.
- Agente LaTeX/BibTeX: edicion de `plantilla.tex`, `refs.bib` y verificacion de compilacion.
- Agente de auditoria documental: revision cruzada de citas, figuras, tablas y bibliografia final.
- Agente de normativa: comprobacion de referencias normativas sin URL ni fecha de acceso.

## Pruebas y revision final

- Compilar LaTeX hasta resolver citas y referencias cruzadas.
- Revisar el `.log` para detectar claves indefinidas, entradas duplicadas o referencias no usadas.
- Comparar citas usadas en el `.tex` contra entradas finales de `refs.bib`.
- Revisar visualmente el PDF para confirmar que todos los pies de figura y tabla muestran fuente.
- Verificar que ninguna normativa contiene `url`, `urldate`, `accessdate` o fecha de acceso equivalente.

## Supuestos

- `Catalogo_Solar` se refiere al cuaderno existente `Catalogos_solar`.
- La implementacion si podra leer los archivos adjuntos/proyecto; esta fase de planificacion no los lee.
- El estilo bibliografico existente del proyecto se conservara salvo que impida cumplir el requisito de excluir referencias no citadas.
- Si Exa MCP no esta instalado durante la implementacion, la tarea de bombas queda bloqueada hasta habilitarlo.
