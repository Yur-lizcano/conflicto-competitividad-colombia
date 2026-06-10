# Pobreza Multidimensional y Conflicto Armado en Colombia (2023–2025)

Análisis econométrico de la relación entre el Índice de Pobreza Multidimensional (IPM) y el número de víctimas del conflicto armado en los 33 departamentos de Colombia, controlando por los pilares del Índice de Competitividad Departamental (IDC).

**Autoras:** Yeimy Katteryne Gutiérrez Valderrama · Yurley Lizcano Bonilla  
**Institución:** Programa de Economía — Universidad Surcolombiana  


---

## Pregunta de investigación

¿Cuál es la relación entre el IPM departamental y el número acumulado de víctimas del conflicto armado, considerando las condiciones estructurales de competitividad territorial de los departamentos colombianos entre 2023 y 2025?

---

## Hallazgos principales

- El coeficiente de víctimas es **positivo en los tres modelos**, consistente con la hipótesis, pero no alcanza significancia estadística — lo que sugiere que el conflicto opera sobre la pobreza a través de canales indirectos más que de forma directa.
- Los canales identificables con efectos robustos y significativos son: **tasa de homicidios, afiliación al régimen subsidiado de salud, cobertura eléctrica, calidad educativa e informalidad laboral**.
- La brecha territorial entre el departamento con mayor y menor IPM supera los **68 puntos porcentuales**.
- El test de Hausman (H = 71,81; p < 0,001) favoreció **efectos fijos** como estimador consistente.

---

## Metodología

| Componente | Detalle |
|------------|---------|
| Datos | Panel balanceado, 33 departamentos × 3 años = 99 observaciones |
| Variable dependiente | IPM departamental (DANE, 2023) |
| Variable de interés | ln(Víctimas acumuladas + 1) — Unidad para las Víctimas (2025) |
| Variables de control | 29 indicadores seleccionados por LASSO de 137 disponibles del IDC (CPC, 2025) |
| Selección de variables | LASSO con validación cruzada CV-3 (λ óptimo = 0,2775) |
| Modelos estimados | Pooled OLS, Efectos Fijos (within), Efectos Aleatorios (GLS) |
| Diagnóstico | Test de Hausman |

---

## Fuentes de datos

| Fuente | Variable | Enlace |
|--------|----------|--------|
| DANE | IPM departamental | [dane.gov.co](https://www.dane.gov.co) |
| Unidad para las Víctimas | Registro acumulado de víctimas por departamento | [unidadvictimas.gov.co](https://www.unidadvictimas.gov.co) |
| Consejo Privado de Competitividad (CPC) | Índice de Competitividad Departamental — 137 indicadores | [compite.com.co](https://compite.com.co) |

---

## Estructura del repositorio

```
├── README.md
├── data/
│   └── BASE_YEIMY.xlsx          # Panel consolidado (33 depts × 3 años)
├── code/
│   └── Panel_IPM_Conflicto.ipynb  # Notebook Python: LASSO + modelos de panel
└── outputs/
    └── [tablas y gráficas de resultados]
```

---

## Cómo reproducir el análisis

1. Clona el repositorio
2. Abre `code/Panel_IPM_Conflicto.ipynb` en Google Colab o Jupyter
3. Carga `data/BASE_YEIMY.xlsx` cuando el notebook lo solicite
4. Ejecuta todas las celdas en orden

**Requisitos:** `pandas`, `numpy`, `scikit-learn`, `scipy`, `matplotlib`

---

## Clasificación JEL

I32 · O15 · C23 · D74
