---
title: "Tâche ImportData – Référence de l’API Aspose.Cells Cloud & Exemples cURL"  
second_title: "Document"  
type: docs  
url: /tasks/importdata/  
aliases: [/working-with-importdata-task/]  
keywords: "Aspose.Cells, Tâche ImportData, API Excel, REST, cURL, SDK"  
description: "Découvrez comment importer des données en lot dans des classeurs Excel à l’aide de la tâche ImportData d’Aspose.Cells Cloud. Inclut la syntaxe cURL, le schéma de requête, des exemples d’SDK (C#, PHP, Ruby, Node.js) et la gestion des erreurs."  
weight: 40  
---  

## API REST  

| **API** | **Type** | **Description** | **Lien vers la ressource** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Exécuter une tâche | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) définit une interface de programmation accessible publiquement qui permet des interactions REST directes depuis un navigateur web.  

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour appeler les services Aspose.Cells Cloud. L’exemple ci-dessous montre comment exécuter une tâche **ImportData** à l’aide d’une charge utile JSON correctement formatée.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

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

L’utilisation d’un SDK constitue la méthode la plus efficace pour intégrer ces opérations dans votre application. Les SDK gèrent l’authentification, la construction des requêtes et l’analyse des réponses, vous permettant ainsi de vous concentrer sur la logique métier. Pour obtenir la liste complète des SDK Aspose.Cells Cloud, consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud).

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

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