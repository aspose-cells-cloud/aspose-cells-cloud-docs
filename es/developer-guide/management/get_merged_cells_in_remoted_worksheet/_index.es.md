---
title: "GetMergedCellsInRemotedWorksheet"
ArticleTitle: "Obtener celdas fusionadas en hoja de cálculo remota – Aspose.Cells Cloud API"
second_title: "Documentación"
linktype: "Obtener celdas fusionadas en hoja de cálculo remota"
type: docs
url: /es/cells/mergedcells/get
aliases: []
keywords: "Aspose Cells, Obtener celdas fusionadas, Hoja de cálculo remota, API"
description: "Recupera todas las áreas de celdas fusionadas de una hoja de cálculo remota en un archivo de hoja de cálculo."
weight: 10
---

## El método GetMergedCellsInRemotedWorksheet de los servicios web de Aspose.Cells Cloud

Obtenga todas las áreas de celdas fusionadas de una hoja de cálculo remota.

### Punto de conexión del API web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/mergedcells
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción |
|----------------------|--------|-------------------------------------|-------------|
| name | string | Ruta | Nombre del archivo de hoja de cálculo |
| worksheet | string | Ruta | Nombre de la hoja de cálculo |
| folder | string | Consulta | Ruta en el almacenamiento en la nube del archivo de hoja de cálculo. |
| storageName | string | Consulta | (Opcional) Nombre del almacenamiento si se utiliza un almacenamiento en la nube personalizado. Utiliza el almacenamiento predeterminado si se omite. |
| region | string | Consulta | Configuración regional/lingüística del archivo de hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password | string | Consulta | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| — | — | *Ninguno* |

### **Respuesta**

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

**Códigos de estado de respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | OK | La solicitud se realizó correctamente y se devuelve la lista de áreas de celdas fusionadas. |
| 400 | Solicitud incorrecta | URL no válida o parámetros de solicitud con formato incorrecto. |
| 401 | No autorizado | La autenticación falló o no se proporcionaron credenciales. |
| 413 | Payload demasiado grande | El tamaño del cuerpo de la solicitud excede el límite permitido. |
| 500 | Error interno del servidor | Se produjo una anomalia al obtener los datos del archivo de hoja de cálculo. |

## Cómo usar GetMergedCellsInRemotedWorksheet con SDK

### Especificación de GetMergedCellsInRemotedWorksheet

La [Especificación de la API GetMergedCellsInRemotedWorksheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInRemotedWorksheet) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/Sample.xlsx/worksheets/Sheet1/mergedcells?folder=MyFolder&storageName=MyStorage&region=en-US&password=1234" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

{{< /tab >}}

{{< /tabs >}}

### Uso de los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud mediante diversos SDK:
`[TBD]`
---