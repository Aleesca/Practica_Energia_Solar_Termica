# Explicacion del circuito secundario solar

## Objeto y funcion del circuito

El circuito secundario solar es el circuito de agua asociado al deposito acumulador y al intercambio termico con el circuito primario. Su funcion es recibir la energia captada por el campo solar a traves del intercambiador del acumulador y almacenarla en el agua del deposito.

Este circuito no debe confundirse con el circuito primario solar ni con la red de distribucion de ACS. El circuito primario trabaja con fluido caloportador con anticongelante y transporta la energia desde los captadores hasta el intercambiador. El circuito secundario trabaja con agua y queda vinculado al acumulador, desde el que posteriormente se entrega agua precalentada hacia la distribucion.

## Relacion con el circuito primario y con la distribucion

El intercambio entre el primario y el secundario se produce en el deposito acumulador, mediante un intercambiador centralizado o mediante el serpentin interno del acumulador. De este modo, el fluido caloportador del primario no entra en contacto con el agua sanitaria.

| Circuito | Fluido | Funcion principal |
|---|---|---|
| Primario solar | Agua con anticongelante | Transportar energia desde captadores hasta intercambiador |
| Secundario solar | Agua | Recibir el calor del primario y almacenarlo en el acumulador |
| Distribucion de ACS | Agua sanitaria precalentada | Transportar el agua desde el acumulador hasta las viviendas |

La red de distribucion de ACS empieza aguas abajo del acumulador. Por tanto, el circuito secundario se limita al tramo de intercambio y acumulacion, mientras que la distribucion se dimensiona por el numero de viviendas alimentadas y por los caudales de consumo considerados en cada tramo.

## Datos base del campo solar

El caudal del circuito secundario se obtiene a partir de la superficie total de captacion. La instalacion dispone de 12 captadores solares, con una superficie de 2,33 m2 por captador.

| Magnitud | Valor |
|---|---:|
| Numero de captadores | 12 |
| Superficie por captador | 2,33 m2 |
| Superficie total de captacion | 27,96 m2 |

La superficie total se calcula como:

```text
S_total = n_captadores * S_captador

S_total = 12 * 2,33 = 27,96 m2
```

Esta superficie es el dato de partida para fijar tanto el caudal de circulacion del secundario como la potencia minima de intercambio.

## Caudal de diseno del circuito secundario

Para el circuito secundario se adopta un caudal especifico de 50 l/h*m2. Aplicando este criterio a la superficie total de captacion, se obtiene el caudal de diseno del circuito.

| Magnitud | Valor |
|---|---:|
| Superficie total de captacion | 27,96 m2 |
| Caudal especifico adoptado | 50 l/h*m2 |
| Caudal de diseno del circuito secundario | 1.398 l/h |

```text
Q_secundario = S_total * q_especifico

Q_secundario = 27,96 * 50 = 1.398 l/h
```

Por tanto, el circuito secundario se dimensiona para un caudal de 1.398 l/h. Este valor representa el caudal que debe circular por el lado de agua del intercambio para recoger de forma adecuada la energia transferida desde el circuito primario solar.

## Dimensionamiento hidraulico

En los tramos principales del circuito secundario se adopta DN28. Estos tramos corresponden a la alimentacion desde red hasta el deposito y a la salida desde el deposito hacia la bajante de ACS precalentada.

| Magnitud | Valor |
|---|---:|
| Caudal considerado | 1.398 l/h |
| Diametro adoptado en tramos principales | DN28 |
| Diametro interior considerado | 26 mm |
| Velocidad aproximada | 0,73 m/s |

Con un diametro interior de 26 mm y el caudal de calculo de 1.398 l/h, la velocidad resultante es aproximadamente 0,73 m/s. Este valor se considera adecuado para una instalacion de agua, ya que mantiene una velocidad moderada y evita perdidas de carga excesivas en los tramos principales.

El diametro DN28 queda, por tanto, justificado por el caudal de diseno del secundario y por la velocidad obtenida en la tuberia.

## Perdidas de carga del circuito secundario

Las perdidas de carga del circuito secundario se obtienen sumando la perdida en tuberias y la perdida asociada al lado secundario del intercambiador. En las tuberias se consideran las longitudes rectas, las singularidades y el caudal circulante. Para el intercambiador se adopta una perdida estimada de 1,30 m.c.a. en el lado secundario.

| Concepto | Valor |
|---|---:|
| Perdida de carga en tuberias | 0,63 m.c.a. |
| Perdida de carga en intercambiador, lado secundario | 1,30 m.c.a. |
| Perdida de carga total | 1,93 m.c.a. |

La perdida total se calcula como:

```text
Pdc_total = Pdc_tuberias + Pdc_intercambiador

Pdc_total = 0,63 + 1,30 = 1,93 m.c.a.
```

La altura manometrica minima de calculo para la bomba del circuito secundario es, por tanto, 1,93 m.c.a. Este valor representa la resistencia hidraulica que debe vencer la bomba en el punto de trabajo definido por el caudal de 1.398 l/h.

## Seleccion de la bomba del circuito secundario

La bomba del circuito secundario debe seleccionarse para garantizar el caudal de diseno y la altura manometrica minima calculada.

| Criterio | Valor |
|---|---:|
| Caudal de diseno | 1.398 l/h |
| Altura manometrica minima | 1,93 m.c.a. |
| Caudal comercial de referencia | aprox. 1.400 l/h |
| Altura recomendada con margen | 2,0 a 2,5 m.c.a. |

Aunque el calculo da una altura minima de 1,93 m.c.a., la seleccion comercial debe incorporar margen. Por ello se recomienda escoger una bomba capaz de trabajar aproximadamente con 1.400 l/h y una altura manometrica de 2,0 a 2,5 m.c.a. Este margen permite absorber pequenas perdidas adicionales debidas a accesorios, tolerancias de montaje o diferencias entre el trazado real y el trazado calculado.

## Potencia minima del intercambiador

Para el intercambiador centralizado se adopta un criterio de potencia minima de 600 W por cada metro cuadrado de superficie de captacion. Este criterio asegura que el intercambio entre el primario solar y el agua del secundario sea suficiente para transmitir la energia captada.

| Magnitud | Valor |
|---|---:|
| Superficie total de captacion | 27,96 m2 |
| Criterio de potencia minima | 600 W/m2 |
| Potencia calculada | 16.776 W |
| Potencia redondeada | 16,8 kW |

La potencia minima se calcula como:

```text
P_intercambio = 600 * S_total

P_intercambio = 600 * 27,96 = 16.776 W = 16,8 kW
```

Por tanto, el intercambiador debe ser capaz de transmitir una potencia minima aproximada de 16,8 kW entre el circuito primario solar y el circuito secundario de agua. Si se emplea un deposito con intercambiador interno, esta potencia debe quedar garantizada por el serpentin del acumulador.

## Resumen de criterios de diseno

| Criterio | Resultado adoptado |
|---|---|
| Fluido del circuito secundario | Agua |
| Funcion | Recepcion del calor del primario y acumulacion |
| Numero de captadores | 12 |
| Superficie por captador | 2,33 m2 |
| Superficie total | 27,96 m2 |
| Caudal especifico | 50 l/h*m2 |
| Caudal secundario | 1.398 l/h |
| Diametro principal | DN28 |
| Diametro interior considerado | 26 mm |
| Velocidad aproximada | 0,73 m/s |
| Perdida de carga en tuberias | 0,63 m.c.a. |
| Perdida de carga en intercambiador | 1,30 m.c.a. |
| Perdida de carga total | 1,93 m.c.a. |
| Punto minimo de bomba | 1.398 l/h y 1,93 m.c.a. |
| Margen recomendado de bomba | 2,0 a 2,5 m.c.a. |
| Potencia minima de intercambio | 16,8 kW |

Con estos valores, el circuito secundario queda definido como el circuito de agua que recibe la energia del primario solar en el acumulador. Su dimensionado se basa en la superficie total de captacion, el caudal especifico adoptado, el diametro DN28 en los tramos principales, una perdida total de 1,93 m.c.a. y una potencia minima de intercambio de 16,8 kW.

## Tabla de perdidas de carga por tramo

| Tramo | Caudal (l/h) | DN tramo (mm) | Di tramo (mm) | Velocidad (m/s) | Pdcl (mm.c.a./m) | Espesor aislamiento (mm) | L tramo recto (m) | Singularidad 1 | Nro | Singularidad 2 | Nro | Singularidad 3 | Nro | Singularidad 4 | Nro | Singularidad 5 | Nro | L equiv. singul. (m) | L total (m) | Pdc (mm.c.a.) |
|---|---:|---:|---:|---:|---:|---:|---:|---|---:|---|---:|---|---:|---|---:|---|---:|---:|---:|---:|
| Red-Deposito | 1.398 | 28 | 26,0 | 0,73 | 23,0 | 20 | 17 | Codo de 90 grados | 2 | --- |  | --- |  | --- |  | --- |  | 1,52 | 18,52 | 425,3 |
| Deposito-Bajan | 1.398 | 28 | 26 | 0,73 | 23,0 | 20 | 6,58 | Codo de 90 grados | 3 | --- |  | --- |  | --- |  | --- |  | 2,28 | 8,86 | 203,4 |
