---
title: "ConvertWorksheetToPdf"
ArticleTitle: "Convertir hoja de cálculo a PDF – API de Aspose.Cells Cloud"
second_title: "Document"
linktitle: "ConvertWorksheetToPdf"
type: docs
url: /es/cells/convert/worksheet/pdf
aliases: []
keywords: "Aspose.Cells, Convertir hoja de cálculo a PDF, API"
description: "Convierte una hoja de cálculo de un archivo de hoja de cálculo a PDF mediante Aspose.Cells Cloud."
weight: 10
---

## ConvertWorksheetToPdf de los servicios web de Aspose.Cells Cloud

Este método lee un archivo de hoja de cálculo desde el sistema de archivos local, convierte su hoja en un archivo PDF y devuelve el resultado convertido. Debe especificarse correctamente la ruta del archivo de origen y el formato de destino. Asegúrese de que existan los permisos necesarios para leer el archivo de origen y escribir el archivo convertido, si corresponde. El proceso de conversión se realiza completamente en el servidor en la nube, eliminando la necesidad de almacenamiento en la nube o descargas externas.

Las características clave incluyen conversión nativa en la nube, reducción de la carga de recursos en la nube y un flujo de trabajo simplificado.

### Punto de conexión de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                            |
|----------------------|---------|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet          | File    | FormData                                | Cargar archivo de hoja de cálculo.                                                                                                     |
| worksheet            | String  | Query                                   | Nombre de la hoja de cálculo.                                                                                                          |
| outPath              | String  | Query                                   | (Opcional) Ruta de la carpeta donde se almacena el libro. El valor predeterminado es null.                                            |
| outStorageName       | String  | Query                                   | Nombre del almacenamiento para el archivo de salida.                                                                                   |
| fontsLocation        | String  | Query                                   | Usar fuentes personalizadas.                                                                                                           |
| AutoRowsFit          | Boolean | Query                                   | (Opcional) Ajusta automáticamente todas las filas en las hojas de cálculo.                                                            |
| AutoColumnsFit       | Boolean | Query                                   | (Opcional) Ajusta automáticamente todas las columnas en las hojas de cálculo.                                                         |
| region               | String  | Query                                   | Configuración de región/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Influye en el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | String  | Query                                   | Contraseña para abrir el archivo de hoja de cálculo.                                                                                   |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| [TBD]                |      |             |

### **Respuesta**

```json
{
  "file": "<flujo binario del PDF generado>"
}
```

**Códigos de estado de respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | OK | La hoja se convirtió correctamente a PDF y se devolvió como un flujo de archivos. |
| 400 | Solicitud incorrecta | Parámetros de solicitud inválidos o URL con formato incorrecto. |
| 401 | No autorizado | La autenticación falló o no se proporcionaron credenciales. |
| 404 | No encontrado | El archivo de origen no es accesible. |
| 413 | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño permitido. |
| 500 | Error interno del servidor | El archivo de hoja de cálculo encontró una anomalias durante la conversión. |

## Cómo usar ConvertWorksheetToPdf con SDK

### Especificación de ConvertWorksheetToPdf

La [Especificación de la API ConvertWorksheetToPdf](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#Conversion/ConvertWorksheetToPdf) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Usar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf?worksheet=Hoja1&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&AutoRowsFit=true&AutoColumnsFit=true&region=es-ES&password=SecretPwd" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <token JWT>" \
  -F "Spreadsheet=@ejemplo.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<flujo binario del PDF generado>"
}
```

{< /tab >}

{< /tabs >}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud mediante varios SDK:
`[TBD]`
---