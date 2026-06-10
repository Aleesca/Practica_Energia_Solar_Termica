# Justificación del circuito secundario

El circuito secundario corresponde al circuito de agua que recibe el calor procedente del circuito primario a través del intercambiador del depósito acumulador. En esta instalación, el circuito secundario está asociado al agua del acumulador y al intercambio térmico entre el circuito solar y el agua sanitaria.

El fluido del circuito secundario es agua, a diferencia del circuito primario, donde circula fluido caloportador con anticongelante. La función del circuito secundario es recoger la energía aportada por los captadores solares y almacenarla en el depósito acumulador, desde el cual posteriormente se distribuye agua precalentada hacia las viviendas.

El caudal del circuito secundario se ha determinado a partir de la superficie total de captación y del caudal específico adoptado para este circuito. Con 12 captadores y una superficie de 2,33 m² por captador, la superficie total de captación es:

```text
S total = 12 · 2,33 = 27,96 m²
```

Adoptando un caudal específico de 50 l/h·m², el caudal del circuito secundario resulta:

```text
Q secundario = 27,96 · 50 = 1.398 l/h
```

Por tanto, el caudal de diseño del circuito secundario es de 1.398 l/h.

En los tramos principales del circuito secundario, correspondientes a la alimentación desde red hasta el depósito y desde el depósito hasta la bajante, se ha adoptado DN28. Con este diámetro interior de 26 mm y un caudal de 1.398 l/h, la velocidad del agua es aproximadamente 0,73 m/s, valor adecuado para este tipo de instalación.

Las pérdidas de carga en los tramos del circuito secundario se han calculado considerando las longitudes rectas, las singularidades y el caudal circulante. En la hoja de cálculo se obtiene una pérdida de carga de tuberías aproximada de 0,63 m.c.a. Además, se considera una pérdida de carga estimada de 1,3 m.c.a. en el lado secundario del intercambiador.

La pérdida de carga total del circuito secundario se calcula como:

```text
Pdc total = Pdc tuberías + Pdc intercambiador

Pdc total = 0,63 + 1,30 = 1,93 m.c.a.
```

Por tanto, para la bomba del circuito secundario se adopta un caudal de 1.398 l/h y una altura manométrica mínima de 1,93 m.c.a. Se recomienda seleccionar una bomba comercial capaz de trabajar con un caudal aproximado de 1.400 l/h y una altura manométrica de unos 2,0 a 2,5 m.c.a., dejando margen frente a pérdidas adicionales.

Para la selección del intercambiador de calor centralizado se ha considerado una potencia mínima de intercambio de 600 W/m² de superficie de captación. Con una superficie total de 27,96 m², la potencia mínima de intercambio resulta:

```text
P = 600 · 27,96 = 16.776 W = 16,8 kW
```

Por tanto, el intercambiador debe ser capaz de transmitir una potencia mínima aproximada de 16,8 kW entre el circuito primario solar y el circuito secundario de agua. En el caso de emplearse un depósito con intercambiador interno, esta potencia debe ser garantizada por el serpentín del acumulador.
