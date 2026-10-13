# 🚀 Sideproject — Radar del tipo de cambio

**Repositorio:** `sideproject-tipo-de-cambio` · **Tipo:** ETL + análisis + dashboard · **Tiempo:** 6–8 h · **Después de:** las tres carpetas de este módulo

> Reglas, README y lista de cierre: [`06_ingenieria_de_datos/SIDEPROJECTS.md`](docs/REGLAS.md). **No hay solución: el diseño es tuyo.**

## El caso

Una tienda en línea compra en dólares y vende en pesos. Quiere entender cómo se ha movido el tipo de cambio en los últimos dos años para decidir cuándo comprar. Tú preparas los datos, los analizas y entregas un tablero interactivo.

Datos: API pública y sin clave. Desde pandas: `pd.read_json("https://api.frankfurter.dev/v1/2024-10-01..2026-09-30?base=USD&symbols=MXN,EUR")`.

## Qué practicas

| Carpeta | Dónde aparece |
|---|---|
| `01_core_python` | Funciones documentadas, una clase para el pipeline, excepciones |
| `02_analisis_datos` | pandas, limpieza, series de tiempo (medias móviles, remuestreo) |
| `03_visualizacion` | Matplotlib para el análisis, Plotly para el tablero |

## Hitos

**Hito 1 — Extraer y guardar.** Descarga los datos y guárdalos crudos en `data/raw/`.
*Comprueba:* si ya existe el archivo de hoy, no se descarga otra vez.

**Hito 2 — Transformar.** Una tabla con una fila por día: fecha, MXN, EUR. Decide qué hacer con sábados, domingos y festivos.
*Comprueba:* no hay fechas repetidas ni huecos sin explicar.

**Hito 3 — Analizar.** Variación diaria en %, media móvil de 7 y 30 días, el mejor y el peor mes, y la volatilidad por trimestre.
*Comprueba:* verifica a mano la variación de tres días.

**Hito 4 — Visualizar.** Tres gráficas de análisis (Matplotlib o Seaborn) y un tablero en Plotly exportado a HTML.
*Comprueba:* alguien ajeno entiende la conclusión mirando solo el tablero.

**Hito 5 — Concluir.** En el README, tres hallazgos con su gráfica y una recomendación para la tienda.
*Comprueba:* cada hallazgo se apoya en un número.

## Preguntas para defenderlo

- ¿Rellenaste los fines de semana o los dejaste vacíos? ¿Cómo cambia eso la media móvil?
- ¿Qué gráfica descartaste y por qué?
- ¿Tu recomendación se sostendría con otros dos años de datos?

## Súbelo de nivel

- Que se actualice solo con los días nuevos (carga incremental).
- Añade una tercera moneda sin tocar las funciones de análisis.
