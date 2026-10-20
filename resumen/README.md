# Resumen de documentos

Página de la comunidad ChatGPT-IA-edu para preparar, con el asistente de IA que
cada persona prefiera, la ficha de un documento para la biblioteca digital del
grupo de Telegram: título, referencia APA 7, resumen, palabras clave y licencia,
lista para pegar en Telegram.

Dirección: https://chatgpt-ia-edu.github.io/resumen/ (también https://ja.cat/resum).

## Cómo funciona

Cada botón copia las instrucciones al portapapeles y abre el asistente elegido
en otra pestaña. En los que lo admiten (ChatGPT, Claude, Perplexity y Grok), las
instrucciones van también en la dirección y aparecen ya escritas o se envían
solas; en los demás, se pegan. Después se adjunta el documento, o se pega su
enlace o su texto. El detalle de cada asistente está en el
[ADR 2](docs/adr/0002-abrir-asistentes-con-parametro-q.md).

La página no guarda ni envía nada. Solo recuerda en el navegador el idioma y el
tema elegidos.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La página entera: estilos, textos en cinco idiomas, lista de asistentes y, en el bloque `<script type="text/plain" id="instrucciones">`, las instrucciones para el asistente. Es el único sitio donde están. |
| `CHANGELOG.md` | Notas de cada versión. |
| `docs/adr/` | Registro de decisiones. |
| `LICENSE.txt` | Licencia del código (AGPL v3 o posterior). |
| `LICENSE-CONTENIDOS` | Licencia de los contenidos (CC BY-SA 4.0). |

## Cambiar las instrucciones

Se editan dentro de `index.html`, en el bloque `id="instrucciones"`. Si cambian
mucho de longitud, hay que repetir la prueba del ADR 2, porque la dirección de
los asistentes que las reciben por parámetro crece con ellas.

## Comprobaciones tras cada cambio

1. Cada botón copia las instrucciones (pegar en un editor y ver que llegan
   enteras, hasta la última línea).
2. ChatGPT y Claude se abren con las instrucciones escritas y completas.
3. Perplexity las envía y pide el documento.
4. Gemini, Copilot, Le Chat, Lumo y DeepSeek se abren vacíos y el aviso dice
   que hay que pegar.
5. «Copiar» y «Descargar» funcionan, y «Ver las instrucciones» las muestra.
6. Los cinco idiomas cambian todos los textos y se recuerdan al recargar.
7. El tema sigue al del sistema y el botón lo cambia y lo recuerda.
8. En el móvil, los botones se ven en dos columnas sin desbordar.
9. Firefox y Chrome se comportan igual.

## Créditos

Autor: Juan José de Haro, para la comunidad ChatGPT-IA-edu. Iconos de
[Lucide](https://lucide.dev/) (licencia ISC). Página e instrucciones hechas con
IA (Claude Code, octubre de 2026),
[nivel 4 del MIAE](https://jjdeharo.github.io/miae/?nivel=4). Las traducciones
de la página son automáticas y no las ha revisado un traductor profesional.
