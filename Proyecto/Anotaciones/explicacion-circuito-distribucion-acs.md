# Explicacion del circuito de distribucion de ACS

## Objeto y funcion del circuito

El circuito de distribucion de ACS corresponde a la red que transporta el agua sanitaria precalentada desde el deposito acumulador hasta las viviendas. En esta instalacion, el agua precalentada sale del acumulador situado en la azotea y se conduce mediante una bajante principal situada en el patio interior.

Cada vivienda dispone de una derivacion desde la bajante hasta la entrada de su caldera individual. Por tanto, la instalacion solar no alimenta directamente los puntos finales de consumo, como duchas, lavabos o fregaderos. La funcion de la red solar de distribucion es entregar agua precalentada a cada caldera, y la caldera individual actua como apoyo cuando la temperatura aportada por el sistema solar no sea suficiente.

Esta configuracion permite que la instalacion solar reduzca la energia necesaria para producir ACS en cada vivienda, manteniendo al mismo tiempo el sistema individual de apoyo existente en cada una de ellas.

## Relacion con el circuito primario y secundario

La distribucion de ACS empieza aguas abajo del deposito acumulador. Antes de este punto, el circuito primario solar transporta energia desde los captadores hasta el intercambiador, y el circuito secundario recibe esa energia y la almacena en el agua del acumulador.

| Circuito | Fluido | Funcion principal |
|---|---|---|
| Primario solar | Agua con anticongelante | Transportar energia desde captadores hasta intercambiador |
| Secundario solar | Agua sanitaria en acumulacion | Recibir el calor del primario y almacenarlo en el acumulador |
| Distribucion de ACS | Agua sanitaria precalentada | Transportar el agua desde el acumulador hasta las calderas individuales |

Por esta razon, los criterios de calculo de la distribucion son distintos a los del primario y del secundario. En el primario y el secundario se dimensionan circuitos de intercambio y acumulacion, mientras que en la distribucion se dimensiona una red de consumo hacia viviendas. El dato determinante deja de ser la superficie de captacion y pasa a ser el numero de viviendas alimentadas por cada tramo.

## Edificio y grupos de consumo

Para el dimensionamiento de la red se considera cada vivienda como un grupo de consumo equivalente. Este criterio es adecuado porque la red solar no llega hasta cada aparato sanitario, sino hasta la entrada de la caldera individual de la vivienda.

El edificio cuenta con 5 plantas y 2 viviendas por planta:

```text
N = numero de plantas * viviendas por planta

N = 5 * 2 = 10 viviendas
```

| Magnitud | Valor |
|---|---:|
| Numero de plantas | 5 |
| Viviendas por planta | 2 |
| Total de viviendas | 10 |
| Grupos de consumo considerados | 10 |
| Caudal equivalente por vivienda | 0,25 l/s |

El caudal equivalente adoptado para cada vivienda es de 0,25 l/s. Este valor representa el caudal de diseno de entrada a la caldera individual de una vivienda de dos dormitorios y ocupacion maxima de 4 personas. No supone que todos los aparatos sanitarios funcionen simultaneamente, sino que establece un caudal equivalente para dimensionar la alimentacion solar a cada vivienda.

## Caudales por tramo de bajante

En la bajante principal, el numero de viviendas servidas disminuye a medida que se alimentan las derivaciones de cada planta. Por ello, los tramos superiores conducen el caudal de mas viviendas y requieren mayor diametro, mientras que los tramos inferiores conducen menos caudal.

El caudal de cada tramo se calcula multiplicando el numero de viviendas servidas por el caudal equivalente de una vivienda:

```text
Q_tramo = numero de viviendas servidas * 0,25 l/s
```

| Tramo | Grupos de consumo servidos | Calculo | Caudal adoptado |
|---|---:|---:|---:|
| Bajante - P5 | 10 | 10 * 0,25 | 2,50 l/s |
| P5 - P4 | 8 | 8 * 0,25 | 2,00 l/s |
| P4 - P3 | 6 | 6 * 0,25 | 1,50 l/s |
| P3 - P2 | 4 | 4 * 0,25 | 1,00 l/s |
| P2 - P1 | 2 | 2 * 0,25 | 0,50 l/s |

La reduccion progresiva del caudal justifica que el diametro de la bajante tambien se reduzca por tramos. El tramo superior debe transportar el caudal total de las 10 viviendas, mientras que el tramo inferior solo transporta el caudal correspondiente a las viviendas que quedan aguas abajo.

## Diametros adoptados en la bajante

Con los caudales anteriores se seleccionan diametros de tuberia disponibles, procurando mantener velocidades razonables y perdidas de carga admisibles. Se emplean diametros mayores en los tramos superiores de la bajante y diametros menores en los tramos inferiores.

| Tramo | Caudal adoptado | Diametro adoptado |
|---|---:|---:|
| Bajante - P5 | 2,50 l/s | DN42 |
| P5 - P4 | 2,00 l/s | DN42 |
| P4 - P3 | 1,50 l/s | DN35 |
| P3 - P2 | 1,00 l/s | DN28 |
| P2 - P1 | 0,50 l/s | DN22 |

El mantenimiento de DN42 en los dos primeros tramos responde al mayor caudal circulante en la parte alta de la red. A partir del tramo P4 - P3, el caudal acumulado disminuye y se adoptan diametros progresivamente menores: DN35, DN28 y DN22.

## Derivaciones a vivienda

Cada derivacion desde la bajante hasta una caldera individual alimenta una unica vivienda. Por tanto, cada derivacion se dimensiona para un solo grupo de consumo.

```text
Q_vivienda = 0,25 l/s

Q_vivienda = 0,25 * 3600 = 900 l/h
```

| Elemento | Grupos de consumo | Caudal adoptado | Diametro adoptado |
|---|---:|---:|---:|
| Derivacion a vivienda | 1 | 0,25 l/s = 900 l/h | DN18 |

El diametro DN18 se adopta para las derivaciones individuales porque el caudal transportado es mucho menor que en la bajante principal. Estas derivaciones no distribuyen agua a todos los aparatos sanitarios de la vivienda, sino que alimentan la entrada de la caldera individual con agua precalentada.

## Retorno de recirculacion

La red incorpora un retorno de recirculacion desde la parte inferior de la instalacion hasta el deposito acumulador. Este retorno tiene una funcion distinta a la bajante de consumo: no transporta el caudal simultaneo de las viviendas, sino un caudal reducido destinado a mantener la temperatura del ACS en la red.

La recirculacion evita que el agua precalentada permanezca enfriandose en la bajante durante periodos sin consumo y reduce los tiempos de espera cuando una vivienda demanda ACS. Por ello, el caudal de recirculacion se dimensiona de forma independiente respecto al caudal de consumo de la bajante.

Para el retorno se adopta:

```text
Q_retorno = 0,10 l/s

Q_retorno = 0,10 * 3600 = 360 l/h
```

| Magnitud | Valor |
|---|---:|
| Caudal de retorno adoptado | 0,10 l/s = 360 l/h |
| Diametro adoptado | DN18 |
| Diametro interior considerado | 16 mm |
| Velocidad aproximada | 0,50 m/s |
| Longitud considerada | 17 m |
| Perdida de carga aproximada | 0,36 m.c.a. |

Con una tuberia DN18 y un diametro interior de 16 mm, el caudal de 0,10 l/s produce una velocidad aproximada de 0,50 m/s. Este valor es adecuado para una red de recirculacion, ya que permite mantener movimiento en el circuito sin introducir velocidades excesivas ni perdidas de carga elevadas.

La longitud considerada para el retorno es de 17 m, correspondiente a la subida desde la parte inferior de la red hasta el deposito acumulador. Para este recorrido se obtiene una perdida de carga aproximada de 0,36 m.c.a.

## Bomba de recirculacion

La bomba de recirculacion debe vencer la perdida de carga del retorno y garantizar el caudal adoptado de 360 l/h. A diferencia de las bombas asociadas a los circuitos primario y secundario, esta bomba no se dimensiona para transportar la potencia solar entre captadores, intercambiador y acumulador, sino para mantener la circulacion del ACS precalentada en la red de distribucion.

| Criterio | Valor |
|---|---:|
| Caudal de diseno | 360 l/h |
| Perdida de carga aproximada del retorno | 0,36 m.c.a. |
| Altura requerida | Igual o superior a 0,36 m.c.a. |
| Criterio de seleccion | Bomba comercial con margen suficiente |

Aunque la perdida calculada es reducida, la seleccion comercial debe incorporar margen para absorber perdidas adicionales por accesorios, valvulas, trazado real y tolerancias de montaje. Por tanto, se seleccionara una bomba capaz de proporcionar aproximadamente 360 l/h con una altura manometrica superior a la perdida calculada del retorno.

## Resumen del dimensionamiento

El circuito de distribucion queda definido por una bajante principal de caudal decreciente, derivaciones individuales a cada caldera y un retorno de recirculacion independiente del caudal de consumo.

| Elemento | Criterio principal | Resultado |
|---|---|---:|
| Viviendas alimentadas | 5 plantas * 2 viviendas/planta | 10 viviendas |
| Caudal por vivienda | Grupo de consumo equivalente | 0,25 l/s |
| Caudal maximo en bajante | 10 viviendas * 0,25 l/s | 2,50 l/s |
| Diametro maximo en bajante | Tramos superiores | DN42 |
| Diametro minimo en bajante | Tramo P2 - P1 | DN22 |
| Derivaciones a vivienda | 1 vivienda por derivacion | DN18 |
| Caudal de recirculacion | Retorno independiente del consumo | 360 l/h |
| Diametro del retorno | Tuberia de recirculacion | DN18 |
| Perdida de carga del retorno | Longitud considerada de 17 m | 0,36 m.c.a. |

La red de distribucion, por tanto, no se dimensiona como una red interior completa de aparatos sanitarios, sino como una red de ACS precalentada que alimenta las calderas individuales. Esta distincion es importante porque separa el caudal de consumo considerado para cada vivienda del caudal reducido de recirculacion, y evita confundir la bajante solar con la instalacion interior de ACS de cada vivienda.

## Tabla de tramos en la impulsion de la bajante

La tabla siguiente recoge el detalle de los tramos considerados en la impulsion de la bajante, incluyendo las derivaciones a vivienda, los diametros adoptados, velocidades, espesores de aislamiento y perdidas termicas asociadas.

| Tramo | Tramo recirculacion | n grupos consumo | Coeficiente simultaneidad | Caudal (l/s) | Caudal (l/h) | DN tramo (mm) | Di tramo (mm) | Velocidad (m/s) | Espesor aislam. (mm) | Perdidas (W/m) | L tramo recto (m) | Perdidas (W) |
|---|:---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Bajante-P5 | No | 10 | 0,45 | 2,50 | 9.000 | 42 | 40 | 1,99 | 30 | 12,9 | 2,6 | 33,54 |
| P5-V10 | No | 1 | 1,00 | 0,25 | 900 | 18 | 16 | 1,24 | 20 | 7,5 | 5,65 | 42,375 |
| P5-V9 | No | 1 | 1,00 | 0,25 | 900 | 18 | 16 | 1,24 | 20 | 7,5 | 5,65 | 42,375 |
| P5-P4 | No | 8 | 0,48 | 2,00 | 7.200 | 42 | 40 | 1,59 | 30 | 12,9 | 2,6 | 33,54 |
| P4-V8 | No | 1 | 1,00 | 0,25 | 900 | 18 | 16 | 1,24 | 20 | 7,5 | 5,65 | 42,375 |
| P4-V7 | No | 1 | 1,00 | 0,25 | 900 | 18 | 16 | 1,24 | 20 | 7,5 | 5,65 | 42,375 |
| P4-P3 | No | 6 | 0,50 | 1,50 | 5.400 | 35 | 33 | 1,76 | 20 | 11,4 | 2,6 | 29,64 |
| P3-V6 | No | 1 | 0,00 | 0,25 | 900 | 18 | 16 | 1,24 | 20 | 7,5 | 5,65 | 42,375 |
| P3-V5 | No | 1 | 0,00 | 0,25 | 900 | 18 | 16 | 1,24 | 20 | 7,5 | 5,65 | 42,375 |
| P3-P2 | No | 4 | 0,00 | 1,00 | 3.600 | 28 | 26 | 1,89 | 20 | 9,8 | 2,6 | 25,48 |
| P2-V4 | No | 1 | 0,00 | 0,25 | 900 | 18 | 16 | 1,24 | 20 | 7,5 | 5,65 | 42,375 |
| P2-V3 | No | 1 | 0,00 | 0,25 | 900 | 18 | 16 | 1,24 | 20 | 7,5 | 5,65 | 42,375 |
| P2-P1 | No | 2 | 0,00 | 0,50 | 1.800 | 22 | 20 | 1,59 | 20 | 8,4 | 2,6 | 21,84 |
| P1-V2 | No | 1 | 0,00 | 0,25 | 900 | 18 | 16 | 1,24 | 20 | 7,5 | 5,65 | 42,375 |
| P1-V1 | No | 1 | 0,00 | 0,25 | 900 | 18 | 16 | 1,24 | 20 | 7,5 | 5,65 | 42,375 |
| P1-Deposito | Si | 0 | 0,00 | 0,00 | 0 | 18 | 16 | 0,00 | 20 | 7,5 | 17 | 127,5 |
