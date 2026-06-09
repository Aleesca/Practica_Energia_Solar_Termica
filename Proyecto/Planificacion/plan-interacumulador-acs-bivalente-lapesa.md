# Plan de Implementacion: Recomendacion de Interacumulador ACS Bivalente Lapesa

## Resumen

El objetivo de este plan es definir el proceso para comprobar, a partir de los notebooks `Catalogo_solar` y `Energia_Solar_Termica`, que deposito de acumulacion sugerido corresponde a una instalacion con:

- 10 captadores sugeridos
- 23,3 m2 de superficie de captacion sugerida
- 1500 L de volumen de acumulacion sugerido

Si la informacion no aparece en los notebooks, se hara una busqueda complementaria con MCP `exa deep search`. Con los datos obtenidos se ajustara la recomendacion de un interacumulador ACS bivalente Lapesa disponible en el catalogo de `Catalogo_solar`.

El resultado final se documentara en un nuevo archivo Markdown dentro de `Proyecto/Anotaciones/` y se revisara `Proyecto/Anotaciones/seleccion-equipos-solar-centralizado.md` para mantener coherencia tecnica.

## Cambios clave

- Verificar primero en `Energia_Solar_Termica` la relacion entre superficie de captacion, numero de captadores y volumen de acumulacion recomendado.
- Verificar en `Catalogo_solar` los modelos Lapesa disponibles y filtrar los interacumuladores ACS bivalentes compatibles con 1500 L o con la equivalencia tecnica mas cercana.
- Usar `exa deep search` solo si los notebooks no aportan la informacion necesaria para justificar la recomendacion.
- Redactar una recomendacion tecnica final con:
  - modelo recomendado,
  - volumen nominal,
  - justificacion por compatibilidad con 23,3 m2 y 10 captadores,
  - alternativa si no existe coincidencia exacta.
- Actualizar o revisar la nota existente `seleccion-equipos-solar-centralizado.md` para alinear la decision de acumulacion con la nueva recomendacion.

## Estructura del archivo final

1. Datos de partida
2. Consulta en `Energia_Solar_Termica`
3. Consulta en `Catalogo_solar`
4. Búsqueda externa con `exa deep search` si hace falta
5. Comparativa de candidatos Lapesa
6. Recomendacion final del interacumulador
7. Revisión de coherencia con la anotacion existente

## Criterios de aceptacion

- El plan queda guardado en `Proyecto/Planificacion/plan-interacumulador-acs-bivalente-lapesa.md`.
- La investigacion se basa primero en los notebooks y solo usa `exa deep search` como apoyo si falta informacion.
- La recomendacion final identifica un unico modelo principal o explica claramente la alternativa elegida.
- Se deja preparado el contenido para crear un nuevo `.md` en `Proyecto/Anotaciones/`.
- Se revisa `Proyecto/Anotaciones/seleccion-equipos-solar-centralizado.md` sin romper su coherencia tecnica.

## Supuestos

- Se toma como valido el objetivo de 1500 L salvo que la documentacion indique una correccion tecnica justificable.
- Si no existe un modelo exacto de 1500 L en Lapesa, se elegira el mas cercano por volumen y compatibilidad tecnica.
- No se ejecuta ninguna consulta a los notebooks ni a Exa en esta fase.
- El alcance es documental y de planificacion; la implementacion queda para una fase posterior.
