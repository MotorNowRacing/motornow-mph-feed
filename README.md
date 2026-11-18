# MotorNow MP-H Elite Series — feed público

Datos destinados a los widgets de resultados y clasificación de la página MP-H de MotorNow.

## Endpoints estables
- [standings.json](https://raw.githubusercontent.com/MotorNowRacing/motornow-mph-feed/main/standings.json)
- [races.json](https://raw.githubusercontent.com/MotorNowRacing/motornow-mph-feed/main/races.json)
- [latest.json](https://raw.githubusercontent.com/MotorNowRacing/motornow-mph-feed/main/latest.json)

**Estado actual: estructura creada, sin contenido aprobado para publicación.** Los JSON llevan `publishable: false` y listas vacías; WordPress no debe tratarlos como clasificación oficial. El plugin local de clasificación exige un snapshot validado (`status: ARCHIVED_SNAPSHOT`) y seguirá recurriendo a su copia local mientras no reciba un feed compatible.

## Seguridad y flujo de trabajo
Los datos se procesan en `MotorNowRacing/motornow-stats` (privado), y aquí solo llegan conjuntos revisados para la web. Ningún token, contraseña, clave, credencial, imagen original no autorizada ni fuente de trabajo privada debe copiarse a este repositorio.

El futuro proceso de sincronización deberá reemplazar los mismos archivos en `main` cuando exista aprobación editorial; `races.json` conserva el historial sin duplicar IDs de sesión. Los PNG/SVG solo se harán públicos tras aprobación.

El repositorio público es el punto de lectura, **no** la fuente de autoridad del campeonato.
