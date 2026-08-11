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

- Elevación del terreno en ambos extremos.
- Altura de cada antena sobre el terreno.
- Curvatura terrestre efectiva calculada automáticamente con `k = 4/3`.
- Ninguno, uno o varios obstáculos.
- Posición y altura de cada obstáculo.
- Curvatura terrestre efectiva.
- Radio F1 específico en cada punto.
- Despeje vertical y porcentaje respecto de F1.
- Perfil gráfico generado por la propia aplicación.

La curvatura efectiva se calcula con:

```text
b = (d1 × d2) / (2 × k × R)
```

usando las distancias en metros, `R = 6.371.000 m` y el factor estándar `k = 4/3`. Este valor se aplica internamente y el usuario no necesita ingresarlo.

## Interpretación del despeje

| Despeje respecto de F1 | Interpretación geométrica |
|---:|---|
| `≥ 100%` | Primera zona completamente despejada |
| `≥ 60%` | Cumple el criterio habitual de despeje |
| `> 0% a < 60%` | Hay línea visual, pero el despeje es insuficiente |
| `≤ 0%` | El terreno u obstáculo alcanza o cruza la línea visual |

El antiguo límite del 40% fue retirado porque no constituye un umbral técnico general. El 60% se mantiene como referencia principal.

## Validaciones

- Acepta coma o punto como separador decimal.
- Rechaza campos vacíos y caracteres no numéricos.
- Distancia, frecuencia y alturas de antena deben ser mayores que cero.
- Las alturas de obstáculos pueden ser cero.
- Las elevaciones de los terrenos A y B pueden ser negativas.
- Todo obstáculo debe ubicarse entre las antenas.
- Los resultados se calculan con precisión completa y se muestran truncados a dos decimales, sin redondear.

## Alcance y supuestos

El modo avanzado interpola la elevación del terreno entre los extremos y aplica la curvatura efectiva sobre ese perfil. La base de cada obstáculo se estima automáticamente según su posición; el usuario sólo ingresa su altura sobre el terreno. Para conservar la fórmula de la consigna, F1 se calcula con `F1 = 8.656 × √(D / f)` para todo el enlace.

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
