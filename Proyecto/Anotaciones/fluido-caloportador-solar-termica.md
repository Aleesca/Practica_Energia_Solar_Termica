# Determinacion del caudal especifico del fluido caloportador

Esta anotacion tecnica fija el caudal especifico de diseno del fluido caloportador en el circuito primario de la instalacion solar termica centralizada. El criterio se obtiene de la documentacion de Viessmann consultada en el notebook `Catalogos_solar` y se aplica al campo definitivo de captadores seleccionado para el proyecto.

La instalacion adopta un campo solar formado por **12 captadores Viessmann Vitosol 200-FM, modelo vertical SV2F**, distribuidos en **dos filas de 6 captadores**. Esta configuracion no modifica el caudal especifico recomendado por el fabricante, pero si determina el caudal total que debe mover la bomba solar y el reparto hidraulico entre filas.

## 1. Datos de partida de la instalacion

| Parametro | Valor |
| --- | ---: |
| Tipo de instalacion | Solar termica centralizada para ACS |
| Captador seleccionado | Viessmann Vitosol 200-FM SV2F |
| Numero total de captadores | 12 |
| Distribucion del campo | 2 filas de 6 captadores |
| Superficie de apertura por captador usada en Excel | 2,33 m2 |
| Superficie de apertura por fila usada en Excel | 13,98 m2 |
| Superficie de apertura total usada en Excel | 27,96 m2 |
| Superficie de absorcion por captador segun Viessmann | 2,31 m2 |
| Superficie de absorcion por fila para caudal fabricante | 13,86 m2 |
| Superficie de absorcion total para caudal fabricante | 27,72 m2 |

El libro `Calculos/herramienta_calculo.xlsm` solo admite una superficie por captador y la arrastra al resto de calculos. En ese libro debe mantenerse la **superficie de apertura de 2,33 m2**, porque es la superficie usada en el balance energetico, en la superficie de captacion resultante y en las relaciones de acumulacion del proyecto. La **superficie de absorcion de 2,31 m2** se usa aqui solo para interpretar fielmente el caudal especifico del fabricante, ya que Viessmann define el caudal volumetrico especifico sobre esa magnitud.

## 2. Criterio de catalogo Viessmann

La documentacion de planificacion de Viessmann expresa el caudal del circuito solar como caudal volumetrico especifico en:

```text
L/(h·m²)
```

La magnitud de referencia indicada para esta unidad es la superficie de absorcion del captador. Para el Vitosol 200-FM SV2F, el catalogo especifico del captador recoge:

| Superficie del captador SV2F | Valor |
| --- | ---: |
| Superficie bruta | 2,51 m² |
| Superficie de apertura | 2,33 m² |
| Superficie de absorcion | 2,31 m² |

El manual de planificacion permite trabajar con distintos regimenes de caudal. En la tabla de dimensionado hidraulico aparecen valores de **25, 30, 35, 40, 50, 60 y 80 L/(h·m²)**. Los valores de 25 a 30 L/(h·m²) corresponden al funcionamiento con caudal bajo, mientras que los valores superiores se asocian a regimenes de caudal mas elevado.

## 3. Valor de diseno adoptado

Se adopta como valor de diseno:

```text
q_especifico = 25 L/(h·m²)
```

Este valor corresponde a un funcionamiento de **caudal bajo** y es coherente con los ejemplos de calculo de Viessmann para instalaciones con regulacion solar capaz de modular el caudal de la bomba. El caudal bajo reduce el consumo electrico de bombeo y es compatible con el captador seleccionado siempre que se garantice una circulacion uniforme en cada bateria.

La eleccion de 25 L/(h·m²) no implica que la instalacion no pueda funcionar a caudal compensado. Si se instala una regulacion solar modulante, el sistema puede ajustar automaticamente el caudal en funcion de la radiacion y de las temperaturas del acumulador, tomando este valor como referencia de dimensionado hidraulico.

## 4. Compatibilidad con la superficie usada en Excel

Existe una diferencia pequena entre las dos superficies del captador:

| Magnitud | Valor por captador | Uso en el proyecto |
| --- | ---: | --- |
| Superficie de apertura | 2,33 m2 | Superficie unica introducida en Excel |
| Superficie de absorcion | 2,31 m2 | Referencia del caudal especifico Viessmann |

Por tanto, no conviene cambiar el Excel a 2,31 m2, porque alteraria el balance f-Chart, la superficie de captacion, la relacion volumen/superficie y las anotaciones ya coherentes con **27,96 m2**. Para la parte hidraulica se documenta la equivalencia:

```text
25 L/(h·m²_abs) * 2,31 / 2,33 = 24,8 L/(h·m²_apertura)
```

En la practica, si el Excel obliga a usar la misma superficie de apertura de 2,33 m2 y se introduce **25 L/(h·m²)** como caudal especifico, el resultado queda ligeramente conservador:

```text
Q_total_Excel = 25 L/(h·m²) * 27,96 m² = 699 L/h
```

La diferencia frente al calculo estricto sobre absorcion es:

```text
699 L/h - 693 L/h = 6 L/h
```

Es una desviacion del orden del 0,9 %, despreciable para el predimensionado de bomba y equilibrado. Por coherencia documental, se mantiene como valor de diseno **25 L/(h·m²)** y se indica que en el Excel se aplica sobre la superficie de apertura.

## 5. Calculo del caudal por fila y total segun referencia Viessmann

La relacion de calculo aplicada es:

```text
Q = q_especifico * A_absorcion
```

donde:

* `Q` es el caudal volumetrico en L/h.
* `q_especifico` es el caudal especifico en L/(h·m²).
* `A_absorcion` es la superficie de absorcion de los captadores en m².

### Superficie por fila

```text
A_fila = 6 captadores * 2,31 m²/captador = 13,86 m²
```

### Superficie total del campo

```text
A_total = 12 captadores * 2,31 m²/captador = 27,72 m²
```

### Caudal por fila

```text
Q_fila = 25 L/(h·m²) * 13,86 m² = 346,5 L/h
```

Conversion a L/min:

```text
346,5 L/h / 60 = 5,78 L/min
```

### Caudal total del campo

```text
Q_total = 25 L/(h·m²) * 27,72 m² = 693 L/h
```

Conversion a L/min:

```text
693 L/h / 60 = 11,55 L/min
```

## 6. Resultado de diseno

El caudal especifico adoptado para el fluido caloportador del circuito primario es:

| Magnitud | Valor adoptado |
| --- | ---: |
| Caudal especifico | **25 L/(h·m²)** |
| Regimen de funcionamiento | Caudal bajo |
| Superficie de referencia del fabricante | Superficie de absorcion |
| Superficie unica mantenida en Excel | Superficie de apertura |
| Caudal por fila de 6 captadores segun absorcion | **346,5 L/h** (**5,78 L/min**) |
| Caudal total para 12 captadores segun absorcion | **693 L/h** (**11,55 L/min**) |
| Caudal total equivalente si se aplica en Excel sobre apertura | **699 L/h** (**11,65 L/min**) |

Por tanto, la bomba solar y los elementos de regulacion del primario deben poder establecer un caudal total de referencia de aproximadamente **693-699 L/h**, repartido en dos ramales equilibrados de aproximadamente **346,5-349,5 L/h** cada uno. Para el Excel se puede mantener **25 L/(h·m²)** sobre la superficie de apertura sin introducir una inconsistencia relevante.

## 7. Implicaciones hidraulicas

La configuracion en dos filas de 6 captadores no cambia el caudal especifico de diseno, ya que este depende del modelo de captador, de la superficie de absorcion y del modo de funcionamiento seleccionado. Su efecto principal esta en el reparto del caudal:

* Cada fila debe recibir aproximadamente la mitad del caudal total.
* El trazado debe favorecer el equilibrado hidraulico entre ambas filas, preferiblemente mediante longitudes equivalentes o retorno invertido.
* Si las perdidas de carga de las dos filas no son equivalentes, se deben prever elementos de equilibrado para evitar que una fila trabaje con caudal insuficiente.
* La bomba solar debe seleccionarse considerando el caudal total y la perdida de carga del circuito mas desfavorable, no solo el caudal especifico.
* El dimensionado de tuberias debe mantener velocidades compatibles con una circulacion estable y con perdidas de carga razonables.

El funcionamiento a caudal bajo es tecnicamente adecuado siempre que el fluido caloportador circule de forma segura y uniforme por todos los captadores. La regulacion modulante de la bomba, si se incorpora, permite adaptar el caudal real a las condiciones de radiacion y temperatura, manteniendo el valor calculado como referencia de diseno.

## 8. Referencias y fuentes

* NotebookLM `Catalogos_solar` (ID: `7d1bf88b-463a-4291-9201-1959144a5921`).
* `Vitosol-200-FM.pdf`: catalogo especifico del captador Viessmann Vitosol 200-FM, modelo SV2F/SH2F. Fuente de las superficies bruta, de apertura y de absorcion.
* `Intrucciones_planificacion_captadores_Viessmann.pdf`: manual de planificacion de captadores Viessmann. Fuente del criterio de caudal volumetrico especifico en L/(h·m²), de la referencia a superficie de absorcion y de la tabla de caudales de 25 a 80 L/(h·m²).
* Anotaciones relacionadas:
  * `seleccion-equipos-solar-centralizado.md`.
  * `balance-energetico-solar-termica.md`.
  * `seleccion-interacumulador-acs-bivalente-lapesa.md`.
