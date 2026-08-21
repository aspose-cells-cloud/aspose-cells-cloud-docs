---
title: "Archivo de solicitud de soporte en la API de tareas"
second_title: "Documentos"
type: docs
url: /tasks/support-request-file/
aliases: [/support-request-file-in-task-api/]
keywords: "Aspose.Cells, API REST, Excel, Nube"
description: "La API de Aspose.Cells Cloud permite el procesamiento basado en tareas de archivos de solicitud para libros de Excel."
weight: 10
ArticleTitle: "Archivo de solicitud de soporte en la API de tareas de Aspose.Cells"
---

## API REST

| **API** | **Tipo** | **Descripción** | **Enlace al recurso** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Ejecutar tarea | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

**Parámetros de solicitud**

| Parámetro | Tipo | Obligatorio | Descripción |
|-----------|------|------------|-------------|
| TaskDescription | object | Sí | Contenedor para una única definición de tarea. |
| TaskType | string | Sí | Tipo de tarea, por ejemplo, `ImportData` o `SaveResult`. |
| Workbook.FileSourceType | string | Sí | Fuente del archivo del libro de cálculo (`CloudFileSystem`, `InMemoryFiles`). |
| Workbook.FilePath | string | Sí | Ruta al archivo del libro de cálculo en la fuente seleccionada. |
| ImportBatchDataOption.DestinationWorksheet | string | Sí | Nombre de la hoja de cálculo de destino para los datos importados. |
| ImportBatchDataOption.IsInsert | boolean | Sí | Indica si se deben insertar filas (`true`) o sobrescribir (`false`). |
| ImportBatchDataOption.Source.FileSourceType | string | Sí | Fuente del archivo de solicitud (`RequestFiles`). |
| ImportBatchDataOption.Source.FilePath | string | Sí | Ruta al archivo de solicitud que contiene los datos por lotes. |
| SaveResultTaskParameter.ResultSource | string | Sí | Fuente del archivo de resultado (`InMemoryFiles`). |
| SaveResultTaskParameter.ResultDestination.DestinationType | string | Sí | Tipo de destino para el resultado (`CloudFileSystem`). |
| SaveResultTaskParameter.ResultDestination.InputFile | string | Sí | Nombre del archivo de entrada del libro de cálculo. |
| SaveResultTaskParameter.ResultDestination.OutputFile | string | Sí | Nombre deseado para el archivo de salida. |

**Respuesta**

| Campo | Tipo | Descripción |
|-------|------|-------------|
| Code | integer | Código de estado HTTP (por ejemplo, 200 para éxito). |
| Status | string | Estado de la operación (`OK` o mensaje de error). |
| Result | object | Detalles de la ejecución de la tarea, incluidos los archivos generados. |

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
  -H "accept: application/json" \
  -H "Content-Type: application/json" \
  -H "x-aspose-client: Containerize.Swagger" \
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
  "Code": 200,
  "Status": "OK",
  "Result": {
    "GeneratedFiles": [
      {
        "FilePath": "ImpDataBook.xlsx",
        "FileUrl": "https://api.aspose.cloud/v3.0/cells/storage/file/ImpDataBook.xlsx"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

Para obtener más información sobre tareas relacionadas, consulte las páginas sobre la [tarea ImportData](/cells/tasks/importdata/) y la [tarea SaveResult](/cells/tasks/save-result/).

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="1" tabID="4" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< /tabs >}}