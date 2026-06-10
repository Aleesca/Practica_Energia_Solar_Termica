# Selección de Bombas de Circulación Grundfos para la Instalación Solar Térmica

Esta anotación técnica detalla la selección, justificación y especificaciones técnicas de los equipos de bombeo hidráulico necesarios para la instalación solar térmica colectiva y sus circuitos asociados. El diseño se unifica bajo el catálogo del fabricante **Grundfos**, asegurando la homogeneidad, compatibilidad y alta eficiencia energética del sistema.

---

## 1. Resumen Ejecutivo

El diseño hidráulico de la planta de energía solar térmica y del sistema de recirculación de ACS requiere la especificación de **dos equipos de bombeo independientes**, cada uno operando en condiciones y fluidos de trabajo distintos:

1.  **Bomba del Circuito Primario Solar (Azotea):** **Grundfos ALPHA SOLAR 25-75 180** (Modelo de rotor húmedo y alta eficiencia diseñado específicamente para aplicaciones solares térmicas, instalado en la cubierta para hacer circular el fluido caloportador en el circuito cerrado solar primario, compatible con PWM y mezclas de glicol).
2.  **Bomba de Recirculación de ACS (Anillo de Consumo):** **Grundfos ALPHA2 25-40 N 180** (Modelo en acero inoxidable, idóneo para instalaciones colectivas, dotado de regulación electrónica y función inteligente AUTOADAPT).

El circuito de apoyo de la caldera no requiere un circulador externo independiente en esta delimitación de diseño técnico, eliminando cualquier bomba de apoyo de caldera de este alcance.

---

## 2. Inventario Técnico de la Instalación y Parámetros de Diseño

Los datos fijos del proyecto que determinan los puntos de trabajo de las bombas son:

*   **Campo de Captadores:** 12 colectores planos **Viessmann Vitosol 200-FM (SV2F)** en 2 filas paralelas de 6 captadores (sistema Tichelmann de retorno invertido).
*   **Superficie de Absorción Total:** **$27,72\text{ m}^2$** ($2,31\text{ m}^2$ por captador).
*   **Caudal Solar de Diseño:** **$693\text{ L/h}$** ($11,55\text{ L/min}$) en régimen de caudal bajo (*Low-Flow*), dividido en dos ramales de **$346,5\text{ L/h}$** cada uno.
*   **Fluido del Primario:** Mezcla de agua y glicol propileno (anticongelante atóxico) con una concentración del **30% al 50%** (Zona climática D2, Salamanca).
*   **Depósito de Acumulación:** Interacumulador bivalente de **$2.000\text{ litros}$** (**Lapesa Master Inox MXV-2000 SS2B**) con serpentín solar inferior de **$3,4\text{ m}^2$** y serpentín de apoyo superior de **$2,0\text{ m}^2$**.
*   **Ubicación de Equipos:** Tanto el campo solar de captadores como el interacumulador bivalente Lapesa se ubican en la **azotea (cubierta)** del edificio.

---

## 3. Ubicación y Justificación de cada Equipo de Bombeo

Para garantizar la durabilidad, el rendimiento térmico y la seguridad higiénico-sanitaria de la instalación, se define a continuación la ubicación física exacta y la justificación técnica para cada una de las bombas del sistema:

### A. Bomba del Circuito Primario Solar (Grundfos ALPHA SOLAR 25-75 180)
*   **Ubicación Física:** Se debe instalar en la **tubería de retorno del primario solar**, en la cubierta (azotea), es decir, en el tramo frío que conecta la salida del serpentín inferior del interacumulador con la entrada al campo de captadores.
*   **Justificación Técnica:**
    1.  **Protección contra Altas Temperaturas:** Al situar la bomba en la zona fría de retorno, se evita que sus juntas, cojinetes y la electrónica integrada se expongan a las elevadas temperaturas de impulsión ($>95^\circ\text{C}$) procedentes de los paneles solares.
    2.  **Prevención de Cavitación:** El fluido caloportador en el retorno se encuentra a menor temperatura, lo que aumenta la presión neta de aspiración positiva (NPSH) disponible y elimina el riesgo de cavitación por vaporización local del fluido en el rodete.
    3.  **Montaje del Eje:** El motor debe orientarse de forma que el **eje de rotación quede estrictamente en posición horizontal** para asegurar que el propio fluido lubrique continuamente los cojinetes y se facilite la purga de aire.
    4.  **Comportamiento Hidráulico (Circuito Cerrado):** Dado que todo el circuito primario solar se ubica en la azotea y funciona como un bucle hidráulico cerrado, la columna ascendente y la descendente se equilibran hidrostáticamente. La bomba no necesita vencer la cota estática de la altura del edificio (13 o 15.5 m), corrigiendo la interpretación errónea de requerir altura manométrica para elevar el agua. La altura necesaria responde únicamente a la pérdida de carga dinámica por fricción de tuberías, accesorios e intercambiador, calculada en aproximadamente **$2,21\text{ m.c.a.}$** para un caudal de diseño de **$699\text{ L/h}$**. La bomba **ALPHA SOLAR 25-75 180**, con una altura manométrica máxima de $7,5\text{ m.c.a.}$, ofrece el rango de trabajo ideal con un margen de seguridad óptimo.

### B. Circuito Secundario Solar (Bomba NO Requerida)
*   **Justificación Técnica:** Al seleccionarse un interacumulador bivalente con serpentín inferior interno, el calor se transfiere directamente de forma estática al agua de consumo contenida en el acumulador. No existe un intercambiador de placas externo y, por lo tanto, **se prescinde por completo de bomba secundaria solar**. El agua de consumo se calienta directamente en el serpentín inferior y asciende por termosifón interno, manteniendo una estratificación térmica óptima.

### C. Bomba de Recirculación de ACS (Grundfos ALPHA2 25-40 N 180)
*   **Ubicación Física:** Se debe colocar en la **tubería de retorno del anillo de recirculación de ACS**, en la azotea, inmediatamente antes de su conexión al interacumulador (en la toma de retorno del depósito Lapesa).
*   **Justificación Técnica:**
    1.  **Cierre de Bucle:** Mueve el agua sanitaria que se ha enfriado en las montantes de distribución del edificio de vuelta al acumulador para su recalentamiento, manteniendo el anillo a $>50^\circ\text{C}$ contra la proliferación de *Legionella* (según exigencias del **R.D. 487/2022**).
    2.  **Accesorios de Seguridad:** Debe contar obligatoriamente con una **válvula de retención a la salida** (para evitar flujos inversos de agua fría de red hacia el anillo de recirculación) y un **filtro de impurezas a la entrada** (para proteger el rotor de depósitos calcáreos y lodos).

---

## 4. Especificaciones y Justificaciones de las Bombas Grundfos Prescritas

A continuación se detallan el equipo prescrito, su ubicación, su justificación funcional y las especificaciones técnicas para cada uno de los circuladores de alta eficiencia de Grundfos:

### 1. Bomba del Circuito Primario Solar: Grundfos ALPHA SOLAR 25-75 180
*   **¿Qué bomba se instala?** Circulador electrónico de alta eficiencia específico para sistemas solares térmicos.
*   **¿Dónde se instala?** En la tubería de retorno del primario solar, en la cubierta (azotea), a la entrada al campo de captadores.
*   **¿Por qué se instala?** Mueve el fluido caloportador (agua con propilenglicol al 30-50%) a lo largo de las tuberías y captadores. Al ser un circuito cerrado de azotea, no hay requisitos de elevación estática. La bomba solo debe vencer la resistencia de fricción dinámica del primario solar ($\approx 2,21\text{ m.c.a.}$ a $699\text{ L/h}$). La ALPHA SOLAR 25-75 180 se adapta perfectamente a este punto de trabajo operando cerca de su punto de máxima eficiencia, consume entre 2 W y 45 W y permite regular su velocidad mediante señal externa **PWM** (Pulse Width Modulation) desde el controlador solar, maximizando la eficiencia térmica del campo.
*   **Especificaciones Técnicas:**
    *   **Número de Producto:** **98989300**
    *   **Material del Cuerpo:** Fundición de hierro con recubrimiento por cataforesis (apto para circuito cerrado).
    *   **Altura Manométrica Máxima ($H_{max}$):** **$7,5\text{ m.c.a.}$** (75 dm).
    *   **Caudal Máximo ($Q_{max}$):** $3,5\text{ m}^3\text{/h}$ (adecuado para operar con el caudal de diseño de $0,7\text{ m}^3\text{/h}$).
    *   **Temperatura de Líquido:** $2^\circ\text{C}$ a $110^\circ\text{C}$.
    *   **Compatibilidad con Glicol:** Apto para mezclas de agua y glicol propileno hasta el **50%** de concentración.
    *   **Tipo de Conexión:** Rosca G 1 1/2" (DN25), con longitud entre bocas de $180\text{ mm}$ (conexión directa mediante racores de unión rosca-soldar a tubería de cobre DN22).
    *   **Modo de Control:** Control de velocidad constante por curvas o regulación externa mediante señal **PWM** (Perfil C).
    *   **Consumo Eléctrico:** De $2\text{ W}$ a $45\text{ W}$ ($\text{EEI} \le 0,20$).
*   **Ficha Técnica Oficial (Grundfos Product Center):**
    > [Grundfos ALPHA SOLAR 25-75 180 (98989300) - Ficha Técnica Oficial](https://product-selection.grundfos.com/product-detail.product-detail.html?productnumber=98989300)

---

### 2. Bomba de Recirculación de ACS: Grundfos ALPHA2 25-40 N 180
El punto de cálculo de la red de recirculación de ACS en el circuito de distribución es:
*   **Caudal de Cálculo:** **$370\text{ L/h}$** ($0,37\text{ m}^3\text{/h}$).
*   **Altura Manométrica de Cálculo:** **$0,41\text{ m.c.a.}$**

**Criterios de Margen de Selección:**
*   **Margen de Caudal:** Se adopta un margen de seguridad de aproximadamente el **15%** (caudal objetivo de **$425\text{ L/h}$**) para compensar pérdidas por derivaciones secundarias y garantizar que el agua de retorno cumpla estrictamente con la temperatura mínima de $>50^\circ\text{C}$ contra legionela.
*   **Margen de Altura Manométrica:** Se aplica un margen del **50% al 100%** (altura objetivo de **$0,6\text{ a }0,8\text{ m.c.a.}$**) para compensar la resistencia adicional introducida por accesorios de instalación (codos, tes, filtros de protección), la válvula de retención obligatoria (que requiere una presión mínima de apertura) y el incremento de rugosidad por calcificación e incrustaciones en tuberías de cobre a largo plazo.

*   **¿Qué bomba se instala?** Circulador electrónico de alta eficiencia con cuerpo de acero inoxidable.
*   **¿Por qué se selecciona?** Es el modelo óptimo para instalaciones colectivas (10 viviendas). Su cuerpo de acero inoxidable cumple rigurosamente con la normativa sanitaria para agua de consumo. Gracias a la tecnología de regulación de velocidad y la función inteligente **AUTOADAPT**, la bomba modulará su velocidad de forma automática para situarse exactamente en el punto real del anillo, reduciendo su consumo eléctrico al mínimo (hasta 3 W) y eliminando el riesgo de ruidos o de erosión por altas velocidades en las tuberías de cobre de DN18. Deja además un generoso margen hidráulico de seguridad (hasta 4,0 m.c.a.) para compensar el envejecimiento de la red.
*   **Especificaciones Técnicas:**
    *   **Número de Producto:** **99411365**
    *   **Material del Cuerpo:** **Acero Inoxidable (AISI 304)**, obligatorio para evitar corrosión galvánica y asegurar higiene alimentaria.
    *   **Altura Manométrica Máxima ($H_{max}$):** **$4,0\text{ m.c.a.}$**
    *   **Caudal Máximo ($Q_{max}$):** $2,4\text{ m}^3\text{/h}$.
    *   **Temperatura de Líquido:** $2^\circ\text{C}$ a $110^\circ\text{C}$.
    *   **Tipo de Conexión:** Rosca G 1 1/2" (DN25), con longitud entre bocas de $180\text{ mm}$.
    *   **Consumo Eléctrico:** De $3\text{ W}$ a $18\text{ W}$ ($\text{EEI} \le 0,15$).
*   **Ficha Técnica Oficial (Grundfos Product Center):**
    > [Grundfos ALPHA2 25-40 N 180 (99411365) - Ficha Técnica Oficial](https://product-selection.grundfos.com/product-detail.product-detail.html?productnumber=99411365)

---

## 5. Matriz de Especificaciones Técnicas (Unificada Grundfos)

| Variable de Selección | Bomba Primario Solar <br>(Retorno en Azotea) | Bomba Recirculación ACS <br>(Retorno Anillo) |
| :--- | :---: | :---: |
| **Modelo Prescrito** | **Grundfos ALPHA SOLAR 25-75 180** | **Grundfos ALPHA2 25-40 N 180** |
| **Número de Producto** | **98989300** | **99411365** |
| **Material del Cuerpo** | Fundición de Hierro (Cataforesis) | **Acero Inoxidable (AISI 304)** |
| **Altura Nominal Máxima** | **$7,5\text{ m.c.a.}$** (Para Pdc de 2,21 m.c.a.)| **$4,0\text{ m.c.a.}$** (Para Pdc de 0,41 m.c.a.)|
| **Caudal Máximo** | $3,5\text{ m}^3\text{/h}$ | $2,4\text{ m}^3\text{/h}$ |
| **Fluido de Trabajo** | Agua + Glicol Propileno (30-50%) | Agua Potable Sanitaria |
| **Rango de Temperatura** | $2^\circ\text{C}$ a $110^\circ\text{C}$ | $2^\circ\text{C}$ a $110^\circ\text{C}$ |
| **Tipo de Conexión** | Rosca G 1 1/2" | Rosca G 1 1/2" (DN25) |
| **Longitud entre Bocas** | $180\text{ mm}$ | $180\text{ mm}$ |
| **Consumo Eléctrico** | **$2 - 45\text{ W}$** | **$3 - 18\text{ W}$** |
| **Índice Eficiencia (EEI)**| $\le 0,20$ | $\le 0,15$ |
| **Modo de Control** | PWM externo (Perfil C) / Curvas | AUTOADAPT / Presión variable |

---

## 6. Evaluación Hidráulica y Consideraciones de Montaje

### A. Comportamiento en Circuito Cerrado
El circuito primario solar y el retorno de la recirculación de ACS operan como circuitos hidráulicos donde los cambios de elevación geométrica están compensados por las columnas de ida y retorno en equilibrio. Las bombas de circulación solo deben dimensionarse para vencer las pérdidas dinámicas de carga por fricción del trazado, accesorios y captadores/interacumulador.

### B. Transiciones de Diámetro en Sala Técnica de Azotea
La bomba ALPHA SOLAR 25-75 180 seleccionada cuenta con conexiones roscadas de G 1 1/2". Dado que el diámetro de la tubería de cobre de los tramos comunes del primario es DN22, se debe prescribir en el plano de montaje:
*   La conexión mediante **racores de unión rosca-soldar de 1 1/2" a 22 mm**. Esto simplifica enormemente la instalación en comparación con modelos embridados DN40 (como la antigua MAGNA3), eliminando la necesidad de contrabridas reductoras cónicas y reduciendo el riesgo de fugas y las pérdidas de carga locales en singularidades.

---

## 7. Referencias y Fuentes

*   **Notebook de Consulta:** `Energia_Solar_Termica` (ID: `62b2af52-7df4-455e-9334-8b10ebd8118d`).
*   **Anotaciones Técnicas Relacionadas:**
    *   [especificacion-antecedentes-y-datos-de-partida.md](file:///h:/Unidades%20compartidas/Practicas_Inst2/6_Energia_Solar/Proyecto/Especificaciones/especificacion-antecedentes-y-datos-de-partida.md)
    *   [fluido-caloportador-solar-termica.md](file:///h:/Unidades%20compartidas/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/fluido-caloportador-solar-termica.md)
    *   [seleccion-interacumulador-acs-bivalente-lapesa.md](file:///h:/Unidades%20compartidas/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/seleccion-interacumulador-acs-bivalente-lapesa.md)
    *   [explicacion-circuito-primario-solar.md](file:///h:/Unidades%20compartidas/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/explicacion-circuito-primario-solar.md)
    *   [explicacion-circuito-distribucion-acs.md](file:///h:/Unidades%20compartidas/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/explicacion-circuito-distribucion-acs.md)
*   **Documentación de Fabricante (Grundfos Product Center):**
    *   Ficha técnica oficial de bomba solar: [Grundfos ALPHA SOLAR 25-75 180](https://product-selection.grundfos.com/product-detail.product-detail.html?productnumber=98989300)
    *   Ficha técnica oficial de recirculación ACS: [Grundfos ALPHA2 25-40 N 180](https://product-selection.grundfos.com/product-detail.product-detail.html?productnumber=99411365)
