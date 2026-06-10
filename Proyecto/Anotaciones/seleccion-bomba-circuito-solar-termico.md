# Selección de Bomba Comercial para el Circuito Solar Térmico y Análisis de Bombeo

> Relacionado con: [3.3. Condicionantes de Integración Física](../Especificaciones/especificacion-antecedentes-y-datos-de-partida.md#h2-33-condicionantes-de-integración-física) y [3.4. Equipamiento de Referencia y Fluidos](../Especificaciones/especificacion-antecedentes-y-datos-de-partida.md#h2-34-equipamiento-de-referencia-y-fluidos)

Esta anotación técnica justifica la necesidad, ubicación y selección de los equipos de bombeo hidráulico para la instalación solar térmica colectiva y su sistema bivalente de acumulación. La investigación se fundamenta en la consulta del cuaderno de trabajo de NotebookLM `Energia_Solar_Termica` y en la búsqueda profunda de catálogos comerciales de fabricantes europeos (con prioridad en firmas alemanas).

---

## 1. Resumen Ejecutivo

El diseño hidráulico de una instalación solar térmica centralizada con acumulación bivalente requiere determinar con precisión en qué tramos es estrictamente necesaria la circulación forzada y en cuáles se puede prescindir de ella. 

Se concluye que la instalación requiere **tres bombas de circulación independientes** (circuito primario solar, circuito de apoyo de caldera y anillo de recirculación de ACS) y **prescinde de bomba en el circuito secundario solar** debido al intercambio térmico directo por serpentín interno. Para el circuito primario solar, dado que la bomba se ubica en el sótano y debe superar la altura estática del edificio hasta la azotea (mínimo de $15,5\text{ m}$ para la fase de llenado inicial o en caso de un esquema de vaciado por gravedad/drainback), se selecciona como opción preferente el circulador de rotor húmedo de alta eficiencia **Grundfos MAGNA3 40-180 F** (con una altura nominal máxima de $18\text{ m.c.a.}$), quedando modelos de Wilo como alternativas equivalentes.

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

## 4. Búsqueda Profunda de Alternativas Comerciales (Alta Altura Manométrica)

Dado que la bomba del primario solar estará ubicada en el sótano del edificio y debe satisfacer una elevación de columna de fluido de al menos **$15,5\text{ m}$** hasta la azotea (para permitir el llenado inicial de la red, purgar el aire y posibilitar un eventual sistema de vaciado por gravedad o drainback), los circuladores domésticos estándar roscados (con límites de $7-8\text{ m}$ de altura máxima) son insuficientes. 

Mediante búsqueda profunda en catálogos de fabricantes europeos, se seleccionan tres alternativas de alta eficiencia embridadas (DN40) capaces de proporcionar la altura manométrica exigida:

### 1. Opción Preferente: Grundfos MAGNA3 40-180 F (Dinamarca)
Circulador de rotor húmedo de alta eficiencia con modulación electrónica avanzada para instalaciones comerciales.
*   **Ficha Técnica Oficial (Grundfos Product Center):** [Model 97924272](https://product-selection.grundfos.com/product-detail.product-detail.html?productnumber=97924272)
*   **Altura Manométrica Máxima ($H_{max}$):** **$18,0\text{ m.c.a.}$** (180 dm), lo que supera el requisito mínimo de $15,5\text{ m}$ para elevar el fluido hasta la azotea.
*   **Caudal Máximo ($Q_{max}$):** $20\text{ m}^3\text{/h}$ (permite trabajar de forma holgada en el punto de diseño de $0,69\text{ m}^3\text{/h}$).
*   **Rango de Temperatura del Fluido:** $-10^\circ\text{C}$ a $110^\circ\text{C}$.
*   **Compatibilidad con Glicol:** Sí, apto para mezclas de agua/glicol propileno hasta el **50%**.
*   **Control y Regulación:** Control automático inteligente (AUTOADAPT, FLOWADAPT), modulación por presión proporcional/constante, temperatura constante y modos de control externos (compatible con lógica de consigna externa).
*   **Consumo Eléctrico:** De $9\text{ W}$ a $604\text{ W}$ ($\text{EEI} \le 0,18$).
*   **Conexiones:** Conexión embridada DN40 (PN 6/10) con una longitud entre bocas de $220\text{ mm}$ (requiere bridas de adaptación para las tuberías de DN25 del primario).

### 2. Alternativa Comercial 1: Wilo-Yonos MAXO 40/0,5-16 (Alemania)
Circulador de rotor húmedo estándar de alta eficiencia con brida DN40.
*   **Ficha Técnica Oficial (Catálogo Wilo):** [Wilo-Yonos MAXO 40/0,5-16](https://wilo.com)
*   **Altura Manométrica Máxima ($H_{max}$):** **$17,6\text{ m.c.a.}$** (supera los $15,5\text{ m}$ mínimos).
*   **Caudal Máximo ($Q_{max}$):** $27,6\text{ m}^3\text{/h}$.
*   **Rango de Temperatura del Fluido:** $-20^\circ\text{C}$ a $110^\circ\text{C}$.
*   **Compatibilidad con Glicol:** Sí, apto para mezclas hasta el **50%** de glicol.
*   **Control y Regulación:** Presión diferencial variable ($\Delta p-v$), presión diferencial constante ($\Delta p-c$) y 3 velocidades fijas.
*   **Consumo Eléctrico:** $40\text{ W}$ a $800\text{ W}$ ($\text{EEI} \le 0,20$).
*   **Conexiones:** Embridada DN40 (PN 6/10) con longitud entre bocas de $250\text{ mm}$.

### 3. Alternativa Comercial 2: Wilo-Stratos MAXO 40/0,5-16 (Alemania)
Circulador inteligente ("Smart-Pump") de rotor húmedo y máxima eficiencia con comunicación integrada.
*   **Ficha Técnica Oficial (Catálogo Wilo):** [Wilo-Stratos MAXO 40/0,5-16](https://wilo.com)
*   **Altura Manométrica Máxima ($H_{max}$):** **$16,3\text{ m.c.a.}$** (suficiente para cubrir la cota de $15,5\text{ m}$).
*   **Caudal Máximo ($Q_{max}$):** $30,2\text{ m}^3\text{/h}$.
*   **Rango de Temperatura del Fluido:** $-10^\circ\text{C}$ a $110^\circ\text{C}$.
*   **Compatibilidad con Glicol:** Sí, apto para mezclas hasta el **50%**.
*   **Control y Regulación:** Funciones avanzadas de control de temperatura y caudal (*Dynamic Adapt plus*, *Multi-Flow Adaptation*), conectividad Bluetooth, entradas analógicas y digitales, y bus de comunicación para integración en domótica (BMS).
*   **Consumo Eléctrico:** $15\text{ W}$ a $640\text{ W}$ ($\text{EEI} \le 0,17$).
*   **Conexiones:** Embridada DN40 (PN 6/16) con longitud entre bocas de $250\text{ mm}$.

### Matriz Comparativa de Equipos de Bombeo Solar (Alta Presión)

| Parámetro Técnico | Grundfos MAGNA3 40-180 F <br>**(PREFERENTE)** | Wilo-Yonos MAXO 40/0,5-16 <br>*(ALTERNATIVA 1)* | Wilo-Stratos MAXO 40/0,5-16 <br>*(ALTERNATIVA 2)* |
| :--- | :---: | :---: | :---: |
| **Origen del Fabricante** | Dinamarca / Presencia Global | Alemania | Alemania |
| **Altura Manométrica Máxima**| **$18,0\text{ m.c.a.}$** | $17,6\text{ m.c.a.}$ | $16,3\text{ m.c.a.}$ |
| **Caudal Máximo** | $20,0\text{ m}^3\text{/h}$ | $27,6\text{ m}^3\text{/h}$ | **$30,2\text{ m}^3\text{/h}$** |
| **Temperatura del Fluido** | $-10^\circ\text{C}$ a $110^\circ\text{C}$ | **$-20^\circ\text{C}$ a $110^\circ\text{C}$** | $-10^\circ\text{C}$ a $110^\circ\text{C}$ |
| **Límite Máx. de Glicol** | 50% | 50% | 50% |
| **Modos de Regulación** | Modulación completa, auto-adaptativa, señal externa | Presión variable / constante / fija | Inteligente, domótica avanzada, adaptabilidad total |
| **Consumo Eléctrico (P1)** | **$9 - 604\text{ W}$** | $40 - 800\text{ W}$ | $15 - 640\text{ W}$ |
| **Dimensiones / Conexión** | DN40 embridada, L = 220 mm | DN40 embridada, L = 250 mm | DN40 embridada, L = 250 mm |
| **Facilidad de Integración** | Excelente (estándar comercial) | Excelente (robusto y sencillo) | Excelente (máxima conectividad BMS) |

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

### C. Condicionamiento de la Selección y Dimensionado Físico
La selección definitiva del modelo dentro de la gama de alta presión queda sujeta a las siguientes verificaciones en la fase final de diseño:
*   **Superación de la Altura Estática (15,5 m):** Los modelos seleccionados (**Grundfos MAGNA3 40-180 F** con $18\text{ m.c.a.}$, **Wilo-Yonos MAXO 40/0,5-16** con $17,6\text{ m.c.a.}$ y **Wilo-Stratos MAXO 40/0,5-16** con $16,3\text{ m.c.a.}$) garantizan que el sistema pueda completarse físicamente de fluido desde el sótano a la azotea, venciendo la presión hidrostática durante el llenado inicial o en ciclos de drainback.
*   **Adaptación de Diámetros:** Al tratarse de bombas con conexiones embridadas de DN40, y siendo la red de distribución de cobre de menor sección (típicamente DN25 o DN32), se prescribirá la instalación de **contrabridas reductoras cónicas** a la entrada y salida de la bomba para asegurar una transición hidráulica suave y evitar turbulencias o pérdidas de carga singulares elevadas en la aspiración.
*   **Punto de Operación en Régimen Estable:** Una vez que el circuito está lleno y presurizado, la altura necesaria para mantener la circulación baja significativamente (pues solo se requiere vencer la fricción, típicamente de $3$ a $6\text{ m.c.a.}$). Gracias a la modulación electrónica automática de las gamas MAGNA3 y Stratos/Yonos MAXO, las bombas reducirán su velocidad y consumo eléctrico a una fracción del máximo, operando en su zona de alta eficiencia y previniendo problemas de ruidos en la red.

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
    *   Catálogo Técnico Grundfos: [Ficha Técnica Oficial - Grundfos Product Center (MAGNA3 40-180 F)](https://product-selection.grundfos.com/product-detail.product-detail.html?productnumber=97924272)
    *   Catálogo Técnico Wilo: *Wilo-Yonos MAXO / Wilo-Stratos MAXO Catalogues* (Glandless high-efficiency circulation pumps for commercial applications).
*   **Anotaciones Técnicas Relacionadas:**
    *   [especificacion-antecedentes-y-datos-de-partida.md](../Especificaciones/especificacion-antecedentes-y-datos-de-partida.md)
    *   [fluido-caloportador-solar-termica.md](fluido-caloportador-solar-termica.md)
    *   [seleccion-interacumulador-acs-bivalente-lapesa.md](seleccion-interacumulador-acs-bivalente-lapesa.md)
