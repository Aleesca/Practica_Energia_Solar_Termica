# Product Requirements Document (PRD): Antecedentes y Datos de Partida

## Problem Statement

El proyecto de energía solar térmica centralizada hibridada con gas natural necesita una base sólida y documentada para su memoria técnica. Específicamente, la sección de "Antecedentes y datos de partida" en la plantilla LaTeX (`Practica_Solar-LaTeX/plantilla.tex`) está actualmente vacía. Sin un marco de requisitos y datos de partida claro y trazable, existe el riesgo de introducir datos incoherentes o no verificados y de desviar el alcance del proyecto.

## Solution

Desarrollar e implementar la sección de "Antecedentes y datos de partida" de manera modular e iterativa utilizando un flujo multiagente. El proceso consiste en:
1. Crear una base técnica de especificación en Markdown a partir del alcance, notas de ingeniería y datos de partida normalizados.
2. Usar un agente investigador (`solar-termica-researcher`) para recopilar la evidencia y asegurar la trazabilidad de los datos de Salamanca, zona climática, ocupación, demanda de ACS y equipos de referencia.
3. Redactar el contenido modular en Markdown (`Proyecto/Especificaciones/especificacion-antecedentes-y-datos-de-partida.md` o similar).
4. Traducir y consolidar dicho contenido en LaTeX dentro de la sección existente `\section{Antecedentes y datos de partida}` en `Practica_Solar-LaTeX/plantilla.tex` usando `latex-writer`.
5. Validar semántica, estática y dinámicamente el resultado final con `latex-validator`.

## User Stories

1. Como redactor técnico del proyecto, quiero disponer de un PRD local y detallado, para evitar tomar decisiones de diseño implícitas o improvisadas durante la redacción de la memoria.
2. Como ingeniero de diseño, quiero que todos los datos geoclimáticos de Salamanca (latitud, longitud, zona de radiación III, zona climática D2) estén documentados con su fuente de origen, para asegurar el cumplimiento del CTE y RITE.
3. Como diseñador hidráulico, quiero justificar por qué se selecciona un esquema solar térmico centralizado frente a uno distribuido, para que la memoria técnica refleje criterios sanitarios (prevención de legionella RD 487/2022) y de optimización de espacio.
4. Como integrador de sistemas, quiero especificar los equipos de referencia (Viessmann Vitosol 200-FM, Lapesa Master Inox MXV-2000 SS2B) con sus características físicas y el régimen hidráulico (Tichelmann, Low-Flow), para dar soporte a los cálculos hidráulicos y térmicos posteriores.
5. Como revisor del proyecto, deseo que las bombas de circulación se mencionen únicamente como elementos de principio existentes sin dimensionamiento ni selección de modelos, para respetar los límites de exclusión de alcance definidos.
6. Como maquetador de LaTeX, quiero que el fragmento de "Antecedentes y datos de partida" se inserte exclusivamente en la sección existente de `plantilla.tex` sin alterar otras secciones del preámbulo ni de los anexos, para mantener la integridad del documento global.
7. Como validador editorial, quiero verificar estáticamente (booktabs, etiquetas de tablas/figuras, referencias relativas) y dinámicamente (compilación limpia) el archivo LaTeX final, para asegurar la calidad final de la entrega.

## Implementation Decisions

- **Mapeo modular**: El borrador técnico se mantendrá en `Proyecto/Especificaciones/especificacion-antecedentes-y-datos-de-partida.md` como fuente de verdad modular de la sección.
- **Trazabilidad estricta**: Cada dato numérico de entrada (coordenadas, demanda de 1064 L/día, etc.) debe estar mapeado con su fuente de origen en una sección de trazabilidad en la especificación y en el reporte del investigador.
- **Consolidación en LaTeX**: La escritura final en `Practica_Solar-LaTeX/plantilla.tex` se delegará al agente `latex-writer`, quien debe estructurar el contenido en subsecciones acordes a la especificación, respetando la estructura principal de la plantilla.
- **Evitación de duplicados**: Los archivos adjuntos de catálogos y fichas técnicas en los anexos de la plantilla no se modificarán ni se duplicarán; solo se referenciarán de manera lógica.
- **Uso de perfiles de compilación**: La validación de compilación dinámica se realizará utilizando el comando `pdflatex` o el compilador por defecto del proyecto.

## Testing Decisions

- **Validación Semántica**: Contraste automático y por revisión manual entre los datos definitivos del PRD, el alcance, las notas y el texto consolidado en `plantilla.tex`.
- **Validación Estática de LaTeX**: Comprobación estricta de:
  - Formato de tablas con `booktabs` (sin líneas verticales, etc.).
  - Presencia de `\caption{}` y `\label{}` en todas las tablas y figuras.
  - Trazabilidad y resolución de referencias y citas bibliográficas cruzadas.
- **Validación de Compilación**: Ejecución del compilador LaTeX (`pdflatex`) en la carpeta `Practica_Solar-LaTeX/` sobre `plantilla.tex` para asegurar que el documento se genera sin errores críticos (`FAIL`).

## Out of Scope

- Modificación de cualquier sección de la plantilla de LaTeX distinta de `Antecedentes y datos de partida` (por ejemplo, `Cálculos` o `Esquema de principio` no se completarán en esta fase).
- Redacción de teoría solar general o descripciones académicas de relleno no justificadas por los datos de Salamanca o los equipos del proyecto.
- Selección o dimensionamiento de las bombas de circulación de primario, recirculación o calderas.

## Further Notes

- Los adjuntos y fichas técnicas están pre-cargados en la carpeta `Figuras/` de la plantilla LaTeX (por ejemplo, fichas de Viessmann, Lapesa and bombas Grundfos). Se consideran fuentes canonizadas y no deben leerse o re-escribirse a menos que se requiera validar su correspondencia.
