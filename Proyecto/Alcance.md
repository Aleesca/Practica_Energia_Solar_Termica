# Alcance del proyecto

## Objetivo del proyecto

El proyecto consiste en elaborar la memoria tecnica de una instalacion de energia solar termica centralizada para produccion de agua caliente sanitaria (ACS) en el edificio de viviendas usado en la practica de gas natural.

La instalacion se plantea sobre cubierta plana, con captadores solares planos situados en la azotea. El ACS producida se almacena en deposito o depositos centralizados y se distribuye a las viviendas mediante un patinillo de comunicaciones, quedando hibridada con la produccion auxiliar mediante calderas de gas natural.

Este documento define el alcance del trabajo y sirve como referencia para organizar los calculos, la memoria, los planos y los anexos. No desarrolla los calculos tecnicos.

## Datos de partida

- Fuente principal del alcance: `00_Data/Enunciado_practica.pdf`.
- Edificio: edificio de viviendas correspondiente a la practica de gas natural.
- Tipo de cubierta asumida: cubierta plana o azotea.
- Sistema solar: captadores solares planos para produccion de ACS.
- Sistema de acumulacion: deposito o depositos centralizados de ACS.
- Integracion hidraulica: distribucion de ACS por patinillo de comunicaciones hacia cada vivienda.
- Sistema auxiliar: calderas de gas natural existentes o consideradas en la practica de gas natural.
- Demanda de ACS: se determina a partir del numero de dormitorios de los planos proporcionados y conforme al documento HE-4 del CTE.
- Ubicacion: la que corresponda al grupo de practicas segun la tabla incluida en el enunciado.
- Herramienta de apoyo: hoja Excel de Gas Natural indicada en el enunciado y disponible en la documentacion de la practica.

## Calculos incluidos

El proyecto incluye los siguientes calculos y justificaciones tecnicas:

1. Demanda energetica de ACS.
2. Datos climaticos y de radiacion solar aplicables a la ubicacion del edificio.
3. Determinacion de la superficie de captadores solares.
4. Determinacion de la acumulacion de ACS.
5. Caracteristicas basicas de la edificacion necesarias para justificar la instalacion.
6. Circuito primario de captacion solar para edificio multifamiliar con acumulacion de ACS centralizada.
7. Circuito secundario para edificio multifamiliar con acumulacion de ACS centralizada.
8. Circuito de distribucion de ACS para edificio multifamiliar con acumulacion de ACS centralizada.
9. Intercambiadores de calor agua/agua.

Los calculos deberan documentar datos de partida, unidades, supuestos, resultados y coherencia con el enunciado de la practica.

## Calculos excluidos

La bomba de circulacion queda expresamente fuera del alcance de este proyecto.

Por tanto, en este trabajo:

- no se calcula la bomba de circulacion;
- no se dimensiona la bomba de circulacion;
- no se selecciona ningun modelo de bomba de circulacion;
- no se estima la potencia de la bomba de circulacion;
- no se estiman perdidas de carga para seleccionar la bomba de circulacion;
- no se desarrolla ningun criterio de seleccion asociado a bombas de circulacion.

Aunque el enunciado menciona "intercambiadores de calor agua/agua y bombas de circulacion", este alcance limita esa parte del trabajo a los intercambiadores de calor agua/agua. Las bombas de circulacion solo podran citarse como elemento existente del esquema de principio si fuera necesario para entender la instalacion, pero sin calculo, dimensionamiento, seleccion ni criterio tecnico asociado.

## Memoria a presentar

La entrega final sera una memoria en formato PDF que incluya, como minimo, los siguientes apartados:

- Indice.
- Antecedentes y datos de partida.
- Calculos.
- Esquemas de principio y planos.
- Anexos.

Los anexos deberan incorporar las fichas tecnicas necesarias para justificar los equipos considerados dentro del alcance, especialmente:

- captadores solares;
- deposito o sistema de acumulacion;
- intercambiadores de calor.

Las fichas de bombas no forman parte obligatoria del alcance, salvo que se incorporen solo como informacion auxiliar no calculada y sin criterio de seleccion.

## Entregables

- Memoria tecnica final en PDF.
- Esquemas de principio de la instalacion solar termica hibridada con gas natural.
- Planos necesarios para ubicar y explicar la instalacion.
- Anexos con fichas tecnicas de equipos incluidos en el alcance.
- Calculos justificativos de ACS, radiacion, captacion, acumulacion, circuitos e intercambiadores.

Fecha de entrega indicada en el enunciado: 10 de junio de 2026.

## Criterios de revision

Antes de cerrar la memoria, se revisara que:

- la demanda de ACS se ha obtenido a partir de los dormitorios y del CTE HE-4;
- la ubicacion empleada coincide con el grupo de practicas correspondiente;
- los datos climaticos y de radiacion solar estan identificados;
- la superficie de captadores y la acumulacion quedan justificadas;
- los circuitos primario, secundario y de distribucion de ACS quedan descritos y calculados dentro del alcance;
- los intercambiadores agua/agua quedan justificados;
- la memoria contiene los apartados minimos exigidos por el enunciado;
- los planos y esquemas permiten entender la hibridacion con el sistema de gas natural;
- no se ha calculado, dimensionado, seleccionado ni justificado ninguna bomba de circulacion.

## Referencias y flujo de trabajo

El flujo de trabajo documental sera:

1. Tomar el enunciado de la practica como fuente principal de requisitos.
2. Extraer de los planos de la practica de gas natural los datos necesarios del edificio y las viviendas.
3. Determinar la demanda de ACS segun dormitorios y CTE HE-4.
4. Obtener datos climaticos y de radiacion para la ubicacion del grupo.
5. Desarrollar los calculos incluidos en este alcance.
6. Seleccionar y documentar equipos incluidos: captadores, acumulacion e intercambiadores.
7. Preparar esquemas, planos, anexos y memoria final.
8. Revisar explicitamente que la bomba de circulacion permanece fuera del alcance.

Para el desarrollo tecnico posterior se podran usar las referencias del proyecto y la guia local `.agents/skills/doc_tecnica_solar_hibrida/`, siempre respetando los limites establecidos en este documento.
