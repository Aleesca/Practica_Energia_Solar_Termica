# Plan de Implementación: Determinación del caudal específico del fluido caloportador

## Resumen

El objetivo es preparar una anotación técnica que consulte NotebookLM en el cuaderno `Catalogos_solar` para sintetizar las características ya definidas de la instalación solar térmica y determinar el caudal específico necesario del fluido caloportador, expresado en `L/(h·m²)`.

Entregables previstos:

- Plan: `Proyecto/Planificacion/plan-fluido-caloportador-solar-termica.md`
- Explicación técnica: `Proyecto/Anotaciones/fluido-caloportador-solar-termica.md`

## Decisiones Arquitectónicas

- **Cuaderno NotebookLM**: `Catalogos_solar`, usando el ID ya documentado `7d1bf88b-463a-4291-9201-1959144a5921`.
- **Consulta técnica**: usar `nlm notebook query` o herramienta equivalente de NotebookLM para preguntar por el caudal recomendado del fluido caloportador para los captadores seleccionados y por los criterios de diseño aplicables.
- **Base del cálculo**: priorizar el dato de catálogo/fabricante recuperado en NotebookLM y acompañarlo de una justificación técnica.
- **Unidad final obligatoria**: `L/(h·m²)`.
- **Documento final**: Markdown independiente en `Proyecto/Anotaciones/`, legible sin depender de la conversación.

## Fases de Implementación

### Fase 1: Consulta técnica a NotebookLM

**Historias cubiertas**: obtener de `Catalogos_solar` las características relevantes de la instalación y de los captadores solares ya seleccionados.

**Qué construir**

Realizar una consulta al cuaderno `Catalogos_solar` que solicite:

- Características técnicas relevantes de la instalación solar térmica definida hasta el momento.
- Modelo de captador seleccionado y superficie de referencia aplicable.
- Recomendación de caudal del circuito primario o del fluido caloportador.
- Unidad original del dato y conversión, si procede, a `L/(h·m²)`.
- Fuentes concretas citadas por NotebookLM.

**Criterios de aceptación**

- [ ] La respuesta identifica el captador o familia de captadores usada en el proyecto.
- [ ] La respuesta aporta un valor de caudal específico o los datos necesarios para calcularlo.
- [ ] Las citas o referencias del cuaderno quedan recogidas para el documento final.
- [ ] Si hay más de un valor posible, se justifica cuál se adopta.

---

### Fase 2: Determinación del caudal específico

**Historias cubiertas**: convertir la información de catálogo en un valor técnico utilizable para diseño.

**Qué construir**

Analizar la respuesta de NotebookLM y fijar el valor de diseño del caudal específico del fluido caloportador en `L/(h·m²)`. Si el catálogo entrega un caudal por captador, convertirlo dividiendo por la superficie de referencia correspondiente. Si entrega un rango, seleccionar un valor de diseño y justificarlo.

Fórmula de referencia:

```text
q_especifico = Q_captador / A_referencia
```

donde:

- `q_especifico` se expresa en `L/(h·m²)`.
- `Q_captador` es el caudal recomendado por captador en `L/h`.
- `A_referencia` es la superficie de apertura, absorción o captación usada por el catálogo.

**Criterios de aceptación**

- [ ] El documento distingue claramente dato de catálogo, conversión y valor adoptado.
- [ ] La superficie usada para normalizar el caudal queda identificada.
- [ ] El resultado final aparece de forma explícita en `L/(h·m²)`.
- [ ] Se explica si el valor corresponde a caudal bajo, nominal o recomendado por fabricante.

---

### Fase 3: Redacción del Markdown explicativo

**Historias cubiertas**: entregar una explicación técnica clara y reutilizable dentro del proyecto.

**Qué construir**

Crear `Proyecto/Anotaciones/fluido-caloportador-solar-termica.md` con esta estructura:

1. Contexto de la instalación solar térmica.
2. Características relevantes recuperadas de `Catalogos_solar`.
3. Dato de caudal del fabricante o fuente técnica.
4. Cálculo o conversión a `L/(h·m²)`.
5. Valor de diseño adoptado.
6. Implicaciones para el circuito primario: bomba, equilibrado hidráulico y compatibilidad con captadores.
7. Referencias y citas del notebook.

**Criterios de aceptación**

- [ ] El archivo contiene una explicación completa y trazable.
- [ ] El valor final de caudal específico es fácil de localizar.
- [ ] Las referencias a NotebookLM y documentos fuente quedan incluidas.
- [ ] La redacción mantiene el estilo técnico de las anotaciones existentes del proyecto.

## Plan de Verificación

- Comprobar que el nombre del cuaderno y su ID coinciden con los usados en planes previos.
- Verificar que la consulta a NotebookLM devuelve fuentes relacionadas con captadores solares y caudal del circuito primario.
- Revisar la coherencia dimensional de la conversión a `L/(h·m²)`.
- Comparar el valor adoptado con rangos habituales de diseño para instalaciones solares térmicas.
- Confirmar que el Markdown final puede leerse como documento independiente.

## Supuestos

- El cuaderno correcto es `Catalogos_solar` con ID `7d1bf88b-463a-4291-9201-1959144a5921`.
- La instalación solar térmica mantiene la selección ya documentada de captadores Viessmann y esquema centralizado.
- Si NotebookLM proporciona varios caudales admisibles, se adoptará el recomendado por fabricante o el valor nominal más conservador técnicamente.
- Antes de ejecutar la consulta será necesario refrescar la autenticación de NotebookLM si sigue caducada.
