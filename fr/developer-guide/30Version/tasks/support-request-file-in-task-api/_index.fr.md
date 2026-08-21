---
title: "Fichier de demande de support dans l’API Task"
second_title: "Document"
type: docs
url: /fr/tasks/support-request-file/
aliases: [/support-request-file-in-task-api/]
keywords: "Aspose.Cells, API REST, Excel, Cloud"
description: "L’API Aspose.Cells Cloud permet le traitement basé sur des tâches des fichiers de demande pour les classeurs Excel."
weight: 10
ArticleTitle: "Fichier de demande de support dans l’API Task d’Aspose.Cells"
---

## API REST

| **API** | **Type** | **Description** | **Lien de la ressource** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Exécuter une tâche | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) définit une interface de programmation accessible publiquement et vous permet d’effectuer directement des interactions REST depuis un navigateur web.

**Paramètres de la requête**

| Paramètre | Type | Obligatoire | Description |
|-----------|------|-------------|-------------|
| TaskDescription | object | Oui | Conteneur pour une seule définition de tâche. |
| TaskType | string | Oui | Type de tâche, par exemple `ImportData` ou `SaveResult`. |
| Workbook.FileSourceType | string | Oui | Source du fichier classeur (`CloudFileSystem`, `InMemoryFiles`). |
| Workbook.FilePath | string | Oui | Chemin d’accès au fichier classeur dans la source sélectionnée. |
| ImportBatchDataOption.DestinationWorksheet | string | Oui | Nom de la feuille cible pour les données importées. |
| ImportBatchDataOption.IsInsert | boolean | Oui | Indique s’il faut insérer des lignes (`true`) ou écraser (`false`). |
| ImportBatchDataOption.Source.FileSourceType | string | Oui | Source du fichier de demande (`RequestFiles`). |
| ImportBatchDataOption.Source.FilePath | string | Oui | Chemin d’accès au fichier de demande contenant les données en lot. |
| SaveResultTaskParameter.ResultSource | string | Oui | Source du fichier de résultat (`InMemoryFiles`). |
| SaveResultTaskParameter.ResultDestination.DestinationType | string | Oui | Type de destination pour le résultat (`CloudFileSystem`). |
| SaveResultTaskParameter.ResultDestination.InputFile | string | Oui | Nom du fichier classeur d’entrée. |
| SaveResultTaskParameter.ResultDestination.OutputFile | string | Oui | Nom souhaité pour le fichier de sortie. |

**Réponse**

| Champ | Type | Description |
|-------|------|-------------|
| Code | integer | Code d’état HTTP (par exemple, 200 pour une opération réussie). |
| Status | string | Statut de l’opération (`OK` ou message d’erreur). |
| Result | object | Détails de l’exécution de la tâche, y compris les fichiers éventuellement générés. |

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

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

Pour plus d’informations sur les tâches associées, consultez les pages consacrées à la [tâche ImportData](/cells/tasks/importdata/) et à la [tâche SaveResult](/cells/tasks/save-result/).

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la meilleure façon d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="1" tabID="4" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< /tabs >}}