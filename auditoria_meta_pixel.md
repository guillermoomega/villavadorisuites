# Auditoría Meta Pixel — Gran Vadori + Villa Vadori Suites

## Prompt para Claude Code (correr en cada repo por separado)

### Repo villavadorisuites.ar
> Buscá en todos los archivos .html del repo las apariciones del Meta Pixel ID `862026866969490` (buscá tanto el snippet base de `fbevents.js` como el número de ID). Como el sitio es un one-pager, debería aparecer una sola vez en el `<head>` de la única página. Confirmame que está presente y en qué archivo.

### Repo Gran Vadori (granvadori.com.ar)
> Buscá en todos los archivos .html del repo (al menos `index.html` y `carta.html`) las apariciones del Meta Pixel — tanto el snippet base de `fbevents.js` como cualquier ID de pixel asociado a Gran Vadori. Decime en qué archivos está presente y en cuáles falta. Si falta en alguno, agregá el mismo snippet completo (incluyendo el `<noscript>` del final) en el `<head>`, idéntico al que ya está en el archivo donde sí funciona — no inventes un ID nuevo, copiá el existente.

## Qué revisar además (manual, 5 min)

1. **Meta Events Manager → Test Events:** abrí cada URL de cada sitio con esa pestaña abierta y confirmá que dispara el evento `PageView`.
2. **Extensión "Meta Pixel Helper" (Chrome):** instalarla y navegar página por página — te marca en el momento si el pixel está presente y activo, y si hay errores (ej. pixel duplicado, ID incorrecto).
3. Si Gran Vadori usa un Pixel ID distinto al de VVS, confirmar cuál es el correcto para cada negocio antes de que Claude Code copie el snippet — no asumir que es el mismo `862026866969490` de VVS.
