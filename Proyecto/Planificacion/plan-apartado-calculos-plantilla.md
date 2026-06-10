# Plan: Redaccion Secuencial Del Apartado De Calculos En `plantilla.tex`

> Fuentes referenciadas:
> - `Practica_Solar-LaTeX/plantilla.tex`
> - `Proyecto/Especificaciones/desarrollo-apartado-calculos-plantilla.md`
> - `.agents/agents/task-orchestrator.md`
> - `.agents/agents/solar-termica-researcher.md`
> - `.agents/agents/latex-writer.md`
> - `.agents/agents/latex-validator.md`

## Resumen

Crear un flujo de implementacion, coordinado por `.agents/agents/task-orchestrator.md`, para redactar el apartado de calculos en `Practica_Solar-LaTeX/plantilla.tex` siguiendo las directrices de `Proyecto/Especificaciones/desarrollo-apartado-calculos-plantilla.md`.

El flujo debe ejecutar agentes de forma estrictamente secuencial, nunca simultanea:

1. `.agents/agents/solar-termica-researcher.md`
2. `.agents/agents/latex-writer.md`
3. `.agents/agents/latex-validator.md`

## Cambios Clave

- Definir que `task-orchestrator.md` actua como coordinador unico del proceso.
- Asegurar que antes de cada tarea se referencien explicitamente estos archivos:
  - `Practica_Solar-LaTeX/plantilla.tex`
  - `Proyecto/Especificaciones/desarrollo-apartado-calculos-plantilla.md`
  - `.agents/agents/task-orchestrator.md`
  - `.agents/agents/solar-termica-researcher.md`
  - `.agents/agents/latex-writer.md`
  - `.agents/agents/latex-validator.md`
- El orquestador debe impedir ejecucion paralela y pasar el resultado de cada agente al siguiente.
- El investigador debe preparar criterios tecnicos y contenido base para calculos solares termicos.
- El escritor LaTeX debe integrar el apartado en `plantilla.tex`.
- El validador debe revisar compilabilidad, coherencia LaTeX, estructura, referencias y cumplimiento de las directrices.

## Fases De Implementacion

### Fase 1: Preparar Orquestacion Secuencial

Configurar el flujo logico en torno a `.agents/agents/task-orchestrator.md`.

Criterios de aceptacion:

- El plan de ejecucion lista los agentes en orden fijo.
- No hay tareas simultaneas.
- Cada paso declara entradas y salidas.
- Todos los archivos relevantes quedan referenciados explicitamente.

### Fase 2: Investigacion Tecnica

Ejecutar conceptualmente `.agents/agents/solar-termica-researcher.md` usando como contexto:

- `Proyecto/Especificaciones/desarrollo-apartado-calculos-plantilla.md`
- `Practica_Solar-LaTeX/plantilla.tex`

Criterios de aceptacion:

- Se obtiene una base tecnica para el apartado de calculos.
- Se identifican magnitudes, formulas, supuestos y criterios de redaccion.
- La salida queda preparada para ser consumida por `latex-writer.md`.

### Fase 3: Redaccion En LaTeX

Ejecutar conceptualmente `.agents/agents/latex-writer.md` con la salida de investigacion y las directrices.

Criterios de aceptacion:

- El apartado de calculos queda redactado para integrarse en `Practica_Solar-LaTeX/plantilla.tex`.
- La redaccion respeta la estructura esperada por `desarrollo-apartado-calculos-plantilla.md`.
- El contenido usa sintaxis LaTeX adecuada para ecuaciones, unidades, tablas o referencias internas si proceden.

### Fase 4: Validacion Tecnica Y LaTeX

Ejecutar conceptualmente `.agents/agents/latex-validator.md` sobre el resultado redactado.

Criterios de aceptacion:

- Se revisa que el contenido sea coherente con `plantilla.tex`.
- Se comprueba que el apartado cumpla las directrices del archivo de especificacion.
- Se identifican errores de LaTeX, referencias rotas, formulas mal formadas o problemas de estructura.
- La salida final incluye correcciones concretas o confirmacion de validez.

## Plan De Pruebas

- Verificar que el flujo menciona y usa todos los archivos requeridos.
- Confirmar que el orden de agentes es estrictamente secuencial.
- Revisar que ninguna fase dependa de ejecucion simultanea.
- Validar que la salida final pueda incorporarse a `Practica_Solar-LaTeX/plantilla.tex`.
- Comprobar que el resultado respeta `Proyecto/Especificaciones/desarrollo-apartado-calculos-plantilla.md`.

## Supuestos

- Este plan no lee ni interpreta el contenido interno de los archivos referenciados.
- El contenido real de `plantilla.tex` y de las directrices se consultara durante la implementacion.
- Los agentes se ejecutaran uno detras de otro bajo control de `task-orchestrator.md`.
- La implementacion final modificara `Practica_Solar-LaTeX/plantilla.tex`, pero este plan no realiza cambios.
