# Mis Líderes: cómo obtener el APK

Esta carpeta es el proyecto de la app Android. GitHub la compila gratis y te da el archivo `.apk`. No necesitas instalar nada en tu computadora.

## 1. Subir el proyecto a GitHub

1. Entra a https://github.com e inicia sesión (o crea una cuenta gratis).
2. Toca **New repository**. Ponle de nombre `mis-lideres-apk`, déjalo en **Public** y toca **Create repository**.
3. Toca **uploading an existing file**. Descomprime el zip y arrastra estos elementos:
   `www` (carpeta), `resources` (carpeta), `package.json` y `capacitor.config.json`.
   Toca **Commit changes**.

## 2. Crear el compilador automático

GitHub no deja subir esta parte arrastrando archivos, así que se crea a mano:

1. En tu repositorio toca **Add file**, luego **Create new file**.
2. En el nombre escribe exactamente: `.github/workflows/build-apk.yml`
   (al escribir cada `/` se crea la carpeta sola).
3. Abre el archivo `build-apk.yml` que viene en el zip, copia todo su contenido y pégalo en el cuadro grande.
4. Toca **Commit changes**.

## 3. Compilar

1. Ve a la pestaña **Actions**. Si GitHub pide permiso para activarlos, acepta.
2. Elige **Construir APK** en la lista de la izquierda y toca **Run workflow**, luego el botón verde.
3. Espera entre 5 y 10 minutos hasta que aparezca una marca verde.

## 4. Descargar y compartir

Cuando termine, tu APK queda en este enlace (cambia `TU-USUARIO` por tu usuario de GitHub):

`https://github.com/TU-USUARIO/mis-lideres-apk/releases/download/apk/MisLideres.apk`

Envía ese enlace a tus líderes por WhatsApp. También puedes bajar el archivo y enviarlo directamente. El repositorio debe ser **Public** para que ellos puedan descargarlo sin cuenta.

## 5. Instalar en cada teléfono Android

1. Descargar el archivo `MisLideres.apk`.
2. Abrirlo. Android pedirá permitir instalar apps de esta fuente (Chrome, WhatsApp o Archivos). Se activa una sola vez.
3. Tocar **Instalar**.

## Cargar una lista desde Excel

1. Abre la app y baja hasta **Cargar lista desde Excel**.
2. Toca **Elegir archivo** y selecciona un archivo `.xlsx` o `.csv` (puedes usar `plantilla-lideres.xlsx`).
3. La app lee el nombre y el teléfono de cada fila y los agrega a la lista. Al terminar te dice cuántos agregó, cuántos estaban repetidos y cuántas filas tenían datos incompletos.

- Reconoce las columnas por su título (Nombre, Líder, Teléfono, Celular, WhatsApp...). Si el archivo no tiene títulos, toma la primera columna como nombre y la segunda como teléfono.
- El teléfono puede ir con o sin 0 inicial, con espacios, guiones o con +58.
- Si el archivo tiene varias hojas, usa las que traen teléfonos.
- Los archivos Excel antiguos (`.xls`) no se pueden leer. Ábrelos en Excel y guárdalos como `.xlsx`.
- **Vaciar lista** borra todos los líderes, y pide confirmar antes de hacerlo.

## Si algo falla

- Si el proceso en **Actions** sale con una X roja, entra a él, copia las últimas líneas del error y envíamelas.
- Cada líder tiene su propia lista, guardada en su teléfono. Si desinstala la app, la pierde.
- Si ya habías subido la versión anterior, reemplaza `www/index.html` en tu repositorio por el nuevo (en GitHub: abre el archivo, toca el lápiz, borra todo, pega el nuevo y **Commit changes**). Se vuelve a compilar solo y el enlace de descarga sigue igual. Tus líderes instalan el APK nuevo encima del anterior y conservan su lista.
