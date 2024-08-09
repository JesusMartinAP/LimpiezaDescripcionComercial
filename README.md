# LimpiezaDescripcionComercial
Marathon

### Resumen del Script

Este script automatiza varias tareas de limpieza, validación y procesamiento de datos en un archivo Excel, asegurando que los datos cumplan con ciertos requisitos específicos. A continuación, se detalla lo que realiza el script:

1. **Carga del Archivo Excel**:
   - Permite al usuario subir un archivo Excel con extensión `.xlsx` o `.xls`.
   - El archivo se lee en un DataFrame para su posterior procesamiento.

2. **Limpieza de Texto**:
   - Elimina caracteres no deseados como comillas simples y dobles, así como símbolos de marca registrada y de marca comercial de las columnas "Descripción comercial" y "Nombre Comercial".

3. **Validación de Capitalización**:
   - Asegura que solo la primera letra en la columna "Recomendaciones de uso" esté en mayúscula.
   - Registra en una nueva columna si el texto cumple o no con este criterio.

4. **Validación de la Estructura HTML**:
   - Valida que el HTML en la columna "Descripción comercial" siga la estructura requerida:
     - Debe empezar con una etiqueta `<h3>` cuyo contenido coincida con el "Nombre Comercial".
     - Debe incluir al menos un párrafo `<p>`.
     - Debe contener un segundo `<h3>` con el texto "Beneficios del producto".
     - Debe contar con al menos una lista `<ul>`.

5. **Registro de Validaciones**:
   - Se crea una columna "Validación" que registra cualquier problema encontrado con caracteres no deseados en las columnas "Descripción comercial" y "Nombre Comercial".
   - La columna "Validación" también registra si la capitalización de "Recomendaciones de uso" es incorrecta.

6. **Guardado del Archivo Modificado**:
   - El DataFrame procesado se guarda en un nuevo archivo Excel, que se descarga automáticamente al final de la ejecución del script.

Este script es útil para asegurar la coherencia y calidad de los datos antes de utilizarlos en una tienda en línea u otro entorno donde la precisión del contenido es crucial.
