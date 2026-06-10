# Anotación Técnica: Acumulación Solar Centralizada vs. Individualizada

> Relacionado con: [Especificación: Antecedentes y Datos de Partida](../Especificaciones/especificacion-antecedentes-y-datos-de-partida.md#h2-22-justificación-del-sistema-centralizado)

Esta anotación técnica resuelve la elección de la configuración de acumulación solar (centralizada o individualizada) para un edificio plurifamiliar que cuenta con una instalación receptora de gas natural existente.

---

## 1. Pregunta técnica

* **¿Es preferible un sistema de acumulación solar centralizado o uno individualizado para la producción de agua caliente sanitaria (ACS) en un edificio plurifamiliar con instalación de gas natural preexistente?**
* **¿Condiciona la instalación receptora de gas natural (con contadores individuales en las viviendas y conexión a redes de media presión A) la elección de la configuración del sistema solar?**

---

## 2. Contexto de la instalación existente

El edificio de viviendas objeto del proyecto cuenta con las siguientes características térmicas y de gas natural de partida (según [datos_GN.md](../../00_Data/datos_GN.md) y [Alcance.md](../Alcance.md)):

* **Instalación Receptora de Gas (IRG):** Distribución individualizada con contadores en vivienda y conexión a red de gas en Media Presión A (MPA, presiones de operación de hasta 0.4 bar).
* **Sistema de apoyo o auxiliar:** Calderas murales mixtas individuales de gas natural de **22 kW** de potencia útil para calefacción y ACS en cada vivienda.
* **Poder Calorífico Superior (PCS) del Gas Natural:** **40.68 MJ/m³(s)**.
* **Otros consumos de gas en las viviendas:** Cocinas (**5 kW**), hornos (**12 kW**) y secadoras (**11.3 kW**).

---

## 3. Consulta a notebooks

La resolución técnica se apoya en las consultas automatizadas realizadas a los cuadernos de trabajo a través del NotebookLM CLI (`nlm`):

### A. Notebook: `Energia_Solar_Termica` (ID: `62b2af52-7df4-455e-9334-8b10ebd8118d`)
* **Eficiencia y simultaneidad:** La acumulación centralizada es térmicamente más eficiente de forma global y reduce costes de inversión. Aprovecha el factor de simultaneidad y disminuye las arrancadas y paradas del sistema de apoyo.
* **Pérdidas térmicas:** La acumulación centralizada genera pérdidas continuas importantes en las tuberías de distribución colectiva de ACS (pérdidas por disponibilidad las 24 horas del día). En cambio, la acumulación distribuida solo tiene pérdidas en el circuito de distribución solar durante las horas de sol. Sin embargo, la suma de las pérdidas de los tanques individuales pequeños suele superar a la de un gran acumulador centralizado.
* **Esquema de acoplamiento:** Para edificios con apoyo distribuido (calderas individuales existentes), la guía técnica de referencia (IDAE) propone la **instalación solar centralizada con sistema de apoyo distribuido conectado en serie**. En este esquema, el agua se precalienta centralmente y se suministra a la entrada de las calderas individuales.
* **Compatibilidad de calderas:** Las calderas individuales mixtas de gas natural deben estar preparadas para recibir agua precalentada por el sol y modular la aportación de su quemador. Si el equipo auxiliar o sus conexiones no toleran temperaturas elevadas (el agua solar puede superar los 60 °C en verano), se exige instalar válvulas mezcladoras termostáticas o válvulas de tres vías diversoras (*by-pass* automático de la caldera) para evitar daños en el equipo y riesgos de quemaduras.

### B. Notebook: `Catalogos_solar` (ID: `7d1bf88b-463a-4291-9201-1959144a5921`)
* **Soluciones de gran capacidad (Centralizadas):**
  * **Lapesa:** Recomienda las series **Master Inox** (acero inoxidable) y **Master Vitro** (acero vitrificado) en capacidades de **1.500 a 6.000 litros** (e industriales hasta 12.000 litros). Destacan por sus serpentines modulares desmontables de acero inoxidable de hasta 10 m², lo que facilita las labores de mantenimiento antilegionella (conforme a R.D. 487/2022).
  * **Baxi:** Ofrece el sistema compacto **Drain-Back DB** (modelos DB 40S, 50, 100, 150) aptos para campos solares de hasta 150 m² (60 colectores), acoplados a interacumuladores de gran volumen como **AS X-1 E** y **AS X-IN E**.
* **Soluciones domésticas (Individuales):**
  * **Lapesa:** Serie **Geiser Inox** (60 a 1.000 litros) y **Coral Vitro** (80 a 1.500 litros). Destaca el interacumulador **Coral Solvitro** (150 a 500 litros), una solución integral que incorpora serpentín de alta eficiencia, vaso de expansión y estación de control solar premontados en el depósito.
  * **Baxi:** Ofrece los kits compactos forzados **Solar Easy ACS / ACS Slim** y el sistema autovaciante **Solar Easy DB** (hasta 4 paneles), además de los sistemas termosifónicos **STS** (150 a 300 litros).
  * **Tradesa:** Gama de circulación natural **Tradesol CN** (160, 200 y 300 litros), sistemas Drain Back domésticos (150 a 300 litros) e interacumuladores solares **FC1** con un solo serpentín (160 a 500 litros).

---

## 4. Consulta externa con Exa Deep Search

La validación técnica del diseño final se apoyará en una consulta en profundidad con **Exa Deep Search** sobre los siguientes aspectos específicos:
1. **Rendimiento de calderas de modulación con agua precalentada:** Evaluación del caudal mínimo de encendido del quemador y el rango de modulación de calderas murales comunes de 22 kW al recibir agua a temperaturas variables (30 °C - 55 °C).
2. **Requisitos de seguridad y control de sobretemperaturas:** Verificación de las recomendaciones técnicas de by-pass termostático a la entrada de calderas según fabricantes líderes (Baxi, Saunier Duval, Junkers) para prevenir fallos en componentes hidráulicos internos de calderas domésticas.
3. **Cumplimiento de la normativa legionelosis (R.D. 487/2022 y RITE):** Reglas específicas para el mantenimiento de la temperatura del agua en las redes de distribución colectivas (>50 °C en el punto de consumo) en esquemas con acumulación centralizada y apoyo individual.

---

## 5. Comparación técnica

| Criterio Técnico / Económico | Acumulación Solar Centralizada | Acumulación Solar Individualizada (Distribuida) |
| :--- | :--- | :--- |
| **Rendimiento térmico global** | **Óptimo.** Menor pérdida conjunta gracias a la relación superficie/volumen favorable de un gran depósito. | **Menor.** Pérdidas acumuladas mayores por la suma de múltiples depósitos pequeños en cada vivienda. |
| **Pérdidas en red de distribución** | **Elevadas.** Hay circulación continua en la columna/recirculación común de distribución de ACS. | **Mínimas.** El circuito solar solo bombea energía térmica durante las horas de radiación. |
| **Inversión inicial** | **Bajo.** Un único depósito centralizado, menor cantidad de componentes hidráulicos comunes. | **Muy alto.** Multiplica depósitos, vasos de expansión, bombas de carga y tuberías por cada vivienda. |
| **Uso de espacio** | **Óptimo.** Ocupa espacio común (sala de máquinas o azotea), sin restar metros útiles en viviendas. | **Deficiente.** Requiere reservar espacio significativo dentro de cada vivienda para el depósito (150-300L). |
| **Medición de consumos** | Requiere contadores individuales de ACS en la acometida de cada vivienda para reparto de gastos. | No requiere contadores de ACS comunitarios (cada usuario consume de su depósito individual). |
| **Prevención de Legionella (R.D. 487/2022)** | **Estricta.** Obliga a un mantenimiento riguroso de temperaturas (>60 °C en acumulación) y choques térmicos. | **Exenta.** Los depósitos individuales dentro de viviendas particulares no se consideran redes colectivas. |

---

## 6. Relación con la instalación de gas natural

Es fundamental aclarar la separación física y conceptual de ambos sistemas para evitar errores de diseño:

1. **La instalación de gas natural existente NO condiciona la elección del sistema de acumulación solar:** 
   La instalación receptora de gas (IRG) es un servicio de suministro de energía que opera de manera independiente. Funciona en Media Presión A con contadores individuales con el único propósito de alimentar el combustible para los consumos de cada vivienda (caldera de 22 kW, cocina, horno, secadora). La decisión de centralizar o individualizar el agua caliente solar depende de parámetros arquitectónicos, espaciales, de eficiencia de almacenamiento y de coste, pero no de la presión o configuración del tubo de gas.
2. **La hibridación ocurre en el acoplamiento hidráulico de ACS:**
   * **En acumulación centralizada con apoyo individual (Recomendado):** El agua fría de red entra al interacumulador solar centralizado (por ejemplo, gama *Master Vitro* de Lapesa), donde se precalienta. Posteriormente, una red de distribución común de agua precalentada suministra este fluido a cada vivienda. En la vivienda, la línea entra en serie a la caldera mural de gas natural de 22 kW existente. Si la temperatura solar es suficiente (ej. >50 °C), la caldera no enciende el quemador (o se realiza un *by-pass* automático mediante válvula de tres vías). Si la temperatura es insuficiente, la caldera de 22 kW aporta la potencia térmica necesaria para alcanzar la consigna de uso.
   * **En acumulación individualizada:** Se requeriría llevar un bucle hidráulico del primario solar desde el tejado a cada vivienda para alimentar un serpentín en un acumulador doméstico (ej. *Coral Solvitro* o *FC1*). El agua fría se precalentaría localmente dentro de cada vivienda y pasaría en serie a la caldera.
3. **El único condicionante real del gas natural es la aptitud de la caldera:**
   El apoyo de gas natural debe ser capaz de regular la combustión en serie con entradas de agua caliente fluctuantes y disponer de protecciones (válvulas termostáticas mezcladoras) para evitar que agua a más de 60 °C deteriore los componentes de la caldera mixta individual.

---

## 7. Conclusión recomendada

Para este edificio plurifamiliar con calderas mixtas de gas natural individuales existentes, la solución óptima es la **acumulación solar centralizada con sistema de apoyo individual distribuido** (esquema mixto).

### Justificación:
1. **Espacio en viviendas:** Evita penalizar a los vecinos obligándolos a destinar espacio útil dentro de sus hogares para interacumuladores individuales.
2. **Viabilidad económica:** Reduce drásticamente los costes de instalación al evitar la compra de múltiples depósitos, vasos de expansión solar individuales y la complejidad de canalizar tuberías de refrigeración solar individuales hasta cada piso.
3. **Facilidad de mantenimiento:** Concentra la acumulación solar en cubierta o zonas comunes (utilizando depósitos industriales eficientes como la serie *Master Vitro* de Lapesa), facilitando los mantenimientos preventivos y la limpieza antilegionella.
4. **Hibridación sencilla:** Aprovecha las calderas individuales de 22 kW existentes como apoyo térmico directo en serie, garantizando la continuidad del suministro de ACS con la simple incorporación de una válvula mezcladora termostática a la entrada de cada caldera para protección del equipo contra sobretemperaturas veraniegas. La red receptora de gas natural permanece inalterada y segura.
