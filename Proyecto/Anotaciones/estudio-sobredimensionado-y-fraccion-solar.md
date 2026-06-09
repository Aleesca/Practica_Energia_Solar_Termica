# Estudio Técnico: Justificación del Sobredimensionamiento y Coherencia de la Fracción Solar

Esta anotación técnica analiza y valida la hipótesis planteada por el usuario sobre la idoneidad de no limitarse a los datos estrictamente sugeridos (10 captadores y 1.500 L) para el diseño del campo solar y el volumen de acumulación. Se evalúan las implicaciones hidráulicas, normativas y el riesgo de sobrecalentamiento bajo el CTE HE4 y el RITE, aplicando fuentes y criterios técnicos europeos.

---

## 1. Análisis Técnico de la Propuesta de Sobredimensionamiento

La propuesta de incrementar el número de captadores de 10 a 12 o 14, manteniendo la paridad del número de colectores, es **técnicamente muy correcta y lógica** por las siguientes razones de ingeniería:

### A. Paridad y Equilibrio Hidráulico (Retorno Invertido o Tichelmann)
Para garantizar que todos los colectores solares reciban el mismo caudal de fluido caloportador y operen a la misma temperatura, las instalaciones centralizadas colectivas se dividen en subcampos hidráulicos (baterías en paralelo).
*   **Con 10 captadores:** El diseño obliga a un único grupo largo en paralelo de 10 captadores (límite recomendado por fabricantes para evitar pérdidas de carga excesivas) o a dividirlo en 2 grupos de 5.
*   **Con 12 captadores:** Permite dividir el campo de forma simétrica y equilibrada en 2 filas de 6 captadores o en 3 filas de 4 captadores.
*   **Con 14 captadores:** Permite una distribución simétrica en 2 filas de 7 captadores.
*   *Conclusión:* La paridad (y en particular el número 12 o 14) facilita el equilibrado mediante circuitos en retorno invertido (Tichelmann), garantizando que las pérdidas de carga en los subcampos sean idénticas y evitando flujos preferenciales.

### B. Factor de Ensuciamiento y Pérdidas del Sistema (Safety Margin)
Los cálculos teóricos de fracción solar (ej. método f-Chart) asumen colectores limpios y condiciones óptimas de radiación. En la realidad, factores como:
*   La acumulación de polvo, polución y excrementos de aves (factor de suciedad o *dirty factor*, que suele reducir el rendimiento entre un 5% y un 10%).
*   Las pérdidas térmicas en las largas tuberías de distribución y retorno del circuito primario (especialmente en azoteas).
*   El envejecimiento natural de los materiales del captador.

Justifican que el diseñador aplique un margen de seguridad (sobredimensionamiento moderado) del 10% al 20% en área de captación para asegurar que la fracción solar real en condiciones de operación no caiga por debajo del mínimo exigido por el CTE HE4.

---

## 2. Relación Volumen/Superficie de Captación ($V/S_c$)

De acuerdo con el **CTE HE4** (Exigencia de contribución mínima de energía renovable para ACS) y el **RITE**, se debe cumplir obligatoriamente la relación de diseño entre el volumen de acumulación solar ($V$, en litros) y la superficie total de captadores ($S_c$, en $\text{m}^2$):

$$50 < \frac{V}{S_c} < 180 \text{ litros/m}^2$$

La guía de diseño del **IDAE** y las buenas prácticas de la **ASIT** (Asociación de la Industria Solar Térmica) estrechan este rango a un valor recomendado de **$60\text{ a }100\text{ l/m}^2$**, situando el **óptimo técnico en $75\text{ l/m}^2$**.

Utilizando la superficie de apertura útil del captador seleccionado vertical **Viessmann Vitosol 200-FM SV2F** ($2,33\text{ m}^2$ por unidad), evaluamos los escenarios con el volumen de ACS:

### Escenario 1: Campo de 10 captadores ($S_c = 23,30\text{ m}^2$)
*   **Con 1.500 L:** $\frac{1500}{23,30} = 64,37\text{ l/m}^2$. Cumple el mínimo normativo de $60\text{ l/m}^2$ (hipótesis inicial de relación mínima) y se encuentra dentro de la zona de diseño segura.
*   **Con 2.000 L:** $\frac{2000}{23,30} = 85,83\text{ l/m}^2$. Se acerca más al valor óptimo de $75-90\text{ l/m}^2$.

### Escenario 2: Campo de 12 captadores ($S_c = 27,96\text{ m}^2$)
*   **Con 1.500 L:** $\frac{1500}{27,96} = 53,65\text{ l/m}^2$. **Riesgo técnico.** Aunque cumple el mínimo absoluto del CTE ($>50\text{ l/m}^2$), queda por debajo del mínimo de $60\text{ l/m}^2$ recomendado por el IDAE/RITE. Este sistema tiene poco volumen para tanta potencia de captación, lo que provocará que el depósito se caliente muy rápido en verano y la instalación entre en estancamiento (vaporización del fluido).
*   **Con 2.000 L:** $\frac{2000}{27,96} = 71,53\text{ l/m}^2$. **Óptimo.** Coincide casi perfectamente con la hipótesis de diseño ideal ($75\text{ l/m}^2$). Proporciona inercia térmica suficiente y seguridad contra sobrecalentamientos.

### Escenario 3: Campo de 14 captadores ($S_c = 32,62\text{ m}^2$)
*   **Con 1.500 L:** $\frac{1500}{32,62} = 45,98\text{ l/m}^2$. **Técnicamente prohibido.** Cae por debajo del límite de $50\text{ l/m}^2$ del CTE HE4. El sistema sufrirá graves problemas de sobrecalentamiento continuo en los meses de verano.
*   **Con 2.000 L:** $\frac{2000}{32,62} = 61,31\text{ l/m}^2$. **Cumple.** Se sitúa justo por encima del umbral de $60\text{ l/m}^2$, representando el mínimo de acumulación segura para este área de captación.
*   **Con 2.500 L:** $\frac{2500}{32,62} = 76,64\text{ l/m}^2$. **Óptimo.** Mantiene la proporción ideal de $75\text{ l/m}^2$.

---

## 3. Coherencia con la Fracción Solar y Riesgo de Sobrecalentamiento

La fracción solar anual de partida sugerida es del **67,8%**. 
*   Si aumentamos el número de captadores a 12 o 14 captadores sin aumentar proporcionalmente la demanda del edificio, la fracción solar resultante aumentará (por ejemplo, a valores en torno al 75% o 80%).
*   **El límite del RITE y CTE HE4:** Para evitar la degradación de la instalación, la normativa prohíbe diseños que generen sobrecalentamientos incontrolados. Específicamente:
    *   La fracción solar mensual en cualquier mes no debería superar el 100% de la demanda energética.
    *   Si en los meses de verano (Junio, Julio, Agosto) la producción solar supera de forma sistemática y holgada la demanda mensual, se deben instalar medidas de protección obligatorias: **sistemas de disipación de calor** (como un aerotermo en el circuito primario), **sistemas drain-back** (autovaciado que vacía los colectores cuando no hay demanda) o **sistemas de sombreado parcial**.

---

## 4. Comparativa de Opciones de Diseño (Estudio Síntesis)

| Configuración | Área Captación ($S_c$) | Volumen ACS ($V$) | Relación $V/S_c$ | Viabilidad Normativa | Riesgo de Sobrecalentamiento | Recomendación de Protección |
| :--- | :---: | :---: | :---: | :--- | :--- | :--- |
| **10 Captadores (Sugerido)** | $23,30\text{ m}^2$ | 1.500 L | $64,37\text{ l/m}^2$ | Cumple (Mín. RITE/IDAE) | Bajo / Controlado | Estándar |
| **12 Captadores (Equilibrado)**| $27,96\text{ m}^2$ | 1.500 L | $53,65\text{ l/m}^2$ | Al límite (No recomendado) | **Alto** en verano | Requiere disipación obligatoria |
| **12 Captadores + 2.000 L** | $27,96\text{ m}^2$ | **2.000 L** | **$71,53\text{ l/m}^2$** | **Excelente (Óptimo)** | Moderado / Seguro | Vaso de expansión holgado |
| **14 Captadores (Oversized)**| $32,62\text{ m}^2$ | 2.000 L | $61,31\text{ l/m}^2$ | Cumple (Límite inferior) | Moderado / Alto | Requiere disipación nocturna o aerotermo |
| **14 Captadores + 2.500 L** | $32,62\text{ m}^2$ | **2.500 L** | **$76,64\text{ l/m}^2$** | **Excelente (Óptimo)** | Moderado | Requiere disipación aerotermo |

---

## 5. Conclusión y Recomendación Final de Ingeniería

La lógica del diseñador de **no quedarse estrictamente con los datos sugeridos teóricos y buscar un sobredimensionado par (12 o 14 captadores)** es totalmente correcta y recomendada para garantizar la resiliencia de la instalación ante ensuciamientos y facilitar el equilibrado hidráulico.

No obstante, **no se puede sobredimensionar el campo de captación de forma aislada**. Si se decide aumentar el número de captadores para asegurar el cumplimiento del 67,8% de fracción solar anual:

1.  **Si se opta por 12 captadores ($27,96\text{ m}^2$):** Es obligatorio migrar el volumen de acumulación de 1.500 L a **2.000 litros** (modelo **Lapesa Master Inox MXV-2000 SS2B** o **Geiser Inox G 2000 S2**). Esto mantiene la relación $V/S_c$ en un óptimo $71,53\text{ l/m}^2$, evitando el estancamiento prematuro del sistema y garantizando una excelente inercia.
2.  **Si se opta por 14 captadores ($32,62\text{ m}^2$):** El volumen mínimo aceptable es de 2.000 L, pero lo óptimo es seleccionar **2.500 litros** de acumulación (modelo **Lapesa Geiser Inox G 2500 S2** o **Coral Vitro CV-2500-M2B**). En este caso, al aumentar de forma tan significativa la superficie de captación, la fracción solar de verano superará previsiblemente el 100% de la demanda mensual de ACS, por lo que **se debe prescribir obligatoriamente un sistema de disipación de calor (aerotermo disipador)** en el primario solar para evitar la ebullición del glicol.
