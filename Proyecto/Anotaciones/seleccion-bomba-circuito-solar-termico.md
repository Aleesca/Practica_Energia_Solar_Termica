# Selección de Bomba Comercial para el Circuito Solar Térmico y Análisis de Bombeo

Esta anotación técnica justifica la necesidad, ubicación y selección de los equipos de bombeo hidráulico para la instalación solar térmica colectiva y su sistema bivalente de acumulación. La investigación se fundamenta en la consulta del cuaderno de trabajo de NotebookLM `Energia_Solar_Termica` y en la búsqueda profunda de catálogos comerciales de fabricantes europeos (con prioridad en firmas alemanas).

---

## 1. Resumen Ejecutivo

El diseño hidráulico de una instalación solar térmica centralizada con acumulación bivalente requiere determinar con precisión en qué tramos es estrictamente necesaria la circulación forzada y en cuáles se puede prescindir de ella. 

Se concluye que la instalación requiere **tres bombas de circulación independientes** (circuito primario solar, circuito de apoyo de caldera y anillo de recirculación de ACS) y **prescinde de bomba en el circuito secundario solar** debido al intercambio térmico directo por serpentín interno. Para el circuito primario solar, se prescribe como opción preferente la bomba de alta eficiencia **Grundfos ALPHA SOLAR 25-75 180**, quedando como alternativas viables los modelos de Wilo.

---

## 2. Inventario Técnico de la Instalación

Para el análisis hidráulico y la selección de los equipos, se consolidan los siguientes datos de diseño de la instalación:

*   **Campo Solar:** 12 colectores planos **Viessmann Vitosol 200-FM (SV2F vertical)** con tecnología de protección contra sobretemperaturas **ThermProtect**. Distribuidos en 2 filas paralelas de 6 captadores cada una.
*   **Superficie de Captación:** Superficie de absorción total de **$27,72\text{ m}^2$** ($2,31\text{ m}^2$ por captador) y de apertura de **$27,96\text{ m}^2$** ($2,33\text{ m}^2$ por captador).
*   **Régimen Hidráulico:** Caudal específico de diseño de **$25\text{ L/(h}\cdot\text{m}^2\text{ de absorción)}$** (funcionamiento a *Caudal Bajo* o *Low-Flow*).
*   **Caudal Total de Referencia del Primario:** **$693\text{ L/h}$** ($11,55\text{ L/min}$) de caudal nominal, distribuido de forma equilibrada mediante un esquema de retorno invertido (**Tichelmann**) en dos ramales de **$346,5\text{ L/h}$** ($5,78\text{ L/min}$) cada uno.
*   **Fluido Caloportador:** Mezcla de agua y glicol propileno (anticongelante atóxico de uso solar) con una concentración estimada del **30% al 50%** según los requisitos de protección contra heladas de Salamanca (Zona Climática D2).
*   **Sistema de Acumulación:** Interacumulador bivalente **Lapesa Master Inox MXV-2000 SS2B** de **$2.000\text{ litros}$** de capacidad, fabricado en acero inoxidable AISI 316 L.
    *   *Serpentín inferior (Solar):* Superficie de intercambio de **$3,4\text{ m}^2$**.
    *   *Serpentín superior (Apoyo):* Superficie de intercambio de **$2,0\text{ m}^2$**.
*   **Sistema Auxiliar de Respaldo:** Caldera mural mixta centralizada de gas natural de **$22\text{ kW}$** de potencia útil de diseño.

---

## 3. Justificación de Ubicación y Necesidades de Bombeo

De acuerdo con las consultas técnicas realizadas en el cuaderno de trabajo `Energia_Solar_Termica` (ID: `62b2af52-7df4-455e-9334-8b10ebd8118d`), se define la estructura de bombeo de la instalación:

### A. Ubicación de la Bomba Solar (Circuito Primario)
La bomba del circuito solar primario debe ubicarse en la **tubería de retorno** (el tramo de tubería fría que conduce el fluido desde la salida del serpentín inferior del interacumulador hacia la entrada de los colectores solares en la azotea). Esta ubicación es crítica por las siguientes razones:
1.  **Protección Térmica:** El fluido caloportador en el retorno se encuentra a la temperatura más baja del bucle solar. Al situar la bomba en este tramo, se evita que sus componentes internos (principalmente el motor de rotor húmedo y las juntas) se expongan a las elevadas temperaturas de impulsión provenientes de los colectores (que en condiciones de alta radiación superan los $90^\circ\text{C}$ y en estancamiento pueden degradar el circulador).
2.  **Prevención de la Cavitación:** La menor temperatura del fluido en el retorno aumenta la presión de vapor del líquido, reduciendo drásticamente el riesgo de cavitación en la aspiración del rodete.
3.  **Montaje Físico:** De acuerdo con la normativa técnica de Viessmann, la bomba debe montarse siempre con su **eje de rotación en posición estrictamente horizontal** para garantizar la correcta lubricación de los cojinetes por el propio fluido de trabajo y facilitar la purga de aire.

### B. Análisis de Otros Bucles y Circuitos
1.  **Circuito Secundario Solar: Bomba NO Requerida.** Al seleccionar un interacumulador bivalente con serpentín inferior interno, el calor se transfiere directamente de forma estática al agua de consumo contenida en el acumulador. No existe un intercambiador de placas externo y, por lo tanto, **se prescinde por completo de bomba secundaria solar**. El agua de consumo se calienta directamente y asciende por termosifón interno, manteniendo una estratificación térmica óptima.
2.  **Circuito de Apoyo (Caldera): Bomba SÍ Requerida.** Para transferir el calor de la caldera de gas natural de $22\text{ kW}$ al serpentín superior del interacumulador en periodos de baja radiación, se requiere un circulador en el bucle cerrado caldera-serpentín. Habitualmente, esta bomba se integra en el propio chasis de la caldera mural de gas natural.
3.  **Bucle de Recirculación de ACS: Bomba SÍ Requerida.** Al tratarse de una distribución centralizada para 10 viviendas, la distancia a los grifos genera pérdidas térmicas continuas. El **R.D. 487/2022** exige mantener la temperatura del agua por encima de $50^\circ\text{C}$ en los puntos de consumo para evitar la proliferación de *Legionella*. Por ello, es obligatorio instalar una bomba de recirculación de ACS en el **tramo final de la tubería de retorno de la red**, antes de conectarse nuevamente al interacumulador. Esta bomba debe contar con **cuerpo de bronce o acero inoxidable** para resistir la corrosión del agua sanitaria aireada y evitar incrustaciones calcáreas.
4.  **Calderas Murales Mixtas Individuales en Viviendas (si se optara por un esquema de apoyo individual): Bomba NO Requerida.** En caso de utilizar calderas mixtas individuales en cada vivienda como apoyo del agua precalentada solar centralizada:
    *   *Para ACS (Agua Caliente Sanitaria):* No necesitan (ni deben) contar con bombas circuladoras externas de ACS. El agua sanitaria se desplaza por las calderas individuales impulsada únicamente por la **presión de la red de suministro público**. La instalación de una bomba de recirculación forzada en una caldera instantánea provocaría que el fluxóstato del equipo detectara una demanda permanente, manteniéndolo encendido continuamente con un severo aumento en el consumo de gas y el desgaste prematuro del quemador.
    *   *Para Calefacción:* Las calderas murales ya incorporan de fábrica su propia **bomba circuladora interna** dentro de su chasis. Por lo tanto, tampoco se requiere un circulador externo para este servicio en condiciones normales de diseño.
    *   *Esquema de Integración:* La conexión hidráulica se realiza mediante un kit de derivación y mezcla termostática (Kit Solar) que bypassera la caldera cuando el agua solar es suficiente ($>45^\circ\text{C}$) y la derivará a su entrada cuando requiera recalentamiento de apoyo.

---

## 4. Búsqueda Profunda de Alternativas Comerciales

Mediante búsqueda profunda de fabricantes europeos líderes en tecnología de bombeo (priorizando los alemanes Wilo y Grundfos), se han seleccionado tres alternativas de alta eficiencia compatibles con la aplicación solar térmica (resistentes al glicol y con control PWM):

### 1. Opción Preferente: Grundfos ALPHA SOLAR 25-75 180 (Dinamarca)
Es un circulador de alta eficiencia con motor de imanes permanentes diseñado específicamente para sistemas solares térmicos.
*   **Ficha Técnica Oficial (Grundfos Product Center):** [Model 98989300](https://product-selection.grundfos.com/product-detail.product-detail.html?productnumber=98989300)
*   **Altura Manométrica Máxima ($H_{max}$):** $7,5\text{ m}$ (75 dm)
*   **Caudal Nominal ($Q_{nom}$):** $1,85\text{ m}^3\text{/h}$ (adecuado para cubrir el punto de diseño de $0,69\text{ m}^3\text{/h}$)
*   **Rango de Temperatura del Fluido:** $2^\circ\text{C}$ a $110^\circ\text{C}$ (soporta picos de temperatura en instalaciones solares)
*   **Compatibilidad con Glicol:** Sí, apto para mezclas de agua/glicol propileno hasta el **50%**.
*   **Control de Velocidad:** Admite control externo mediante señal **PWM** (Pulse Width Modulation) de perfil solar, permitiendo a la centralita solar regular el caudal de forma continua. También dispone de 3 velocidades constantes.
*   **Consumo Eléctrico:** Muy bajo, de $2\text{ W}$ a $45\text{ W}$ (Índice de Eficiencia Energética $\text{EEI} \le 0,20$).
*   **Conexiones:** Rosca exterior G 1 1/2" (DN25), con longitud entre bocas de $180\text{ mm}$.

### 2. Alternativa Comercial 1: Wilo-Yonos PARA ST 25/7.0 PWM2 (Alemania)
Circulador de rotor húmedo de alta eficiencia para aplicaciones solares térmicas.
*   **Altura Manométrica Máxima ($H_{max}$):** $7,3\text{ m}$
*   **Caudal Máximo ($Q_{max}$):** $3,3\text{ m}^3\text{/h}$
*   **Rango de Temperatura del Fluido:** Hasta $110^\circ\text{C}$ (a una temperatura ambiente de $55^\circ\text{C}$).
*   **Compatibilidad con Glicol:** Sí, hasta el **50%** de concentración de glicol.
*   **Control de Velocidad:** Control externo de velocidad mediante señal **PWM2** de lógica solar.
*   **Consumo Eléctrico:** $3\text{ W}$ a $45\text{ W}$.
*   **Conexiones:** Rosca G 1 1/2" (DN25) con longitud entre bocas de $180\text{ mm}$ (también disponible en versión de $130\text{ mm}$).

### 3. Alternativa Comercial 2: Wilo-Yonos PICO-STG 25/1-7.5 (Alemania)
Bomba circuladora de alta eficiencia para instalaciones solares y geotérmicas con interfaz de usuario integrada.
*   **Altura Manométrica Máxima ($H_{max}$):** $7,5\text{ m}$
*   **Caudal Máximo ($Q_{max}$):** $\approx 2,4\text{ m}^3\text{/h}$
*   **Rango de Temperatura del Fluido:** $0^\circ\text{C}$ a $110^\circ\text{C}$
*   **Compatibilidad con Glicol:** Sí, hasta el **50%**.
*   **Control de Velocidad:** Modos de presión diferencial variable ($\Delta p-v$), velocidad constante y control externo iPWM2 (solar).
*   **Características Adicionales:** Incorpora visualizador LED para el ajuste del punto de consigna y visualización del consumo instantáneo. Dispone de cuerpo con recubrimiento cataforético contra la corrosión por condensación.

### Matriz Comparativa de Equipos de Bombeo Solar

| Parámetro Técnico | Grundfos ALPHA SOLAR 25-75 180 <br>**(PREFERENTE)** | Wilo-Yonos PARA ST 25/7.0 PWM2 <br>*(ALTERNATIVA 1)* | Wilo-Yonos PICO-STG 25/1-7.5 <br>*(ALTERNATIVA 2)* |
| :--- | :---: | :---: | :---: |
| **Origen del Fabricante** | Dinamarca / Presencia Global | Alemania | Alemania |
| **Altura Manométrica Máxima**| **$7,5\text{ m.c.a.}$** | $7,3\text{ m.c.a.}$ | **$7,5\text{ m.c.a.}$** |
| **Caudal Máximo** | $1,85\text{ m}^3\text{/h}$ | **$3,3\text{ m}^3\text{/h}$** | $2,4\text{ m}^3\text{/h}$ |
| **Temperatura del Fluido** | $2^\circ\text{C}$ a $110^\circ\text{C}$ | $0^\circ\text{C}$ a $110^\circ\text{C}$ | $0^\circ\text{C}$ a $110^\circ\text{C}$ |
| **Límite Máx. de Glicol** | 50% | 50% | 50% |
| **Señal de Control** | PWM Solar / 3 curvas constantes | PWM2 Solar | iPWM2 Solar / $\Delta p-v$ / Constante |
| **Consumo Eléctrico (P1)** | **$2 - 45\text{ W}$** | $3 - 45\text{ W}$ | $3 - 45\text{ W}$ |
| **Dimensiones / Conexión** | DN25 (G 1 1/2"), L = 180 mm | DN25 (G 1 1/2"), L = 180 mm | DN25 (G 1 1/2"), L = 180 mm |
| **Facilidad de Integración** | Excelente (estándar en grupos solar) | Excelente (integración OEM) | Excelente (pantalla de control local) |

---

## 5. Evaluación Hidráulica y Limitaciones de Dimensionado

### A. Concepto Fundamental: Altura Estática en Circuitos Cerrados
En ingeniería hidráulica de edificación, suele cometerse el error de sumar la altura geométrica del edificio (la distancia vertical entre la sala técnica del sótano/planta baja y los captadores en la cubierta) al dimensionar la altura manométrica ($H_p$) de la bomba de circulación. 

> [!IMPORTANT]
> **Aclaración sobre Circuitos Cerrados:** El circuito primario solar, el circuito de apoyo de la caldera y el bucle de recirculación de ACS son **circuitos hidráulicos cerrados y presurizados**. En un circuito cerrado, la columna de fluido que sube hacia la cubierta se equilibra exactamente con el peso de la columna de fluido que baja de retorno. Por tanto, **la altura geométrica o estática del edificio no influye en la altura manométrica de la bomba**. 
> 
> La bomba solo debe seleccionarse para vencer las **pérdidas de carga por fricción (dinámicas)** generadas por la viscosidad del fluido caloportador al circular a través de las tuberías, codos, válvulas, colectores solares e intercambiadores.

### B. Parámetros Faltantes para el Cálculo Definitivo
Para cerrar el punto de trabajo definitivo de la bomba ($Q$ y $H$) en la fase de cálculo de detalle, actualmente se identifican los siguientes parámetros faltantes en la documentación de partida del proyecto:
1.  **Trazado y Longitud de Tubería:** Longitud lineal exacta de ida y retorno del circuito primario (desde el interacumulador en la planta baja hasta el campo solar en azotea, incluyendo la red Tichelmann de distribución entre colectores).
2.  **Diámetro Comercial y Material de la Red:** Definición definitiva del diámetro interior y espesor de las tuberías de cobre que componen las columnas hidráulicas solares.
3.  **Accesorios y Válvulas (Pérdidas Singulares):** Número exacto de codos a $90^\circ$, tes de derivación, válvulas de corte, válvulas de retención antitermosifón, purgadores de aire y el caudalímetro/grupo de llenado solar.
4.  **Curvas de Pérdida de Carga de los Equipos:** La curva de pérdida de carga interna de los captadores **Viessmann Vitosol 200-FM SV2F** operando con glicol a bajas temperaturas, y la pérdida de carga del serpentín inferior del interacumulador **Lapesa MXV-2000 SS2B** (que tiene una superficie de intercambio de $3,4\text{ m}^2$).
5.  **Ajuste por Viscosidad del Glicol:** Las curvas comerciales de las bombas se ensayan con agua pura a $20^\circ\text{C}$. Dado que se utiliza glicol propileno al 30-50%, la densidad y viscosidad cinemática del fluido aumentan, incrementando las pérdidas de carga en un **$15\% - 30\%$** en comparación con el agua sola. La altura manométrica calculada debe corregirse con este factor.

### C. Condicionamiento de la Selección
Debido a estos parámetros faltantes, la selección final de la bomba queda condicionada a que las pérdidas de carga dinámicas del circuito primario solar (corregidas por el factor de viscosidad del glicol) no superen el rango de trabajo de los circuladores prescritos:
*   Con el caudal de diseño de **$693\text{ L/h}$** ($0,69\text{ m}^3\text{/h}$), la bomba **Grundfos ALPHA SOLAR 25-75** puede aportar una altura manométrica de hasta **$6,8\text{ m.c.a.}$** (metros de columna de agua), lo cual es sumamente holgado para una instalación centralizada de 12 captadores en un edificio plurifamiliar estándar de 3 a 5 plantas.
*   Si tras realizar el cálculo de pérdidas de carga detallado la altura dinámica resultante fuese inferior a $3,5\text{ m.c.a.}$, se podría pasar a un modelo menor (como la *Grundfos ALPHA SOLAR 25-60* o *Wilo-Yonos PARA ST 25/6.0*) para optimizar el consumo de energía eléctrica y reducir el riesgo de ruidos hidráulicos por exceso de presión en las tuberías.

---

## 6. Prescripción de Control y Regulación (Señal PWM)

Se prescribe obligatoriamente la conexión del circulador primario solar a la centralita de control solar mediante un cable de control de señal **PWM (Pulse Width Modulation) de tipo solar (PWM2)**. 

### Justificación de la Regulación Modulante:
1.  **Optimización Térmica:** La centralita de regulación solar medirá la diferencia de temperatura entre la salida del campo solar ($T_c$) y la parte inferior del interacumulador ($T_{dep}$). Modulando la velocidad de la bomba por PWM entre el **$10\%$ y el $100\%$**, el sistema adaptará el caudal real a la irradiancia instantánea. En días nublados o a primera/última hora, reducirá el caudal para mantener la temperatura de impulsión por encima del nivel de aprovechamiento, y en momentos de alta irradiancia aumentará el caudal para transferir el máximo de energía útil.
2.  **Prevención del Estancamiento:** Al operar coordinadamente con la tecnología **ThermProtect** de los colectores Viessmann, la centralita detendrá la bomba de forma segura cuando el interacumulador alcance los $60^\circ\text{C}$ de consigna sanitarios. El captador cambiará la estructura de sus cristales para reflejar la radiación sobrante y evitará la vaporización del glicol, protegiendo la vida útil del fluido y de la bomba.

---

## 7. Referencias y Fuentes

*   **Notebook de Consulta:** `Energia_Solar_Termica` (ID: `62b2af52-7df4-455e-9334-8b10ebd8118d`).
    *   *Documento de Conceptos Generales:* Requisitos de ubicación de bombas en zonas frías del primario y en el tramo de retorno de recirculación.
    *   *Casos Prácticos:* Dimensionado y cálculo de pérdida de carga del tramo de retorno ACS y especificación del cuerpo de bronce/inox para evitar la cal.
*   **Fichas de Fabricantes:**
    *   Catálogo Técnico Grundfos: [Ficha Técnica Oficial - Grundfos Product Center (ALPHA SOLAR 25-75 180)](https://product-selection.grundfos.com/product-detail.product-detail.html?productnumber=98989300)
    *   Ficha de Producto Wilo: *Wilo-Yonos PARA ST / Wilo-Yonos PICO-STG Datasheets* (OEM solar pumps and high-efficiency circulators).
*   **Anotaciones Técnicas Relacionadas:**
    *   [especificacion-antecedentes-y-datos-de-partida.md](file:///H:/Unidades%20compartidas/Practicas_Inst2/6_Energia_Solar/Proyecto/Especificaciones/especificacion-antecedentes-y-datos-de-partida.md)
    *   [fluido-caloportador-solar-termica.md](file:///H:/Unidades%20compartidas/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/fluido-caloportador-solar-termica.md)
    *   [seleccion-interacumulador-acs-bivalente-lapesa.md](file:///H:/Unidades%20compartidas/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/seleccion-interacumulador-acs-bivalente-lapesa.md)
