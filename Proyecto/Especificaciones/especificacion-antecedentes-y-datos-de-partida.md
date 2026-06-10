# Especificación de Maquetación: Antecedentes y Datos de Partida

Este documento detalla la estructura, formato y contenido técnico que debe guiar la redacción del apartado de **Antecedentes y Datos de Partida** en la memoria del proyecto de energía solar térmica centralizada. 

Esta especificación consolida los datos del enunciado y las notas del equipo de ingeniería para asegurar coherencia técnica y facilitar la trazabilidad mediante referencias cruzadas.

---

## 1. Directrices Generales de Maquetación

Para garantizar una presentación premium, ordenada y homogénea, el redactor debe aplicar las siguientes reglas:
1. **Jerarquía:** Respetar estrictamente la jerarquía de encabezados (`H2` para subsecciones principales, `H3` para detalles de integración y equipos).
2. **Visualización de Datos:** Los datos numéricos de entrada e hipótesis de diseño deben presentarse en tablas Markdown alineadas a la derecha para columnas numéricas.
3. **Llamadas de Atención (Alerts):** Utilizar bloques informativos de tipo `> [!NOTE]` para destacar justificaciones de diseño singulares y `> [!TIP]` para justificaciones normativas o de cumplimiento del CTE y RITE.

---

## 2. Plantilla: Antecedentes del Proyecto

A continuación, se detalla el contenido técnico y la maquetación exacta para la sección de Antecedentes de la memoria.

### H2: 2.1. Origen y Objeto del Encargo
*   **Origen del Encargo:** Promovido a solicitud de la propiedad para la ejecución de una reforma y mejora de la eficiencia energética en un edificio residencial plurifamiliar preexistente.
*   **Objeto de la Instalación:** El presente proyecto tiene por objeto definir y dimensionar una instalación solar térmica centralizada para la producción de Agua Caliente Sanitaria (ACS), hibridada con un sistema de apoyo auxiliar centralizado mediante caldera de gas natural.

### H2: 2.2. Justificación del Sistema Centralizado
*   **Selección de Esquema:** Se adopta un esquema completamente centralizado (acumulación y apoyo centralizados en sala técnica común).
*   **Ventajas Técnicas:** 
    *   Simplificación de la hidráulica al interior de las viviendas y supresión de calderas individuales mixtas.
    *   Optimización del mantenimiento preventivo y correctivo al unificar los equipos de intercambio en un único espacio técnico.
    *   Liberación de superficie útil y eliminación de conductos individuales de evacuación en cada vivienda.
*   **Criterio de Control Sanitario:** El volumen total de acumulación centralizada y la red de distribución se dimensionan para asegurar las temperaturas de consigna reglamentarias para prevenir la proliferación de microorganismos.

### H2: 2.3. Normativa de Aplicación
La instalación se proyecta en estricto cumplimiento del marco reglamentario estatal vigente:

1.  **CTE DB-HE4 (Código Técnico de la Edificación - Ahorro de Energía):** Define la contribución mínima de energía renovable para la producción de ACS en el edificio residencial.
2.  **RITE (Reglamento de Instalaciones Térmicas en los Edificios - R.D. 1027/2007):** Establece las exigencias de eficiencia energética, seguridad y mantenimiento para la red térmica centralizada.
3.  **Real Decreto 487/2022:** Regula las medidas sanitarias y los requisitos de inspección y limpieza periódica física de los depósitos acumuladores de ACS para la prevención y el control de la legionelosis.
4.  **Real Decreto 919/2006:** Reglamento técnico de distribución y utilización de combustibles gaseosos, aplicable a la instalación del quemador de la caldera auxiliar centralizada de gas natural.
5.  **Norma UNE 60670:** Gobierna el diseño, ventilación, seguridad y configuración de la sala de calderas para el sistema auxiliar de gas natural en Media Presión A.

---

## 3. Plantilla: Datos de Partida de la Instalación

A continuación, se presenta la maquetación exacta de los datos numéricos y físicos fijos tomados como punto de partida.

### H2: 3.1. Ubicación Geográfica y Climatología
*   **Referencia Catastral:** `5089301TL7358G0001ZD` *(Obtenida de [Enunciado_practica.pdf](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/00_Data/Enunciado_practica.pdf) para el Grupo G1-1)*.
*   **Coordenadas Geográficas:** Latitud $40^\circ 58'\ 8.31''\text{ N}$ ($40.968975^\circ$), Longitud $5^\circ 40'\ 29.95''\text{ O}$ ($-5.674986^\circ$) *(Trazado desde [posicion_edificio.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/posicion_edificio.md))*.
*   **Ubicación Física:** Salamanca.

| Parámetro Geoclimático | Valor / Clasificación | Origen del Dato |
| :--- | :---: | :--- |
| **Zona Climática (CTE DB-HE1)** | **D2** | Severidad climática D (invierno), 2 (verano) |
| **Zona de Radiación Solar (CTE DB-HE4)** | **Zona III** | Irradiancia horizontal diaria media anual: $3.8 - 4.2\text{ kWh/(m}^2\cdot\text{día)}$ |

> [!NOTE]
> Las coordenadas geográficas sirven exclusivamente para establecer las variables climatológicas fijas de radiación global media diaria ($H_{dia}$), temperatura media ambiental ($T_{amb}$) y temperatura de entrada del agua fría de red ($T_{red}$). El azimut físico y la inclinación son parámetros geométricos independientes fijados por el diseño de la planta.

### H2: 3.2. Edificación, Ocupación y Perfil de Demanda
*   **Tipología:** Edificio residencial plurifamiliar.
*   **Número de Viviendas:** 10 viviendas de diseño estándar.
*   **Ocupación de Diseño:** 40 personas (en base al recuento de dormitorios según planos de proyecto).
*   **Temperatura de Referencia para ACS:** $60^\circ\text{C}$ *(Regulado por exigencia sanitaria antilegionella)*.
*   **Demanda Diaria Unificada de ACS:** **$1.064\text{ litros/día}$** a $60^\circ\text{C}$.

### H2: 3.3. Condicionantes de Integración Física
La configuración estructural del edificio impone los siguientes límites físicos para la distribución e implantación de los equipos:
*   **Ubicación del Campo Solar:** Cubierta plana transitable (azotea) libre de obstáculos y sombras de edificaciones adyacentes.
*   **Trazado de Columnas Hidráulicas:** Canalización vertical de tuberías de ida y retorno del circuito primario y secundario a través del patinillo de comunicaciones común del edificio.
*   **Ubicación de Acumuladores:** Sala de máquinas/sala técnica común del edificio en planta baja, con acceso técnico dimensionado para el volteo de equipos.

### H2: 3.4. Equipamiento de Referencia y Fluidos
Se predefinen los siguientes equipos de catálogo comercial para el dimensionado físico del sistema:

*   **Modelo de Colector Solar:** **Viessmann Vitosol 200-FM (SV2F vertical)** con protección integrada contra sobretemperaturas **ThermProtect**.
*   **Distribución del Campo Solar:** 12 colectores planos distribuidos simétricamente en 2 filas paralelas de 6 unidades.
*   **Parámetros Físicos del Colector (por unidad):**
    *   Superficie Bruta: **$2.51\text{ m}^2$**
    *   Superficie de Apertura: **$2.33\text{ m}^2$**
    *   Superficie de Absorción: **$2.31\text{ m}^2$**
*   **Orientación e Inclinación del Soporte:**
    *   Inclinación ($\beta$): $60^\circ$ respecto a la horizontal *(justificada para favorecer captación invernal y autolimitar la estival)*.
    *   Azimut ($\alpha$): $+20^\circ$ *(desviación de $20^\circ$ al Oeste respecto al Sur geográfico)*.
*   **Depósito Acumulador Prescrito:** **Lapesa Master Inox MXV-2000 SS2B** (Acero Inoxidable AISI 316 L).
    *   Capacidad Nominal: **$2.000\text{ litros}$** (Bivalente con serpentines desmontables).
    *   Relación Volumen/Superficie de Apertura ($V/S_c$): **$71.53\text{ l/m}^2$** *(Óptimo del IDAE)*.
    *   Serpentín Inferior (Solar): Desmontable de acero inoxidable con **$3.4\text{ m}^2$** de superficie de intercambio.
    *   Serpentín Superior (Apoyo): Desmontable de acero inoxidable con **$2.0\text{ m}^2$** de superficie de intercambio.
    *   Boca de Hombre Lateral: Brida con diámetro nominal **BH DN400** para inspección física.
*   **Fluido Caloportador y Régimen Hidráulico:**
    *   Caudal Volumétrico Específico ($q_{esp}$): **$25\text{ L/(h}\cdot\text{m}^2\text{ de absorción)}$** *(Régimen Low-Flow)*.
    *   Caudal de Referencia de Diseño del Circuito Primario: **$693\text{ L/h}$** ($11.55\text{ L/min}$) o **$699\text{ L/h}$** ($11.65\text{ L/min}$).
    *   Esquema de Retorno: Configuración en retorno invertido (sistema **Tichelmann**) para asegurar la igualdad de pérdida de carga y un caudal idéntico entre ambos ramales.
*   **Respaldo Auxiliar (Gas Natural):**
    *   Caldera Centralizada: Caldera mural mixta de **$22\text{ kW}$** de potencia útil de diseño.
    *   Combustible: Gas Natural con Poder Calorífico Superior (PCS) normalizado de **$40.68\text{ MJ/m}^3\text{(s)}$**.

---

## 4. Matriz de Trazabilidad y Referencias Cruzadas (Origen de Datos)

Para asegurar la verificación y justificación documental de cada dato de partida, se detalla la procedencia exacta de la información técnica del proyecto:

| Sección de Memoria | Ficheros Técnicos de Origen (Anotaciones / Enunciado) | Parámetro Clave Extraído |
| :--- | :--- | :--- |
| **2.1. Origen y Objeto** | - [Enunciado_practica.pdf](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/00_Data/Enunciado_practica.pdf)<br>- [Alcance.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Alcance.md) | - Producción centralizada de ACS hibridada. |
| **2.2. Justificación** | - [acumulacion-solar-centralizada-vs-individualizada.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/acumulacion-solar-centralizada-vs-individualizada.md)<br>- [seleccion-equipos-solar-centralizado.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/seleccion-equipos-solar-centralizado.md) | - Selección del esquema de acumulación centralizada frente a esquemas mixtos o distribuidos. |
| **2.3. Normativa** | - [seleccion-interacumulador-acs-bivalente-lapesa.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/seleccion-interacumulador-acs-bivalente-lapesa.md)<br>- [datos_grupo_G1-1.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/.agents/skills/doc_tecnica_solar_hibrida/references/datos_grupo_G1-1.md) | - CTE DB-HE4, RITE, R.D. 487/2022 (prevención legionella), R.D. 919/2006 y UNE 60670. |
| **3.1. Ubicación** | - [Enunciado_practica.pdf](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/00_Data/Enunciado_practica.pdf)<br>- [posicion_edificio.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/posicion_edificio.md) | - Ref. Catastral: `5089301TL7358G0001ZD`. GPS Salamanca y zona climática HE1/HE4. |
| **3.2. Edificación y Demanda**| - [balance-energetico-solar-termica.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/balance-energetico-solar-termica.md) | - 10 viviendas, 40 personas y demanda de $1.064\text{ L/día}$ a $60^\circ\text{C}$. |
| **3.3. Integración Física** | - [justificacion_azimut_captadores.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/justificacion_azimut_captadores.md)<br>- [seleccion-equipos-solar-centralizado.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/seleccion-equipos-solar-centralizado.md) | - Montaje en azotea, paso por patinillo vertical y espacio para interacumulador en sala técnica. |
| **3.4. Equipamiento** | - [seleccion-interacumulador-acs-bivalente-lapesa.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/seleccion-interacumulador-acs-bivalente-lapesa.md)<br>- [fluido-caloportador-solar-termica.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/fluido-caloportador-solar-termica.md)<br>- [datos_gas-natural.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/datos_gas-natural.md) | - Colectores Vitosol 200-FM SV2F, acumulador Lapesa MXV-2000 SS2B, caudal $25\text{ L/(h}\cdot\text{m}^2\text{)}$, caldera de $22\text{ kW}$ y PCS. |
