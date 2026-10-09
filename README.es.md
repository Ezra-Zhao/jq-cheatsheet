# Hoja de referencia de jq · jq Cheatsheet

> 🌍 [中文](README.md) · [Português](README.pt.md)

Una **hoja de referencia de una sola página** para jq: 30 filtros verificados uno por uno con datos reales (probados en jq 1.7). Cada entrada responde solo tres preguntas — **qué hace, un comando listo para copiar y pegar, y etiquetas de uso**. Sin funciones inventadas ni sintaxis improvisada.

## Para quién es

Para desarrolladores backend, ingenieros SRE/DevOps y cualquiera que trabaje con JSON a diario. Si cada vez que analizas la respuesta de una API tienes que buscar la sintaxis de jq, esta hoja te ayuda a memorizar los filtros más usados de una vez.

## Cómo usarla

1. Ve directo a **[CHEATSHEET.md](CHEATSHEET.md)** — el cuerpo de la referencia; los filtros en inglés los entiende cualquier desarrollador.
2. Instala jq primero: `brew install jq` en macOS, `sudo apt install jq` en Debian/Ubuntu.
3. Guarda el `config.json` de ejemplo que está al final de la página y ejecuta cada filtro a mano: en una hora lo dominas.

## Qué incluye

| Categoría | Contenido |
|---|---|
| 📥 Básicos | Formato legible, extraer campos, salida cruda con `-r`, salida compacta con `-c` (4) |
| 🧭 Anidados y arreglos | Rutas profundas, índices, expansión con `.[]`, conteo con `length` (4) |
| 🔎 Filtrado | `select` por número, por texto y con condiciones combinadas (3) |
| 🔄 Transformación | `map` para extraer campos, remodelar objetos y agregar campos calculados (3) |
| 🔗 Tuberías y construcción | Encadenar con `|`, sintaxis corta `{a, b}`, armar objetos resumen (3) |
| 🔤 Cadenas y números | `tostring`/`tonumber`, `split`/`join`, regex con `test()` (3) |
| 📊 Agregación | Ordenar, deduplicar, agrupar y contar, sumar, máximo/mínimo (5) |
| 🗝️ Claves | `keys`/`has`/`del` (1) |
| 🛠️ Casos reales | `curl \| jq`, estadísticas de logs, `--arg` para variables del shell, `--slurp` (4) |

Cada filtro se ejecutó con jq 1.7 sobre datos reales; los ejemplos de entrada y salida están en los comentarios.

## Por qué estos 30

- **Frecuencia primero**: cada categoría cubre comandos que de verdad se escriben a diario; nada de funciones exóticas que nunca se usan.
- **Cierre práctico**: los últimos 4 son escenarios reales de producción (consumir APIs, leer logs, pasar variables), listos para usar.

## Contribuciones bienvenidas

¿Un filtro incorrecto, un caso de uso faltante o una traducción mejorable? Los *pull requests* son bienvenidos. Mantén el formato de cada entrada (qué hace / comando / etiquetas) y **ejecuta cada filtro con jq real antes de enviarlo**.

## Licencia

MIT © 2026 Guangyi Zhao. Ver [LICENSE](LICENSE).
