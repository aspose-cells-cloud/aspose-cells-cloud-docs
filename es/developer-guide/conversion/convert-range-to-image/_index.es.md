---
title: "Convertir rango de Excel a imagen – Aspose.Cells Cloud API"
description: "Convierta un rango específico de un archivo local de Excel a PNG, JPEG, SVG, TIFF o BMP mediante la API REST de Aspose.Cells Cloud – no es necesario cargar el libro completo."
keywords: "Aspose.Cells Cloud, convertir rango a imagen, API de Excel, formatos de imagen, PNG, JPEG, SVG, TIFF, BMP"
slug: convert-range-to-image
api_version: "v4.0"
date: 2026-07-30
---

La llamada lee un archivo de hoja de cálculo local, convierte el rango especificado y devuelve la imagen como un flujo binario.

## Método para convertir rango a imagen

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **Seguridad y autenticación**

Las APIs de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

## Parámetros de solicitud

| Nombre             | Ubicación                        | Tipo    | Obligatorio | Descripción                                                                     |
|--------------------|----------------------------------|---------|-------------|---------------------------------------------------------------------------------|
| **Spreadsheet**    | Datos de formulario (`multipart/form-data`) | Archivo | **Sí**      | El archivo de Excel que se va a procesar.                                       |
| **worksheet**      | Consulta                         | Cadena  | **Sí**      | Nombre de la hoja de cálculo que contiene el rango (por ejemplo, `Hoja1`).      |
| **range**          | Consulta                         | Cadena  | **Sí**      | Área de celdas que se va a convertir, por ejemplo, `A1:C10`.                    |
| **format**         | Consulta                         | Cadena  | **Sí**      | Formato de imagen de salida (`png`, `jpeg`, `svg`, `tiff`, `bmp`).              |
| **printHeadings**  | Consulta                         | Booleano | No         | `true` para incluir encabezados de filas/columnas en la imagen.                 |
| **outPath**        | Consulta                         | Cadena  | No          | Ruta de carpeta para el archivo generado si desea guardarlo en el almacenamiento en la nube. |
| **outStorageName** | Consulta                         | Cadena  | No          | Nombre del servicio de almacenamiento (por ejemplo, `MiAlmacenamiento`).        |
| **fontsLocation**  | Consulta                         | Cadena  | No          | URL o ruta a fuentes personalizadas utilizadas durante la conversión.           |
| **region**         | Consulta                         | Cadena  | No          | Identificador regional (por ejemplo, `es-ES`, `fr-FR`). Afecta el formateo de números y fechas. |
| **password**       | Consulta                         | Cadena  | No          | Contraseña para libros cifrados.                                                 |
| **AutoRowsFit**    | Consulta                         | Booleano | No         | Ajustar automáticamente las filas antes de representar.                         |
| **AutoColumnsFit** | Consulta                         | Booleano | No         | Ajustar automáticamente las columnas antes de representar.                      |

## Respuesta

La API devuelve el archivo HTML convertido como un **flujo binario** (`application/octet-stream`).

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

### Ejemplo de respuesta correcta (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423
```

Guarde el cuerpo de la respuesta en un archivo (por ejemplo, `report.png`) para ver la imagen renderizada en un navegador web.

---

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                      |
|--------|-------------------------|------------------------------------------------------------------|
| 200    | Correcto                | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT inválido o ausente.                                    |
| 413    | Carga útil demasiado grande | El archivo subido excede el límite de tamaño.                 |
| 500    | Error interno del servidor | Error inesperado en el servidor.                               |

## ¿Cómo usar la API Convert Range to Image con SDK?

### Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToImage) describe una API públicamente accesible, lo que permite interactuar directamente mediante REST desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/image?format=png&worksheet=Hoja1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.png"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423
```

{{< /tab >}}

{{< /tabs >}}

## Utilice los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar, ya que oculta los detalles de bajo nivel, permitiéndole convertir un rango de datos en un archivo de imagen con un código mínimo.  
Consulte la lista completa de SDK de Aspose.Cells Cloud en nuestro [repositorio de GitHub](https://github.com/aspose-cells-cloud).

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK. Si la carga desde Gist está bloqueada, puede descargar los ejemplos directamente desde el repositorio.

---