# Selección de Bombas de Circulación Grundfos para la Instalación Solar Térmica

Esta anotación técnica detalla la selección, justificación y especificaciones técnicas de todos los equipos de bombeo hidráulico necesarios para la instalación solar térmica colectiva y sus circuitos asociados. El diseño se unifica bajo el catálogo del fabricante **Grundfos**, eliminando comparativas con otros fabricantes para asegurar la homogeneidad y compatibilidad del sistema.

---

## 1. Resumen Ejecutivo

El diseño hidráulico de la planta de energía solar térmica y del sistema bivalente de acumulación requiere la especificación de **tres equipos de bombeo independientes**, cada uno operando en condiciones y fluidos de trabajo distintos:

1.  **Bomba del Circuito Primario Solar (Sótano a Azotea):** **Grundfos MAGNA3 40-180 F** (Modelo comercial de alta presión, necesario para elevar el fluido caloportador a la cota de la azotea).
2.  **Bomba de Recirculación de ACS (Anillo de Consumo):** **Grundfos ALPHA2 25-40 N 180** (Modelo en acero inoxidable, obligatorio por normativa de salud pública).
3.  **Bomba del Circuito de Apoyo de Caldera (Sala Técnica):** **Grundfos ALPHA2 25-60 180** (Modelo en fundición de hierro para el bucle cerrado caldera-serpentín).

---

## 2. Inventario Técnico de la Instalación y Parámetros de Diseño

Los datos fijos del proyecto que determinan los puntos de trabajo de las bombas son:

*   **Campo de Captadores:** 12 colectores planos **Viessmann Vitosol 200-FM (SV2F)** en 2 filas paralelas de 6 captadores (sistema Tichelmann de retorno invertido).
*   **Superficie de Absorción Total:** **$27,72\text{ m}^2$** ($2,31\text{ m}^2$ por captador).
*   **Caudal Solar de Diseño:** **$693\text{ L/h}$** ($11,55\text{ L/min}$) en régimen de caudal bajo (*Low-Flow*), dividido en dos ramales de **$346,5\text{ L/h}$** cada uno.
*   **Fluido del Primario:** Mezcla de agua y glicol propileno (anticongelante atóxico) con una concentración del **30% al 50%** (Zona climática D2, Salamanca).
*   **Depósito de Acumulación:** Interacumulador bivalente de **$2.000\text{ litros}$** (**Lapesa Master Inox MXV-2000 SS2B**) con serpentín solar inferior de **$3,4\text{ m}^2$** y serpentín de apoyo superior de **$2,0\text{ m}^2$**.
*   **Sistema de Apoyo:** Caldera mural centralizada de gas natural de **$22\text{ kW}$**.

---

## 3. Ubicación y Justificación de cada Equipo de Bombeo

Para garantizar la durabilidad, el rendimiento térmico y la seguridad higiénico-sanitaria de la instalación, se define a continuación la ubicación física exacta y la justificación técnica para cada una de las bombas del sistema:

### A. Bomba del Circuito Primario Solar (Grundfos MAGNA3 40-180 F)
*   **Ubicación Física:** Se debe instalar en la **tubería de retorno del primario solar**, es decir, en el tramo frío que conecta la salida del serpentín inferior del interacumulador con la entrada al campo de captadores en la azotea.
*   **Justificación Técnica:**
    1.  **Protección contra Altas Temperaturas:** Al situar la bomba en la zona fría de retorno, se evita que sus juntas, cojinetes y la electrónica integrada del motor de rotor húmedo se expongan a las elevadas temperaturas de impulsión ($>95^\circ\text{C}$) procedentes de los paneles solares.
    2.  **Prevención de Cavitación:** El fluido caloportador en el retorno se encuentra a menor temperatura, lo que aumenta la presión neta de aspiración positiva (NPSH) disponible y elimina el riesgo de cavitación por vaporización local del fluido en el rodete.
    3.  **Montaje del Eje:** El motor debe orientarse de forma que el **eje de rotación quede estrictamente en posición horizontal** para asegurar que el propio fluido lubrique continuamente los cojinetes y se facilite la purga de aire.

### B. Circuito Secundario Solar (Bomba NO Requerida)
*   **Justificación Técnica:** Al seleccionarse un interacumulador bivalente con serpentín inferior interno, el calor se transfiere directamente de forma estática al agua de consumo contenida en el acumulador. No existe un intercambiador de placas externo y, por lo tanto, **se prescinde por completo de bomba secundaria solar**. El agua de consumo se calienta directamente y asciende por termosifón interno, manteniendo una estratificación térmica óptima.

### C. Bomba de Recirculación de ACS (Grundfos ALPHA2 25-40 N 180)
*   **Ubicación Física:** Se debe colocar en la **tubería de retorno del anillo de recirculación de ACS**, inmediatamente antes de su conexión al interacumulador (en la toma intermedia-baja de retorno del depósito Lapesa).
*   **Justificación Técnica:**
    1.  **Cierre de Bucle:** Mueve el agua sanitaria que se ha enfriado en las montantes de distribución del edificio de vuelta al acumulador para su recalentamiento, manteniendo el anillo a $>50^\circ\text{C}$ contra legionela.
    2.  **Accesorios de Seguridad:** Debe contar obligatoriamente con una **válvula de retención a la salida** (para evitar flujos inversos de agua fría de red hacia el anillo de recirculación) y un **filtro de impurezas a la entrada** (para proteger el rotor de depósitos calcáreos y lodos).

### D. Bomba de Apoyo de la Caldera (Grundfos ALPHA2 25-60 180)
*   **Ubicación Física:** Se instalará en la **tubería de retorno del lazo de intercambio** (el tramo que sale de la parte superior del serpentín de apoyo superior del interacumulador y se dirige hacia el retorno de la caldera).
*  
 **Justificación Técnica:**
    1.  **Protección de la Electrónica del Circulador:** Aunque los circuladores Grundfos toleran hasta $110^\circ\text{C}$, situarla en el retorno (donde el agua ya ha cedido su calor en el serpentín superior, bajando de $80^\circ\text{C}$ a unos $60^\circ\text{C}$) reduce significativamente el estrés térmico de la bomba y prolonga su vida útil.
    2.  **Optimización del Caudal de Caldera:** Al succionar desde el interacumulador y empujar el agua hacia el retorno de la caldera, se asegura una presión de aspiración estable en la caldera, previniendo choques térmicos y garantizando que el intercambiador de calor de la caldera trabaje en régimen óptimo.
    3.  **Válvula Antirretorno:** Se instalará una válvula de retención a la salida de la bomba para impedir que el agua del circuit## 4. Especificaciones y Justificaciones de las Bombas Grundfos Prescritas

A continuación se detallan el equipo prescrito, su ubicación, su justificación funcional y las especificaciones técnicas para cada uno de los tres circuladores de alta eficiencia de Grundfos:

### 1. Bomba del Circuito Primario Solar: Grundfos MAGNA3 40-180 F
*   **¿Qué bomba se instala?** Circulador de rotor húmedo de alta eficiencia y alta altura manométrica.
*   **¿Dónde se instala?** En la tubería de retorno del primario solar, en la sala de máquinas del sótano, inmediatamente a la salida del serpentín inferior del interacumulador Lapesa.
*   **¿Por qué se instala?** Es imprescindible para impulsar el fluido caloportador (agua + glicol propileno 30-50%) a lo largo de todo el bucle solar primario. Dado que la sala técnica está en el sótano y los captadores en la azotea, la bomba debe poder vencer la cota estática de **$13\text{ m}$** durante la fase de llenado inicial de la red o en sistemas de vaciado por gravedad (drainback), por lo que se requiere un modelo con altura nominal de $18\text{ m.c.a.}$, superando los límites de los circuladores domésticos estándar. Su posición en el retorno frío la protege contra sobretemperaturas.
*   **Especificaciones Técnicas:**
    *   **Número de Producto:** **97924272**
    *   **Material del Cuerpo:** Fundición de hierro con recubrimiento por cataforesis (apto para circuito cerrado).
    *   **Altura Manométrica Máxima ($H_{max}$):** **$18,0\text{ m.c.a.}$** (180 dm).
    *   **Caudal Máximo ($Q_{max}$):** $20,0\text{ m}^3\text{/h}$ (adecuado para operar con el caudal de diseño de $0,69\text{ m}^3\text{/h}$).
    *   **Temperatura de Líquido:** $-10^\circ\text{C}$ a $110^\circ\text{C}$.
    *   **Compatibilidad con Glicol:** Apto para mezclas de agua y glicol propileno hasta el **50%** de concentración.
    *   **Tipo de Conexión:** Brida DN40 (PN 6/10) con una longitud entre bocas de $220\text{ mm}$ (requiere contrabridas reductoras cónicas céntricas para tubería DN25).
    *   **Modo de Control:** Velocidad variable electrónica compatible con lógica de consigna externa.
    *   **Consumo Eléctrico:** De $9\text{ W}$ a $604\text{ W}$ ($\text{EEI} \le 0,18$).
*   **Ficha Técnica Oficial (Grundfos Product Center):**
    > [Grundfos MAGNA3 40-180 F (97924272) - Ficha Técnica Oficial](https://product-selection.grundfos.com/product-detail.product-detail.html?productnumber=97924272)

---

### 2. Bomba de Recirculación de ACS: Grundfos ALPHA2 25-40 N 180
*   **¿Qué bomba se instala?** Circulador electrónico de alta eficiencia en acero inoxidable.
*   **¿Dónde se instala?** En la tubería de retorno del anillo de recirculación de ACS en el sótano, justo antes de reingresar al interacumulador Lapesa por su toma intermedia-baja.
*   **¿Por qué se instala?** Impulsa el agua sanitaria que se ha enfriado en las montantes de distribución del edificio de vuelta al acumulador para su recalentamiento, manteniendo la red a $>50^\circ\text{C}$ sanitarios (exigencia del **R.D. 487/2022** contra legionela).
*   **Especificaciones Técnicas:**
    *   **Número de Producto:** **99411365**
    *   **Material del Cuerpo:** **Acero Inoxidable (AISI 304)**, obligatorio por normativa sanitaria para evitar corrosión galvánica y cal en circuitos de agua potable abierta.
    *   **Altura Manométrica Máxima ($H_{max}$):** **$4,0\text{ m.c.a.}$** (suficiente para vencer las pérdidas dinámicas de fricción del retorno, estimadas en $\approx 0,84-1,7\text{ m.c.a.}$).
    *   **Caudal Máximo ($Q_{max}$):** $2,4\text{ m}^3\text{/h}$.
    *   **Temperatura de Líquido:** $2^\circ\text{C}$ a $110^\circ\text{C}$.
    *   **Tipo de Conexión:** Rosca G 1 1/2" (DN25), con longitud entre bocas de $180\text{ mm}$.
    *   **Modo de Control:** Regulación electrónica, velocidad fija y función inteligente **AUTOADAPT** (aprende y memoriza las horas de uso de los grifos en las viviendas para optimizar la recirculación).
    *   **Consumo Eléctrico:** De $3\text{ W}$ a $18\text{ W}$ ($\text{EEI} \le 0,15$).
*   **Ficha Técnica Oficial (Grundfos Product Center):**
    > [Grundfos ALPHA2 25-40 N 180 (99411365) - Ficha Técnica Oficial](https://product-selection.grundfos.com/product-detail.product-detail.html?productnumber=99411365)

---

### 3. Bomba del Circuito de Apoyo de Caldera: Grundfos ALPHA2 25-60 180
*   **¿Qué bomba se instala?** Circulador electrónico de alta eficiencia para bucles cerrados de calefacción.
*   **¿Dónde se instala?** En la tubería de retorno del lazo de intercambio en el sótano, que va desde la salida del serpentín de apoyo superior del interacumulador Lapesa hasta la conexión de retorno de la caldera.
*   **¿Por qué se instala?** Es necesaria para hacer circular el agua de calefacción entre la caldera auxiliar de $22\text{ kW}$ y el serpentín superior de intercambio del acumulador. Situarla en el retorno (donde el agua ya ha cedido calor en el serpentín, bajando a unos $60^\circ\text{C}$ en vez de los $80^\circ\text{C}$ de la ida) reduce el estrés térmico de la bomba y prolonga su vida útil, además de garantizar una presión de succión estable para el intercambiador de la caldera.
*   **Especificaciones Técnicas:**
    *   **Número de Producto:** **99411175**
    *   **Material del Cuerpo:** Fundición de hierro (apto para circuito cerrado de calefacción).
    *   **Altura Manométrica Máxima ($H_{max}$):** **$6,0\text{ m.c.a.}$** (suficiente para vencer las resistencias de la caldera y del serpentín superior de $2,0\text{ m}^2$).
    *   **Caudal Máximo ($Q_{max}$):** $3,2\text{ m}^3\text{/h}$ (permite absorber el caudal nominal de unos $0,95 - 1,89\text{ m}^3\text{/h}$ requerido para la potencia de caldera de $22\text{ kW}$).
    *   **Temperatura de Líquido:** $2^\circ\text{C}$ a $110^\circ\text{C}$.
    *   **Tipo de Conexión:** Rosca G 1 1/2" (DN25), con longitud entre bocas de $180\text{ mm}$.
    *   **Modo de Control:** Regulación electrónica, control proporcional y función AUTOADAPT.
    *   **Consumo Eléctrico:** De $3\text{ W}$ a $34\text{ W}$ ($\text{EEI} \le 0,17$).
*   **Ficha Técnica Oficial (Grundfos Product Center):**
    > [Grundfos ALPHA2 25-60 180 (99411175) - Ficha Técnica Oficial](https://product-selection.grundfos.com/products/alpha2/alpha2-25-60-180-99411175)

---

## 5. Matriz de Especificaciones Técnicas (Unificada Grundfos)

| Variable de Selección | Bomba Primario Solar <br>(Sótano-Azotea) | Bomba Recirculación ACS <br>(Retorno Anillo) | Bomba Apoyo Caldera <br>(Lazo Intercambio) |
| :--- | :---: | :---: | :---: |
| **Modelo Prescrito** | **Grundfos MAGNA3 40-180 F** | **Grundfos ALPHA2 25-40 N 180** | **Grundfos ALPHA2 25-60 180** |
| **Número de Producto** | **97924272** | **99411365** | **99411175** |
| **Material del Cuerpo** | Fundición de Hierro (Cataforesis) | **Acero Inoxidable (AISI 304)** | Fundición de Hierro |
| **Altura Nominal Máxima** | **$18,0\text{ m.c.a.}$** | $4,0\text{ m.c.a.}$ | $6,0\text{ m.c.a.}$ |
| **Caudal Máximo** | $20,0\text{ m}^3\text{/h}$ | $2,4\text{ m}^3\text{/h}$ | $3,2\text{ m}^3\text{/h}$ |
| **Fluido de Trabajo** | Agua + Glicol Propileno (30-50%) | Agua Potable Sanitaria | Agua de Calefacción (VDI 2035) |
| **Rango de Temperatura** | $-10^\circ\text{C}$ a $110^\circ\text{C}$ | $2^\circ\text{C}$ a $110^\circ\text{C}$ | $2^\circ\text{C}$ a $110^\circ\text{C}$ |
| **Tipo de Conexión** | Brida DN40 (PN 6/10) | Rosca G 1 1/2" (DN25) | Rosca G 1 1/2" (DN25) |
| **Longitud entre Bocas** | $220\text{ mm}$ | $180\text{ mm}$ | $180\text{ mm}$ |
| **Consumo Eléctrico** | $9 - 604\text{ W}$ | **$3 - 18\text{ W}$** | $3 - 34\text{ W}$ |
| **Índice Eficiencia (EEI)**| $\le 0,18$ | $\le 0,15$ | $\le 0,17$ |
| **Modo de Control** | Velocidad Variable / Señal Externa | AUTOADAPT / Presión variable | AUTOADAPT / Presión variable |

---

## 6. Evaluación Hidráulica y Consideraciones de Montaje

### A. Comportamiento en Circuito Cerrado vs. Llenado
*   **Fase de Llenado Inicial:** La bomba **MAGNA3 40-180 F** en el sótano debe elevar el fluido los $15,5\text{ m}$ de cota estática hasta la azotea. Su altura máxima de $18,0\text{ m.c.a.}$ asegura que el circuito pueda purgarse y llenarse de fluido caloportador sin necesidad de bombas auxiliares de carga permanente.
*   **Fase de Régimen Estable:** Una vez purgado y presurizado, el primario solar se comporta como un circuito cerrado. La presión estática se equilibra en los dos ramales de subida y bajada. La bomba reduce su velocidad modulante, consumiendo un mínimo de potencia eléctrica para vencer únicamente las pérdidas de carga dinámicas de fricción de la red (estimadas entre $3$ y $6\text{ m.c.a.}$).

### B. Transiciones de Diámetro en Sala Técnica
La bomba MAGNA3 seleccionada cuenta con conexiones embridadas DN40. Dado que el diámetro de la tubería de cobre del circuito primario es típicamente DN25 o DN32, se debe prescribir obligatoriamente en el plano de montaje:
*   La instalación de **contrabridas reductoras cónicas concéntricas** a la entrada (aspiración) y salida (impulsión) del circulador solar. Esto garantiza una transición de diámetros progresiva, reduciendo las turbulencias y las pérdidas de carga localizadas.

---

## 7. Referencias y Fuentes

*   **Notebook de Consulta:** `Energia_Solar_Termica` (ID: `62b2af52-7df4-455e-9334-8b10ebd8118d`).
    *   *Documento de Conceptos Generales:* Criterios de dimensionado y requerimientos de recirculación sanitaria (Legionella).
    *   *Casos Prácticos:* Pérdida de carga de tramos de recirculación de ACS y cuerpo de bronce/acero inoxidable.
*   **Documentación de Fabricante (Grundfos Product Center):**
    *   Ficha técnica oficial de bomba solar: [Grundfos MAGNA3 40-180 F](https://product-selection.grundfos.com/product-detail.product-detail.html?productnumber=97924272)
    *   Ficha técnica oficial de recirculación ACS: [Grundfos ALPHA2 25-40 N 180](https://product-selection.grundfos.com/product-detail.product-detail.html?productnumber=99411365)
    *   Ficha técnica oficial de apoyo caldera: [Grundfos ALPHA2 25-60 180](https://product-selection.grundfos.com/products/alpha2/alpha2-25-60-180-99411175)
*   **Anotaciones Técnicas Relacionadas:**
    *   [especificacion-antecedentes-y-datos-de-partida.md](../Especificaciones/especificacion-antecedentes-y-datos-de-partida.md)
    *   [fluido-caloportador-solar-termica.md](fluido-caloportador-solar-termica.md)
    *   [seleccion-interacumulador-acs-bivalente-lapesa.md](seleccion-interacumulador-acs-bivalente-lapesa.md)
