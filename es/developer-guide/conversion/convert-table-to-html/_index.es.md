---
title: "Aspose.Cells Cloud – Convertir tabla a HTML"
description: "Convierta rápidamente tablas de Excel a HTML con la API de Aspose.Cells Cloud: segura, que conserva el formato y fácil de integrar."
keywords: "Aspose.Cells, Excel a HTML, convertir tabla a HTML, API en la nube, conversión de hojas de cálculo"
weight: 100
date: 2026-07-30
last_updated: 2026-07-30
version: "v4.0"
url: /convert-table-to-html/
type: docs
---

**Resumen rápido**: Este endpoint lee un libro de Excel local, extrae la **tabla** especificada, la convierte en un archivo **HTML** y devuelve el resultado como un flujo descargable. No es necesario cargar previamente el archivo en el almacenamiento de Aspose Cloud.

## API ConvertTableToHTML

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

### Parámetros de la solicitud

| Nombre             | Ubicación  | Tipo      | Obligatorio | Descripción                                                                                                      |
|--------------------|------------|-----------|-------------|------------------------------------------------------------------------------------------------------------------|
| **Spreadsheet**    | Form‑Data  | `File`    | **Sí**      | El libro de Excel que contiene la tabla que se va a convertir.                                                  |
| **worksheet**      | Query      | `String`  | **Sí**      | Nombre de la hoja de cálculo que contiene la tabla.                                                             |
| **tableName**      | Query      | `String`  | **Sí**      | Nombre exacto de la tabla que se va a convertir.                                                                |
| **outPath**        | Query      | `String`  | No          | Ruta de carpeta en el almacenamiento de Aspose Cloud donde se guardará el archivo HTML (opcional).             |
| **outStorageName** | Query      | `String`  | No          | Nombre del almacenamiento para el archivo de salida (opcional).                                                |
| **fontsLocation**  | Query      | `String`  | No          | Ruta a una carpeta que contiene fuentes personalizadas necesarias para la conversión.                           |
| **region**         | Query      | `String`  | No          | Identificador regional (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato de números y fechas.                  |
| **password**       | Query      | `String`  | No          | Contraseña para abrir un libro protegido.                                                                       |
| **AutoRowsFit**    | Query      | `Boolean` | No          | Ajustar automáticamente todas las filas de la hoja de cálculo (`true`/`false`).                                 |
| **AutoColumnsFit** | Query      | `Boolean` | No          | Ajustar automáticamente todas las columnas de la hoja de cálculo (`true`/`false`).                              |

### **Respuesta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Códigos de estado HTTP**

| Código | Significado           | Descripción                                                          |
|--------|-----------------------|----------------------------------------------------------------------|
| 200    | OK                    | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta  | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado         | Token JWT inválido o ausente.                                        |
| 413    | Carga demasiado grande | El archivo subido supera el límite de tamaño.                       |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                   |

## ¿Cuándo usar la API Convert Table to HTML?

- **Contenido web dinámico**: Inserte tablas de precios, cronogramas o listas de productos directamente en páginas web o CMS.
- **Plantillas de correo electrónico**: Genere fragmentos de HTML para resúmenes de pedidos u otros informes que se muestren de forma coherente en distintos clientes de correo electrónico.
- **Paneles de control y herramientas de informes**: Muestre datos de hojas de cálculo en tiempo real sin cargar el libro completo ni utilizar componentes de cuadrícula pesados.
- **Vistas previas de documentos**: Ofrezca vistas previas rápidas y que conservan el formato de secciones específicas de hojas de cálculo.

## ¿Cómo usar la API Convert Table to HTML con SDK?

### Especificación de la API Convert Table to HTML

La [Especificación de la API Convert Table to HTML](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToHTML) proporciona una interfaz de programación accesible públicamente, lo que permite interactuar directamente con REST desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/html?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
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

Usar los SDK es la forma más rápida de desarrollar, ya que ocultan los detalles de bajo nivel y le permiten convertir datos de tablas de hojas de cálculo en un archivo CSV con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver la lista completa de SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante distintos SDK: