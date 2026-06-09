# Plan: Definición de `alcance.md` para la práctica de Energía Solar

## Resumen

Este plan define cómo redactar el archivo `alcance.md` a partir del contenido de `00_Data/Enunciado_practica.pdf`, sin implementar todavía los cálculos ni modificar la memoria. El objetivo es convertir el enunciado en una guía de trabajo clara y verificable para el proyecto.

Punto obligatorio: **la bomba de circulación no se calculará**. Debe quedar indicado de forma explícita y sin ambigüedades en el documento final.

## Cambios previstos

- Crear `Proyecto/Planificacion/alcance.md` como documento de alcance del proyecto.
- Extraer del PDF los requisitos que sí forman parte de la práctica.
- Definir con claridad los cálculos incluidos y los cálculos excluidos.
- Describir la memoria a presentar, sus apartados mínimos y los entregables.
- Añadir una exclusión visible y repetida sobre la bomba de circulación:
  - no se calcula;
  - no se dimensiona;
  - no se selecciona;
  - no se estima su potencia ni su pérdida de carga;
  - no se desarrolla ningún criterio de selección asociado.

## Estructura del archivo

El archivo `alcance.md` debería organizarse en estas secciones:

1. `Objetivo del proyecto`
2. `Datos de partida`
3. `Cálculos incluidos`
4. `Cálculos excluidos`
5. `Memoria a presentar`
6. `Entregables`
7. `Criterios de revisión`
8. `Referencias y flujo de trabajo`

## Flujo de trabajo

1. Leer `00_Data/Enunciado_practica.pdf`.
2. Identificar todos los cálculos exigidos por el enunciado.
3. Redactar `alcance.md` como documento de alcance, no como resolución técnica.
4. Revisar que la exclusión de la bomba de circulación aparezca de forma inequívoca.
5. Activar después las referencias correspondientes en `.agents/` siguiendo el flujo de trabajo definido en el proyecto.

## Validación

- Confirmar que el archivo resultante está en Markdown válido.
- Verificar que se listan todos los cálculos realmente exigidos por el enunciado.
- Verificar que la memoria queda bien definida en estructura y contenido mínimo.
- Comprobar que la bomba de circulación queda fuera del alcance sin excepciones.
- Confirmar que no se introduce ningún procedimiento de cálculo para la bomba.

## Supuestos

- Por ahora no se implementa ningún cálculo.
- El PDF `00_Data/Enunciado_practica.pdf` es la única fuente para cerrar el alcance.
- El flujo de `.agents/` se aplicará después de dejar cerrado el documento `alcance.md`.
