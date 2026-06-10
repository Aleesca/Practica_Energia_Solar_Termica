# Plan: Antecedentes y Datos de Partida

> Source PRD: [Solicitud de estructuración de antecedentes y datos de partida](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Planificacion/plan-antecedentes-y-datos-de-partida.md)

## Decisiones arquitectónicas

Durable decisions that apply across all phases:

- **Estructura del Documento**: La especificación técnica final se redacta en formato Markdown (`.md`) dentro de [Especificaciones](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Especificaciones/).
- **Alineación con Ingeniería Real**: Se estructurará el documento en dos grandes bloques diferenciados: `2. Antecedentes` (que contiene el contexto histórico, origen, objeto y marco normativo) y `3. Datos de Partida` (que define las restricciones físicas, geográficas, perfiles de ocupación y fichas técnicas de equipos).
- **Esquema de Referencias Cruzadas**: Vinculación explícita bidireccional entre los condicionantes del enunciado de la práctica y las notas técnicas de ingeniería recopiladas en la carpeta de anotaciones.
- **Formato Visual**: Estructuración rígida de datos mediante tablas Markdown alineadas a la derecha para columnas numéricas, bloques explicativos de tipo `> [!NOTE]` y `> [!TIP]`, sin fórmulas ni operaciones matemáticas.

---

## Phase 1: Lectura de Fuentes y Captura de Referencia Catastral

**User stories**:
- Identificar la ubicación, el grupo de prácticas y extraer la referencia catastral desde el enunciado de la práctica.
- Leer y procesar las anotaciones de ingeniería existentes en el proyecto sin omitir datos operativos.

### What to build
Un resumen estructurado con las coordenadas geográficas del edificio, su zona climática y de radiación, la demanda diaria de ACS y las características técnicas de los captadores solares y acumuladores seleccionados.

### Acceptance criteria
- [x] Referencia catastral `5089301TL7358G0001ZD` identificada para el Grupo G1-1 (Salamanca) a partir del enunciado de la práctica [Enunciado_practica.pdf](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/00_Data/Enunciado_practica.pdf).
- [x] Datos geográficos consolidados a partir de [posicion_edificio.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/posicion_edificio.md) (Latitud $40^\circ 58'\ 8.31''\text{ N}$, Longitud $5^\circ 40'\ 29.95''\text{ O}$).
- [x] Características técnicas del captador **Viessmann Vitosol 200-FM SV2F** y del acumulador **Lapesa Master Inox MXV-2000 SS2B** recopiladas de las anotaciones técnicas de [Anotaciones](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/).

---

## Phase 2: Mapeo Estructural y Referencias Cruzadas

**User stories**:
- Justificar técnicamente la colocación geométrica (inclinación y azimut) y calcular las pérdidas del plano de captación conforme al CTE DB-HE4.
- Justificar el volumen de acumulación de 2.000 L seleccionado y las condiciones de hibridación con el circuito primario y la caldera auxiliar.

### What to build
Cálculo analítico detallado de las pérdidas por orientación e inclinación en Salamanca y la argumentación de la relación volumen/superficie ($V/S_c$) para evitar sobrecalentamientos estivales y cumplir con la normativa antilegionella.

### Acceptance criteria
- [x] Pérdidas por inclinación ($4.35\%$ - analizadas cualitativamente en especificaciones) y azimut ($1.40\%$) justificadas bajo el límite máximo del 10% del CTE DB-HE4 ($P_{total} = 5.75\%$).
- [x] Justificación técnica de la inclinación a $60^\circ$ (mejora en invierno, autolimitación de sobrecalentamiento en verano) documentada.
- [x] Relación de acumulación $\frac{V}{S_c} = 71.53\text{ l/m}^2$ justificada como óptima frente al CTE/RITE y vinculada al cumplimiento del **R.D. 487/2022** (serpentines desmontables mediante brida lateral DN400).

---

## Phase 3: Creación de la Especificación de Maquetación

**User stories**:
- Disponer de un documento plantilla en Markdown que sirva de guía y maquetación de referencia para la sección de Antecedentes y Datos de Partida en la memoria.
- Presentar la tabla mensual f-Chart de balance energético y verificar los límites de sobreproducción.

### What to build
Creación de la especificación técnica en Markdown con la estructura final de encabezados de la memoria, placeholders con datos reales, tablas alineadas, bloques informativos y matriz de trazabilidad de archivos.

### Acceptance criteria
- [x] Archivo [especificacion-antecedentes-y-datos-de-partida.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Especificaciones/especificacion-antecedentes-y-datos-de-partida.md) creado en [Proyecto/Especificaciones](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Especificaciones/).
- [x] Tabla de balance mensual f-Chart (demanda de $22.856\text{ kWh/año}$ y fracción anual resultante del $75.3\%$) integrada y formateada.
- [x] Límites de sobreproducción verificados (mes máximo agosto con $106\% < 110\%$, y únicamente 3 meses por encima del $100\%$).
- [x] Matriz de trazabilidad cruzada y enlaces absolutos a los archivos de origen plenamente operativos.

---

## Phase 4: Restructuración y Alineación con Estándares de Ingeniería Real

**User stories**:
- Adaptar las especificaciones de maquetación para reflejar cómo se estructura la documentación en proyectos de ingeniería reales de energía solar térmica.
- Separar de forma tajante el contexto del proyecto (Antecedentes) de los parámetros técnicos inalterables de diseño (Datos de Partida).
- Incorporar el encargo, el marco normativo nacional aplicable y los condicionantes físicos del edificio (azotea, patinillos).

### What to build
Actualización de [especificacion-antecedentes-y-datos-de-partida.md](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Especificaciones/especificacion-antecedentes-y-datos-de-partida.md) reestructurando el contenido en:
- `## 2. Antecedentes del Proyecto` (Origen y objeto del encargo, justificación del sistema y Normativa de aplicación detallada).
- `## 3. Datos de Partida` (Ubicación climática, Ocupación y demanda de consumo, Integración física del edificio [cubierta y patinillo de comunicaciones] y Equipamiento de referencia de catálogo).

### Acceptance criteria
- [x] Documento de especificaciones dividido rigurosamente en las secciones principales "Antecedentes" y "Datos de Partida".
- [x] Inclusión de una sección formal de **Normativa de aplicación** que recoja: CTE DB-HE4 (Contribución solar mínima para ACS), RITE (R.D. 1027/2007, Reglamento de Instalaciones Térmicas), R.D. 487/2022 (Prevención y control de Legionelosis), R.D. 919/2006 (Reglamento de Gas Natural), y normas UNE 60670.
- [x] Inclusión de una sección de **Condicionantes de Integración Física** del edificio (montaje en cubierta plana transitada/azotea y distribución colectiva por el patinillo de comunicaciones vertical).
- [x] Ausencia absoluta verificada de fórmulas matemáticas, ecuaciones en LaTeX y balances mensuales calculados de f-Chart.
- [x] Enlaces cruzados plenamente funcionales a los archivos origen de [Anotaciones](file:///H:/Shared%20drives/Practicas_Inst2/6_Energia_Solar/Proyecto/Anotaciones/).
