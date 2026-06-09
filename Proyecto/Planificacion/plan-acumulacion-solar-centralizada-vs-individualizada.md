# Plan: Consulta sobre acumulacion solar centralizada vs individualizada

## Resumen

El objetivo es redactar una anotacion tecnica en Markdown que resuelva si es mejor una acumulacion solar centralizada o individualizada para un edificio plurifamiliar con instalacion de gas natural existente.

La nota debe aclarar si la instalacion receptora de gas natural, con contadores en vivienda y conexion a redes en media presion A, condiciona realmente la eleccion del sistema solar, o si la decision depende sobre todo del esquema de ACS, del espacio disponible, del apoyo termico y de la arquitectura hidraulica.

El resultado final se guardara en `Proyecto/Anotaciones/` y dejara indicado que la validacion tecnica se apoyara en `exa deep search`.

## Cambios clave

- Redactar una comparativa tecnica entre:
  - acumulacion solar centralizada,
  - acumulacion solar individualizada,
  - relacion de ambas opciones con la instalacion existente de gas natural.
- Consultar los notebooks `Catalogos_solar` y `Energia_solar_termica`.
- Usar el MCP de `exa deep search` para contraste tecnico y documental externo.
- Dejar una conclusion clara sobre:
  - si la instalacion de gas condiciona o no la decision,
  - en que casos conviene centralizar,
  - en que casos conviene individualizar.

## Estructura del archivo final

1. Pregunta tecnica
2. Contexto de la instalacion existente
3. Consulta a notebooks
4. Consulta externa con Exa Deep Search
5. Comparacion tecnica
6. Relacion con la instalacion de gas natural
7. Conclusion recomendada

## Criterios de aceptacion

- El archivo se crea en `Proyecto/Planificacion/`.
- El contenido deja claro que la respuesta se construira con notebooks y con `exa deep search`.
- La conclusion distingue entre la instalacion solar y la instalacion de gas, sin mezclar ambas como si fueran el mismo sistema.
- No se ejecuta ninguna consulta a NotebookLM en esta fase.

## Supuestos

- No se leen archivos adjuntos ni se conecta al notebook durante esta fase.
- El plan es solo documental; la implementacion y la investigacion quedan para una fase posterior.
- Si no aparece una restriccion normativa concreta, se asumira que la decision entre acumulacion centralizada e individualizada no depende por si sola del tipo de instalacion receptora de gas.
