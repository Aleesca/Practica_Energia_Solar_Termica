# Plan: Implementación de Antecedentes y Datos de Partida

> Source PRD: PRD conversacional sobre creación del PRD local y redacción del apartado `Antecedentes y datos de partida` en `Practica_Solar-LaTeX/plantilla.tex`.

## Resumen
Convertir el PRD anterior en una implementación por fases, usando el flujo de agentes definido en `.agents/agents/`. El resultado operativo será un PRD local, una base técnica trazable, una redacción modular y la consolidación final en LaTeX.

## Decisiones Arquitectónicas
- **Destino del PRD**: crear un archivo local Markdown, recomendado en `Proyecto/Planificacion/prd_antecedentes_datos_partida.md`.
- **Plan de implementación**: guardar el plan generado por `prd-to-plan` en `plans/antecedentes-datos-partida.md` cuando se active la ejecución.
- **Orquestación**: usar `task-orchestrator` como coordinador principal.
- **Investigación**: usar `solar-termica-researcher` para recopilar datos, fuentes, cálculos, huecos y trazabilidad.
- **Redacción intermedia**: preparar contenido modular en `Proyecto/Especificaciones/` antes de tocar LaTeX.
- **Consolidación final**: usar `latex-writer` para insertar contenido solo en la sección existente `\section{Antecedentes y datos de partida}`.
- **Validación**: usar `latex-validator` para validación semántica, estática y, al final, compilación real.

---

## Phase 1: Crear PRD Local

**User stories**: disponer de un PRD local que gobierne la redacción del apartado y evite decisiones implícitas durante la ejecución.

### What to build
Crear un PRD Markdown con la estructura de `write-a-prd`: problema, solución, historias de usuario, decisiones de implementación, decisiones de prueba, fuera de alcance y notas. El PRD debe dejar claro que los adjuntos se mencionan como fuentes pendientes hasta que se autorice su lectura.

### Acceptance criteria
- [ ] Existe un PRD local en `Proyecto/Planificacion/prd_antecedentes_datos_partida.md`.
- [ ] El PRD define como salida final la sección `Antecedentes y datos de partida` en `plantilla.tex`.
- [ ] El PRD exige trazabilidad de datos técnicos y marca los adjuntos como pendientes de lectura.
- [ ] El PRD declara fuera de alcance la modificación de secciones no relacionadas de la plantilla.

---

## Phase 2: Abrir Tarea con `task-orchestrator`

**User stories**: coordinar el trabajo documental sin activar agentes fuera del flujo permitido.

### What to build
Preparar la tarea objetivo para el orquestador con sección, entradas canónicas, salida esperada y huecos. El orquestador debe reconocer que la salida primaria técnica es modular y que LaTeX es consolidación posterior.

### Acceptance criteria
- [ ] La tarea objetivo queda definida como `Antecedentes y datos de partida`.
- [ ] Las fuentes canónicas disponibles quedan listadas: `Proyecto/Alcance.md`, `Proyecto/Anotaciones/`, `Proyecto/Especificaciones/`, `00_Data/`, `Calculos/` y `Practica_Solar-LaTeX/plantilla.tex`.
- [ ] Las fuentes ausentes quedan señaladas sin bloquear el flujo.
- [ ] La tarea restringe agentes a `solar-termica-researcher`, `latex-writer` y `latex-validator`.

---

## Phase 3: Investigar Fuentes Técnicas

**User stories**: reunir datos fiables para antecedentes, contexto, condiciones de partida y huecos sin redactar todavía la memoria final.

### What to build
Encargar a `solar-termica-researcher` un informe técnico trazable por fuentes, datos, cálculos, artefactos reutilizables y vacíos. Debe distinguir energía solar térmica, respaldo de gas natural, condicionantes físicos del edificio y normativa aplicable.

### Acceptance criteria
- [ ] El informe cita cada fuente usada.
- [ ] Los datos técnicos relevantes quedan separados de los huecos.
- [ ] No se inventan datos, figuras ni normativa.
- [ ] Los adjuntos no leídos quedan marcados como pendientes de verificación.
- [ ] El informe recomienda qué debe entrar y qué debe quedar fuera de la redacción.

---

## Phase 4: Redactar Base Modular

**User stories**: disponer de un borrador técnico revisable antes de consolidar en LaTeX.

### What to build
Crear o actualizar una especificación Markdown en `Proyecto/Especificaciones/` con la redacción base del apartado. La estructura debe separar antecedentes, datos de partida, criterios asumidos y datos pendientes.

### Acceptance criteria
- [ ] Existe una especificación modular para `Antecedentes y datos de partida`.
- [ ] La redacción no introduce teoría general sin soporte documental.
- [ ] Cada dato técnico queda trazado o marcado como pendiente.
- [ ] La redacción mantiene separados el sistema solar térmico y el respaldo de gas natural.
- [ ] El contenido está listo para transformación editorial a LaTeX.

---

## Phase 5: Consolidar en `plantilla.tex`

**User stories**: integrar el contenido validado en la memoria LaTeX sin alterar la estructura principal del documento.

### What to build
Usar `latex-writer` para convertir la base modular en contenido LaTeX e insertarlo dentro de `\section{Antecedentes y datos de partida}` en `Practica_Solar-LaTeX/plantilla.tex`.

### Acceptance criteria
- [ ] La sección existente se conserva y se rellena con contenido técnico validado.
- [ ] No se crean secciones principales nuevas.
- [ ] Las tablas usan formato compatible con el proyecto.
- [ ] Las figuras y citas solo se incluyen si están verificadas.
- [ ] No hay rutas absolutas en recursos LaTeX.

---

## Phase 6: Validar y Cerrar

**User stories**: confirmar que el contenido es coherente, compilable y trazable antes de dar la tarea por terminada.

### What to build
Aplicar `latex-validator` sobre el resultado. Validar coherencia semántica, formato estático y compilación de `Practica_Solar-LaTeX/plantilla.tex` cuando exista contexto compilable.

### Acceptance criteria
- [ ] La validación semántica pasa contra PRD, alcance y fuentes usadas.
- [ ] La validación estática no detecta problemas críticos de LaTeX.
- [ ] La compilación de `plantilla.tex` no presenta errores críticos.
- [ ] El cierre documenta fuentes usadas, salida generada, validación aplicada y pendientes reales.

## Supuestos
- El plan parte del PRD conversacional anterior, no de un archivo PRD ya existente.
- En Plan Mode no se crean archivos ni se modifica el repositorio.
- Al ejecutar, el plan debe guardarse según la skill `prd-to-plan` en `plans/antecedentes-datos-partida.md`.
