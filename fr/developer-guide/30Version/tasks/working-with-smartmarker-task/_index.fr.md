---
title: "Travail avec la tâche SmartMarker dans l’API Aspose.Cells Cloud"
type: docs
url: /fr/tasks/smartmarker/
aliases: [  /fr/working-with-smartmarker-task/ ]
keywords: "tâche SmartMarker, Aspose.Cells Cloud, API REST, Excel, automatisation de feuilles de calcul"
description: "Découvrez comment utiliser la tâche SmartMarker de l’API Aspose.Cells Cloud à l’aide d’exemples cURL et SDK, incluant le schéma de requête et la gestion des erreurs."
weight: 60
ArticleTitle: "Travail avec la tâche SmartMarker dans l’API Aspose.Cells Cloud"
---

## API REST

**SmartMarker** est une fonctionnalité de l’API Aspose.Cells Cloud qui fusionne des données provenant de sources XML ou JSON dans des espaces réservés d’un modèle Excel, produisant ainsi un classeur entièrement rempli. Elle est généralement utilisée pour la génération de rapports, les publipostages et la création de feuilles de calcul pilotées par les données.

**Prérequis**

- API Aspose.Cells Cloud version 3.0 ou ultérieure.  
- Jeton d’accès OAuth2/JWT valide (transmis dans l’en-tête `Authorization: Bearer <token>`).  
- Fichiers sources (classeur modèle et fichier de données) chargés dans le stockage Aspose Cloud ou accessibles via un type de système de fichiers pris en charge.  
- Point de terminaison HTTPS (toutes les requêtes doivent utiliser TLS).

| **API** | **Type** | **Description** | **Lien vers la ressource** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Exécuter une tâche | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment exécuter une tâche SmartMarker, puis enregistrer le classeur résultat.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <your_access_token>" \
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

### Schéma de requête (extrait)

| Élément | Type | Obligatoire | Description |
| ------- | ---- | ---------- | ----------- |
| `TaskData` | objet | Oui | Élément racine contenant un ou plusieurs objets `TaskDescription`. |
| `Tasks` | tableau d’objets | Oui | Collection de tâches à exécuter dans l’ordre. |
| `TaskDescription.TaskType` | chaîne | Oui | Type de tâche (`SmartMarker`, `SaveResult`, etc.). |
| `SmartMarkerTaskParameter.SourceWorkbook` | objet | Oui | Indique l’emplacement du classeur modèle. |
| `SmartMarkerTaskParameter.DestinationWorkbook` | objet | Oui | Indique l’emplacement de stockage du classeur intermédiaire. |
| `SmartMarkerTaskParameter.xmlFile` | objet | Oui | Source de données (XML/JSON) utilisée par SmartMarker. |
| `SaveResultTaskParameter.ResultDestination` | objet | Oui | Définit la manière dont le classeur final est renvoyé (par exemple, `OutputStream`). |

### Gestion des erreurs

L’API peut renvoyer les codes d’état HTTP suivants :

- **400 Bad Request** – charge utile de requête mal formée ou champs obligatoires manquants.  
- **401 Unauthorized** – jeton d’authentification invalide ou manquant.  
- **404 Not Found** – l’un des fichiers sources spécifiés est introuvable.  
- **500 Internal Server Error** – une erreur inattendue côté serveur s’est produite.

Vérifiez le corps de la réponse pour y trouver un objet `Error` contenant un `Code` et un `Message` descriptif.

L’utilisation d’un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

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