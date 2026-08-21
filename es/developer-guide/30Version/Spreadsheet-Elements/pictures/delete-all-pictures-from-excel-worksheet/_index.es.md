---
title: "Eliminar todas las imágenes de una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Borrar"
type: docs
url: /pictures/clear/
aliases: [/delete-all-pictures-from-excel-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, eliminar todas las imágenes, hoja de cálculo, API REST, borrar imágenes"
description: "Aprenda a eliminar todas las imágenes de una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud con ejemplos de cURL y SDK."
weight: 60
ArticleTitle: "Cómo eliminar todas las imágenes de una hoja de cálculo de Excel con Aspose.Cells Cloud"
---

Esta API REST elimina **todas** las imágenes de una hoja de cálculo.

**Requisitos previos**  
- Una cuenta activa de Aspose.Cells Cloud con un token de acceso OAuth 2.0 válido.  
- Se requiere la versión 3.0 (o posterior) de la API; las versiones anteriores están obsoletas.  
- El archivo de Excel de destino debe estar almacenado en una ubicación de almacenamiento admitida (predeterminada o personalizada).

**Compatibilidad de versiones**  
El endpoint sigue la especificación de la API Cells Cloud 3.0. Asegúrese de que sus bibliotecas cliente y las URL de solicitud apunten a `api.aspose.cloud/v3.0`.

## DeleteWorksheetPictures API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                    |
| -------------------- | ------ | --------- | ---------------------------------------------- |
| name                 | string | Path      | Nombre del archivo de Excel.                   |
| sheetName            | string | Path      | Nombre de la hoja de cálculo que contiene imágenes. |
| folder               | string | Query     | Carpeta donde se almacena el archivo.          |
| storageName          | string | Query     | Nombre del servicio de almacenamiento.         |

### Respuestas de error

| Código HTTP | Descripción                                                                   |
| ----------- | ----------------------------------------------------------------------------- |
| 401         | No autorizado: token ausente o no válido.                                     |
| 404         | No encontrado: el archivo, hoja de cálculo o índice de salto de página especificado no existe. |
| 400         | Solicitud incorrecta: sintaxis de solicitud mal formada o parámetros no válidos. |
| 500         | Error interno del servidor: se encontró una condición inesperada.             |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/DeleteWorksheetPictures) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/pictures" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK gestiona los detalles de bajo nivel, para que usted pueda centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPictures.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPictures.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPictures.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPictures.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPictures.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPictures.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPictures.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPictures.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Notas:** La operación DELETE no admite paginación y está sujeta a los límites estándar de tasa de la API de Aspose.Cells Cloud (100 solicitudes por minuto por defecto). Ajuste la lógica de su cliente en consecuencia.

**Consulte también**:  
- [/pictures/delete/](../delete/) – Eliminar una imagen específica de una hoja de cálculo.  
- [/pictures/add/](../add/) – Agregar una imagen a una hoja de cálculo.  
---