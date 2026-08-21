---
title: "Trabajo con la tarea SmartMarker en la API de Aspose.Cells Cloud"
type: docs
url: /tasks/smartmarker/
aliases: [/working-with-smartmarker-task/]
keywords: "tarea SmartMarker, Aspose.Cells Cloud, API REST, Excel, automatización de hojas de cálculo"
description: "Aprenda a usar la tarea SmartMarker de la API de Aspose.Cells Cloud con ejemplos en cURL y SDK, incluyendo el esquema de solicitud y el manejo de errores."
weight: 60
ArticleTitle: "Trabajo con la tarea SmartMarker en la API de Aspose.Cells Cloud"
---

## API REST

**SmartMarker** es una función de la API de Aspose.Cells Cloud que fusiona datos desde fuentes XML o JSON en marcadores de posición dentro de una plantilla de Excel, produciendo un libro completamente rellenado. Se utiliza típicamente para generación de informes, combinación de correspondencia y creación de hojas de cálculo impulsadas por datos.

**Prerrequisitos**

- Versión 3.0 o posterior de la API de Aspose.Cells Cloud.  
- Un token de acceso OAuth2/JWT válido (pasado en el encabezado `Authorization: Bearer <token>`).  
- Archivos de origen (libro de plantilla y archivo de datos) cargados en el almacenamiento de Aspose Cloud o accesibles mediante un tipo de sistema de archivos compatible.  
- Endpoint HTTPS (todas las solicitudes deben utilizar TLS).

| **API** | **Tipo** | **Descripción** | **Enlace del recurso** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Ejecutar tarea | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo ejecutar una tarea SmartMarker y posteriormente guardar el libro resultado.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <su_token_de_acceso>" \
     -d '{
  "TaskData": {
    "Tasks": [
      {
        "TaskDescription": {
          "TaskType": "SmartMarker",
          "SmartMarkerTaskParameter": {
            "SourceWorkbook": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "Designer.xlsx"
            },
            "DestinationWorkbook": {
              "FileSourceType": "InMemoryFiles",
              "FilePath": "Temp.xlsx"
            },
            "xmlFile": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "DataSet.xml"
            }
          }
        }
      },
      {
        "TaskDescription": {
          "TaskType": "SaveResult",
          "SaveResultTaskParameter": {
            "ResultSource": "InMemoryFiles",
            "ResultDestination": {
              "DestinationType": "OutputStream",
              "InputFile": "Temp.xlsx",
              "OutputFile": "Output.xlsx"
            }
          }
        }
      }
    ]
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Result": {
    "FileLink": "https://api.aspose.cloud/v3.0/storage/file/Output.xlsx",
    "FileSize": 254321,
    "FileName": "Output.xlsx"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Esquema de solicitud (extracto)

| Elemento | Tipo | Obligatorio | Descripción |
| ------- | ---- | -------- | ----------- |
| `TaskData` | objeto | Sí | Elemento raíz que contiene uno o más objetos `TaskDescription`. |
| `Tasks` | matriz de objetos | Sí | Colección de tareas que se ejecutarán en orden. |
| `TaskDescription.TaskType` | cadena | Sí | Tipo de tarea (`SmartMarker`, `SaveResult`, etc.). |
| `SmartMarkerTaskParameter.SourceWorkbook` | objeto | Sí | Especifica la ubicación del libro de plantilla. |
| `SmartMarkerTaskParameter.DestinationWorkbook` | objeto | Sí | Especifica dónde se almacena el libro intermedio. |
| `SmartMarkerTaskParameter.xmlFile` | objeto | Sí | Fuente de datos (XML/JSON) utilizada por SmartMarker. |
| `SaveResultTaskParameter.ResultDestination` | objeto | Sí | Define cómo se devuelve el libro final (por ejemplo, `OutputStream`). |

### Manejo de errores

La API puede devolver los siguientes códigos de estado HTTP:

- **400 Bad Request (Solicitud incorrecta)** – carga de solicitud mal formada o campos obligatorios ausentes.  
- **401 Unauthorized (No autorizado)** – token de autenticación inválido o ausente.  
- **404 Not Found (No encontrado)** – uno de los archivos de origen especificados no se puede localizar.  
- **500 Internal Server Error (Error interno del servidor)** – se produjo un error inesperado del lado del servidor.

Consulte el cuerpo de la respuesta para encontrar un objeto `Error` que incluya un `Code` y un `Message` descriptivo.

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="1" tabID="4" tabName1="C#" >}}

{{< tab tabNum="1" >}}
```csharp
var xml = @"<TaskData>
    <Tasks>
        <TaskDescription>
            <TaskType>SmartMarker</TaskType>
            <SmartMarkerTaskParameter>
                <SourceWorkbook>
                    <FileSourceType>CloudFileSystem</FileSourceType>
                    <FilePath>Designer.xlsx</FilePath>
                </SourceWorkbook>
                <DestinationWorkbook>
                    <FileSourceType>InMemoryFiles</FileSourceType>
                    <FilePath>Temp.xlsx</FilePath>
                </DestinationWorkbook>
                <xmlFile>
                    <FileSourceType>CloudFileSystem</FileSourceType>
                    <FilePath>DataSet.xml</FilePath>
                </xmlFile>
            </SmartMarkerTaskParameter>
        </TaskDescription>
        <TaskDescription>
            <TaskType>SaveResult</TaskType>
            <SaveResultTaskParameter>
                <ResultSource>InMemoryFiles</ResultSource>
                <ResultDestination>
                    <DestinationType>OutputStream</DestinationType>
                    <InputFile>Temp.xlsx</InputFile>
                    <OutputFile>Output.xlsx</OutputFile>
                </ResultDestination>
            </SaveResultTaskParameter>
        </TaskDescription>
    </Tasks>
</TaskData>";

ServiceHelper helper = new ServiceHelper(sid, key);
using (HttpWebResponse response = helper.CallPost(
       "https://api.aspose.cloud/v3.0/cells/task/runtask",
       xml,
       "application/xml"))
{
    if (response.StatusCode == HttpStatusCode.OK)
    {
        Console.WriteLine("OK");
        using (Stream st = response.GetResponseStream())
        using (FileStream fs = new FileStream("Output.xlsx", FileMode.OpenOrCreate))
        {
            st.CopyTo(fs);
        }
    }
}
```
{{< /tab >}}

{{< /tabs >}}
---