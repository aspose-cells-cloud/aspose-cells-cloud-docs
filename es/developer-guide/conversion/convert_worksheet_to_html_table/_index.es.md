---
title: "Convertir hoja de cálculo a tabla HTML"
ArticleTitle: "Convertir hoja de cálculo a tabla HTML – Aspose.Cells Cloud API"
second_title: "Documentos"
linktype: "ConvertWorksheetToHtmlTable"
type: docs
url: /es/cells/convert/worksheet/html-table
aliases: []
keywords: "Aspose.Cells, ConvertWorksheetToHtmlTable, tabla HTML, API"
description: "Convierte una hoja de cálculo de un archivo en una unidad local en un archivo de tabla HTML utilizando Aspose.Cells Cloud."
weight: 100
---

## La operación Convertir hoja de cálculo a tabla HTML de los servicios web de Aspose.Cells Cloud

Esta operación lee un archivo de hoja de cálculo desde el sistema de archivos local, convierte su hoja especificada en una tabla HTML y devuelve el resultado convertido como un flujo de archivos. La conversión se realiza íntegramente en el servidor en la nube, por lo que no es necesario subir previamente archivos al almacenamiento en la nube. Admite configuraciones regionales y libros protegidos con contraseña.

### Punto de conexión de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción |
|----------------------|--------|-----------------------------------------|-------------|
| Spreadsheet          | File   | FormData                                | Cargar archivo de hoja de cálculo. |
| worksheet            | String | Query                                   | Nombre de la hoja de cálculo. (obligatorio) |
| region               | String | Query                                   | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | String | Query                                   | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| *Ninguno*            | *Ninguno* | *No se requiere cuerpo JSON; el archivo se envía como multipart/form-data.* |

### **Respuesta**

```json
{
  "File": "flujo binario de la tabla HTML generada"
}
```

**Códigos de estado de respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | Correcto | La hoja de cálculo se convirtió correctamente en una tabla HTML y se devolvió como un flujo de archivos. |
| 400 | Solicitud incorrecta | URL de solicitud no válida o parámetros obligatorios ausentes. |
| 401 | No autorizado | La autenticación falló o no se proporcionaron credenciales. |
| 404 | No encontrado | El archivo de origen no es accesible. |
| 500 | Error interno del servidor | Se produjo una anomalia en la hoja de cálculo al obtener los datos de conversión. |
| 413 | Payload demasiado grande | El archivo cargado supera el límite de tamaño permitido. |

## Cómo usar la operación Convertir hoja de cálculo a tabla HTML con SDK

### Especificación de Convertir hoja de cálculo a tabla HTML

La [Especificación de la API Convertir hoja de cálculo a tabla HTML](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtmlTable) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Utilice HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table?worksheet={worksheet}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "flujo binario de la tabla HTML generada"
}
```

{< /tab >}

{< /tabs >}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para ver la lista completa de SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells Cloud utilizando diversos SDK:
`[TBD]`
---