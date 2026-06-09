# Plan: Balance energético solar térmico

## Resumen

Preparar un documento independiente que recoja la tabla de balances energéticos y la gráfica original extraídas de `Calculos/herramienta_calculo.xlsm`, y enlazar ese análisis con `Proyecto/Anotaciones/seleccion-interacumulador-acs-bivalente-lapesa.md`.

La discusión técnica se apoyará en una consulta a NotebookLM sobre el notebook `Energía_solar_térmica` para identificar las 3 limitaciones técnicas principales, los meses más críticos y su impacto sobre la selección del interacumulador.

## Cambios Clave

- Extraer del archivo `.xlsm` la tabla mensual de balance energético y la gráfica original asociada.
- Reutilizar la gráfica existente del Excel en formato de imagen, sin recrearla mediante script Python.
- Crear un Markdown independiente para la discusión del balance energético, con tabla, imagen, interpretación mensual y conclusiones técnicas.
- Añadir una referencia desde la nota del interacumulador al nuevo documento de balance.
- Incorporar una síntesis técnica basada en NotebookLM con las 3 limitaciones principales y los meses más críticos.

## Entregables

- `Proyecto/Anotaciones/balance-energetico-solar-termica.md`
- Imagen exportada de la gráfica original del Excel
- Referencia cruzada desde `Proyecto/Anotaciones/seleccion-interacumulador-acs-bivalente-lapesa.md`

## Plan de Verificación

- Comprobar que la tabla incorporada coincide con los valores del Excel.
- Verificar que la imagen enlazada corresponde a la gráfica original y no a una recreación.
- Revisar que el documento independiente puede leerse sin depender de contexto externo.
- Confirmar que la nota del interacumulador enlaza al nuevo análisis.
- Validar que la discusión técnica recoge las 3 limitaciones, los meses críticos y su relación con la cobertura energética.

## Supuestos

- El notebook de NotebookLM se denomina exactamente `Energía_solar_térmica`.
- La gráfica de balance ya existe en `herramienta_calculo.xlsm`.
- El documento independiente se guardará en `Proyecto/Anotaciones/`.
- La imagen exportada se guardará en una ruta estable dentro de `Proyecto/Anotaciones/`.
