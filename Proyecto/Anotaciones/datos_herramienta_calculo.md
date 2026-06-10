# Datos extraidos de `herramienta_calculo.xlsm` y tramo mas desfavorable

Fecha de extraccion: 2026-06-10  
Origen: `Calculos/herramienta_calculo.xlsm`  
Modo de lectura: solo lectura; no se ha modificado ni guardado el Excel.

## 1. Criterio aplicado

La consulta al notebook `Energia_Solar_Termica` indica que, para seleccionar la bomba y determinar el caso hidraulicamente mas exigente, debe tomarse el **recorrido del fluido con mayor perdida de carga total**.

El criterio documentado por el notebook es:

- La perdida de carga total suma las perdidas en tuberias, las perdidas singulares de accesorios, el intercambiador y los captadores cuando estos datos existen.
- La perdida de cada tramo de tuberia depende del caudal, diametro interior, perdida unitaria, longitud recta y longitud equivalente de singularidades.
- La longitud de calculo es `L_total = L_recta + L_singularidades`.
- La perdida de un tramo se calcula como `Pdc_tramo = Pdc_unitaria * L_total`.
- Para la bomba se usa la altura manometrica asociada al recorrido mas desfavorable y al caudal del circuito.

Fuente NotebookLM: notebook `Energia_Solar_Termica`, fuente citada `619ee7b3-cad9-49f2-ab18-3a430c48e63f`.

## 2. Configuracion activa del proyecto

| Dato | Celda | Valor |
| --- | ---: | ---: |
| Localizacion | `Datos!G5` | SALAMANCA |
| Latitud | `Datos!G7` | 40,968975 grados N |
| Inclinacion captadores | `Datos!G8` | 60 grados |
| Azimut captadores | `Datos!G9` | 20 grados |
| Perdidas por orientacion | `Datos!G10` | 0,014 |
| Perdidas por sombras | `Datos!G11` | 0 |
| Topologia de acumulacion | `Datos!AA51` | 1 |
| Texto de topologia | `Datos!AA52` | Edif. Multifamiliar: Acumulacion solar CENTRALIZADA |
| Viviendas | `Principal!H12` | 10 |
| Personas | `Principal!H13` | 40 |
| Caudal minimo ACS | `Principal!H14` | 28 l/(persona dia viv) |
| Temperatura ACS | `Principal!H15` | 60 grados C |
| Factor simultaneidad | `Principal!H16` | 0,95 |
| Caudal ACS demandado | `Principal!H17` | 1064 l/dia |
| Numero de captadores seleccionados | `Principal!G63` | 12 |
| Acumulacion seleccionada | `Principal!G65` | 2000 l |

La topologia activa apunta a la hoja `CH_Prim`, titulada internamente como circuito primario de captacion solar para edificio multifamiliar con acumulacion de ACS centralizada.

## 3. Datos hidraulicos del circuito primario activo (`CH_Prim`)

Datos generales:

| Dato | Celda | Valor |
| --- | ---: | ---: |
| Numero de captadores | `CH_Prim!H5` | 12 |
| Superficie de cada captador | `CH_Prim!H6` | 2,33 m2/captador |
| Caudal especifico de fluido caloportador | `CH_Prim!H7` | 25 l/(h m2) |
| Caudal del circuito primario | `CH_Prim!H8` | 699 l/h |
| Velocidad maxima aconsejada | `CH_Prim!H11` | 2,5 - 3 m/s |

Tabla comparativa de tramos:

| Tramo | Caudal (l/h) | Di (mm) | Velocidad (m/s) | Pdc unitaria (mm.c.a./m) | Aislamiento (mm) | L recta (m) | Singularidades eq. (m) | L total (m) | Pdc tramo (mm.c.a.) | Pdc tramo (m.c.a.) |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| C1-A | 349,5 | 16 | 0,483 | 26,479 | 30 | 6,06 | 3,00 | 9,06 | 239,898 | 0,2399 |
| C2-A | 349,5 | 16 | 0,483 | 26,479 | 30 | 1,03 | 0,15 | 1,18 | 31,245 | 0,0312 |
| A-Deposito | 699 | 20 | 0,619 | 30,859 | 30 | 3,78 | 0,20 | 3,98 | 122,818 | 0,1228 |
| Deposito-B | 699 | 20 | 0,619 | 30,859 | 30 | 3,65 | 0,20 | 3,85 | 118,806 | 0,1188 |
| B-C2 | 349,5 | 16 | 0,483 | 26,479 | 30 | 1,34 | 0,15 | 1,49 | 39,453 | 0,0395 |
| B-C1 | 349,5 | 16 | 0,483 | 26,479 | 30 | 1,34 | 0,65 | 1,99 | 52,693 | 0,0527 |

Totales y seleccion de bomba en la hoja:

| Magnitud | Celda | Valor |
| --- | ---: | ---: |
| Perdida de carga en tuberias, `Pdctuberias` | `CH_Prim!H41` | 0,362715 m.c.a. |
| Formula perdida total | `CH_Prim!H48` | `H41+H45+H46/1000` |
| Perdida de carga total | `CH_Prim!H48` | 0,362715 m.c.a. |
| Formula altura manometrica | `CH_Prim!H53` | `H48+H49` |
| Altura manometrica | `CH_Prim!H53` | 0,362715 m.c.a. |

El total de tuberias `0,362715 m.c.a.` coincide exactamente con:

```text
C1-A        0,239898 m.c.a.
A-Deposito 0,122818 m.c.a.
----------------------------
Total       0,362715 m.c.a.
```

Por tanto, el recorrido mas desfavorable del circuito primario activo es:

```text
C1-A -> A-Deposito
```

Dentro de ese recorrido, el tramo individual mas desfavorable es:

```text
C1-A, con 0,239898 m.c.a.
```

## 4. Comparacion con otros totales hidraulicos del libro

Estos valores se han leido para control, pero no se toman como configuracion activa porque `Datos!AA51 = 1` selecciona acumulacion centralizada.

| Hoja | Configuracion representada | Perdida tuberias (m.c.a.) | Perdida total / altura (m.c.a.) | Uso en la conclusion |
| --- | --- | ---: | ---: | --- |
| `CH_Prim` | Multifamiliar, acumulacion centralizada, primario | 0,362715 | 0,362715 | Activa |
| `CH_Sec` | Multifamiliar, acumulacion centralizada, secundario | 0,305740 | 0,305740 | Control; tabla de tramos no poblada |
| `CH_PrimMixta` | Multifamiliar, acumulacion mixta, primario | 1,893203 | 3,423203 | No activa |
| `CH_AIndMixta` | Mixta, centralizada a interacumuladores individuales | 1,307701 | 1,807701 | No activa |
| `CH_AcumInd` | Multifamiliar, acumulacion individual | 3,604104 | 4,134104 | No activa |
| `CH_Unif` | Unifamiliar a medida | 0,668945 | 1,498945 / 5,498945 | No activa |

## 5. Conclusion

Aplicando el criterio del notebook, la seleccion debe basarse en el recorrido con mayor perdida de carga total, no solo en el tramo aislado con mayor perdida.

Para la configuracion activa del Excel (`Edif. Multifamiliar: Acumulacion solar CENTRALIZADA`), el **recorrido mas desfavorable del circuito primario** es:

```text
C1-A -> A-Deposito
```

con:

```text
Pdc tuberias = 0,362715 m.c.a.
Altura manometrica cacheada en la hoja = 0,362715 m.c.a.
```

Si se necesita nombrar un unico tramo, el tramo individual mas desfavorable es:

```text
C1-A
```

porque tiene la mayor perdida de carga individual de la tabla activa:

```text
Pdc C1-A = 239,898 mm.c.a. = 0,239898 m.c.a.
```

## 6. Observaciones

- El Excel se ha leido en modo no destructivo; no se ha recalculado ni guardado.
- Los valores usados son valores cacheados del `.xlsm`.
- En `CH_Prim`, las celdas `H45` y `H46` estan vacias. La formula de `H48` las suma como cero: `H41+H45+H46/1000`.
- En `CH_Prim`, `H53` calcula la altura manometrica como `H48+H49`; `H49` no contiene valor visible, por lo que la altura cacheada coincide con `H48`.
- La hoja `CH_Sec` conserva un total cacheado de `0,305740 m.c.a.`, pero no muestra una tabla de tramos poblada en las filas equivalentes a `CH_Prim`; por eso no se usa para identificar el tramo.
- La columna visible `mas desfavorable?` no contiene marcas en las filas de tramos de `CH_Prim`; la identificacion se ha reconstruido a partir del total de tuberias y de la suma de los tramos que lo componen.
