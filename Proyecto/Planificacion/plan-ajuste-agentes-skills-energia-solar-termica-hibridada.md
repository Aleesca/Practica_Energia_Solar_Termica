# Plan: Ajuste de agentes y skills al proyecto de energia solar termica hibridada con gas natural

> Fuente: solicitud de planificacion para adaptar `.agents/`, especialmente `.agents/agents/glp-researcher.md` y `.agents/skills/doc_tecnica_glp/`, al nuevo proyecto de energia solar termica hibridada al sistema de gas natural.

## Decisiones arquitectonicas

Decisiones estables que aplican durante toda la implementacion:

- **Dominio objetivo**: energia solar termica hibridada con gas natural.
- **Alcance documental**: todos los agentes y skills bajo `.agents/` deben quedar alineados con el nuevo dominio, manteniendo referencias cruzadas consistentes entre agentes, skills, flujos de trabajo y documentacion tecnica.
- **Agente principal a transformar**: el agente actual relacionado con GLP pasa a representar investigacion y soporte del sistema solar termico hibridado con gas natural.
- **Skill principal a transformar**: la skill actual `doc_tecnica_glp` pasa a cubrir documentacion tecnica del sistema solar termico hibridado con gas natural.
- **Referencias cruzadas**: cada agente o skill que dependa de otro debe enlazarlo por nombre final, ruta final y responsabilidad final.
- **Trazabilidad**: las menciones a GLP se conservaran solo cuando sean historicas, comparativas o necesarias para migracion; el nuevo lenguaje por defecto sera energia solar termica, hibridacion, respaldo de gas natural, seguridad, dimensionamiento, operacion y documentacion tecnica.
- **Renombrado final**: los renombrados se realizaran despues de ajustar contenido y referencias, para reducir enlaces rotos intermedios.
- **Validacion**: cada fase debe dejar una salida verificable: inventario, matriz de cambios, contenido actualizado, referencias cruzadas, renombrado y comprobacion final.

---

## Phase 1: Inventario controlado de agentes y skills

**Historias cubiertas**: como mantenedor del proyecto, necesito saber que agentes y skills existen y como se relacionan antes de modificar el sistema.

### What to build

Realizar un inventario de `.agents/` cuando comience la implementacion, identificando agentes, skills, rutas, nombres publicados, dependencias declaradas, menciones a GLP y referencias internas. Esta fase no modifica archivos; produce una base de decision para el resto del trabajo.

### Acceptance criteria

- [ ] Existe un inventario de agentes y skills bajo `.agents/`.
- [ ] Estan identificadas las referencias a `glp-researcher.md` y `doc_tecnica_glp`.
- [ ] Estan identificadas las menciones de GLP que deben migrarse, conservarse o eliminarse.
- [ ] Estan identificadas las referencias cruzadas existentes y las referencias ausentes.
- [ ] No se ha modificado ningun archivo funcional o documental en esta fase.

---

## Phase 2: Taxonomia del nuevo dominio y matriz de migracion

**Historias cubiertas**: como responsable tecnico, necesito que el cambio de GLP a energia solar termica hibridada con gas natural sea coherente en vocabulario, responsabilidades y limites.

### What to build

Definir la taxonomia comun del nuevo proyecto: nombre del sistema, componentes principales, roles de agentes, responsabilidades de skills, criterios de seguridad, calculo, normativa, documentacion y operacion. Con esa taxonomia, construir una matriz que indique como se transforma cada referencia GLP al nuevo dominio.

### Acceptance criteria

- [ ] Existe una nomenclatura canonica para energia solar termica hibridada con gas natural.
- [ ] Cada termino GLP relevante tiene una decision: migrar, conservar con contexto, sustituir o eliminar.
- [ ] La matriz cubre agentes, skills, nombres visibles, descripciones, rutas sugeridas y referencias cruzadas.
- [ ] Las responsabilidades del agente principal y de la skill tecnica quedan diferenciadas.
- [ ] La taxonomia puede aplicarse de forma repetible al resto de `.agents/`.

---

## Phase 3: Adaptacion del agente de investigacion

**Historias cubiertas**: como usuario del proyecto, necesito un agente especializado que investigue y razone sobre energia solar termica hibridada con gas natural, no sobre GLP como dominio principal.

### What to build

Actualizar el agente actualmente denominado `glp-researcher.md` para que su proposito, instrucciones, criterios de busqueda, fuentes esperadas, limites tecnicos y salidas se orienten al sistema solar termico hibridado con gas natural. El agente debe enlazar a la skill tecnica transformada y a las demas skills relevantes.

### Acceptance criteria

- [ ] El agente describe el nuevo dominio con precision.
- [ ] Las instrucciones de investigacion cubren solar termica, integracion hidraulica, respaldo con gas natural, seguridad, regulacion, rendimiento y mantenimiento.
- [ ] Las referencias a GLP han sido migradas segun la matriz de migracion.
- [ ] El agente referencia las skills pertinentes por nombre y ruta final previstos.
- [ ] El agente conserva una seccion de limites y supuestos para evitar mezclar GLP, gas natural y solar termica sin contexto.

---

## Phase 4: Adaptacion de la skill de documentacion tecnica

**Historias cubiertas**: como redactor o tecnico, necesito una skill que produzca documentacion tecnica consistente para instalaciones solares termicas hibridadas con gas natural.

### What to build

Transformar la skill actual `doc_tecnica_glp` para que genere, revise o estructure documentacion tecnica del nuevo sistema: memoria tecnica, esquemas, criterios de dimensionamiento, operacion, mantenimiento, seguridad, integracion con gas natural y evidencias de cumplimiento.

### Acceptance criteria

- [ ] La skill declara claramente su nuevo proposito y entradas esperadas.
- [ ] Los flujos de trabajo cubren documentacion tecnica solar termica y respaldo de gas natural.
- [ ] Las plantillas, ejemplos o criterios internos dejan de asumir GLP como combustible principal.
- [ ] La skill enlaza al agente de investigacion actualizado y a las skills complementarias.
- [ ] La skill incluye criterios de salida verificables: estructura documental, supuestos, calculos requeridos, riesgos y referencias.

---

## Phase 5: Ajuste transversal del resto de skills en `.agents/`

**Historias cubiertas**: como mantenedor del repositorio, necesito que todas las skills convivan con el nuevo proyecto y no contradigan al agente o skill principal.

### What to build

Revisar cada skill existente bajo `.agents/skills/` y aplicar ajustes minimos: descripcion, disparadores, referencias al nuevo agente, referencias a la nueva skill tecnica, terminologia compartida y limites de uso. Esta fase debe evitar reescrituras amplias cuando una skill solo necesita un enlace o aclaracion.

### Acceptance criteria

- [ ] Cada skill queda clasificada como afectada, no afectada o dependiente.
- [ ] Las skills afectadas usan la taxonomia comun del nuevo proyecto.
- [ ] Las skills dependientes enlazan al agente y a la skill tecnica con nombres finales.
- [ ] No quedan instrucciones que obliguen a tratar GLP como dominio principal del proyecto.
- [ ] Las modificaciones son proporcionales al rol real de cada skill.

---

## Phase 6: Red de referencias cruzadas

**Historias cubiertas**: como usuario de las skills, necesito saber que agente o skill usar y como pasar de una a otra sin perder contexto.

### What to build

Crear una red explicita de referencias cruzadas: agente principal hacia skill tecnica, skill tecnica hacia agente principal, skills complementarias hacia ambos cuando corresponda, y referencias entre skills auxiliares si comparten entradas o salidas. Las referencias deben usar rutas y nombres finales previstos antes del renombrado.

### Acceptance criteria

- [ ] Cada referencia cruzada incluye nombre, ruta y motivo de uso.
- [ ] El agente principal y la skill tecnica se enlazan mutuamente.
- [ ] Las skills auxiliares enlazan solo cuando hay dependencia real.
- [ ] No existen referencias duplicadas, ambiguas o circulares sin proposito.
- [ ] Hay una matriz final de referencias para validar el renombrado.

---

## Phase 7: Renombrado del agente y de la skill

**Historias cubiertas**: como mantenedor, necesito que los nombres finales reflejen el nuevo proyecto y que los enlaces sigan funcionando.

### What to build

Renombrar el agente `glp-researcher.md` y la skill `doc_tecnica_glp` a nombres alineados con energia solar termica hibridada con gas natural. Actualizar todas las referencias internas a las rutas finales.

### Acceptance criteria

- [ ] El nuevo nombre del agente refleja investigacion sobre energia solar termica hibridada con gas natural.
- [ ] El nuevo nombre de la skill refleja documentacion tecnica del nuevo sistema.
- [ ] Todas las referencias a rutas antiguas se han actualizado o justificado.
- [ ] No quedan enlaces rotos dentro de `.agents/`.
- [ ] La historia de migracion queda documentada en el plan o en una nota de cambios.

---

## Phase 8: Validacion final y entrega

**Historias cubiertas**: como responsable del proyecto, necesito una comprobacion final que demuestre que la migracion es coherente y usable.

### What to build

Ejecutar una revision final de consistencia: nombres, rutas, referencias cruzadas, lenguaje del nuevo dominio, ausencia de contradicciones, cobertura de todas las skills y trazabilidad de decisiones. Preparar un resumen de entrega con archivos modificados, renombrados realizados, riesgos residuales y recomendaciones.

### Acceptance criteria

- [ ] Se verifica que todas las skills bajo `.agents/` han sido consideradas.
- [ ] Se verifica que agente y skill principal usan los nombres finales.
- [ ] Se verifica que no hay referencias internas rotas.
- [ ] Se verifica que el lenguaje tecnico distingue solar termica, gas natural y antiguas referencias a GLP.
- [ ] Se entrega un resumen final con cambios, validaciones y posibles tareas pendientes.

---

## Secuencia recomendada de ejecucion

1. Inventariar `.agents/` sin modificar contenido.
2. Definir taxonomia y matriz de migracion.
3. Actualizar primero el agente principal.
4. Actualizar despues la skill tecnica principal.
5. Ajustar el resto de skills por dependencia real.
6. Completar referencias cruzadas.
7. Renombrar agente y skill.
8. Validar enlaces, terminologia y cobertura.

## Riesgos y controles

- **Riesgo**: dejar referencias a GLP como dominio principal.
  **Control**: busqueda final por terminos GLP y revision caso por caso.
- **Riesgo**: romper rutas al renombrar.
  **Control**: renombrado al final, despues de tener la matriz de referencias.
- **Riesgo**: sobreadaptar skills no relacionadas.
  **Control**: clasificacion previa de afectacion y cambios minimos.
- **Riesgo**: mezclar gas natural con GLP en criterios tecnicos.
  **Control**: taxonomia explicita y seccion de limites en agente y skill tecnica.
- **Riesgo**: referencias cruzadas excesivas.
  **Control**: cada enlace debe tener un motivo funcional.

## Salidas esperadas

- Inventario de agentes y skills.
- Matriz de migracion terminologica y funcional.
- Agente principal adaptado y renombrado.
- Skill tecnica adaptada y renombrada.
- Resto de skills ajustadas al nuevo proyecto cuando corresponda.
- Matriz de referencias cruzadas.
- Resumen de validacion final.
