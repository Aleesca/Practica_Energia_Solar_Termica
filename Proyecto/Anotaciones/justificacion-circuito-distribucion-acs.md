# Justificación del circuito de distribución de ACS

El circuito de distribución corresponde a la red que transporta el agua sanitaria precalentada desde el depósito acumulador hasta las viviendas. En esta instalación, el agua precalentada se conduce desde el depósito situado en la azotea hasta las calderas individuales de cada vivienda mediante una bajante principal situada en el patio interior. Cada vivienda dispone de una derivación desde la bajante hacia su caldera individual.

La instalación solar no alimenta directamente los puntos finales de consumo, como duchas, lavabos o fregaderos. El agua precalentada llega a la entrada de la caldera individual de cada vivienda, y la caldera actúa como sistema de apoyo, elevando la temperatura del agua cuando el aporte solar no sea suficiente. Por esta razón, para el dimensionamiento de la red de distribución solar se considera cada vivienda como un grupo de consumo equivalente.

El edificio cuenta con 5 plantas y 2 viviendas por planta, por lo que el número total de grupos de consumo considerados es:

```text
Nº grupos de consumo = 5 · 2 = 10 viviendas
```

En la bajante principal, el número de grupos de consumo disminuye a medida que se alimentan las viviendas de cada planta. Por tanto, se consideran los siguientes grupos por tramo:

```text
Bajante - P5: 10 grupos
P5 - P4: 8 grupos
P4 - P3: 6 grupos
P3 - P2: 4 grupos
P2 - P1: 2 grupos
```

Cada derivación hacia una vivienda se considera como un único grupo de consumo:

```text
Derivación a vivienda = 1 grupo
```

Para una vivienda de dos dormitorios y ocupación máxima de 4 personas se adopta un caudal equivalente de 0,25 l/s por vivienda. Este valor representa el caudal de diseño de entrada a la caldera individual, sin considerar que todos los aparatos sanitarios funcionen simultáneamente.

Los caudales adoptados en los tramos principales de la bajante son:

```text
Bajante - P5: 10 viviendas · 0,25 = 2,50 l/s
P5 - P4: 8 viviendas · 0,25 = 2,00 l/s
P4 - P3: 6 viviendas · 0,25 = 1,50 l/s
P3 - P2: 4 viviendas · 0,25 = 1,00 l/s
P2 - P1: 2 viviendas · 0,25 = 0,50 l/s
```

En las derivaciones a cada vivienda se adopta:

```text
Q vivienda = 0,25 l/s = 900 l/h
```

Con estos caudales se han seleccionado los diámetros de tubería disponibles, procurando mantener velocidades razonables y pérdidas de carga admisibles. En los primeros tramos de la bajante se emplean diámetros mayores, mientras que en los tramos inferiores y en las derivaciones a vivienda se reducen los diámetros al disminuir el caudal.

Los diámetros adoptados son:

```text
Bajante - P5: DN42
P5 - P4: DN42
P4 - P3: DN35
P3 - P2: DN28
P2 - P1: DN22
Derivaciones a vivienda: DN18
```

El circuito de distribución incorpora además un retorno de recirculación desde la parte inferior de la instalación hasta el depósito acumulador. Este retorno no transporta el caudal de consumo de las viviendas, sino un caudal reducido destinado a mantener la temperatura del ACS en la red y evitar tiempos de espera excesivos.

Para el retorno de recirculación se adopta un caudal de 0,10 l/s, equivalente a 360 l/h. Con una tubería DN18 y diámetro interior de 16 mm, se obtiene una velocidad aproximada de 0,50 m/s, adecuada para una red de recirculación. La longitud considerada para el retorno es de 17 m, correspondiente a la subida desde la parte inferior de la red hasta el depósito acumulador.

La bomba de recirculación se dimensiona, por tanto, para un caudal aproximado de 360 l/h y una altura manométrica suficiente para vencer la pérdida de carga del retorno. En la hoja de cálculo se obtiene una pérdida de carga aproximada de 0,36 m.c.a., por lo que se seleccionará una bomba comercial con margen suficiente.
