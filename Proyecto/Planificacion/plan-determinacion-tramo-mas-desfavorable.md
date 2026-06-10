# Plan: Determinar Tramo Más Desfavorable y Documentar Datos del Excel

## Resumen

Se realizará primero una verificación documental y después el cálculo, sin modificar el Excel. La implementación usará como fuente normativa el notebook `Energia_solar_termica`, extraerá los datos de `Calculos/herramienta_calculo.xlsm`, determinará el tramo más desfavorable según esos criterios y dejará una anotación Markdown en `Proyecto/Anotaciones/` con todos los datos relevantes del Excel y la conclusión.

## Cambios y Entregables

- Consultar el notebook `Energia_solar_termica` para identificar explícitamente los criterios de tramo más desfavorable.
- Leer `Calculos/herramienta_calculo.xlsm` en modo no destructivo, preservando hojas, tablas, valores, fórmulas visibles y unidades cuando estén disponibles.
- Determinar el tramo más desfavorable aplicando solo los criterios encontrados en el notebook, sin introducir criterios externos salvo que falte información.
- Crear un archivo Markdown en `Proyecto/Anotaciones/`, por ejemplo `datos_herramienta_calculo.md`, con:
  - origen del archivo Excel;
  - fecha de extracción;
  - listado estructurado de datos por hoja/sección;
  - criterios aplicados;
  - tabla comparativa de tramos;
  - tramo identificado como más desfavorable;
  - observaciones sobre datos faltantes, fórmulas no evaluables o supuestos.
- No editar `herramienta_calculo.xlsm`.

## Procedimiento de Implementación

1. Identificar el notebook `Energia_solar_termica` disponible en NotebookLM y consultar los criterios sobre pérdida de carga, caudal, longitud, diámetro, accesorios, altura manométrica u otros factores que el notebook establezca.
2. Abrir el `.xlsm` solo para lectura. Si hay valores calculados cacheados, usarlos; si no, intentar recalcular con Excel/COM en modo no destructivo y cerrar sin guardar.
3. Inventariar las hojas y localizar las secciones relacionadas con tramos de instalación.
4. Normalizar los datos necesarios para comparar tramos: nombre del tramo, longitud, caudal, diámetro, material, pérdidas lineales, pérdidas singulares, accesorios, altura o cualquier campo exigido por el criterio del notebook.
5. Aplicar el criterio del notebook para ordenar/comparar los tramos.
6. Generar el Markdown en `Proyecto/Anotaciones/` con todos los datos extraídos y una conclusión trazable.
7. Revisar que el Markdown permita auditar cómo se llegó al tramo más desfavorable.

## Criterios de Validación

- El criterio usado queda citado o resumido desde el notebook, no inferido libremente.
- El tramo seleccionado puede verificarse desde una tabla comparativa.
- Todos los datos usados del Excel aparecen en el Markdown.
- Las fórmulas no evaluadas, celdas vacías o unidades ambiguas quedan marcadas como observaciones.
- El Excel original queda sin cambios.

## Supuestos

- El notebook `Energia_solar_termica` está disponible para consulta mediante NotebookLM o una fuente local accesible.
- El Excel contiene datos suficientes para identificar tramos de instalación.
- Si el Excel requiere macros para recalcular resultados, se priorizarán valores ya calculados o recálculo seguro sin guardar cambios.
- El archivo Markdown final se ubicará en `Proyecto/Anotaciones/` y no reemplazará anotaciones existentes salvo que el usuario indique un nombre concreto.
