# Dimensionado del circuito primario: accesorios en T y longitud equivalente

> Relacionado con: [Seleccion de bombas de circulacion Grundfos para la instalacion solar termica](seleccion-bomba-circuito-solar-termico.md)

Esta anotacion documenta el criterio seguido para introducir las piezas en T del circuito primario solar en `Calculos/herramienta_calculo.xlsm`. La cuestion es importante porque el libro no trata las T como una longitud fisica real, sino como una **longitud equivalente de tuberia recta** que se suma al tramo para calcular la perdida de carga.

En consecuencia, una misma T puede aumentar mucho o poco la perdida de carga segun el tipo elegido. La seleccion correcta no depende de la longitud real del tramo, sino de **como circula el fluido por la T** dentro del recorrido mas desfavorable.

## 1. Criterio de calculo usado por el Excel

En las hojas hidraulicas del libro, como `CH_Prim`, la perdida de carga de cada tramo se calcula a partir de:

```text
L_total = L_recta_real + L_equivalente_singularidades
```

y posteriormente:

```text
Pdc_tramo = perdida_lineal_mmca_m * L_total
```

Donde:

| Magnitud | Significado |
| --- | --- |
| `L_recta_real` | Longitud fisica medida del tramo de tuberia |
| `L_equivalente_singularidades` | Longitud equivalente anadida por codos, curvas, reducciones, T, valvulas, etc. |
| `Pdc_tramo` | Perdida de carga del tramo en mm.c.a. |

Por tanto, cuando se selecciona una T tipo 1, tipo 2 o tipo 3, el libro no cambia la longitud real instalada. Lo que cambia es la **resistencia hidraulica equivalente** que esa T introduce en el tramo.

## 2. Valores de longitud equivalente para las T

La tabla interna del Excel asigna a cada tipo de T los siguientes valores de longitud equivalente, en metros de tuberia recta:

| Accesorio | DN18 | DN22 | DN28 | DN35 | DN42 | DN54 |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| T tipo 1 | 0,15 m | 0,20 m | 0,30 m | 0,40 m | 0,50 m | 0,60 m |
| T tipo 2 | 2,50 m | 3,00 m | 3,60 m | 4,10 m | 4,60 m | 5,00 m |
| T tipo 3 | 1,68 m | 1,80 m | 1,92 m | 2,40 m | 3,00 m | 3,60 m |

La diferencia entre los tres tipos es grande. Por ejemplo, en DN28:

```text
T tipo 1 = 0,30 m equivalentes
T tipo 2 = 3,60 m equivalentes
T tipo 3 = 1,92 m equivalentes
```

Esto explica por que la perdida de carga cambia de forma apreciable al elegir una T u otra.

## 3. Aplicacion al tramo real de 3,65 m

Para un tramo con longitud real:

```text
L_recta_real = 3,65 m
```

si se instala una sola T DN28, la longitud hidraulica resultante seria:

| Tipo de T | Calculo | Longitud hidraulica resultante |
| --- | ---: | ---: |
| T tipo 1 | 3,65 + 0,30 | 3,95 m |
| T tipo 2 | 3,65 + 3,60 | 7,25 m |
| T tipo 3 | 3,65 + 1,92 | 5,57 m |

Por tanto, aunque la tuberia instalada mida fisicamente **3,65 m**, el tramo puede comportarse hidraulicamente como un tramo de **3,95 m**, **5,57 m** o **7,25 m**, segun la T seleccionada.

Si existen varias T en el mismo tramo, sus longitudes equivalentes se suman. Por ejemplo, dos T tipo 2 DN28 anadirian:

```text
2 * 3,60 = 7,20 m equivalentes
```

y el tramo de 3,65 m pasaria a calcularse como:

```text
3,65 + 7,20 = 10,85 m hidraulicos
```

## 4. Interpretacion de T tipo 1, tipo 2 y tipo 3

La eleccion del tipo de T debe hacerse segun el recorrido del fluido por la pieza:

| Tipo | Interpretacion hidraulica | Criterio de uso |
| --- | --- | --- |
| T tipo 1 | Paso favorable por la T, normalmente paso recto por el colector principal | Usar cuando el fluido atraviesa la T practicamente en linea recta y la derivacion no forma parte del recorrido analizado |
| T tipo 2 | Paso desfavorable, normalmente entrada o salida por el ramal a 90 grados | Usar cuando el recorrido mas desfavorable obliga al fluido a girar por la derivacion de la T |
| T tipo 3 | Caso intermedio de division o mezcla de caudal | Usar cuando la T trabaja como punto de reparto o union de caudales y no corresponde claramente al paso recto ni al giro mas desfavorable |

En instalaciones solares con baterias de captadores y retorno invertido, es habitual encontrar T que solo sirven para repartir o recoger caudales entre ramales. En esos casos no debe elegirse automaticamente el tipo mas penalizante para todas las piezas. Hay que identificar el recorrido hidraulico mas desfavorable y decidir en cada T si el fluido:

1. pasa recto por la T;
2. gira por el ramal;
3. se reparte o se mezcla con otro caudal.

## 5. Criterio adoptado para el proyecto

Para el dimensionado del circuito primario se adopta el siguiente criterio:

| Situacion en obra | Tipo a introducir en Excel |
| --- | --- |
| El fluido pasa por la T siguiendo el tubo principal | T tipo 1 |
| El fluido entra o sale por la boca lateral de la T, con cambio de direccion de 90 grados | T tipo 2 |
| La T funciona como punto de reparto o union de caudales entre ramales | T tipo 3 |

Este criterio evita dos errores habituales:

1. **Infravalorar las perdidas**, introduciendo todas las T como tipo 1 aunque algunas obliguen al fluido a girar por el ramal.
2. **Sobredimensionar la bomba**, introduciendo todas las T como tipo 2 aunque muchas sean pasos rectos o puntos de reparto.

## 6. Impacto sobre la seleccion de la bomba

La perdida de carga total del circuito primario condiciona directamente la altura manometrica necesaria de la bomba solar. Por eso, la seleccion de accesorios en T afecta a:

| Elemento afectado | Consecuencia |
| --- | --- |
| Perdida de carga de tuberias | Aumenta al crecer la longitud equivalente |
| Perdida de carga total del circuito | Aumenta si el recorrido desfavorable incluye T tipo 2 o varias T tipo 3 |
| Punto de trabajo de la bomba | Se desplaza hacia mayor altura manometrica requerida |
| Margen de seguridad | Puede reducirse si se subestiman las singularidades |

No obstante, la longitud real de 3,65 m no debe sustituirse por la longitud equivalente de la T. La forma correcta es conservar la longitud real del tramo y anadir las singularidades mediante el campo correspondiente del Excel.

## 7. Conclusion

La diferencia entre T tipo 1, tipo 2 y tipo 3 es una diferencia de **resistencia hidraulica**, no de longitud geometrica instalada. Para el tramo real de **3,65 m**, la perdida de carga cambia porque el Excel suma una longitud equivalente distinta segun el camino del fluido por la T.

El criterio de proyecto sera:

```text
T tipo 1 -> paso recto
T tipo 2 -> giro por ramal a 90 grados
T tipo 3 -> reparto o mezcla de caudal
```

Con este criterio, el dimensionado del circuito primario refleja mejor el comportamiento real de los accesorios y evita tanto infravalorar las perdidas como sobredimensionar innecesariamente la bomba.
