# juego-poliedros

Repositorio con dos aplicaciones web independientes (cada una es un único archivo HTML, sin instalación).

## 🧊 Aventura Geométrica — `index.html.html`
Juego interactivo de poliedros para 4º de Primaria.

## 📝 Corrector de Exámenes Tipo Test — `corrector-examenes.html`
Corrige automáticamente exámenes tipo test a partir de un **PDF escaneado**, usando la visión de la IA de Claude (`claude-opus-4-8`).

### Cómo funciona
1. **API key**: introduce tu clave de la API de Claude (se guarda solo en tu navegador). Consíguela en [console.anthropic.com](https://console.anthropic.com/).
2. **Plantilla**: sube la plantilla con las respuestas correctas (PDF/imagen) y deja que la IA las extraiga, o escríbelas a mano. Puedes revisar y editar la clave de respuestas.
3. **Examen del alumno**: sube el PDF o las imágenes del examen escaneado.
4. **Criterios**: define puntos por acierto, resta por error o por respuesta en blanco, y la nota máxima.
5. Pulsa **Corregir**: la IA transcribe el examen, detecta las respuestas marcadas y la app señala aciertos/errores y calcula la nota.

El resultado muestra el documento transcrito con cada pregunta marcada como correcta ✓, incorrecta ✗ o en blanco —, junto con la nota final. Se puede **imprimir o guardar como PDF**.

> Uso: ábrelo directamente en el navegador (`corrector-examenes.html`) o publícalo con GitHub Pages. La clave y los documentos se procesan en tu equipo y se envían directamente a la API de Anthropic; nada se guarda en un servidor propio.
>
> Nota: la lectura de escaneos (sobre todo manuscritos) puede contener errores; revisa siempre la corrección.
