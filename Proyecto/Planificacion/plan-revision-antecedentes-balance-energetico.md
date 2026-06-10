# Plan: Revision de Antecedentes y Datos de Partida

> Fuentes de referencia: `Practica_Solar-LaTeX/plantilla.tex`, `Proyecto/Anotaciones/balance-energetico-solar-termica.md` y la grafica correspondiente en `Practica_Solar-LaTeX/Figuras/`.

## Resumen

Actualizar el apartado de antecedentes y datos de partida de `Practica_Solar-LaTeX/plantilla.tex` para incorporar una explicacion clara del balance energetico de una instalacion solar termica, tomando como referencia conceptual `Proyecto/Anotaciones/balance-energetico-solar-termica.md`, e incluir la grafica asociada disponible en `Practica_Solar-LaTeX/Figuras/`.

## Decisiones Principales

- Mantener la estructura LaTeX existente de `plantilla.tex`, integrando el nuevo contenido dentro del apartado actual de antecedentes y datos de partida.
- Incorporar la explicacion del balance energetico como texto tecnico redactado, no como una transcripcion literal extensa.
- Anadir la grafica mediante el mecanismo de figuras ya usado en la plantilla, con pie de figura, etiqueta `\label{...}` y referencia cruzada desde el texto.
- Mantener un tono academico y coherente con una practica de energia solar termica.

## Fase 1: Localizar el punto de integracion

Identificar en `plantilla.tex` el bloque correspondiente a antecedentes y datos de partida, delimitando donde debe entrar la nueva explicacion sin alterar apartados ajenos.

### Criterios de aceptacion

- [ ] El nuevo contenido queda dentro del apartado correcto.
- [ ] No se cambia la estructura general del documento.
- [ ] No se modifican secciones no relacionadas.

## Fase 2: Incorporar la explicacion del balance energetico

Anadir una explicacion breve y tecnica del balance energetico aplicado a la instalacion solar termica, cubriendo:

- Energia solar captada por los colectores.
- Perdidas termicas del sistema.
- Energia util transferida al fluido o acumulador.
- Relacion entre demanda termica, aporte solar y energia auxiliar.
- Utilidad del balance para justificar el dimensionado y el rendimiento del sistema.

### Criterios de aceptacion

- [ ] El texto queda redactado en estilo academico.
- [ ] La explicacion conecta explicitamente con los datos de partida del proyecto.
- [ ] Se evita duplicar contenido innecesario o introducir desarrollo excesivo.

## Fase 3: Insertar la grafica del balance energetico

Incluir en el apartado la grafica existente en `Practica_Solar-LaTeX/Figuras/`, usando una figura LaTeX con:

- Ruta relativa coherente con el resto del documento.
- Tamano adecuado para lectura.
- Pie de figura descriptivo.
- Etiqueta estable para referencia cruzada.
- Mencion en el texto antes o despues de la figura.

### Criterios de aceptacion

- [ ] La grafica aparece integrada en el flujo del apartado.
- [ ] El pie de figura explica que representa.
- [ ] La figura se referencia desde el texto mediante `\ref` o equivalente.

## Fase 4: Revision de coherencia LaTeX

Comprobar que la edicion mantiene coherencia formal con la plantilla:

- Sintaxis LaTeX valida.
- Referencias y etiquetas sin conflicto evidente.
- Nombres de figuras y rutas compatibles.
- Estilo de redaccion uniforme con el resto del documento.

### Criterios de aceptacion

- [ ] El documento compila sin errores derivados de esta modificacion.
- [ ] No hay referencias rotas introducidas por la nueva figura.
- [ ] La ubicacion de la grafica no interrumpe la lectura del apartado.

## Pruebas y Verificacion

- Compilar `plantilla.tex` con el flujo habitual del proyecto.
- Revisar el PDF generado para confirmar que el texto aparece en antecedentes y datos de partida.
- Verificar que la grafica se renderiza correctamente y no queda desbordada, cortada o mal ubicada.
- Confirmar que el pie de figura y la referencia cruzada aparecen correctamente numerados.
- Hacer una lectura final del apartado para comprobar continuidad tecnica entre antecedentes, datos de partida y balance energetico.

## Supuestos

- La grafica necesaria ya existe dentro de `Practica_Solar-LaTeX/Figuras/`.
- El documento ya dispone de soporte LaTeX para insertar figuras.
- La actualizacion debe limitarse al apartado de antecedentes y datos de partida.
- No se requiere crear una nueva metodologia de calculo, solo explicar e integrar el balance energetico como fundamento tecnico.
