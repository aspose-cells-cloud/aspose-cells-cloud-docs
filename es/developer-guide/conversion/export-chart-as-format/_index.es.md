---
title: "Exportar gráfico de Excel – API de Aspose.Cells Cloud"
second_title: "Documentación"
description: "Convierta un gráfico de un libro de Excel almacenado en la nube a PDF, PNG, SVG u otros formatos con una única llamada REST."
ArticleTitle: "Cómo convertir una hoja de cálculo local en un archivo PDF: guía paso a paso"
linktitle: "Convertir hoja en PDF"
type: docs
url: /export-chart-as-format/
keywords: "Aspose.Cells Cloud, exportar gráfico, API, PDF, PNG, SVG, Excel, REST, conversión en la nube"
weight: 100
---

Convierta un gráfico que se encuentra en un libro almacenado en el almacenamiento de Aspose Cloud a un formato de archivo distinto (PDF, PNG, SVG, …) sin descargar el archivo fuente.

## API ExportChartAsFormat

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### 📦 Parámetros de solicitud

| Nombre             | Tipo    | Ubicación | Obligatorio | Descripción                                                    |
| ------------------ | ------- | --------- | ----------- | -------------------------------------------------------------- |
| **name**           | string  | Ruta      | Sí          | Nombre del archivo del libro.                                  |
| **worksheet**      | string  | Ruta      | Sí          | Nombre de la hoja de cálculo que contiene el gráfico.         |
| **chartIndex**     | integer | Ruta      | Sí          | Índice de base cero del gráfico que se va a exportar.          |
| **format**         | string  | Consulta  | Sí          | Formato de salida deseado (por ejemplo, `png`, `pdf`, `svg`). |
| **folder**         | string  | Consulta  | No          | Ruta de carpeta donde se almacena el libro (valor predeterminado: raíz). |
| **storageName**    | string  | Consulta  | No          | Nombre personalizado de almacenamiento; omitir para usar el almacenamiento predeterminado. |
| **outPath**        | string  | Consulta  | No          | Ruta de carpeta donde se guardará el archivo convertido.       |
| **outStorageName** | string  | Consulta  | No          | Nombre del almacenamiento para el archivo de salida.           |
| **fontsLocation**  | string  | Consulta  | No          | Ruta a una carpeta que contiene fuentes personalizadas.        |
| **region**         | string  | Consulta  | No          | Configuración regional (por ejemplo, `es-ES`, `fr-FR`).        |
| **password**       | string  | Consulta  | No          | Contraseña para abrir un libro protegido.                      |

### **Respuesta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**Códigos de estado HTTP**

| Código | Significado            | Descripción                                                       |
| ------ | ---------------------- | ----------------------------------------------------------------- |
| 200    | Correcto               | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta   | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado          | Token JWT no válido o ausente.                                    |
| 413    | Payload demasiado grande | El archivo cargado excede el límite de tamaño.                 |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                |

## ¿Cómo usar la API Export Chart as Format con SDK?

### Especificación de la API Export Chart as Format

La [Especificación de la API Export Chart as Format](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportChartAsFormat) proporciona una interfaz de programación accesible públicamente y permite interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}?format={format}" \
  -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (codificado en Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nombre de archivo opcional"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Usar un SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel, lo que permite convertir datos de tablas de hojas de cálculo en un archivo PDF con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK: