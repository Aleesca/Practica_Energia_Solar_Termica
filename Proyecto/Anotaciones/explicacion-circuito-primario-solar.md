# Explicacion del circuito primario solar

## Objeto y funcion del circuito

El circuito primario solar es el circuito cerrado situado en la azotea que transporta la energia termica desde el campo de captadores hasta el intercambiador del deposito acumulador. En el circula el fluido caloportador, formado por agua con anticongelante, por lo que queda separado del agua sanitaria del circuito secundario.

Este circuito esta formado por los captadores solares, las tuberias de ida y retorno, la bomba de circulacion, el fluido caloportador y el lado primario del intercambiador. Su funcion no es distribuir ACS a las viviendas, sino recoger la energia solar disponible en cubierta y entregarla al acumulador mediante intercambio termico.

## Configuracion del campo solar

La instalacion cuenta con 12 captadores solares Vitosol 200-FM SV2F, colocados en posicion vertical. Para repartir el caudal y limitar las perdidas de carga, los captadores se agrupan en dos baterias hidraulicas de 6 captadores cada una, identificadas como C1 y C2.

| Magnitud | Valor |
|---|---:|
| Numero de captadores | 12 |
| Modelo | Vitosol 200-FM SV2F |
| Posicion de montaje | Vertical |
| Numero de baterias | 2 |
| Captadores por bateria | 6 |
| Superficie de apertura por captador | 2,33 m2 |
| Superficie total de captacion | 27,96 m2 |
| Volumen por captador | 1,83 l |
| Volumen total en captadores | 21,96 l |

La superficie total de captacion se obtiene multiplicando el numero de captadores por la superficie de apertura unitaria:

```text
S_total = n_captadores * S_captador

S_total = 12 * 2,33 = 27,96 m2
```

El volumen contenido en los captadores se calcula del mismo modo:

```text
V_captadores = n_captadores * V_captador

V_captadores = 12 * 1,83 = 21,96 l
```

## Caudal de diseno y reparto hidraulico

El caudal total adoptado para el circuito primario es de 699 l/h. Al existir dos baterias de captadores, el caudal se reparte en dos ramas iguales, por lo que cada bateria trabaja con 349,5 l/h.

```text
Q_bateria = Q_total / n_baterias

Q_bateria = 699 / 2 = 349,5 l/h
```

| Tramo | Caudal considerado | Diametro adoptado |
|---|---:|---:|
| Tramos comunes entre deposito y bifurcacion | 699 l/h | DN22 |
| Rama de bateria C1 | 349,5 l/h | DN18 |
| Rama de bateria C2 | 349,5 l/h | DN18 |

Los tramos comunes se dimensionan para conducir el caudal total del primario, mientras que las ramas de captadores solo conducen la mitad del caudal. Por ello se adopta DN22 en los tramos comunes y DN18 en cada rama de captadores. Esta configuracion permite mantener velocidades reducidas y perdidas de carga admisibles.

## Perdida de carga del circuito primario

Para calcular la perdida de carga se toma el recorrido hidraulicamente mas desfavorable, correspondiente al ramal C1. En dicho recorrido se suman tres contribuciones principales:

| Concepto | Valor |
|---|---:|
| Perdida en tuberias del recorrido mas desfavorable | 0,534 m.c.a. |
| Perdida en el lado primario del intercambiador | 1,5 m.c.a. |
| Perdida por captador | 30 mm.c.a. |
| Captadores atravesados en la bateria desfavorable | 6 |
| Perdida total en captadores | 180 mm.c.a. = 0,18 m.c.a. |

La perdida en captadores se obtiene multiplicando la perdida unitaria por el numero de captadores atravesados:

```text
Pdc_captadores = n_captadores_bateria * Pdc_captador

Pdc_captadores = 6 * 30 = 180 mm.c.a. = 0,18 m.c.a.
```

La perdida de carga total del circuito primario resulta de sumar tuberias, intercambiador y captadores:

```text
Pdc_total = Pdc_tuberias + Pdc_intercambiador + Pdc_captadores

Pdc_total = 0,534 + 1,5 + 0,18 = 2,214 m.c.a.
```

Por tanto, para la seleccion de la bomba del circuito primario se adopta un punto de trabajo de 699 l/h y una altura manometrica minima aproximada de 2,21 m.c.a. La bomba comercial debe seleccionarse con margen suficiente sobre este punto para absorber pequenas desviaciones de montaje, accesorios adicionales o variaciones reales de funcionamiento.

## Volumen de fluido del circuito

El volumen total del circuito primario se calcula sumando el volumen de las tuberias, el volumen contenido en los captadores y el volumen correspondiente al intercambiador.

| Elemento | Volumen |
|---|---:|
| Tuberias | 5,22 l |
| Captadores | 21,96 l |
| Intercambiador | 20 l |
| Volumen total del circuito primario | 47,18 l |

```text
V_total = V_tuberias + V_captadores + V_intercambiador

V_total = 5,22 + 21,96 + 20 = 47,18 l
```

Este volumen es el dato base para dimensionar el vaso de expansion, ya que determina la cantidad de fluido caloportador que puede dilatarse con los cambios de temperatura del circuito solar.

## Vaso de expansion

Para el vaso de expansion del circuito primario se consideran los siguientes datos:

| Magnitud | Valor |
|---|---:|
| Volumen total del circuito | 47,18 l |
| Presion inicial | 1,5 kg/cm2 |
| Presion final | 4 kg/cm2 |
| Coeficiente de dilatacion | 0,08 |
| Volumen calculado del vaso | aprox. 6 l |
| Volumen comercial seleccionado | 8 l |

El volumen calculado del vaso es aproximadamente 6 l. Como criterio de seleccion, se adopta el volumen comercial inmediatamente superior, por lo que se selecciona un vaso de expansion de 8 l. Esta seleccion introduce un margen de seguridad frente a la dilatacion del fluido caloportador y frente a tolerancias de montaje o funcionamiento.

## Relacion con el resto de circuitos

El circuito primario no debe confundirse con el circuito secundario ni con la distribucion de ACS. El secundario recibe el calor del primario a traves del intercambiador y trabaja con agua, con un caudal de 1.398 l/h, DN28 y una perdida total aproximada de 1,93 m.c.a. Ademas, el intercambiador debe garantizar una potencia minima aproximada de 16,8 kW.

La red de distribucion de ACS, por su parte, transporta el agua precalentada desde el acumulador hasta las 10 viviendas del edificio. Sus diametros se adaptan al numero de viviendas alimentadas en cada tramo, con DN42, DN35, DN28, DN22 y DN18, e incorpora un retorno de recirculacion de 360 l/h con una perdida aproximada de 0,36 m.c.a.

Estos datos sirven solo como contexto: el dimensionado del primario queda definido por el campo solar, el caudal de 699 l/h, el reparto en dos baterias, la perdida total de 2,214 m.c.a., el volumen de fluido de 47,18 l y el vaso de expansion comercial de 8 l.

## Resumen de criterios de diseno

| Criterio | Resultado adoptado |
|---|---|
| Campo de captadores | 12 Vitosol 200-FM SV2F en posicion vertical |
| Agrupacion hidraulica | 2 baterias de 6 captadores |
| Superficie total | 27,96 m2 |
| Caudal total primario | 699 l/h |
| Caudal por bateria | 349,5 l/h |
| Diametros principales | DN22 en comunes y DN18 en ramas |
| Perdida de carga total | 2,214 m.c.a. |
| Volumen total de fluido | 47,18 l |
| Vaso de expansion | 8 l |

Con estos valores, el circuito primario queda definido como una red cerrada de captacion e intercambio, dimensionada para transportar el aporte solar desde la cubierta hasta el acumulador con caudales equilibrados, perdidas de carga moderadas y margen suficiente en el vaso de expansion.

## Tabla de perdidas de carga por tramo

| Tramo | Recorrido mas desfavorable | Caudal (l/h) | DN tramo (mm) | Di tramo (mm) | Velocidad (m/s) | Pdc lineal (mm.c.a./m) | Espesor aislamiento (mm) | L tramo recto (m) | Singularidad 1 | Nº | Singularidad 2 | Nº | Singularidad 3 | Nº | Singularidad 4 | Nº | Singularidad 5 | Nº | L equiv. singul. (m) | L total (m) | Pdc (mm.c.a.) |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---|---:|---|---:|---|---:|---|---:|---|---:|---:|---:|---:|
| C1-A | Si | 349,5 | 18 | 16 | 0,48 | 26,5 | 30 | 6,06 | Codo de 90º | 1 | T tipo2 | 1 | --- |  | --- |  | --- |  | 3 | 9,06 | 239,9 |
| C2-A | No | 349,5 | 18 | 16 | 0,48 | 26,5 | 30 | 1,03 | T tipo1 | 1 | --- |  | --- |  | --- |  | --- |  | 0,15 | 1,18 | 31,2 |
| A-Deposito | No | 699 | 22 | 20 | 0,62 | 30,9 | 30 | 3,78 | T tipo1 | 1 | --- |  | --- |  | --- |  | --- |  | 0,2 | 3,98 | 122,8 |
| Deposito-B | No | 699 | 22 | 20 | 0,62 | 30,9 | 30 | 3,65 | T tipo1 | 1 | --- |  | --- |  | --- |  | --- |  | 0,2 | 3,85 | 118,8 |
| B-C2 | No | 349,5 | 18 | 16 | 0,48 | 26,5 | 30 | 1,34 | T tipo1 | 1 | --- |  | --- |  | --- |  | --- |  | 0,15 | 1,49 | 39,5 |
| B-C1 | No | 349,5 | 18 | 16 | 0,48 | 26,5 | 30 | 6,82 | Codo de 90º | 1 | T tipo1 | 1 | --- |  | --- |  | --- |  | 0,65 | 7,47 | 197,8 |
