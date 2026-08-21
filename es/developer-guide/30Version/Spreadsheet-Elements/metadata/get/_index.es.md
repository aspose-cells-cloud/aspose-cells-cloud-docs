---
title: "Obtener metadatos de archivos de Excel"
second_title: "Documentos"
linktype: "Obtener sin usar almacenamiento"
type: docs
url: /metadata/get/
keywords: "Aspose.Cells, Excel, metadatos, API REST, SDK en la nube"
description: "Recuperar metadatos integrados o personalizados de libros de Excel usando la API REST de Aspose.Cells Cloud. Incluye formato de solicitud, parámetros, código de ejemplo del SDK y manejo de errores."
weight: 23
ArticleTitle: "Obtener metadatos de archivos de Excel - API de Aspose.Cells Cloud"
---

Esta API REST recupera **metadatos** de uno o más archivos de Excel.  
La solicitud debe incluir un encabezado `Authorization: Bearer <access_token>` obtenido mediante el flujo de credenciales de cliente de OAuth 2.0.

**Requisitos previos**: Para llamar a este endpoint, debe tener un token de acceso válido obtenido del endpoint de tokens OAuth 2.0 de Aspose Cloud. Ejemplo de solicitud curl para adquirir un token:

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>"
```

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/get
```

### Parámetro de consulta

| Nombre del parámetro | Tipo   | Descripción                                                                     |
| -------------------- | ------ | ------------------------------------------------------------------------------- |
| type                 | string | `ALL` / `BuiltIn` / `Custom` – especifica qué grupos de metadatos devolver.    |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo      | Descripción                                                     |
| -------------------- | --------- | --------------------------------------------------------------- |
| archivo de Excel     | archivo de datos | El archivo de Excel proporcionado como la primera parte de la solicitud multipart. |

### Respuesta

```json
[
  {
    "Name": "Author",
    "Value": "John Doe",
    "BuiltIn": true,
    "IsReadOnly": false
  },
  {
    "Name": "CustomProp1",
    "Value": "Custom Value",
    "BuiltIn": false,
    "IsReadOnly": false
  }
]
```

| Código | Significado                 | Cuándo                               |
|--------|-----------------------------|--------------------------------------|
| 200    | Correcto                    | Metadatos devueltos.                 |
| 400    | Solicitud incorrecta        | Falta el archivo o la consulta es inválida. |
| 401    | No autorizado               | Token inválido o ausente.             |
| 404    | No encontrado               | El archivo especificado no se encontró. |
| 500    | Error interno del servidor  | Falla inesperada del servidor.        |

La API devuelve estos códigos de estado HTTP estándar junto con un objeto JSON de respuesta de error cuando corresponda.

### Familia de SDK en la nube

El uso de un SDK acelera el desarrollo al manejar los detalles de bajo nivel. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells con varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}
---