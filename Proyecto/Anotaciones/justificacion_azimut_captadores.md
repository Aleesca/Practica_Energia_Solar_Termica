# Justificación Técnica del Azimut e Inclinación de los Captadores Solares

Este documento presenta la justificación técnica de la orientación (azimut) y la inclinación seleccionadas para los captadores solares térmicos de la instalación centralizada de ACS hibridada con gas natural.

---

## 1. Localización Geográfica y Contexto Climático

Los datos geográficos reales de la edificación se han extraído del archivo [posicion_edificio.md](file:///H:/Unidades%20compartidas/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/posicion_edificio.md):

*   **Latitud:** $40^\circ 58'\ 8.31''\text{ N}$ (equivalente a $40.968975^\circ\text{ N}$ en formato decimal).
*   **Longitud:** $5^\circ 40'\ 29.95''\text{ O}$ (equivalente a $5.674986^\circ\text{ O}$ o $-5.674986^\circ$ en formato decimal).wh

### Contexto y Criterios del CTE DB-HE
Conforme al Código Técnico de la Edificación (CTE DB-HE) y las tablas de Censolar/IDAE:
1.  **Zona Climática General (HE1):** Clasificada como **D2** (severidad climática invernal D y estival 2).
2.  **Zona de Radiación Solar (HE4):** Clasificada dentro de la **Zona III** (radiación global media diaria anual sobre superficie horizontal entre $3.8\text{ y }4.2\text{ kWh/m}^2\cdot\text{día}$).
3.  **Utilidad de las Coordenadas:** Las coordenadas geográficas sirven exclusivamente para enmarcar la instalación en su contexto climático, lo cual define los parámetros de irradiancia horizontal diaria media ($H_{dia}$), las temperaturas medias ambientales ($T_{amb}$) y la temperatura de entrada del agua fría de red ($T_{red}$). **No determinan por sí solas el azimut real de los captadores.**

---

## 2. Determinación del Plano de Captación

La instalación se plantea sobre una **cubierta plana transitada (azotea)** del edificio de viviendas (según el [Alcance del proyecto](file:///H:/Unidades%20compartidas/Practicas_Inst2/6_Energia_Solar/Proyecto/Alcance.md)). 

Los captadores solares planos (10 unidades, con una superficie útil de captación de $23.3\text{ m}^2$) se montan sobre estructuras de soporte inclinadas fijadas a bancadas de hormigón sobre la cubierta.

### Parámetros de Orientación e Inclinación en la Herramienta de Cálculo

De la inspección de la herramienta de cálculo [herramienta_calculo.xlsm](file:///H:/Unidades%20compartidas/Practicas_Inst2/6_Energia_Solar/Calculos/herramienta_calculo.xlsm), se han extraído los siguientes valores de diseño adoptados en las celdas `Datos!G8` y `Datos!G9`:

*   **Inclinación de los captadores ($\beta$):** $60^\circ$ respecto a la horizontal.
*   **Azimut de los captadores ($\alpha$):** $20^\circ$ (desviación respecto al Sur geográfico).

### Convenio de Signos de Azimut
En ingeniería solar térmica en España, se adopta la convención estándar donde:
*   El **Sur geográfico exacto** corresponde a $\alpha = 0^\circ$.
*   Las desviaciones hacia el **Oeste** son positivas ($\alpha > 0^\circ$, p. ej., $+90^\circ$ es Oeste).
*   Las desviaciones hacia el **Este** son negativas ($\alpha < 0^\circ$, p. ej., $-90^\circ$ es Este).
*   El azimut adoptado en el proyecto es de **$20^\circ$ (Oeste)**, lo cual corresponde a $\alpha = +20^\circ$.

> [!NOTE]
> En navegación o topografía convencional, el azimut se mide desde el Norte en sentido horario (donde el Norte es $0^\circ$ y el Sur es $180^\circ$). Bajo esta convención alternativa, un azimut de $20^\circ$ al Oeste del Sur equivale a $180^\circ + 20^\circ = 200^\circ$.

---

## 3. Justificación Técnica y Cálculo de Pérdidas

### 3.1. Justificación del Azimut ($\alpha = 20^\circ$)
La orientación de los captadores se desvía $20^\circ$ respecto al Sur exacto para **alinear físicamente las estructuras de soporte con los ejes principales de la edificación** en la azotea. 
Esta alineación evita pérdidas de espacio útil, simplifica el anclaje de las bancadas de hormigón paralelamente a los muretes perimetrales, reduce el impacto estético de la instalación (superposición arquitectónica armoniosa) y simplifica el tendido de las tuberías del circuito primario.

### 3.2. Justificación de la Inclinación ($\beta = 60^\circ$)
Para una demanda anual constante de ACS, la inclinación teóricamente óptima del CTE es igual a la latitud del lugar ($\beta_{opt} = \text{Latitud} \approx 41^\circ$). Sin embargo, se ha seleccionado una inclinación superior de **$60^\circ$** por dos razones de diseño fundamentales:
1.  **Favorecer el rendimiento en invierno:** En los meses invernales (noviembre a febrero), el sol se encuentra a menor altura sobre el horizonte. Una inclinación más vertical ($60^\circ$) capta mejor la radiación solar en este periodo crítico, reduciendo la necesidad de energía auxiliar de gas natural cuando el agua fría de red entra a temperaturas mínimas ($4^\circ\text{C}$ - $5^\circ\text{C}$).
2.  **Prevención de sobrecalentamientos estivales:** En verano (junio a agosto), la radiación solar es muy intensa y el sol está muy alto en el cielo. Una inclinación de $60^\circ$ hace que los rayos solares incidan con un ángulo muy oblicuo, lo cual **autolimita y reduce la producción solar de calor en verano**. Esto protege la instalación contra el estancamiento térmico, impidiendo que el fluido caloportador se degrade (evaporación y polimerización del glicol) y evitando esfuerzos mecánicos perjudiciales para los colectores e intercambiadores.

### 3.3. Cálculo de Pérdidas por Orientación e Inclinación (CTE DB-HE4)
El Código Técnico de la Edificación limita las pérdidas de energía solar debidas a una orientación e inclinación no óptimas. Para el **Caso General** (captadores sobre soporte), las pérdidas máximas acumuladas no deben superar el **10%**.

La fórmula normalizada de cálculo de pérdidas porcentuales (utilizada por Censolar e implementada en la herramienta de cálculo) es:
$$ P_{total}\ (\%) = 100 \cdot \left[ 1.2 \cdot 10^{-4} \cdot (\beta - \beta_{opt})^2 + 3.5 \cdot 10^{-5} \cdot \alpha^2 \right] $$

Sustituyendo los valores de diseño del proyecto:
*   $\beta = 60^\circ$ (Inclinación real)
*   $\beta_{opt} = 40.968975^\circ \approx 41^\circ$ (Latitud de Salamanca / Inclinación óptima)
*   $\alpha = 20^\circ$ (Azimut real)

**1. Pérdidas por Inclinación ($P_i$):**
$$ P_i\ (\%) = 100 \cdot 1.2 \cdot 10^{-4} \cdot (60 - 40.968975)^2 $$
$$ P_i\ (\%) = 1.2 \cdot 10^{-2} \cdot (19.031025)^2 = 1.2 \cdot 10^{-2} \cdot 362.18 \approx 4.35\% $$

**2. Pérdidas por Orientación/Azimut ($P_o$):**
$$ P_o\ (\%) = 100 \cdot 3.5 \cdot 10^{-5} \cdot (20)^2 $$
$$ P_o\ (\%) = 3.5 \cdot 10^{-3} \cdot 400 = 1.40\% $$

**3. Pérdidas Totales por Orientación e Inclinación ($P_{total}$):**
$$ P_{total}\ (\%) = 4.35\% + 1.40\% = 5.75\% $$

> [!TIP]
> Dado que $P_{total} = 5.75\% < 10\%$, la instalación cumple holgadamente con la exigencia reglamentaria del CTE DB-HE4, validando plenamente la decisión de diseño de inclinar los captadores a $60^\circ$ y desviarlos $20^\circ$ al Oeste.

En la herramienta de cálculo, estas pérdidas de orientación se restan de manera directa sobre la radiación global mensual de diseño:
$$ EI = H_{dia} \cdot K \cdot (1 - P_o) \cdot (1 - P_s) $$
Donde el factor $K$ (celdas `Datos!H16:H27`) ya introduce la ganancia por inclinación en Salamanca, $P_o = 1.4\%$ representa la pérdida por azimut y $P_s = 0\%$ representa la ausencia de pérdidas por sombras de obstáculos adyacentes.

---

## 4. Conclusión Técnica

1.  **Insuficiencia de la posición geográfica:** La posición geográfica del edificio **no basta por sí sola** para determinar el azimut de los captadores solares. La latitud y longitud fijan únicamente el potencial solar del emplazamiento y el clima local. El azimut es un parámetro de diseño físico que depende exclusivamente de la orientación del edificio, la disposición de la cubierta y la distribución geométrica de los soportes.
2.  **Cumplimiento Normativo:** Los captadores solares de la instalación del proyecto se orientarán con un **azimut de $20^\circ$ al Oeste ($\alpha = +20^\circ$)** y una **inclinación de $60^\circ$ ($\beta = 60^\circ$)**. Este diseño arroja unas pérdidas anuales combinadas de tan solo el **$5.75\%$**, lo cual cumple de forma reglamentaria con el límite del **$10\%$** del CTE DB-HE4.
3.  **Idoneidad del Diseño:** La inclinación de $60^\circ$ está técnicamente justificada para priorizar la captación en los meses de invierno (mayor demanda útil de calefacción de ACS) y reducir la captación en verano, protegiendo así el sistema contra sobrecalentamientos destructivos.
