# Plan: Obtencion del azimut de los captadores solares

> Source PRD: Consulta sobre como obtener el angulo de orientacion de los captadores para la instalacion problema

## Resumen

Definir el metodo para obtener y justificar el azimut de los captadores solares termicos de la instalacion problema. La latitud y longitud del edificio son utiles para localizar el emplazamiento y apoyar el analisis solar, pero no bastan por si solas para fijar la orientacion real del plano de captacion.

## Decisiones arquitectonicas

- **Entrada geografica**: la latitud y longitud se tomaran de `Proyecto/Anotaciones/posicion_edificio.md`.
- **Fuente tecnica interna**: la implementacion consultara los notebooks `Energia_Solar_Termica` y `Catalogo_Solar`.
- **Fuente externa**: la implementacion usara busqueda web con Exa Deep Search para contrastar criterios tecnicos y documentales.
- **Convencion de azimut**: se expresara respecto al sur geografico y se dejara indicada la convencion de signo usada.
- **Objeto del calculo**: el azimut se asignara al plano real de instalacion, no a la posicion geografica del edificio.

---

## Phase 1: Localizacion y contexto del edificio

**User stories**: identificar si la posicion geografica sirve para algo y ubicar correctamente la instalacion.

### What to build

Recuperar las coordenadas del edificio, usarlas para localizar el emplazamiento sobre cartografia o imagen aerea y dejar claro que esas coordenadas solo aportan contexto espacial y solar. En esta fase se fija el marco del problema: ubicacion, norte geografico y referencia de medida.

### Acceptance criteria

- [x] Las coordenadas del edificio se extraen correctamente de la fuente indicada.
- [x] Queda definido el sistema de referencia usado para orientar la medicion.
- [x] Se distingue de forma explicita entre ubicacion geografica y orientacion del plano de captacion.

---

## Phase 2: Determinacion del plano de captacion

**User stories**: obtener la orientacion real de los captadores segun el tipo de soporte o cubierta.

### What to build

Identificar si los captadores se colocan en cubierta inclinada, cubierta plana con estructura soporte o fachada, y fijar para cada caso como se mide la orientacion del plano. El azimut se derivara de la geometria real de instalacion, no de las coordenadas del edificio.

### Acceptance criteria

- [x] Se identifica el tipo de superficie o soporte de los captadores.
- [x] Se define como medir la orientacion en cada escenario.
- [x] El resultado final queda expresado como azimut respecto al sur geografico.

---

## Phase 3: Contraste tecnico y justificacion

**User stories**: justificar el azimut obtenido y responder si la latitud y longitud bastan o no para el calculo.

### What to build

Consultar los notebooks indicados y realizar busqueda web con Exa Deep Search para contrastar criterios sobre orientacion, inclinacion, perdidas y metodologia de calculo. Con esa informacion se justificara si la orientacion elegida es optima o admisible y si existen perdidas asumibles.

### Acceptance criteria

- [x] Se documenta la justificacion tecnica con fuentes consultadas durante la implementacion.
- [x] Se explica por que latitud y longitud no bastan para fijar el azimut.
- [x] Se recoge la posible necesidad de calcular perdidas por orientacion e inclinacion.

---

## Phase 4: Documento de resultado

**User stories**: disponer de una conclusion clara y reutilizable para la instalacion problema.

### What to build

Generar un resultado final con coordenadas, metodo de medida, azimut final, inclinacion prevista y conclusion tecnica. El documento debe dejar listo el argumento para usarlo en el calculo o memoria de la instalacion.

### Acceptance criteria

- [x] El resultado final incluye coordenadas, azimut e inclinacion.
- [x] La convencion de medida queda escrita de forma no ambigua.
- [x] La conclusion responde de forma directa si la posicion geografica basta o no para obtener el azimut.

