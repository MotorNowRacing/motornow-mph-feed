# MotorNow MP-H Elite Series — feed público

Feed oficial de trabajo para WordPress MotorNow, con actualización automática y posibilidad de rectificación posterior.

## Endpoints fijos
- [standings.json](https://raw.githubusercontent.com/MotorNowRacing/motornow-mph-feed/main/standings.json) — pilotos y clasificación de equipos aprobada por el organizador, obtenida sumando los puntos de sus pilotos.
- [races.json](https://raw.githubusercontent.com/MotorNowRacing/motornow-mph-feed/main/races.json) — historial, puntos, vueltas y tiempos, preservando cada carrera.
- [latest.json](https://raw.githubusercontent.com/MotorNowRacing/motornow-mph-feed/main/latest.json) — última carrera archivada.
- [calendar.json](https://raw.githubusercontent.com/MotorNowRacing/motornow-mph-feed/main/calendar.json) — calendario confirmado y horarios virtuales.

## Política de actualización
Los datos provienen de `MotorNowRacing/motornow-stats` (privado). El workflow `.github/workflows/mph-public-feed.yml` reconstruye el feed después de recibir nuevas carreras archivadas y cada miércoles, con seguridad para los pushes hechos desde GitHub Actions.

El organizador ha autorizado la publicación automática sobre los mismos archivos. Si hay sanciones u otras rectificaciones, se corrige la carrera original o el registro privado `data/wordpress/mph-corrections.json` y se vuelve a generar la clasificación. El historial de Git permite identificar cada revisión.

**Equipos:** Dani Martínez y Hugo Gómez compiten juntos en **MNTeam**. El campeonato de equipos se computa sumando los puntos de sus integrantes.

**Nota:** la publicación automática depende de que el resultado ya esté archivado en el repositorio privado. Las carreras de ensayo, ficheros inválidos y duplicados se bloquean. La pole puede inferirse provisionalmente del P1 de parrilla cuando falte un dato explícito, y corregirse después.

Este feed no contiene contraseñas, tokens ni otras credenciales.
