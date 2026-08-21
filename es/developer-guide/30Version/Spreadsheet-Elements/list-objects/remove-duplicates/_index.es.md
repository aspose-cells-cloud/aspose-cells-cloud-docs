---
title: "Eliminar filas duplicadas de un ListObject – Documentación de la API en la nube de Aspose.Cells"
second_title: "Documento"
linktitle: "Eliminar duplicados"
type: docs
keywords: "eliminar duplicados, listobject, API en la nube de Aspose.Cells, Excel, REST"
url: /list-objects/remove-duplicates/
description: "Aprenda cómo eliminar filas duplicadas de un ListObject en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye el punto de conexión, parámetros, autenticación y ejemplos de solicitudes y respuestas."
weight: 20
---

Esta API REST elimina las filas duplicadas de un **ListObject** en una hoja de cálculo de Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates
```

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                  |
|----------------------|---------|-----------|--------------------------------------------------------------|
| **name**             | String  | Ruta      | El nombre del archivo de Excel.                              |
| **sheetName**        | String  | Ruta      | El nombre de la hoja de cálculo que contiene el objeto de lista. |
| **listObjectIndex**  | Integer | Ruta      | El índice basado en cero del objeto de lista a procesar.     |
| **folder**           | String  | Consulta  | (Opcional) La ruta de la carpeta donde se almacena el archivo. |
| **storageName**      | String  | Consulta  | (Opcional) El nombre del servicio de almacenamiento.         |

### Solicitud de ejemplo (cURL)

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "DuplicateRowsRemoved": 12,
  "Message": "Se eliminaron correctamente las filas duplicadas."
}
```

{{< /tab >}}
{{< /tabs >}}

### Respuesta

En caso de éxito, el servicio devuelve un objeto JSON similar al ejemplo anterior. Los campos son:

- **Code** – Código de estado HTTP (`200` para éxito).
- **Status** – Descripción textual del estado.
- **DuplicateRowsRemoved** – Número de filas eliminadas.
- **Message** – Información adicional sobre la operación.

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                    |
|--------|-----------------------------|----------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente.                                 |
| 413    | Payload demasiado grande    | El archivo cargado excede el límite de tamaño.                 |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                               |

## Familia de SDKs en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el repositorio de GitHub para obtener una lista completa de los SDKs de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectRemoveDuplicates.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectRemoveDuplicates.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectRemoveDuplicates.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectRemoveDuplicates.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectRemoveDuplicates.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectRemoveDuplicates.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectRemoveDuplicates.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectRemoveDuplicates.go" >}}

{{< /tab >}}

{{< /tabs >}}