---
title: "Establecer estilo de rango – API de Aspose.Cells Cloud"
second_title: "Documentación"
linktitle: "Establecer estilo de rango"
type: docs
url: /ranges/update/style/
aliases: [/set-the-style-of-the-range/]
keywords: "Aspose.Cells, estilo de rango, API, Excel, nube"
description: "Aprenda cómo establecer el estilo de un rango de celdas en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye pasos de autenticación, formato de solicitud, detalles de respuesta y ejemplos de SDK para .NET, Java, Python, Go y más."
weight: 70
---

## **Introducción**
Este ejemplo demuestra cómo establecer el estilo de un rango utilizando la API de Aspose.Cells Cloud. Puede invocar la API desde muchos lenguajes de programación, como .NET, Java, PHP, Ruby, Python, JavaScript (jQuery) y otros.

## **Información de la API**

| API                                                   | Tipo | Descripción                              | Enlace al recurso                                                                                                                                 |
| ----------------------------------------------------- | ---- | ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| /cells/{name}/worksheets/{sheetName}/ranges/style     | POST | Establece el estilo de celda de un rango con nombre | [PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle) |

### **Ejemplo con cURL**  

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

**Requisitos previos**  
1. Obtenga un token de acceso mediante el flujo de credenciales de cliente OAuth2 (`POST https://api.aspose.cloud/connect/token`).  
2. Incluya el encabezado `Authorization: Bearer <access_token>` en cada solicitud.  

**Solicitud**  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{
           "Range": {
               "FirstRow": 1,
               "FirstColumn": 1,
               "RowCount": 2,
               "ColumnCount": 2,
               "Worksheet": "Sheet1"
           },
           "Style": {
               "Font": {
                   "IsBold": true,
                   "IsItalic": true,
                   "IsStrikeout": true,
                   "IsSubscript": true,
                   "IsSuperscript": true,
                   "DoubleSize": 1
               }
           }
         }'
```

*El objeto `Range` especifica la celda superior izquierda y el tamaño del rango. El objeto `Style` contiene las opciones de formato que se aplicarán.*  

{{< /tab >}}

{{< tab tabNum="2" >}}

**Respuesta**  

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Manejo de errores**: En caso de llamadas no exitosas, la API devuelve un código de estado HTTP apropiado (por ejemplo, 400, 401, 500) junto con un cuerpo JSON que incluye los campos `Error` y `Message`. Inspeccione el valor de `Code`; cualquier resultado distinto de 200 debe registrarse y procesarse según su política de manejo de errores.  

{{< /tab >}}

{{< /tabs >}}

## **Código fuente del SDK**
Los SDK de Aspose.Cells Cloud se pueden descargar desde la siguiente página: [SDK disponibles](/cells/available-sdks/)

### **Ejemplos de SDK**  
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}