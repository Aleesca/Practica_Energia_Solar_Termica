# Plan de Implementación: Selección de Equipos para Instalación Solar Centralizada

## Resumen

El objetivo de este plan es detallar el procedimiento para seleccionar un captador solar de la marca **Viessmann** y un intercambiador acumulador de ACS bivalente de la marca **Lapesa**, adaptados para una configuración de instalación **completamente centralizada** (acumulación solar centralizada y apoyo térmico centralizado). 

Una vez seleccionados, se documentarán sus características principales en una anotación técnica en `Proyecto/Anotaciones/seleccion-equipos-solar-centralizado.md`.

## Pasos de implementación

1. **Definición de criterios de selección:**
   * **Captador Viessmann:** Se buscarán captadores solares planos (como la gama *Vitosol*), identificando su superficie útil/absorbedora, factor óptico ($\eta_0$), coeficientes de pérdidas térmicas ($a_1, a_2$) y altura del captador (m).
   * **Acumulador Lapesa:** Se seleccionará un acumulador/interacumulador bivalente de gran volumen (gama *Master Inox / Master Vitro* o similar adaptada a centralizado bivalente) que integre dos serpentines (bivalente) para el circuito solar y el circuito de apoyo de caldera centralizada.

2. **Consultas a notebooks con la CLI `nlm`:**
   * Realizar una consulta en el notebook `Catalogos_solar` (ID: `7d1bf88b-463a-4291-9201-1959144a5921`) para buscar la información técnica detallada de los captadores **Vitosol 100-FM** y **Vitosol 200-FM**.
   * Realizar una consulta en el mismo notebook para buscar acumuladores bivalentes de la marca **Lapesa** (por ejemplo, modelos *Master Inox/Vitro* con configuración bivalente u otros depósitos bivalentes de gran capacidad).

3. **Análisis e identificación de características:**
   * Extraer las especificaciones del captador Viessmann:
     * Superficie de captación (absorbedora/apertura) en $m^2$.
     * Factor óptico ($\eta_0$).
     * Coeficiente de pérdidas térmicas de primer orden ($a_1$ en $W/m^2\cdot K$) y de segundo orden ($a_2$ en $W/m^2\cdot K^2$).
     * Altura total o dimensiones del captador (m).
   * Extraer las especificaciones del acumulador bivalente Lapesa:
     * Gama y modelo seleccionado.
     * Material (acero inoxidable *Master Inox* o vitrificado *Master Vitro*).
     * Volumen de acumulación ($L$).
     * Características de los serpentines (superficie de intercambio, potencias).
     * Aptitud para instalación centralizada.

4. **Elaboración de la anotación técnica final:**
   * Crear el archivo `Proyecto/Anotaciones/seleccion-equipos-solar-centralizado.md`.
   * Incluir la descripción del cambio de esquema solicitado por el usuario (de sistema mixto a sistema enteramente centralizado).
   * Exponer la ficha de características principales de los equipos seleccionados.
   * Citar las fuentes del notebook y los documentos consultados.

## Criterios de aceptación

* El plan se aprueba y se guarda en `Proyecto/Planificacion/plan-seleccion-equipos-solar-centralizado.md`.
* La anotación final se creará en `Proyecto/Anotaciones/seleccion-equipos-solar-centralizado.md` siguiendo este plan.
* Los equipos seleccionados deben pertenecer a las marcas solicitadas: **Viessmann** para el captador y **Lapesa** para el intercambiador acumulador.
* Se deben incluir todas las características técnicas requeridas por el usuario.
