# Plan: Refinamiento de la seleccion de bombas del circuito solar termico y ACS

> Fuente de alcance: `Proyecto/Anotaciones/seleccion-bomba-circuito-solar-termico.md`.

## Resumen

El objetivo es revisar y corregir la nota indicada sin implementar cambios en el contenido tecnico definitivo aun. El refinamiento debe aclarar la ubicacion real de la bomba del circuito solar primario, eliminar la bomba de apoyo de caldera y rehacer la seleccion de la bomba de recirculacion de ACS usando datos correctos de calculo y una consulta de mercado con Exa Deep Search.

## Cambios principales

- Corregir la interpretacion de la bomba del circuito solar primario, dejando claro que va en azotea.
- Eliminar la lectura incorrecta de altura nominal para esa bomba, porque no aplica en la forma en que estaba planteada.
- Replantear la bomba de recirculacion de ACS con el punto de calculo del circuito de distribucion:
  - Caudal: `370 L/h`.
  - Altura manometrica: `0.41 m.c.a.`
- Aplicar un margen de seleccion para la bomba de ACS consultando proyectos reales o criterios tecnicos habituales de instalaciones solares termicas, sin fijar ese margen en el plan.
- Buscar y contrastar opciones comerciales Grundfos con `Exa Deep Search`.
- Eliminar por completo la bomba del circuito de apoyo de caldera.

## Fases de trabajo

### Fase 1: Relectura tecnica del alcance

**Objetivo**: identificar con precision que parte del texto afecta a cada bomba y que afirmaciones deben corregirse o retirarse.

**Resultado esperado**:
- Localizacion de los pasajes del documento vinculados al circuito solar primario.
- Localizacion de los pasajes vinculados a la recirculacion de ACS.
- Localizacion de cualquier referencia a la bomba de apoyo de caldera para su eliminacion.

### Fase 2: Correccion del circuito solar primario

**Objetivo**: rehacer la justificacion de la bomba del primario solar para que refleje su ubicacion real en azotea y su condicion hidraulica correcta.

**Resultado esperado**:
- Se elimina la interpretacion de una altura nominal improcedente.
- La justificacion queda referida a la configuracion real del circuito y no a una exigencia de bombeo mal formulada.

### Fase 3: Definicion del margen para ACS con evidencia real

**Objetivo**: decidir el margen de seleccion de la bomba de recirculacion a partir de proyectos reales, referencias tecnicas o practicas habituales del sector.

**Resultado esperado**:
- El margen se justifica con evidencia externa.
- El documento final distingue entre el punto calculado y el punto de seleccion comercial.
- No se fija un valor de margen dentro del plan; se decide durante la ejecucion.

### Fase 4: Busqueda de bomba Grundfos

**Objetivo**: localizar bombas Grundfos que cubran el punto de trabajo de la recirculacion de ACS una vez aplicado el margen justificado.

**Resultado esperado**:
- Busqueda ejecutada con `Exa Deep Search`.
- Identificacion de una bomba principal y, si procede, una alternativa.
- Registro del modelo, rango de trabajo y compatibilidad con ACS.

### Fase 5: Limpieza del documento

**Objetivo**: retirar elementos que ya no deben formar parte de la nota tecnica.

**Resultado esperado**:
- La bomba de apoyo de caldera desaparece del texto.
- Tablas, conclusiones y referencias quedan coherentes entre si.

## Criterios de aceptacion

- La nota revisada sigue siendo un documento de anotacion tecnica y no una implementacion de calculo nueva.
- La bomba solar primaria queda explicada con su ubicacion en azotea y sin la altura nominal improcedente.
- La seleccion de la bomba ACS parte de `370 L/h` y `0.41 m.c.a.` y usa un margen decidido con evidencia de proyectos reales.
- La busqueda comercial se realiza con `Exa Deep Search`.
- No queda ninguna referencia funcional a la bomba de apoyo de caldera.

## Suposiciones

- `370 L` se interpreta como `370 L/h`.
- La salida final seguira siendo un Markdown de planificacion dentro de `Proyecto/Planificacion/`.
- La resolucion del margen de seleccion se dejara para la ejecucion del plan, no para el texto del plan.
