# Evaluación VCER

Rúbrica VCER: Recomendable (100 %)
Versión evaluada: 1.0.0, commit `8a3d529` de `chatgpt-ia-edu.github.io/resumen/`, 20-10-2026.

Cumple lo esencial de la guía y puede utilizarse o publicarse; las mejoras
propuestas lo completan.

Evaluación hecha con las instrucciones de la guía «Vibe coding responsable»
(https://vibe-coding-educativo.github.io/vibe-responsable/es/vcer.html), después
de corregir lo que señaló una primera evaluación de la misma versión (85 %).

| # | Punto | Nota | Justificación |
|---|---|---|---|
| 1 | Contenido | 2 | Las reglas APA 7, los modelos, los criterios de licencia y los avisos de cada asistente coinciden con lo comprobado; conviene que el autor revise las instrucciones enteras. |
| 2 | Datos personales | 2 | No pide datos ni lleva analítica; solo guarda en el navegador el idioma y el tema (`resumen.idioma` y `resumen.oscuro`). |
| 3 | Entender qué hace | 2 | Copia unas instrucciones fijas y abre el asistente elegido, con ellas en la dirección si lo admite; no guarda nada más ni se comunica con ningún servidor, como declaran los créditos y el README. |
| 4 | Dependencias | 2 | No carga nada de fuera: estilos, textos, iconos e instrucciones van en el HTML. Las direcciones externas son destinos que abre la persona (los nueve asistentes, Telegram, las licencias, el MIAE, Lucide y la página VCER). Sin internet funciona entera; solo fallan los asistentes y los enlaces. |
| 5 | Accesibilidad | 2 | axe-core (WCAG 2.2 AA y buenas prácticas) sin infracciones en tema claro y oscuro, también con el aviso, las instrucciones desplegadas y los créditos abiertos; recorrido con el tabulador en orden lógico y con el foco visible; Enter, Escape y vuelta del foco correctos; sin desbordamiento a 320 px. |
| 6 | Material ajeno | 2 | Seis iconos de Lucide (luna, sol, copiar, descargar, enlace externo y cerrar), con licencia ISC, acreditados con enlace en los créditos y en el README; el favicon es el de la web del grupo. |
| 7 | Rastro | 2 | Dos ADR con contexto, alternativas descartadas, evidencia, riesgos y validación. |
| 8 | Uso de IA | 2 | El pie indica la herramienta, la fecha, el nivel 4 del MIAE, el papel del autor y que se ha probado con documentos reales en ChatGPT y Claude. |
| 9 | Licencia | 2 | Autoría y licencias (CC BY-SA 4.0 y AGPL-3.0) a la vista en el pie, con enlace, y `LICENSE.txt` y `LICENSE-CONTENIDOS` en la carpeta. |
| 10 | Reutilización | 2 | Código sin comprimir y comentado; el README explica los archivos, cómo cambiar las instrucciones y qué comprobar tras cada cambio. |

Se probó también en Chromium, Firefox y WebKit, en escritorio, móvil y tableta,
con tema claro y oscuro, sin errores; y una prueba automática de los botones, el
portapapeles, el idioma, el tema y la descarga.

## Mejoras pendientes

1. Comprobar Grok con las instrucciones completas: el aviso «Se envían al
   confirmar» se basa en una prueba con un texto corto.
2. Probar Le Chat y DeepSeek con sesión iniciada, por si admiten el texto en la
   dirección.
3. Probar la página en un iPhone.
