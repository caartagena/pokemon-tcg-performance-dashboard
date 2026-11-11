# Dashboard Pokémon TCG · Seguimiento de mazos

> Google Sheets dashboard for tracking Pokémon TCG match performance by deck, opposing archetype, match format, and turn order.

[Hacer una copia en Google Sheets](https://docs.google.com/spreadsheets/d/1JdKYZhjCDZcFxOrl1LRJWITnz72az6E1vqIhxXUW7Dc/copy) · [Ver la plantilla original](https://docs.google.com/spreadsheets/d/1JdKYZhjCDZcFxOrl1LRJWITnz72az6E1vqIhxXUW7Dc/edit?gid=1795055950#gid=1795055950) · [Publicación en X](https://x.com/CartagenaTCG/status/2023071236985627096)

## Qué resuelve

Después de probar varios mazos, un porcentaje global puede ocultar contra qué rivales se concentran las derrotas o cuánto se ha jugado cada enfrentamiento. El dashboard convierte un registro manual en indicadores para decidir qué probar en la próxima sesión. También deja anotar cambios en la lista y observaciones de juego para recuperar el contexto de un resultado.

## Del registro al dashboard

Cada pestaña de mazo contiene una tabla donde **una fila representa un encuentro registrado**. Si se juega una serie BO3, se registra el resultado de la serie en una fila. Los desplegables estandarizan el arquetipo rival, el resultado (`Win`, `Lose`, `Tie`), el tipo de evento, el formato y el turno de salida. También se pueden registrar el estado emocional y cognitivo, el motivo, las cartas destacadas del rival, los cambios de lista y las observaciones del cruce. Cada mazo tiene un campo opcional para enlazar a su lista o colección de listas en Limitless.

| Vista | Qué permite comparar |
| --- | --- |
| **General** | Encuentros y resultados de todos los mazos, rendimiento en BO1 y BO3, y volumen frente a winrate por mazo. |
| **Pestaña de mazo** | Resultados del mazo, rendimiento en BO3, al salir primero o segundo y por estado registrado. |
| **Tabla y gráfico de cruces** | Número de encuentros y winrate frente a cada arquetipo rival. El gráfico combina barras para el volumen y una línea para el rendimiento. |

La hoja **General** agrega los totales de las pestañas de mazo. Excluye la pestaña de ejemplo y la hoja auxiliar. El winrate global se calcula sobre los resultados acumulados, de modo que cada encuentro tiene el mismo peso. Los indicadores BO1 se obtienen restando los recuentos BO3 del total. Completa el campo **Bo1/Bo3** en cada fila para que el reparto por formato sea correcto.

## Cómo se calcula el rendimiento

**Winrate ajustado = (victorias + 0,5 × empates) ÷ (victorias + derrotas + empates) × 100.** Las derrotas aportan cero y los empates se conservan como categoría propia. Por ejemplo, un récord de 2 victorias, 1 derrota y 1 empate da **62,50 %**.

Para un cruce se aplica la misma fórmula a los resultados del rival seleccionado. La columna **Times Played** cuenta las filas con ese arquetipo. Si se deja el resultado en blanco, ese recuento puede ser mayor que el denominador del winrate. Registrar arquetipo, resultado, formato y turno de salida en la misma fila hace comparables los segmentos.

## Ejemplo de lectura

La pestaña **Ejemplo (No eliminar)** trae siete encuentros BO3, con un récord de **5–2–0** y un winrate de **71,43 %**. Los recuentos de la tabla se pueden comprobar en las filas del ejemplo.

| Segmento | Victorias–derrotas–empates | Encuentros | Winrate |
| --- | ---: | ---: | ---: |
| Salir primero | 2–1–0 | 3 | 66,67 % |
| Salir segundo | 3–1–0 | 4 | 75,00 % |
| Contra Dragapult | 2–0–0 | 2 | 100,00 % |
| Contra Gholdengo | 0–1–0 | 1 | 0,00 % |

El 0 % contra Gholdengo sale de un solo encuentro. Sirve para recuperar las notas de esa derrota y elegir qué volver a probar. Los segmentos por turno, rival y estado registrado son descriptivos. Pueden mezclar rivales, eventos o versiones de lista con características distintas.

## Cómo probarlo

1. [Haz una copia de la plantilla](https://docs.google.com/spreadsheets/d/1JdKYZhjCDZcFxOrl1LRJWITnz72az6E1vqIhxXUW7Dc/copy) en tu Google Drive.
2. En **General**, pulsa **Generar Nuevo Mazo** y ponle nombre. Conserva la pestaña **Ejemplo (No eliminar)**.
3. Registra los encuentros en la pestaña del mazo. Consulta su tabla de cruces y vuelve a **General** para comparar tus mazos.

En una copia sin resultados, el winrate global o por formato puede mostrar `#DIV/0!` hasta que existan encuentros en ese segmento. En la versión revisada, la tarjeta **WinRate Mal Mental** muestra un recuento de victorias con formato porcentual. Para ese segmento, comprueba los resultados en el registro antes de interpretar la cifra.

[Guía original de uso y condiciones de la plantilla](https://docs.google.com/document/d/1bmR7WEYsKhC4NITAMi_PNPld1Lm7H7pypwo-6TB_ejo/edit?usp=sharing)

## Autoría

**Juan Cartagena · @CartagenaTCG.** Proyecto de análisis de datos en Google Sheets. Incluye diseño del registro, validación mediante desplegables, métricas segmentadas, agregación por mazo y visualización de resultados.
