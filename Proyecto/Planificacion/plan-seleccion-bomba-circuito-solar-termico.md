# Plan: Seleccion de bomba comercial para circuito solar termico

> Fuente: solicitud del usuario sobre seleccion de una bomba comercial para la instalacion solar termica, con consulta en NotebookLM `Energia_Solar_Termica` y busqueda Exa de fabricantes europeos, priorizando Alemania.

## Resumen

El objetivo es preparar una anotacion tecnica en `Proyecto/Anotaciones/` que justifique si la instalacion necesita una bomba al salir del sistema bivalente intercambiador-deposito hacia los colectores solares, y si tambien hacen falta bombas en los tramos previos u otros circuitos. La investigacion debe apoyarse en NotebookLM `Energia_Solar_Termica` y en busqueda profunda Exa con fuentes de fabricantes europeos, priorizando fabricantes alemanes.

## Decisiones arquitectonicas

Estas decisiones deben mantenerse constantes durante toda la ejecucion:

- **Documento de salida**: una anotacion Markdown en `Proyecto/Anotaciones/`.
- **Ambito tecnico**: circuito primario solar, enlace con el sistema bivalente, posibles circuitos secundarios y necesidad real de bombeo.
- **Fuentes base**: NotebookLM `Energia_Solar_Termica` y fuentes oficiales de fabricantes europeos.
- **Criterio de seleccion**: prioridad a fabricantes alemanes o europeos con documentacion tecnica oficial.

---

## Fase 1: Inventario tecnico de la instalacion

**Historias cubiertas**: identificar el circuito real, localizar el tramo donde se plantea la bomba y reunir datos para una decision hidraulica.

### Que hay que construir

Revisar la documentacion local relevante del proyecto para identificar los circuitos implicados: primario solar hacia colectores, acumulacion/intercambio, ACS y posibles circuitos auxiliares. Extraer o dejar explicitamente marcados los datos necesarios para dimensionar la impulsion: tipo y numero de colectores, caudal de diseno, longitud de tuberias, diametros, fluido, temperaturas y presiones de trabajo.

### Criterios de aceptacion

- [ ] Queda identificado el circuito en el que se plantea la bomba.
- [ ] Quedan separados los circuitos primario, secundario y auxiliares, si existen.
- [ ] Se listan los datos tecnicos disponibles y los que siguen faltando para cerrar la seleccion.

---

## Fase 2: Consulta tecnica en NotebookLM

**Historias cubiertas**: fundamentar la necesidad de bomba en el primario solar y aclarar si otros circuitos requieren impulsion propia.

### Que hay que construir

Consultar el notebook `Energia_Solar_Termica` para extraer la base tecnica sobre ubicacion de bombas en instalaciones solares termicas, funcionamiento con interacumulador bivalente y condiciones en las que otros circuitos necesitan bombeo independiente. La salida debe dejar trazabilidad suficiente para poder citar la justificacion dentro de la anotacion final.

### Criterios de aceptacion

- [ ] Se obtiene respaldo tecnico para la ubicacion de la bomba en el circuito solar.
- [ ] Se aclara si los tramos previos o secundarios necesitan bomba o pueden apoyarse en la configuracion existente.
- [ ] La evidencia queda lista para trasladarse a la anotacion final.

---

## Fase 3: Busqueda profunda de bombas comerciales

**Historias cubiertas**: encontrar alternativas de fabricante que sean compatibles con la instalacion y comparar opciones reales del mercado.

### Que hay que construir

Usar Exa Deep Search para localizar bombas comerciales de fabricantes europeos con prevalencia alemana. Priorizar fuentes oficiales: fichas tecnicas, catalogos, manuales de instalacion y curvas hidraulicas. Incluir al menos tres alternativas comparables y descartar fuentes no oficiales salvo para localizar documentacion primaria.

### Criterios de aceptacion

- [ ] Se documentan al menos tres opciones comerciales viables.
- [ ] Las fuentes principales son oficiales del fabricante.
- [ ] Al menos una opcion preferente procede de un fabricante aleman o de gran presencia alemana en el sector.

---

## Fase 4: Evaluacion hidraulica de la necesidad de bombas

**Historias cubiertas**: decidir si la bomba se necesita solo en el primario solar o tambien en otros circuitos.

### Que hay que construir

Contrastar la documentacion de la instalacion con la teoria tecnica para decidir donde es necesaria una bomba y donde no. El analisis debe separar con claridad tres casos: bomba necesaria, bomba no necesaria y bomba condicionada a la configuracion final. La conclusion debe contemplar el circuito entre el sistema bivalente y los colectores, y tambien los tramos previos o auxiliares.

### Criterios de aceptacion

- [ ] Se emite una conclusion tecnica sobre el circuito principal hacia colectores.
- [ ] Se determina si hay bombeo adicional en otros circuitos.
- [ ] La conclusion explicita que la seleccion final puede depender de datos de perdida de carga si faltan valores definitivos.

---

## Fase 5: Seleccion comercial final

**Historias cubiertas**: escoger una bomba comercial justificable con parametros de trabajo y respaldo de fabricante.

### Que hay que construir

Comparar las alternativas encontradas segun caudal, altura manometrica, temperatura maxima, compatibilidad con glicol, materiales, eficiencia, control y facilidad de integracion. Elegir una recomendacion principal y una alternativa equivalente. Si faltan datos para cerrar el dimensionado, dejar la seleccion condicionada y explicitar que parametros faltan.

### Criterios de aceptacion

- [ ] Se propone una opcion preferente y al menos una alternativa.
- [ ] Cada opcion incluye datos tecnicos suficientes para evaluar compatibilidad.
- [ ] La recomendacion queda ligada a una justificacion tecnica, no solo comercial.

---

## Fase 6: Redaccion de la anotacion final

**Historias cubiertas**: dejar la explicacion completa y reutilizable en `Proyecto/Anotaciones/`.

### Que hay que construir

Redactar la anotacion final en formato tecnico, coherente con las anotaciones existentes, incluyendo: descripcion del circuito, necesidad de bomba en el tramo hacia colectores, analisis de otros circuitos, comparativa de bombas comerciales y recomendacion final. Cerrar con bibliografia y enlaces separados entre NotebookLM y fabricantes.

### Criterios de aceptacion

- [ ] La nota se guarda en `Proyecto/Anotaciones/`.
- [ ] La explicacion distingue entre necesidad hidraulica y seleccion comercial.
- [ ] Las fuentes externas proceden principalmente de fabricantes europeos, con prevalencia alemana.
- [ ] La conclusion final queda clara y accionable.

## Suposiciones

- El sistema bivalente intercambiador-deposito ya integra el intercambio termico, pero no se presupone que integre toda la impulsion hidraulica hacia colectores.
- La bomba objetivo pertenece al circuito primario solar o grupo de bombeo solar.
- La salida final sera una anotacion tecnica Markdown, no una modificacion de calculos ni planos.
- Se priorizara una recomendacion practica comercial sobre una seleccion definitiva cerrada si faltan datos hidraulicos completos.
