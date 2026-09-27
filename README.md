# Emmy Mecedoras Web — paquete auditado

Este repositorio se utilizará como puente entre ChatGPT, GitHub y AI Studio.

## Archivo que debe subirse

Sube a la raíz del repositorio el archivo `emmy-mecedoras-web-auditado.zip` generado por ChatGPT.

SHA-256 esperado:

`f0519650b5d110a9feb60f16098cf70edff59ca8e2028e8046262caad2bb947a`

El paquete fue saneado antes de prepararse para GitHub: `data/db.json` no contiene datos antiguos ni tokens; conserva únicamente una estructura vacía. Firebase debe seguir siendo la fuente de verdad.

## Instrucción para AI Studio

Después de que el ZIP esté en GitHub, clona este repositorio y ejecuta en la terminal:

```bash
unzip -o emmy-mecedoras-web-auditado.zip -d proyecto-auditado
cd proyecto-auditado
npm install
npm run lint
npm run build
```

Usa el contenido extraído como la nueva base del proyecto, conservando las variables de entorno y el proyecto Firebase externo existente. Lee `AUDITORIA_CHATGPT.md` antes de modificar funcionalidades.

Prioridades: persistencia Firestore, imágenes en Firebase Storage, autorización `admins/{UID}`, ningún error silencioso, y todos los botones de eliminar deben persistir correctamente después de recargar.
