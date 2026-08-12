# 📡 Calculadora de Zona de Fresnel

Aplicación web educativa para calcular la **primera zona de Fresnel (F1)** y estudiar de forma visual el despeje geométrico de un radioenlace.

**Autor:** Facundo Rullo

## Modos disponibles

### Cálculo básico

Conserva exactamente la fórmula entregada en la consigna:

```text
F1 = 8.656 × √(D / f)
```

- `D`: distancia total del enlace, en kilómetros.
- `f`: frecuencia, en GHz.
- `F1`: radio máximo de la primera zona de Fresnel, en metros.

El radio máximo se encuentra en el centro del enlace.

### Análisis avanzado

Agrega:

- Altura de cada antena sobre el terreno.
- Ninguno, uno o varios obstáculos.
- Nombre y altura de cada obstáculo.
- Radio F1 específico en cada punto.
- Evaluación final del enlace.
- Perfil gráfico generado por la propia aplicación.

## Interpretación del resultado

El despeje real se actualiza en cada cálculo y se expresa como porcentaje con la siguiente escala:

- 80% o más: resultado `ANDA`, despeje `Excelente`.
- Desde 60% y menos de 80%: resultado `ANDA`, despeje `Regular`.
- Menos de 60%: `NO ANDA`.

Si falta altura en las antenas, informa cuánto debe aumentarse cada una. Si el problema es un obstáculo, informa cuánto deben subirse ambas antenas o cuánto debe reducirse el obstáculo.

Las correcciones de altura se redondean hacia arriba a dos decimales para no informar una medida insuficiente.

## Validaciones

- Acepta coma o punto como separador decimal.
- Rechaza campos vacíos y caracteres no numéricos.
- Distancia, frecuencia y alturas de antena deben ser mayores que cero.
- Las alturas de obstáculos pueden ser cero.
- Los resultados generales se truncan a dos decimales; las alturas mínimas y correcciones se redondean hacia arriba para asegurar que alcancen.

## Alcance y supuestos

El modo avanzado usa un nivel de terreno común como referencia. Las alturas de las antenas y los obstáculos se miden desde esa base, y los obstáculos se evalúan automáticamente en el centro del enlace. Para conservar la fórmula de la consigna, F1 se calcula con `F1 = 8.656 × √(D / f)` para todo el enlace.

La evaluación describe **geometría, línea visual y despeje de Fresnel**. No garantiza por sí sola el funcionamiento de un enlace. Un diseño completo también necesita potencia transmitida, ganancias de antena, pérdidas, sensibilidad del receptor, margen de desvanecimiento, interferencias y efectos meteorológicos.

## Tecnologías

- HTML5
- CSS3
- JavaScript
- SVG para el perfil visual
- Sin backend, frameworks ni dependencias externas

## Ejecución

Abrí `index.html` directamente en un navegador o visitá:

[https://facundo-rullo.github.io/Zona-Fresnel/](https://facundo-rullo.github.io/Zona-Fresnel/)

## Referencias técnicas

- [ITU-R P.526 — Propagación por difracción](https://www.itu.int/rec/R-REC-P.526/es)
- [ITU-R P.530 — Diseño de sistemas terrenales con visibilidad directa](https://www.itu.int/rec/R-REC-P.530/es)

## Licencia

Proyecto desarrollado con fines académicos.
