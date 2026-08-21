---
title: "Tarea ImportData – Referencia de API de Aspose.Cells Cloud y ejemplos de cURL"  
second_title: "Documento"  
type: docs  
url: /es/tasks/importdata/
aliases: [  /es/working-with-importdata-task/ ]
keywords: "Aspose.Cells, Tarea ImportData, API de Excel, REST, cURL, SDK"  
description: "Aprenda cómo importar datos por lotes en libros de Excel mediante la tarea ImportData de Aspose.Cells Cloud. Incluye sintaxis de cURL, esquema de solicitud, ejemplos de SDK (C#, PHP, Ruby, Node.js) y manejo de errores."  
weight: 40  
---  

## API REST  

| **API** | **Tipo** | **Descripción** | **Enlace del recurso** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Ejecutar tarea | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) define una interfaz de programación accesible públicamente que permite interacciones directas con REST desde un navegador web.  

Puede utilizar la herramienta de línea de comandos **cURL** para invocar los servicios de Aspose.Cells Cloud. El ejemplo siguiente muestra cómo ejecutar una tarea **ImportData** con una carga útil JSON correctamente formateada.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{
  "Tasks": [
    {
      "TaskDescription": {
        "TaskType": "ImportData",
        "ImportDataTaskParameter": {
          "Workbook": {
            "FileSourceType": "CloudFileSystem",
            "FilePath": "TaskBook.xlsx"
          },
          "ImportBatchDataOption": {
            "DestinationWorksheet": "Sheet1",
            "IsInsert": true,
            "Source": {
              "FileSourceType": "RequestFiles",
              "FilePath": "Batch_data_xml.txt"
            }
          }
        }
      }
    },
    {
      "TaskDescription": {
        "TaskType": "ImportData",
        "ImportDataTaskParameter": {
          "Workbook": {
            "FileSourceType": "InMemoryFiles",
            "FilePath": "TaskBook.xlsx"
          },
          "ImportBatchDataOption": {
            "DestinationWorksheet": "Sheet2",
            "IsInsert": true,
            "Source": {
              "FileSourceType": "RequestFiles",
              "FilePath": "Batch_data_xml_2.txt"
            }
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
            "DestinationType": "CloudFileSystem",
            "InputFile": "TaskBook.xlsx",
            "OutputFile": "ImpDataBook.xlsx"
          }
        }
      }
    }
  ]
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "OK",
  "TaskId": "12345678",
  "Result": {
    "FilePath": "ImpDataBook.xlsx",
    "DownloadUrl": "https://api.aspose.cloud/v3.0/cells/storage/file/ImpDataBook.xlsx"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

Utilizar un SDK es la forma más eficiente de integrar estas operaciones en su aplicación. Los SDK manejan la autenticación, la construcción de solicitudes y el análisis de respuestas, permitiéndole centrarse en la lógica de negocio. Para obtener una lista completa de los SDK de Aspose.Cells Cloud, consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud).

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante varios SDK:

{{< tabs tabTotal="5" tabID="8" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Tasks-ImportTaskData-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_run_task-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Tasks-ImportTaskData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ImportData-postImportDataMultipartContent-1.pl" >}}

{{< /tab >}}

{{< /tabs >}}
---