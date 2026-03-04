# 🏪 Alura Store Latam — Análisis de Rendimiento de Tiendas

Proyecto de análisis de datos desarrollado como parte del **Challenge 1 de Data Science** de Alura Latam. El objetivo es evaluar el rendimiento de 4 tiendas a partir de sus datos históricos de ventas y emitir una recomendación estratégica fundamentada en los datos.

---

## 📋 Descripción

Se analizan más de **9,400 registros de ventas** distribuidos entre 4 tiendas, cubriendo el período 2021–2023. A través de métricas de facturación, categorías de productos, calificaciones de clientes y tendencias temporales, se identifica cuál tienda presenta el menor rendimiento y se justifica una recomendación de acción.

---

## 📊 Análisis realizados

| # | Sección | Descripción |
|---|---------|-------------|
| 1 | **Importación de datos** | Carga de CSVs desde el repositorio de Alura vía URL |
| 2 | **Preparación del DataFrame** | Consolidación de las 4 tiendas en `df_total` con columna `Tienda_ID` |
| 3 | **Facturación total** | Ingresos brutos por tienda y total acumulado |
| 4 | **Ventas por categoría** | Desglose de ingresos por categoría de producto |
| 5 | **Calificación promedio** | Satisfacción del cliente (escala 1–5) |
| 6 | **Productos más/menos vendidos** | Ranking de productos por volumen de ventas |
| 7 | **Costo de envío promedio** | Comparación logística entre tiendas |
| 8 | **Gráficos** | 6 visualizaciones comparativas (barras, boxplot, líneas, media móvil, acumulado) |
| 9 | **Informe y recomendación** | Conclusión fundamentada con tabla resumen |

---

## 📈 Gráficos e insights

### Gráfico 1 — Ingresos totales por tienda
Gráfico de barras que compara la facturación bruta acumulada de cada tienda durante todo el período.
> 💡 **Insight:** La Tienda 4 es la de menor ingreso total con ~$1,038M, aproximadamente $112M por debajo de la Tienda 1. La diferencia es consistente y no atribuible a un evento puntual.

---

### Gráfico 2 — Ingreso promedio por venta
Compara el ticket promedio (precio medio por transacción) entre las 4 tiendas.
> 💡 **Insight:** La Tienda 4 tiene el ticket promedio más bajo (~$440,000 USD por venta), lo que indica que su mix de productos es menos lucrativo por transacción, no solo que vende menos volumen.

---

### Gráfico 3 — Costo de envío vs. calificación del cliente
Boxplot que cruza el costo logístico con la satisfacción del cliente en todas las tiendas combinadas.
> 💡 **Insight:** No existe una correlación clara entre costo de envío y calificación — los clientes no penalizan más a las tiendas con envíos más caros, lo que descarta el costo logístico como causa del bajo rendimiento de la Tienda 4.

---

### Gráfico 4 — Lucro hipotético mensual por tienda
Serie temporal del lucro mensual (precio − costo de envío) separado por tienda.
> 💡 **Insight:** La Tienda 4 muestra una caída progresiva en su lucro mensual desde principios de 2022, mientras las demás tiendas mantienen fluctuaciones más estables alrededor de sus promedios.

---

### Gráfico 5 — Tendencia suavizada (Media Móvil 6 meses)
Suaviza las fluctuaciones mensuales para revelar la tendencia estructural de ventas de cada tienda.
> 💡 **Insight:** La Tienda 4 es la **única con una tendencia decreciente sostenida** desde finales de 2021. Las Tiendas 1 y 2 se mantienen estables; la Tienda 3 decayó pero desde un nivel superior. La Tienda 4 termina el período en su punto histórico más bajo.

---

### Gráfico 6 — Ingreso acumulado total por tienda
Muestra la acumulación de ingresos a lo largo del tiempo para visualizar la contribución histórica de cada tienda.
> 💡 **Insight:** La Tienda 4 se mantiene como la línea inferior a lo largo de **todo** el historial. Aunque todas las tiendas crecen en términos acumulados, la Tienda 4 es la que menos contribuye al total, reforzando su posición estructural como la de menor rendimiento.

---
> La **Tienda 4** aparece destacada en **rojo** en todos los gráficos.

---

## 🗂️ Estructura del repositorio

```
📦 alura-store-latam
 ┣ 📓 AluraStoreLatam.ipynb   ← Notebook principal con todo el análisis
 ┗ 📄 README.md               ← Este archivo
```

---

## 🚀 Cómo ejecutar

### Google Colab (recomendado)

1. Abre [Google Colab](https://colab.research.google.com/)
2. Ve a **Archivo → Subir notebook** y sube `AluraStoreLatam(1).ipynb`
3. Ejecuta todas las celdas con **Runtime → Run all**

No se requiere ninguna instalación adicional — los datos se descargan automáticamente desde GitHub.

---

## 🛠️ Tecnologías utilizadas

| Librería | Versión recomendada | Uso |
|---|---|---|
| `pandas` | ≥ 1.5 | Manipulación y análisis de datos |
| `matplotlib` | ≥ 3.5 | Visualizaciones base |
| `seaborn` | ≥ 0.12 | Visualizaciones estadísticas |

---

## 🔍 Conclusión principal

> **La Tienda 4 es la candidata a ser vendida o reestructurada.**

Sus problemas son estructurales:
- Menor facturación total del grupo (~$1,038M vs ~$1,150M de Tienda 1)
- Única tienda con tendencia decreciente sostenida desde finales de 2021
- Menor ingreso promedio por transacción (~$440,000 USD)
- Consistentemente la línea inferior en el ingreso acumulado histórico

---

## 📚 Fuente de datos

Datos provistos por [Alura Latam](https://www.aluracursos.com/) como parte del Challenge 1 de Data Science:  
🔗 [`alura-es-cursos/challenge1-data-science-latam`](https://github.com/alura-es-cursos/challenge1-data-science-latam)

---

## 👤 Autor

Desarrollado como parte del programa **Oracle Next Education (ONE) + Alura Latam**.
