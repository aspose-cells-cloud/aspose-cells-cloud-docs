---
title: "Eliminar filas en blanco de hojas de cálculo"
ArticleTitle: "Eliminar filas en blanco de hojas de cálculo – Aspose.Cells Cloud API"
second_title: "Documentos"
linktitle: "Eliminar filas en blanco de hojas de cálculo"
type: docs
url: /cells/remove/blank-rows
aliases: []
keywords: "Aspose.Cells, eliminar filas en blanco, hoja de cálculo, API"
description: "Elimina todas las filas en blanco de un archivo de hoja de cálculo."
weight: 100
---

## El método Eliminar filas en blanco de hojas de cálculo de Aspose.Cells Cloud Web Services

Este método elimina de una hoja de cálculo aquellas filas completamente vacías, es decir, que no contienen datos ni objetos. Recorre todas las hojas e identifica las filas en las que todas las celdas están vacías. La operación se realiza directamente sobre la hoja de cálculo, garantizando que solo se eliminen las filas sin contenido. Esto ayuda a limpiar la hoja de cálculo y eliminar filas en blanco innecesarias, haciendo que los datos sean más organizados y fáciles de gestionar. Se recomienda al usuario realizar una copia de seguridad de la hoja de cálculo antes de ejecutar esta operación, ya que las filas eliminadas no se pueden recuperar.

### Punto final de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/blank-rows
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción |
|----------------------|--------|-----------------------------------------|-------------|
| Spreadsheet          | File   | FormData                                | Cargar archivo de hoja de cálculo. |
| outPath              | String | Query                                   | (Opcional) Ruta de carpeta donde se almacena el libro. El valor predeterminado es null. |
| outStorageName       | String | Query                                   | Nombre del almacenamiento del archivo de salida. |
| region               | String | Query                                   | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | String | Query                                   | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| Spreadsheet          | File | Cargar archivo de hoja de cálculo. |

### **Respuesta**

```json
{
  "ResponseFile": "binary file stream"
}
```

**Códigos de estado de la respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | OK | Se devuelve el archivo de hoja de cálculo procesado con las filas en blanco eliminadas. |
| 400 | Solicitud incorrecta | URL o parámetros de solicitud no válidos. |
| 401 | No autorizado | La autenticación ha fallado o no se proporcionaron credenciales. |
| 404 | No encontrado | El archivo de origen no es accesible. |
| 413 | Carga útil demasiado grande | El tamaño de la carga útil de la solicitud excede el límite permitido. |
| 500 | Error interno del servidor | La hoja de cálculo ha encontrado una anomalia al obtener los datos. |

## Cómo usar Eliminar filas en blanco de hojas de cálculo con SDK

### Especificación de Eliminar filas en blanco de hojas de cálculo

La [Especificación de la API Eliminar filas en blanco de hojas de cálculo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankRows) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}
{< tab tabNum="1" >}
```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/remove/blank-rows?outPath=outputFolder&outStorageName=MyStorage&region=es-ES&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "binary file stream"
}
```
{< /tab >}
{< /tabs >}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud utilizando diversos SDK:
`[TBD]`
---