# 1. Las instrucciones se publican en una página propia, independientes del asistente

Fecha: 2026-10-20 · Estado: aceptado

## Contexto

Las fichas de la biblioteca digital del grupo ChatGPT-IA-edu se hacían con un
GPT de ChatGPT, «Resumen de documentos para la biblioteca digital», al que
lleva el enlace corto https://ja.cat/resum que aparece al pie de cada ficha.
Juan José de Haro quería pasarlo a Gemini Notebook (el antiguo NotebookLM). El
uso es de cualquier miembro del grupo: cada persona aporta su propio documento.

## Decisión

Las instrucciones se publican en una página del sitio del grupo
(https://chatgpt-ia-edu.github.io/resumen/) que las copia y abre el asistente
que elija cada persona. Las instrucciones están en un único sitio, dentro de
`index.html`, y la página las copia, las descarga y las muestra desde ahí.

Las instrucciones se reescriben para que sirvan en cualquier chat: piden el
documento si todavía no lo hay y no hablan de «fuentes» de un cuaderno.

Toda la ficha sale del archivo que adjunta la persona. El asistente no busca
nada en internet: si solo recibe un enlace o un título, pide el archivo. La
única excepción es la licencia: si el documento no dice nada de ella, puede
consultar la página oficial donde lo publica su autor o su editorial. Así lo
pidió Juan José de Haro el 20-10-2026, después de que en una prueba Claude
buscara el documento en la web y montara la ficha con lo que encontró.

## Alternativas descartadas

- **Cuaderno de Gemini Notebook compartido.** Quien recibe el enlace de un
  cuaderno no puede añadir fuentes, solo consultar las que ya tiene, así que no
  sirve para que cada persona resuma su documento.
- **Gem de Gemini.** Era el equivalente del GPT (gratis, compartible por enlace
  y con archivos propios), pero Google lo retira: desde el 17-11-2026 los Gems
  pasan a ser «skills», que según la prensa son de pago y no están disponibles
  en el Espacio Económico Europeo.
- **Solo el GPT.** Sigue funcionando, pero ata el recurso a una plataforma y a
  una cuenta de ChatGPT.

## Consecuencias

- Sirve con cualquier asistente, también en las instrucciones personalizadas de
  un proyecto, un GPT o un cuaderno de cada persona.
- En los asistentes que no admiten el texto en la dirección hay que pegarlo: un
  paso más que con el GPT.
- Desde la versión 1.0.1, la línea final de cada ficha lleva la dirección de
  esta página en lugar del enlace corto ja.cat/resum, que seguía llevando al
  GPT. Así la ficha remite a la herramienta vigente sin depender del
  acortador.

## Evidencia

- Cuadernos compartidos: ayuda de Google, «Use public notebooks and featured
  notebooks», https://support.google.com/notebooklm/answer/16322204 (los
  lectores pueden seleccionar fuentes, no añadirlas).
- Retirada de los Gems: TechCrunch, 28-09-2026,
  https://techcrunch.com/2026/09/28/google-is-killing-off-geminis-gems-in-favor-of-skills/
  (migración desde el 17-11-2026). Que las skills sean de pago y no estén en el
  EEE procede de prensa y blogs, no de una página de Google: hipótesis
  pendiente de confirmar, aunque no cambia la decisión.

## Riesgos y limitaciones

- Ningún asistente garantiza seguir las instrucciones al pie de la letra: la
  ficha la revisa siempre quien la publica, y la página lo dice.
