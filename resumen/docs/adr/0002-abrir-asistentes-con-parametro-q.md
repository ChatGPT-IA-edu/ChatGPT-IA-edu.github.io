# 2. Cada botón copia las instrucciones y abre el asistente, con ellas en la dirección si lo admite

Fecha: 2026-10-20 · Estado: aceptado

## Contexto

La página debe abrir el chat que elija cada persona con las instrucciones ya
puestas. Varios asistentes aceptan un texto inicial en la dirección
(`?q=…`), pero no todos, no lo documentan y cada uno reacciona de una manera.
Las instrucciones ocupan unos 7.300 caracteres, unos 11.200 una vez codificados
en la dirección.

## Decisión

Cada botón hace dos cosas en el mismo clic: copia las instrucciones al
portapapeles y abre el asistente en otra pestaña. Si el asistente admite el
parámetro `?q=`, la dirección lleva las instrucciones. Cada asistente tiene uno
de estos modos, que la página muestra en el botón y en el aviso que aparece
después:

| Modo | Asistentes | Qué ve la persona |
|---|---|---|
| `rellena` | ChatGPT, Claude | Las instrucciones escritas en el cuadro, sin enviar |
| `envia` | Perplexity | Las instrucciones se envían al abrir; el asistente pide el documento |
| `confirma` | Grok | El asistente pide confirmar el envío; después pide el documento |
| `pegar` | Gemini, Copilot, Le Chat, Lumo, DeepSeek | El asistente vacío; hay que pegar |

Como la copia se hace siempre, si un asistente deja de admitir el parámetro, o
si en el móvil se abre su aplicación y lo pierde, basta con pegar.

## Alternativas descartadas

- **Solo copiar.** Funciona en todos, pero pierde la comodidad de los que sí
  aceptan el texto en la dirección.
- **Enviar el parámetro también a los no comprobados.** Le Chat y DeepSeek
  piden iniciar sesión y no se pudo ver qué hacen con él; se dejan en `pegar`
  hasta comprobarlo.
- **Incluir Duck.ai.** Admite el parámetro, pero no está claro que lea
  documentos adjuntos; se deja fuera.

## Consecuencias

- Al añadir o cambiar un asistente hay que comprobar su modo a mano y anotarlo
  aquí.
- Claude muestra un aviso de seguridad cuando el chat se rellena desde un
  enlace. Es normal y no impide enviarlo.

## Evidencia

Prueba del 20-10-2026 en Chrome con la sesión de Juan José de Haro, primero con
un texto corto («Responde solo: OK-PRUEBA áñ») y después con las instrucciones
completas desde la propia página:

- ChatGPT (`https://chatgpt.com/?q=`): rellena el cuadro sin enviar; con las
  instrucciones completas llegan los 7.320 caracteres hasta la última línea.
  Probado de principio a fin con la guía de IA del INTEF: ficha correcta salvo
  el enlace final en formato Markdown, que se corrigió en las instrucciones.
- Claude (`https://claude.ai/new?q=`): rellena el cuadro completo, con un aviso
  rojo de seguridad.
- Perplexity (`https://www.perplexity.ai/?q=`): envía el texto al abrir.
- Grok (`https://grok.com/?q=`): pide confirmar el envío (prueba corta; con el
  texto largo no se pudo ver la pestaña).
- Gemini (`https://gemini.google.com/app?q=`), Copilot
  (`https://copilot.microsoft.com/?q=`) y Lumo (`https://lumo.proton.me/?q=`):
  ignoran el parámetro.
- Le Chat y DeepSeek: piden iniciar sesión; no comprobado.
- Duck.ai (`https://duck.ai/?q=`): rellena el cuadro.

## Riesgos y limitaciones

- Ninguno de estos parámetros está documentado oficialmente: pueden cambiar sin
  aviso. La copia al portapapeles cubre ese caso.
- No se ha probado en iPhone ni con las aplicaciones de móvil de cada asistente.

## Validación

Repetir la prueba de la tabla tras cualquier cambio en la lista de asistentes o
en la longitud de las instrucciones.
