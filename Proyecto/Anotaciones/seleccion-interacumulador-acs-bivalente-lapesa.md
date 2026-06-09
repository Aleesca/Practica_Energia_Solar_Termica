# Selección de Equipos: Decisión y Justificación del Interacumulador de 2.000 Litros (Lapesa Master Inox)

Esta anotación técnica presenta la justificación de ingeniería, la comparativa de catálogo y la decisión de diseño definitiva para la selección del depósito de acumulación solar de agua caliente sanitaria (ACS) en una instalación centralizada. 

A partir de los datos iniciales y las exigencias de operación, mantenimiento y prevención sanitaria, se decanta formalmente la elección por el modelo de **2.000 litros** de la serie **Master Inox de Lapesa**, descartando la capacidad de 1.500 litros inicialmente propuesta.

---

## 1. Datos de Partida y Propuesta Inicial

La instalación solar térmica proyectada cuenta con las siguientes especificaciones iniciales:
*   **Número de captadores:** 10 captadores solares planos.
*   **Superficie de captación útil ($S_c$):** $23,3\text{ m}^2$ (apoyado en la superficie de apertura útil del captador vertical Viessmann Vitosol 200-FM SV2F, con $2,33\text{ m}^2$ por unidad).
*   **Volumen de acumulación de partida sugerido ($V$):** $1.500\text{ litros}$.

---

## 2. Análisis Crítico y Limitaciones del Volumen de 1.500 Litros

A partir del cuaderno de trabajo `Energia_Solar_Termica` (ID: `62b2af52-7df4-455e-9334-8b10ebd8118d`) y la normativa vigente (RITE e IDAE), se evalúa la idoneidad técnica del volumen de 1.500 litros:

1.  **Relación de diseño y volumen mínimo:**
    $$\frac{V}{S_c} = \frac{1.500\text{ L}}{23,3\text{ m}^2} = 64,37\text{ litros/m}^2$$
    Aunque esta relación se encuentra dentro del rango general admisible ($50-180\text{ l/m}^2$), está muy próxima al límite inferior prescrito por la *Guía Técnica de Energía Solar Térmica del IDAE* (que establece un mínimo de **$60\text{ l/m}^2$**).
2.  **Riesgo de sobrecalentamientos y paradas (Estancamiento):**
    Una relación de $\approx 64\text{ l/m}^2$ reduce la inercia térmica del sistema. En periodos estivales o de baja ocupación, el agua del acumulador alcanzará muy rápido la temperatura de consigna de ACS, provocando que la bomba de recirculación del primario se detenga por seguridad. Esto expone al campo solar a entrar en fase de estancamiento (vaporización del fluido caloportador y degradación prematura del glicol).
3.  **Incompatibilidad con el sobredimensionamiento hidráulico:**
    Como se analiza en el [estudio-sobredimensionado-y-fraccion-solar.md](file:///H:/Unidades%20compartidas/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/estudio-sobredimensionado-y-fraccion-solar.md), para asegurar el cumplimiento del 67,8% de fracción solar y facilitar el equilibrado hidráulico en retorno invertido (Tichelmann), es altamente recomendable estructurar el campo en un número par de captadores (12 o 14).
    *   **Con 12 captadores ($S_c = 27,96\text{ m}^2$):** Un acumulador de 1.500 L daría una relación de **$53,65\text{ l/m}^2$**, quedando por debajo del límite mínimo normativo del IDAE de $60\text{ l/m}^2$.
    *   **Con 14 captadores ($S_c = 32,62\text{ m}^2$):** Daría **$45,98\text{ l/m}^2$**, lo cual está **directamente prohibido** por el CTE HE4 ($V/S_c \ge 50\text{ l/m}^2$).

---

## 3. Justificación Decisiva para los 2.000 Litros: Legionella (R.D. 487/2022) y Catálogo Lapesa

El argumento de mayor peso para decantar la elección hacia los 2.000 litros radica en el binomio **diseño de catálogo del fabricante** y **cumplimiento estricto de la legislación sanitaria**.

### A. Limitación de Catálogo (Lapesa Master Inox)
Consultando el catálogo oficial de Lapesa en el notebook `Catalogos_solar` (ID: `7d1bf88b-463a-4291-9201-1959144a5921`), se extraen las siguientes realidades sobre los modelos bivalentes (con dos serpentines de intercambio):
1.  La gama premium **Master Inox** (fabricada en acero inoxidable AISI 316 L y caracterizada por incorporar **serpentines modulares desmontables y extraíbles**) **no comercializa modelos bivalentes por debajo de los 2.000 litros**. Los modelos bivalentes `MXV-S2B` o `MXV-SS2B` están disponibles únicamente en capacidades de 2.000, 3.500, 5.000 y 6.000 litros.
2.  Para la capacidad de **1.500 litros**, la gama *Master Inox* se limita a versiones *monovalentes* (un único serpentín desmontable solar).
3.  Si se quisiera un interacumulador bivalente de **1.500 litros** en acero inoxidable, la única opción comercial es la serie **Geiser Inox G 1500 S2**. Sin embargo, esta serie cuenta con **serpentines internos soldados fijos (no desmontables)**.

### B. Cumplimiento de la Normativa Antilegionella (R.D. 487/2022)
Para una instalación centralizada plurifamiliar de ACS, la prevención de la legionelosis es prioritaria y está regulada de forma estricta por el **Real Decreto 487/2022**:
*   **Inspección y Limpieza Física:** La normativa exige inspecciones y limpiezas mecánicas periódicas del depósito de ACS para retirar lodos e incrustaciones calcáreas, que constituyen el principal caldo de cultivo del biofilm y de la bacteria *Legionella pneumophila*.
*   **Desmontabilidad como Factor de Seguridad:** El modelo **Master Inox MXV-2000 SS2B** permite la **extracción completa de ambos serpentines** (solar y de apoyo de caldera) a través de su boca de hombre lateral **DN400**. Esto permite realizar tareas de desincrustación de cal y desinfección a fondo de toda la superficie de transferencia de calor y del interior del tanque, algo técnicamente imposible en el modelo *Geiser Inox G 1500 S2* debido a sus serpentines fijos.
*   **Rendimiento Higiénico e Inercia:** El volumen de 2.000 litros proporciona la inercia térmica óptima y, al estar fabricado en acero inoxidable AISI 316 L, es inmune a la corrosión por picaduras y no requiere protección catódica por ánodo de sacrificio (ánodo de magnesio) ni por ánodo electrónico de corriente impuesta. Esto elimina la necesidad de mantenimientos frecuentes de ánodos y el riesgo de su degradación.

---

## 4. Comparativa Técnica de Alternativas Lapesa

| Criterio Técnico | Geiser Inox G 1500 S2 <br>*(Alternativa 1.500 L)* | Coral Vitro CV 1500 M2B <br>*(Opción Vitrificada)* | Master Inox MXV-2000 SS2B <br>**(SELECCIÓN DEFINITIVA)** |
| :--- | :---: | :---: | :---: |
| **Material del depósito** | Acero Inoxidable AISI 316 L | Acero al carbono vitrificado | **Acero Inoxidable AISI 316 L** |
| **Capacidad nominal** | 1.500 litros | 1.500 litros | **2.000 litros** |
| **Relación $V/S_c$ ($23,3\text{ m}^2$)** | $64,37\text{ l/m}^2$ (Límite inferior) | $64,37\text{ l/m}^2$ (Límite inferior) | **$85,83\text{ l/m}^2$** (Óptimo recomendado) |
| **Relación $V/S_c$ ($27,96\text{ m}^2$)** | $53,65\text{ l/m}^2$ (Riesgo / No cumple) | $53,65\text{ l/m}^2$ (Riesgo / No cumple) | **$71,53\text{ l/m}^2$** (Óptimo recomendado) |
| **Tipo de serpentines** | 2 serpentines fijos (soldados) | 1 desmontable + 1 fijo | **2 serpentines desmontables y extraíbles** |
| **Mantenimiento y Legionella** | Complejo (serpentines fijos) | Moderado (requiere inspección ánodo) | **Excelente (limpieza y desmontabilidad total)** |
| **Protección Catódica** | No requiere | Requiere ánodo de magnesio / activo | **No requiere** (sin elementos de desgaste) |
| **Superficie Intercambio Solar**| $3,4\text{ m}^2$ (Fijo) | $3,4\text{ m}^2$ (Inox desmontable) | **$3,4\text{ m}^2$ o $4,2\text{ m}^2$** (Inox desmontable) |
| **Superficie Intercambio Apoyo**| $2,0\text{ m}^2$ (Fijo) | $2,0\text{ m}^2$ (Vitrificado fijo) | **$2,0\text{ m}^2$ o $2,5\text{ m}^2$** (Inox desmontable) |
| **Peso en vacío** | $303\text{ kg}$ | $403\text{ kg}$ | **$345\text{ kg}$** |
| **Dimensiones (Diámetro x Altura)** | $1160\text{ mm} \times 2270\text{ mm}$ | $1160\text{ mm} \times 2320\text{ mm}$ | **$1360\text{ mm} \times 2280\text{ mm}$** |

---

## 5. Justificación del Incremento de Volumen a 2.000 Litros

La adopción definitiva de **2.000 litros** se fundamenta en tres pilares de ingeniería:

1.  **Optimización del rendimiento solar ($V/S_c$):**
    Con un volumen de 2.000 L, la relación de acumulación con el campo inicial de 10 captadores ($23,3\text{ m}^2$) es de **$85,83\text{ l/m}^2$**. Este valor se sitúa en el centro del rango de máxima eficiencia energética anual ($75-90\text{ l/m}^2$). Consigue almacenar más energía en las horas de máxima radiación, reduciendo las arrancadas de la caldera auxiliar y disipando el calor sobrante de manera más uniforme.
2.  **Seguridad legal contra la Legionella (R.D. 487/2022):**
    Al contar con serpentines solares y de apoyo **completamente desmontables**, la comunidad de propietarios puede cumplir al 100% con los protocolos de limpieza física obligatoria que exige el R.D. 487/2022. La gama de 1.500 litros forzaría al uso de serpentines soldados (imposibles de extraer y limpiar en seco) o al uso de depósitos vitrificados con ánodos de sacrificio, de menor vida útil y altos costes recurrentes de revisión.
3.  **Resiliencia y escalabilidad futura:**
    Si durante la fase final de cálculo o montaje en cubierta se opta por la configuración equilibrada de 12 captadores planos ($27,96\text{ m}^2$ de apertura útil), el depósito de **2.000 litros** responde de forma idónea ofreciendo una relación de **$71,53\text{ l/m}^2$**. El volumen de 1.500 L quedaría inhabilitado al no cumplir con el mínimo de 60 l/m² exigido por IDAE/RITE, provocando un grave riesgo de sobrecalentamientos recurrentes y la anulación de la garantía del campo solar.

---

## 6. Decisión y Recomendación de Prescripción Final

Se selecciona formalmente para el proyecto la siguiente especificación técnica:

*   **Equipo:** Interacumulador ACS bivalente vertical de gran capacidad.
*   **Marca y Modelo:** **Lapesa Master Inox MXV-2000 SS2B**.
*   **Volumen Nominal:** **2.000 litros**.
*   **Material de Fabricación:** Acero Inoxidable **AISI 316 L** (depósito y serpentines).
*   **Aislamiento Térmico:** Espuma de poliuretano inyectado de $80\text{ mm}$ de espesor con funda de protección exterior.
*   **Superficies de intercambio:**
    *   Serpentín solar (inferior): **$3,4\text{ m}^2$** (desmontable de acero inoxidable).
    *   Serpentín de apoyo (superior): **$2,0\text{ m}^2$** (desmontable de acero inoxidable).
*   **Acceso técnico:** Boca de hombre DN400 para inspección visual y descalcificación mecánica.

---

## 7. Coherencia Técnica del Proyecto

Esta decisión garantiza la máxima robustez en el diseño de la planta térmica centralizada y mantiene una coherencia total con las demás anotaciones del proyecto:

*   El análisis mensual de cobertura y sobreproducción se recoge en [balance-energetico-solar-termica.md](file:///H:/Unidades%20compartidas/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/balance-energetico-solar-termica.md), donde se comprueba que la configuración definitiva de 12 captadores y 2.000 L alcanza una fracción solar anual suficiente sin superar el 110% de cobertura mensual.
*   Se alinea con la prescripción principal detallada en [seleccion-equipos-solar-centralizado.md](file:///H:/Unidades%20compartidas/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/seleccion-equipos-solar-centralizado.md), consolidando el modelo de 2.000 L y descartando la opción de 1.500 L como propuesta base.
*   Permite adoptar la configuración definitiva de 12 captadores recomendada en el [estudio-sobredimensionado-y-fraccion-solar.md](file:///H:/Unidades%20compartidas/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/estudio-sobredimensionado-y-fraccion-solar.md) sin modificar el acumulador, asegurando un diseño estable y en pleno cumplimiento normativo de RITE, CTE HE4 y R.D. 487/2022.
