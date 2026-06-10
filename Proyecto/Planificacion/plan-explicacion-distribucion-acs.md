# Plan: Desarrollo de la explicacion del circuito de distribucion de ACS

> Fuente principal: `Proyecto/Anotaciones/justificacion-circuito-distribucion-acs.md`, con apoyo contextual de `Proyecto/Anotaciones/justificacion-circuito-primario-solar.md` y `Proyecto/Anotaciones/justificacion-circuito-secundario.md`.

## Resumen

El objetivo es preparar la futura redaccion tecnica del circuito de distribucion de ACS precalentada y de su retorno de recirculacion. El plan extrae caudales, diametros, grupos de consumo, metodologia y datos tabulables de la nota indicada, sin implementar la explicacion final ni leer adjuntos.

## Cambios principales

- Explicar la red que transporta el agua sanitaria precalentada desde el deposito acumulador hasta las calderas individuales de las viviendas.
- Aclarar que la instalacion solar no alimenta directamente los puntos finales de consumo, sino la entrada de cada caldera individual.
- Documentar el criterio de considerar cada vivienda como un grupo de consumo.
- Recoger los caudales por tramo de bajante, las derivaciones a vivienda y los diametros adoptados.
- Documentar el retorno de recirculacion, su caudal, diametro, velocidad, longitud, perdida de carga y criterio de bomba.
- No incorporar datos procedentes de Excel, PDFs, catalogos u otros adjuntos.

## Datos y tablas a extraer

- Edificio y grupos de consumo:
  - Numero de plantas: 5.
  - Viviendas por planta: 2.
  - Total de viviendas/grupos de consumo: 10.
  - Caudal equivalente por vivienda: 0,25 l/s.
- Grupos por tramo:
  - Bajante - P5: 10 grupos.
  - P5 - P4: 8 grupos.
  - P4 - P3: 6 grupos.
  - P3 - P2: 4 grupos.
  - P2 - P1: 2 grupos.
  - Derivacion a vivienda: 1 grupo.
- Caudales adoptados:
  - Bajante - P5: 2,50 l/s.
  - P5 - P4: 2,00 l/s.
  - P4 - P3: 1,50 l/s.
  - P3 - P2: 1,00 l/s.
  - P2 - P1: 0,50 l/s.
  - Derivacion a vivienda: 0,25 l/s = 900 l/h.
- Diametros adoptados:
  - Bajante - P5: DN42.
  - P5 - P4: DN42.
  - P4 - P3: DN35.
  - P3 - P2: DN28.
  - P2 - P1: DN22.
  - Derivaciones a vivienda: DN18.
- Retorno de recirculacion:
  - Caudal adoptado: 0,10 l/s = 360 l/h.
  - Diametro: DN18.
  - Diametro interior: 16 mm.
  - Velocidad aproximada: 0,50 m/s.
  - Longitud considerada: 17 m.
  - Perdida de carga aproximada: 0,36 m.c.a.
  - Criterio de bomba: 360 l/h y altura suficiente para vencer la perdida del retorno, con margen comercial.

## Metodologia y formulas

- Numero total de viviendas:
  `N = numero de plantas * viviendas por planta`
- Caudal por tramo:
  `Q_tramo = numero de viviendas servidas * 0,25 l/s`
- Conversion de caudal por vivienda:
  `0,25 l/s * 3600 = 900 l/h`
- Conversion de caudal de retorno:
  `0,10 l/s * 3600 = 360 l/h`

## Criterios de validacion

- El plan queda centrado en distribucion de ACS y recirculacion.
- Todos los caudales, diametros y datos del retorno presentes en la fuente quedan recogidos en tablas o formulas.
- La futura explicacion diferencia caudal de consumo y caudal de recirculacion.
- La bomba de recirculacion queda definida por 360 l/h y una perdida aproximada de 0,36 m.c.a., dejando la seleccion comercial para una fase posterior.
- No se leen archivos adjuntos ni fuentes no indicadas.

## Supuestos

- Este archivo es un plan pendiente de implementacion, no la explicacion tecnica final.
- La fuente principal es `justificacion-circuito-distribucion-acs.md`.
- No se modificara `plantilla.tex`, el Excel de calculo ni las anotaciones existentes durante esta fase.
