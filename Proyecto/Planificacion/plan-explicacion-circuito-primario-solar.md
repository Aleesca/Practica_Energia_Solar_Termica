# Plan: Desarrollo de la explicacion del circuito primario solar

> Fuentes: `Proyecto/Anotaciones/justificacion-circuito-primario-solar.md`, `Proyecto/Anotaciones/justificacion-circuito-secundario.md` y `Proyecto/Anotaciones/justificacion-circuito-distribucion-acs.md`.

## Resumen

El objetivo es preparar la futura redaccion tecnica de la explicacion del circuito primario solar, extrayendo de las notas existentes todos los calculos, formulas, metodologia y datos tabulables. Este plan no implementa la explicacion final ni modifica documentos de calculo, LaTeX, Excel o adjuntos.

## Cambios principales

- Explicar la funcion del circuito primario como circuito cerrado situado en cubierta/azotea, encargado de transportar energia termica desde los captadores hasta el intercambiador del deposito acumulador.
- Documentar la configuracion del campo solar: 12 captadores Vitosol 200-FM SV2F, en posicion vertical, divididos en 2 baterias de 6 unidades.
- Recoger los datos hidraulicos principales: superficie de captacion, caudal total, reparto por baterias, diametros adoptados, perdidas de carga, volumen de fluido y vaso de expansion.
- Usar los circuitos secundario y distribucion ACS solo como contexto comparativo, sin desplazar el foco del circuito primario.
- No leer ni incorporar datos de archivos adjuntos, PDFs, Excel, catalogos u otras fuentes externas a las tres notas indicadas.

## Datos y tablas a extraer

- Datos de captadores:
  - Numero de captadores: 12.
  - Modelo: Vitosol 200-FM SV2F.
  - Superficie de apertura por captador: 2,33 m2.
  - Superficie total: 27,96 m2.
  - Volumen por captador: 1,83 l.
  - Volumen total en captadores: 21,96 l.
- Configuracion hidraulica:
  - Numero de baterias: 2.
  - Captadores por bateria: 6.
  - Caudal total primario: 699 l/h.
  - Caudal por bateria: 349,5 l/h.
  - Tramos comunes: DN22.
  - Ramas de captadores: DN18.
- Perdidas de carga:
  - Tuberias del recorrido mas desfavorable: 0,534 m.c.a.
  - Intercambiador, lado primario: 1,5 m.c.a.
  - Perdida por captador: 30 mm.c.a.
  - Captadores atravesados en la bateria desfavorable: 6.
  - Perdida total en captadores: 180 mm.c.a. = 0,18 m.c.a.
  - Perdida total del circuito primario: 2,214 m.c.a.
- Volumen del circuito:
  - Tuberias: 5,22 l.
  - Captadores: 21,96 l.
  - Intercambiador: 20 l.
  - Volumen total: 47,18 l.
- Vaso de expansion:
  - Presion inicial: 1,5 kg/cm2.
  - Presion final: 4 kg/cm2.
  - Coeficiente de dilatacion: 0,08.
  - Volumen calculado: aproximadamente 6 l.
  - Volumen comercial seleccionado: 8 l.
- Contexto auxiliar:
  - Circuito secundario: 1.398 l/h, DN28, perdida total 1,93 m.c.a., potencia minima de intercambio 16,8 kW.
  - Distribucion ACS: 10 viviendas, caudales por tramo, diametros DN42/DN35/DN28/DN22/DN18, retorno de recirculacion 360 l/h y perdida aproximada 0,36 m.c.a.

## Metodologia y formulas

- Superficie total de captacion:
  `S_total = numero de captadores * superficie por captador`
- Reparto de caudal por bateria:
  `Q_bateria = Q_total / numero de baterias`
- Perdida de carga en captadores:
  `Pdc_captadores = numero de captadores atravesados * perdida por captador`
- Perdida de carga total:
  `Pdc_total = Pdc_tuberias + Pdc_intercambiador + Pdc_captadores`
- Volumen de captadores:
  `V_captadores = numero de captadores * volumen por captador`
- Volumen total del circuito primario:
  `V_total = V_tuberias + V_captadores + V_intercambiador`
- Seleccion del vaso de expansion:
  documentar el volumen calculado y seleccionar el volumen comercial inmediatamente superior, dejando explicito el margen de seguridad.

## Criterios de validacion

- Todas las cifras del circuito primario presentes en las fuentes quedan recogidas en tablas o formulas.
- La explicacion futura permite reconstruir cada calculo desde los datos base.
- Las magnitudes del secundario y distribucion ACS se usan solo como contexto.
- Cualquier dato no presente en las tres notas se marcara como no disponible, sin buscarlo en adjuntos.
- No se modifica ningun archivo tecnico final durante esta fase.

## Supuestos

- Este plan se guarda como planificacion pendiente, no como implementacion de la explicacion final.
- Las tres notas indicadas son las unicas fuentes permitidas para esta fase.
- La redaccion final se podra incorporar despues a una anotacion tecnica o a la memoria LaTeX, pero esa decision queda fuera de este plan.
