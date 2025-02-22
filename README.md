# appscriptHipervinculoDocs

📌 Generación de Enlaces a Documentos en Google Drive a listarlos en Google Sheets

📂 Descripción

Este script de Google Apps Script permite generar enlaces a documentos de Google Drive y agregarlos en una hoja de cálculo de Google Sheets. A partir de un identificador único en la hoja de cálculo, el script busca el documento correspondiente en una carpeta específica de Google Drive y coloca un enlace con la función HYPERLINK en la columna "PreInforme Doc Link".

📂 Funcionalidades

✔️ Buscar documentos en Google Drive: El script localiza documentos en una carpeta de Drive a partir de un ID.

✔️ Generar enlaces a los documentos: Si el documento es encontrado, se genera un enlace directo a Google Docs.

✔️ Insertar enlaces en la hoja de cálculo: Los enlaces se agregan automáticamente en la columna "PreInforme Doc Link".

✔️ Manejo de errores: Si el documento no se encuentra, se muestra un mensaje en la celda correspondiente.


📂 Uso

✔️ Configurar el ID de la carpeta de destino:

✔️ Reemplazar DESTINATION_FOLDER_ID con el ID de la carpeta de Google Drive donde se almacenan los documentos.


📂 Estructura de la Hoja de Cálculo:

✔️ Debe contener una columna con un identificador único ("ID No.") que coincida con los nombres de los documentos en Google Drive.

✔️ El script busca documentos con el formato ID No..doc dentro de la carpeta de destino.

✔️ Si la columna "PreInforme Doc Link" no existe, se crea automáticamente.


📂 Ejecutar el script:

✔️ Desde el editor de Apps Script, ejecutar la función generateDocLinks().

✔️ Los enlaces a los documentos se insertarán en la hoja de cálculo.


📂 Explicación de Funciones
generateDocLinks()

✔️ Obtiene los valores de la hoja activa y busca la columna "PreInforme Doc Link".

✔️ Si la columna no existe, la agrega automáticamente.
✔️ Itera sobre las filas para buscar el documento correspondiente en Google Drive.

✔️ Si encuentra el documento, genera un enlace con HYPERLINK y lo inserta en la celda correspondiente.
getFileByName(fileName, folderId)

✔️ Busca un archivo por nombre dentro de una carpeta de Google Drive.

✔️ Devuelve el primer archivo encontrado con el nombre exacto.

✔️ Si no encuentra el archivo, devuelve null.


📂 Notas Importantes

✔️ El nombre del archivo en Google Drive debe coincidir exactamente con el "ID No." de la hoja de cálculo, incluyendo la extensión .doc.

✔️ Se debe otorgar permiso al script para acceder a Google Drive y Google Sheets.

✔️ Si los documentos están en una carpeta restringida, el usuario debe tener acceso para poder abrir los enlaces generados.


📂 Autor
María Eugenia Szwedowski
Contacto: +598 91074131
