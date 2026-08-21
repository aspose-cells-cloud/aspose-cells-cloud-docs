---
title: "UnpivotRange"
ArticleTitle: "UnpivotRange – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "UnpivotRange"
type: docs
url: /es/cells/unpivot/range
aliases: []
keywords: "Aspose.Cells, UnpivotRange, API"
description: "Intercambiar filas y columnas en la hoja de cálculo."
weight: 10
---

## El UnpivotRange de los Servicios Web de Aspose.Cells Cloud

Intercambiar filas y columnas en la hoja de cálculo.

### Punto final de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/range
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                                                     |
|----------------------|--------|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet          | File   | FormData                                | Cargar archivo de hoja de cálculo.                                                                                                                              |
| worksheet            | string | Query                                   | Nombre de la hoja de cálculo.                                                                                                                                   |
| cellArea             | string | Query                                   | Rango de datos especificado.                                                                                                                                    |
| skipEmptyValue       | boolean| Query                                   | Si es `true`, omite los valores vacíos. Valor predeterminado: `true`.                                                                                          |
| outPath              | string | Query                                   | (Opcional) Ruta de carpeta donde se almacena el libro de trabajo. El valor predeterminado es `null`.                                                           |
| outStorageName       | string | Query                                   | Nombre del almacenamiento del archivo de salida.                                                                                                                |
| region               | string | Query                                   | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Influye en el formato de números, análisis de fechas y comportamiento específico de la configuración regional. |
| password             | string | Query                                   | Contraseña para abrir el archivo de hoja de cálculo.                                                                                                            |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción |
|----------------------|------|-------------|
| —                    | —    | —           |

### **Respuesta**

```json
{
  "File": "flujo binario"
}
```

**Códigos de estado de respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200    | OK          | Se devuelve el archivo de hoja de cálculo sin estructura de tabla dinámica. |
| 400    | Solicitud incorrecta | Parámetros de solicitud inválidos. |
| 401    | No autorizado | Falló la autenticación. |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño. |
| 500    | Error interno del servidor | El servidor encontró una condición inesperada. |

## Cómo usar UnpivotRange con SDK

### Especificación de UnpivotRange

La [especificación de la API UnpivotRange](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{UnpivotRange}) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells Cloud. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/range?worksheet=Sheet1&cellArea=A1:C10&skipEmptyValue=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=es-ES&password=yourPassword" -X PUT -H "Content-Type: multipart/form-data" -H "Accept: application/octet-stream" -H "Authorization: Bearer <jwt token>" -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "FileUrl": "https://example.com/output/unpivoted.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Utilizar SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud mediante diversos SDK:
 `[TBD]`
---