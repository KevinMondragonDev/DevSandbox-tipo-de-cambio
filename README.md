# sideproject-tipo-de-cambio

> ETL, análisis y tablero interactivo del tipo de cambio USD/MXN de los últimos dos años.

**Estado:** 🚧 sin empezar · **Tipo:** ETL + análisis + dashboard · **Módulo del programa:** 03 · Python para datos

## La problemática

Una tienda en línea compra en dólares y vende en pesos, y decide cuándo comprar a ojo. Necesita entender cómo se ha movido el tipo de cambio: tendencia, volatilidad y los mejores y peores momentos, en un tablero que entienda alguien que no programa.

## Los datos

| Dónde | Qué es |
|---|---|
| <https://api.frankfurter.dev/v1/2024-10-01..2026-09-30?base=USD&symbols=MXN,EUR> | API pública de tipos de cambio, sin clave. Devuelve JSON; se puede leer directo con `pd.read_json` |

## Qué hay que construir

El enunciado completo, con sus hitos y cómo comprobar cada uno, está en [`RETO.md`](RETO.md). No trae solución: el diseño es tuyo.

- [`docs/REGLAS.md`](docs/REGLAS.md): cómo se trabaja un sideproject y qué debe tener este README al terminar.
- [`docs/RUBRICA.md`](docs/RUBRICA.md): con qué criterios se evalúa.

## Cómo se ejecuta

*Pendiente: se escribe al cerrar el primer hito. Los comandos exactos, desde `git clone`.*

## Decisiones

*Pendiente: tres decisiones técnicas y la alternativa que se descartó en cada una.*

## Qué aprendí

*Pendiente.*

---

Reto del programa de Python e ingeniería de datos: [UNIR_Python_Certification](https://github.com/KevinMondragonDev/UNIR_Python_Certification).
