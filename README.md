# maratonsc.github.io

Sitio para publicar la **clasificación en vivo** y el estado de los partidos de la maratón de fútbol sala.

## Qué incluye

- `index.html` con tablero responsive.
- `assets/styles.css` con estilos de la marca.
- `data/maratonsc-data.json` como fuente de datos.

## Cómo funciona

La página carga automáticamente `data/maratonsc-data.json` cada 15 segundos (sin recarga completa), calcula la clasificación y muestra:

- Tabla de clasificación (PJ, victorias, empates, derrotas, GF, GC, diferencia y puntos).
- Partidos en curso.
- Últimos partidos finalizados.
- Partidos pendientes.

## Actualizar resultados sin API (modo simple)

1. Abre `data/maratonsc-data.json`.
2. Escribe el marcador de cada encuentro terminado.
3. Cambia `status` a `finished` cuando acabe el partido, o `live` si aún está en progreso.
4. Haz `git add`, `git commit` y `git push`.

Mientras GitHub Pages recompila, la web pública se actualizará con los cambios.

## Prueba local sin API

1. Desde una terminal en el repositorio ejecuta:

```bash
python -m http.server 4000
```

2. Abre `http://localhost:4000`.
3. Modifica `data/maratonsc-data.json` y recarga la página para ver el cambio.

Nota: sin API externa no hay sincronización instantánea entre administradores; el flujo recomendado es editar el JSON y hacer push al repositorio.
