# Justificación de los circuitos

## Justificación del circuito primario solar

El circuito primario corresponde al circuito cerrado situado en la azotea, encargado de transportar la energía térmica desde los captadores solares hasta el intercambiador del depósito acumulador. Este circuito está formado por los captadores solares, las tuberías de ida y retorno, el fluido caloportador, la bomba de circulación y el lado primario del intercambiador.

La instalación dispone de 12 captadores solares Vitosol 200-FM SV2F, colocados en posición vertical. Los captadores se han dividido en dos baterías de 6 unidades, identificadas como C1 y C2. Esta división permite repartir el caudal entre dos ramas, reduciendo la pérdida de carga en cada una de ellas y manteniendo velocidades adecuadas en las tuberías.

El caudal total del circuito primario se ha calculado a partir de la superficie de captación y del caudal específico adoptado. Con una superficie de apertura de 2,33 m² por captador y 12 captadores, se obtiene una superficie total de captación de 27,96 m². Para el circuito primario se adopta un caudal total de 699 l/h, que se reparte entre las dos baterías de captadores, por lo que cada batería trabaja con 349,5 l/h.

Los tramos comunes entre el depósito y la bifurcación conducen el caudal total de 699 l/h, por lo que se han dimensionado con DN22. Las ramas correspondientes a cada grupo de captadores conducen la mitad del caudal, 349,5 l/h, por lo que se han dimensionado con DN18. Con estos diámetros se obtienen velocidades reducidas y pérdidas de carga admisibles.

Para el cálculo de la pérdida de carga del circuito primario se ha considerado el recorrido hidráulicamente más desfavorable, que corresponde al ramal C1. En este recorrido se suman las pérdidas de carga de las tuberías, del intercambiador y de los captadores atravesados. La pérdida de carga en tuberías del recorrido más desfavorable es de aproximadamente 0,534 m.c.a. A esta se añade una pérdida estimada de 1,5 m.c.a. en el lado primario del intercambiador y una pérdida de 30 mm.c.a. por captador. Al existir 6 captadores en la batería más desfavorable, la pérdida en captadores es de 180 mm.c.a., equivalente a 0,18 m.c.a.

Por tanto, la pérdida de carga total del circuito primario resulta:

```text
Pdc total = Pdc tuberías + Pdc intercambiador + Pdc captadores

Pdc total = 0,534 + 1,5 + 0,18 = 2,214 m.c.a.
```

Se adopta, por tanto, una altura manométrica de cálculo de aproximadamente 2,21 m.c.a. para la selección de la bomba del circuito primario. La bomba deberá ser capaz de proporcionar un caudal de 699 l/h con una altura manométrica igual o superior a 2,21 m.c.a., recomendándose seleccionar un modelo comercial con cierto margen.

Para el cálculo del volumen del circuito primario se ha considerado el volumen de fluido contenido en las tuberías, en los captadores y en el intercambiador. El volumen de los captadores es de 21,96 litros, obtenido como 12 captadores por 1,83 litros por captador. El volumen de las tuberías se obtiene a partir de las longitudes y diámetros introducidos en la hoja de cálculo, resultando aproximadamente 5,22 litros. Para el intercambiador se ha adoptado una estimación de 20 litros. Con ello, el volumen total del circuito primario es aproximadamente:

```text
V circuito primario = V tuberías + V captadores + V intercambiador

V circuito primario = 5,22 + 21,96 + 20 = 47,18 litros
```

Este volumen se emplea para el dimensionamiento del vaso de expansión del circuito primario. Adoptando una presión inicial de 1,5 kg/cm², una presión final de 4 kg/cm² y un coeficiente de dilatación de 0,08, el volumen calculado del vaso de expansión es de aproximadamente 6 litros. Por tanto, se selecciona un vaso comercial de 8 litros, al ser el tamaño inmediatamente superior y aportar margen de seguridad.
