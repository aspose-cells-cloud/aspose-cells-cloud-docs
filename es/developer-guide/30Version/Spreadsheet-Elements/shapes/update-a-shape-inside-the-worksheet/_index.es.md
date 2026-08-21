---
title: "Actualizar una forma en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Actualizar"
type: docs
url: /shapes/update/
aliases: [/update-a-shape-inside-the-worksheet/]
keywords: "actualizar forma API de Excel, Aspose.Cells Cloud, actualización de forma de Excel, API REST, SDK, C#, Java, Python, Node.js, Go, Ruby, PHP, Perl, Swift"
description: "Aprenda cómo actualizar una forma en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye el punto de conexión HTTPS, detalles de autenticación, esquema DTO, uso paso a paso, ejemplo de cURL y ejemplos de código SDK para múltiples lenguajes."
ArticleTitle: "Actualizar una forma en una hoja de cálculo de Excel - API de Aspose.Cells Cloud"
weight: 31
---

Esta API REST actualiza una forma en una hoja de cálculo de Excel.

## Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                                   |
| --------------------- | ------- | --------- | --------------------------------------------------------------------------------------------- |
| **name**             | string  | path      | El nombre del archivo del libro.                                                              |
| **sheetName**        | string  | path      | El nombre de la hoja de cálculo que contiene la forma.                                        |
| **shapeindex**       | integer | path      | El índice basado en cero de la forma dentro de la hoja de cálculo.                            |
| **dto**              | object  | body      | El objeto de transferencia de datos de la forma que contiene las propiedades actualizadas (véase el _esquema DTO_ más abajo). |
| **folder**           | string  | query     | La carpeta donde se almacena el libro.                                                        |
| **storageName**      | string  | query     | El nombre del almacenamiento de Aspose Cloud.                                                 |

### Esquema DTO

El objeto `dto` contiene las propiedades que se pueden actualizar. Todos los campos son opcionales, a menos que se indique lo contrario.

| Campo               | Tipo    | Obligatorio | Descripción                                                                         |
| ------------------- | ------- | ----------- | ----------------------------------------------------------------------------------- |
| **Name**            | string  | No          | Nuevo nombre de la forma.                                                           |
| **UpperLeftRow**    | integer | No          | Índice de fila de la esquina superior izquierda de la forma.                       |
| **UpperLeftColumn** | integer | No          | Índice de columna de la esquina superior izquierda de la forma.                    |
| **Width**           | integer | No          | Anchura de la forma (en puntos).                                                    |
| **Height**          | integer | No          | Altura de la forma (en puntos).                                                     |
| **RotationAngle**   | integer | No          | Ángulo de rotación en grados.                                                       |
| **IsHidden**        | boolean | No          | `true` para ocultar la forma.                                                       |
| **IsLocked**        | boolean | No          | `true` para bloquear la forma.                                                      |
| **Font**            | object  | No          | Configuración de fuente (véase la especificación OpenAPI para subpropiedades).     |
| **...**             | …       | No          | Propiedades adicionales, como `HtmlText`, `AlternativeText`, `ZOrderPosition`, etc. |

> Para obtener una lista completa, consulte la especificación oficial de OpenAPI: <https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape>.

### Encabezados de la solicitud

- `Content-Type: application/json`
- `Accept: application/json`
- `Authorization: Bearer <accessToken>` _(el token JWT del paso de _autenticación_)_

### Cuerpo de la solicitud (ejemplo)

```json
{
  "Name": "MiForma",
  "UpperLeftRow": 2,
  "UpperLeftColumn": 3,
  "Width": 150,
  "Height": 80,
  "RotationAngle": 0,
  "IsHidden": false,
  "IsLocked": false,
  "Font": {
    "Name": "Calibri",
    "Size": 12,
    "IsBold": true,
    "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }
  }
}
```

## Ejemplo con cURL (herramienta de línea de comandos)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <accessToken>" \
  -d '{
        "Name": "FormaActualizada",
        "UpperLeftRow": 1,
        "UpperLeftColumn": 1,
        "Width": 120,
        "Height": 60,
        "IsHidden": false,
        "IsLocked": false
      }'
```

### Respuesta

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Manejo de errores**: la API puede devolver los siguientes códigos de estado:

| Código | Significado             | Causa típica                                        |
| ------ | ----------------------- | --------------------------------------------------- |
| 400    | Solicitud incorrecta    | JSON inválido o campos obligatorios ausentes.       |
| 401    | No autorizado           | Token JWT ausente o inválido.                       |
| 404    | No encontrado           | El libro, la hoja de cálculo o el índice de forma no existen. |
| 500    | Error interno del servidor | Problema inesperado del lado del servidor.        |

**Ejemplos de respuestas de error**

*400 – Solicitud incorrecta*

```json
{
  "Code": 400,
  "Message": "Payload de solicitud inválido. El campo 'Name' excede la longitud máxima."
}
```

*401 – No autorizado*

```json
{
  "Code": 401,
  "Message": "Fallo en la autenticación. Token JWT inválido o caducado."
}
```

*404 – No encontrado*

```json
{
  "Code": 404,
  "Message": "No se encontró el libro, la hoja de cálculo o el índice de forma especificados."
}
```

*500 – Error interno del servidor*

```json
{
  "Code": 500,
  "Message": "Ocurrió un error inesperado en el servidor."
}
```

## Familia de SDK en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que usted se enfoque en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante distintos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}