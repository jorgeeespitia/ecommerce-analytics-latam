# Rentabilidad, funnel y experimentación en un e-commerce multi-país (LATAM)

Análisis de datos de punta a punta de un e-commerce que opera en México, Colombia y Argentina: calidad de datos, rentabilidad, funnel de conversión, retención por cohortes, A/B test y dashboard en Power BI.

> **Aviso:** proyecto académico con **datos simulados** del curso de Data Analyst de TripleTen. No usa información real de ninguna empresa. Los datasets del curso **no se redistribuyen** en este repositorio.

**Herramientas:** Python (pandas, NumPy, SciPy, statsmodels) · SQL (PostgreSQL, SQLAlchemy) · Power BI (DAX)

## Preguntas de negocio

1. ¿Podemos confiar en los datos?
2. ¿El negocio es rentable?
3. ¿Dónde se pierden los usuarios?
4. ¿Los usuarios regresan?
5. ¿El cambio en el checkout genera impacto?

## Hallazgos clave

| Tema | Resultado |
|---|---|
| **Calidad de datos** | Se eliminaron 194 de 25,100 filas de pedidos (0.77 %) con 6 reglas documentadas en una bitácora de limpieza. |
| **Rentabilidad** | Margen bruto de 60.2 %, utilidad después de marketing de 30.3 % y ROAS global de 3.35 (punto de equilibrio ≈ 1.66). |
| **Producto** | 4 de 7 productos superan el 90 % de margen, pero **Laptop-Gaming-16GB tiene margen negativo (−8.6 %)**. |
| **Funnel** | Conversión final de 3.31 % (258 de 7,796 usuarios). Solo el 9.7 % de quienes inician el checkout compra. |
| **Retención** | Estable en ~40–44 % semanal en las cohortes de enero a mayo de 2025. |
| **A/B test** | +0.60 pp en conversión (p = 0.416; IC 95 %: −0.84 a +2.03 pp): resultado **inconcluso**. |

**Recomendaciones:** revisar precio y costo de la laptop (y, después, de la chaqueta y la licuadora), investigar la fricción del checkout y la instrumentación de eventos, y no adoptar el cambio del A/B test con la evidencia actual.

## Dashboard (Power BI)

Dos páginas construidas con los CSV limpios del análisis:

- **Overview Ejecutivo:** KPIs de revenue, costo, marketing y utilidad; ventas por mes; ventas, unidades y gasto de marketing por país.
- **Análisis Comercial:** unidades e ingresos por categoría y canal, ingresos por mes y tablas de detalle, con filtros por país y mes.

## Estructura del repositorio

```
├── notebooks/
│   └── Proyecto_De_datos_a_decisiones.ipynb    # análisis completo (Pasos 1 a 5)
├── reports/
│   └── Proyecto_De_datos_a_decisiones.html     # versión de lectura del notebook
├── dashboard/                                  # PDF del dashboard
├── data/                                       # CSV del curso (no incluidos)
├── LICENSE
└── README.md
```
## Datos y reproducibilidad

Los datos de este proyecto (pedidos, catálogo, campañas de marketing y eventos de usuarios) provienen de un **curso de análisis de datos** y son de uso exclusivo para ese programa, por lo que **no se incluyen en este repositorio** y el análisis no puede ejecutarse de extremo a extremo con un clic.

Para que el trabajo sea revisable de todas formas, el repositorio incluye:

- **Notebook completo** (`notebooks/`): código, decisiones de limpieza y resultados de cada paso, con las salidas visibles.
- **Versión HTML** (`reports/`): el mismo análisis para leerlo sin instalar nada.
- **Dashboard en PDF** (`dashboard/`): resultado final en Power BI.
- **Descripción de las tablas** (más abajo): las columnas y el formato que espera el código.

## Uso responsable de IA

La pregunta de negocio, las reglas de limpieza, la interpretación y las conclusiones son mías. La IA apoyó en la revisión crítica del notebook y del dashboard, en sugerencias de validación y en la corrección de erratas y formato. Verifiqué que las cifras clave coinciden entre el notebook y el dashboard, y excluí un análisis estadístico que no pude explicar con seguridad. Antes de publicar retiré credenciales y enlaces del curso.

## Próximos pasos

- Rehacer el modelo del dashboard como esquema en estrella (país, canal y fecha) para que el gasto de marketing responda a los filtros.
- Añadir un visual de margen por producto, KPIs de margen %, ROAS y unidades por pedido, y una página de detalle por pedido.

## Autor

[@jorgeeespitia](https://github.com/jorgeeespitia)

Licencia [MIT](LICENSE) para el código y el análisis. Los datasets pertenecen al curso.
