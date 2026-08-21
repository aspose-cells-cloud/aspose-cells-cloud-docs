---
title: "Convertir hoja de cálculo a PDF, PNG, CSV y más: API en la nube Aspose.Cells"
second_title: "Documento"
linktitle: "Convertir hoja de cálculo"
type: docs
url: /worksheets/conversion/
aliases:
  - /convert-worksheet-to-image/
  - /worksheets/to-image/
keywords: "Aspose.Cells, conversión de hoja de cálculo, API REST, cURL, SDK, PDF, PNG, CSV"
description: "Aprenda a convertir una única hoja de cálculo de un libro de Excel a PDF, PNG, CSV y más de 15 formatos más utilizando la API REST de Aspose.Cells Cloud. Incluye un ejemplo de cURL, fragmentos de SDK y una referencia completa de parámetros."
weight: 130
ArticleTitle: "Convertir hoja de cálculo a PDF, PNG, CSV y más: API en la nube Aspose.Cells"
---

**API de conversión de hojas de cálculo**: El punto final `GET /cells/{name}/worksheets/{sheetName}` convierte una única hoja de cálculo (una hoja dentro de un libro de Excel) a otro tipo de archivo.

> **Prerrequisito:** Debe tener un token JWT válido y el libro almacenado en una ubicación de almacenamiento compatible con Aspose Cloud antes de invocar este punto final.

Formatos **importables** admitidos (la hoja de cálculo puede leerse desde):

- XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT

Formatos **solo de exportación** admitidos (la hoja de cálculo puede guardarse como):

- PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS

## API REST

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) describe la interfaz accesible públicamente.

### **Parámetros de solicitud**

| Parámetro                | Tipo    | Obligatorio | Valor predeterminado | Valores permitidos                                                      | Descripción                                       |
| ------------------------ | ------- | ----------- | -------------------- | ----------------------------------------------------------------------- | ------------------------------------------------- |
| **format**               | string  | Sí          | –                    | pdf, png, jpeg, bmp, svg, tiff, emf, csv, txt, … (ver lista admitida)   | Formato de salida deseado.                        |
| **verticalResolution**   | integer | No          | 96                   | 72‑600                                                                  | Resolución vertical (DPI) para la salida de imagen. |
| **horizontalResolution** | integer | No          | 96                   | 72‑600                                                                  | Resolución horizontal (DPI) para la salida de imagen. |
| **password**             | string  | No          | –                    | –                                                                       | Contraseña para abrir un libro protegido.         |
| **folder**               | string  | No          | –                    | –                                                                       | Carpeta en la nube donde se almacena el libro origen. |
| **storage**              | string  | No          | –                    | –                                                                       | Nombre del almacenamiento (por ejemplo, “Default”). |

### Respuesta

| Código de estado | Descripción                                                            | Tipo devuelto              |
| ---------------- | ---------------------------------------------------------------------- | -------------------------- |
| **200**          | Conversión exitosa; se devuelve una secuencia binaria del archivo convertido. | `application/octet-stream` |
| **400**          | Solicitud incorrecta: faltan parámetros o estos son inválidos.         | Objeto JSON de error       |
| **401**          | No autorizado: token JWT inválido o ausente.                           | Objeto JSON de error       |
| **404**          | No encontrado: el libro o la hoja de cálculo no existen.              | Objeto JSON de error       |
| **500**          | Error interno del servidor: fallo inesperado.                          | Objeto JSON de error       |

#### Ejemplo de solicitud (cURL)

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=png&verticalResolution=96&horizontalResolution=96" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### Ejemplo de respuesta

```
Imagen convertida (secuencia binaria)
```

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK maneja los detalles de bajo nivel para que usted pueda centrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
---