# juego-poliedros

Repositorio con dos aplicaciones web independientes (cada una es un único archivo HTML, sin instalación).

## 🧊 Aventura Geométrica — `index.html.html`
Juego interactivo de poliedros para 4º de Primaria.

## 📝 Corrector de Exámenes con IA — `corrector-examenes.html`
Corrige automáticamente exámenes a partir de **PDFs escaneados**, usando la visión de la IA de Claude (`claude-opus-4-8`). Admite preguntas **tipo test** y de **desarrollo/respuesta corta**, **corrección por lotes** (varios alumnos a la vez) y **exportación de notas a CSV**.

### Cómo funciona
1. **API key**: introduce tu clave de la API de Claude (se guarda solo en tu navegador). Consíguela en [console.anthropic.com](https://console.anthropic.com/).
2. **Plantilla / criterios**: sube la plantilla (PDF/imagen) y la IA extrae las preguntas, o configúralas a mano. Cada pregunta puede ser:
   - **Test**: defines la respuesta correcta; la comparación es automática y determinista.
   - **Desarrollo**: defines la respuesta modelo / criterios; la IA valora la respuesta del alumno y otorga puntos parciales con una justificación.
   Cada pregunta tiene su propia puntuación (editable).
3. **Exámenes**: sube uno o varios archivos. Cada archivo (PDF o imagen) es el examen de un alumno; se corrigen en lote.
4. **Puntuación global**: resta por error (test) o por blanco, y nota máxima. La nota = (puntos obtenidos ÷ puntos totales) × nota máxima.
5. Pulsa **Corregir exámenes**.

El resultado incluye:
- **Resumen del lote**: estadísticas del grupo (media, aprobados/suspensos, nota máx./mín.) y la lista de **nombre + nota** de todos los alumnos, con botón para copiarla. Se puede **ordenar** (por orden de corrección, por nota o por nombre) y los **suspensos quedan marcados** en rojo.
- **Detalle de notas**: tabla con el **nombre detectado de cada alumno (editable**, por si la IA lo lee mal) y sus marcadores.
- **Detalle por alumno**: cada pregunta transcrita y marcada como correcta ✓, incorrecta ✗, parcial ◐ o en blanco —.

La IA detecta automáticamente el nombre del alumno desde la cabecera del examen. Puedes **exportar las notas a CSV** (resumen + una columna por pregunta) e **imprimir o guardar como PDF**.

> Uso: ábrelo directamente en el navegador (`corrector-examenes.html`) o publícalo con GitHub Pages. La clave y los documentos se procesan en tu equipo y se envían directamente a la API de Anthropic; nada se guarda en un servidor propio.
>
> Nota: la lectura de escaneos (sobre todo manuscritos) puede contener errores; revisa siempre la corrección.
