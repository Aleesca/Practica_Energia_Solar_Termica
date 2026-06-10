# Plan: Desarrollo de la explicacion del circuito secundario solar

> Fuentes: `Proyecto/Anotaciones/justificacion-circuito-secundario.md`, con apoyo contextual de `Proyecto/Anotaciones/justificacion-circuito-primario-solar.md` y `Proyecto/Anotaciones/justificacion-circuito-distribucion-acs.md`.

## Resumen

El objetivo es preparar la futura redaccion tecnica de la explicacion del circuito secundario solar. El plan debe extraer de la nota existente todos los datos, formulas y metodologia relacionados con el circuito de agua que recibe el calor del primario a traves del intercambiador del acumulador. No se implementa la explicacion final ni se leen adjuntos.

## Cambios principales

- Explicar la funcion del circuito secundario como circuito de agua asociado al acumulador y al intercambio termico con el circuito primario solar.
- Diferenciar el fluido del secundario, agua, respecto al fluido caloportador con anticongelante del circuito primario.
- Documentar el calculo del caudal del secundario a partir de la superficie total de captacion y del caudal especifico adoptado.
- Recoger el dimensionamiento de los tramos principales: DN28, diametro interior, velocidad, perdidas de carga y altura manometrica minima.
- Documentar la potencia minima del intercambiador de calor centralizado o serpentín del acumulador.
- No incorporar informacion de Excel, PDFs, catalogos u otros adjuntos.

## Datos y tablas a extraer

- Datos base del campo solar:
  - Numero de captadores: 12.
  - Superficie por captador: 2,33 m2.
  - Superficie total de captacion: 27,96 m2.
- Caudal secundario:
  - Caudal especifico adoptado: 50 l/h*m2.
  - Caudal de diseno del circuito secundario: 1.398 l/h.
- Dimensionamiento hidraulico:
  - Diametro adoptado en tramos principales: DN28.
  - Diametro interior considerado: 26 mm.
  - Velocidad aproximada: 0,73 m/s.
- Perdidas de carga:
  - Perdida de carga en tuberias: 0,63 m.c.a.
  - Perdida de carga en intercambiador, lado secundario: 1,30 m.c.a.
  - Perdida total: 1,93 m.c.a.
  - Criterio de bomba: caudal de 1.398 l/h y altura minima de 1,93 m.c.a.
  - Margen comercial recomendado: aproximadamente 2,0 a 2,5 m.c.a.
- Intercambiador:
  - Criterio de potencia minima: 600 W/m2.
  - Potencia calculada: 16.776 W.
  - Potencia redondeada: 16,8 kW.

## Metodologia y formulas

- Superficie total:
  `S_total = numero de captadores * superficie por captador`
- Caudal secundario:
  `Q_secundario = S_total * caudal especifico`
- Perdida de carga total:
  `Pdc_total = Pdc_tuberias + Pdc_intercambiador`
- Potencia minima de intercambio:
  `P = 600 * S_total`

## Criterios de validacion

- El plan queda centrado en el circuito secundario y no reescribe el primario ni la distribucion ACS.
- Todos los datos numericos del documento fuente quedan recogidos en tablas o formulas.
- La futura explicacion distingue con claridad circuito primario, circuito secundario y red de distribucion.
- La seleccion de bomba queda definida por caudal y altura minima, dejando margen para seleccion comercial posterior.
- No se leen archivos adjuntos ni fuentes no indicadas.

## Supuestos

- Este archivo es un plan pendiente de implementacion, no la explicacion tecnica final.
- La fuente principal es `justificacion-circuito-secundario.md`.
- No se modificara `plantilla.tex`, el Excel de calculo ni las anotaciones existentes durante esta fase.
