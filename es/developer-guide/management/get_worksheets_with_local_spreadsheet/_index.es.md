---
title: "Obtener hojas de cálculo con hoja de cálculo local"
ArticleTitle: "Obtener hojas de cálculo con hoja de cálculo local – Aspose.Cells Cloud"
second_title: "Documentos"
linktype: "Obtener hojas de cálculo con hoja de cálculo local"
type: docs
url: /cells/spreadsheet/worksheets
aliases: []
keywords: "Aspose.Cells, hojas de cálculo, hoja de cálculo local, API"
description: "Obtiene una lista completa de las hojas de cálculo de la hoja de cálculo local activa actualmente."
weight: 1000
---

## El método Get Worksheets With Local Spreadsheet de los servicios web de Aspose.Cells Cloud

Este endpoint accede a la aplicación de hoja de cálculo local (por ejemplo, Excel) mediante interoperabilidad o una API local, recopila el nombre y tipo (por ejemplo, estándar, gráfico, macro) de cada hoja de cálculo, y devuelve la colección como una matriz JSON estructurada. Normalmente se utiliza para rellenar una interfaz de usuario de selección de hojas de cálculo o para auditar el contenido de la hoja de cálculo.

### Endpoint de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción |
|----------------------|--------|-----------------------------------------|-------------|
| Spreadsheet          | Archivo | FormData (Cuerpo HTTP)                 | Subir archivo de hoja de cálculo. |
| region               | Cadena | Consulta                                | Configuración de región/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. *(opcional)* |
| password             | Cadena | Consulta                                | Contraseña para abrir el archivo de hoja de cálculo. *(opcional)* |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo   | Descripción |
|----------------------|--------|-------------|
| Spreadsheet          | Archivo | Subir archivo de hoja de cálculo. |

### **Respuesta**

```json
{
  "Worksheets": [
    {
      "Name": "Hoja1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Gráfico1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... hojas de cálculo adicionales
  ]
}
```

**Códigos de estado de respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | OK | La lista de hojas de cálculo se recuperó correctamente. |
| 400 | Solicitud incorrecta | Solicitud inválida (por ejemplo, URL con formato incorrecto o datos obligatorios ausentes). |
| 401 | No autorizado | La autenticación falló o no se proporcionaron credenciales. |
| 404 | No encontrado | El archivo de origen no es accesible. |
| 413 | Carga demasiado grande | El archivo subido excede el límite de tamaño permitido. |
| 500 | Error interno del servidor | La hoja de cálculo ha experimentado una anomalias al obtener los datos. |

## Cómo utilizar Get Worksheets With Local Spreadsheet con SDK

### Especificación de Get Worksheets With Local Spreadsheet

La [Especificación de la API Get Worksheets With Local Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetWorksheetsWithLocalSpreadsheet) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells Cloud. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets?region=es-ES&password=contraseña" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <token jwt>" \
  -F 'Spreadsheet=@ejemplo.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Hoja1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Gráfico1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... hojas de cálculo adicionales
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells Cloud mediante diversos SDK:
`[TBD]`
---