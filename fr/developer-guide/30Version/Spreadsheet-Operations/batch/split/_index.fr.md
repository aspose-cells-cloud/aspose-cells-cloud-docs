---
title: "Fractionnement par lots"
second_title: "Document"
type: docs
url: /batch/split
keywords: "Fractionnement par lots, Aspose.Cells Cloud, API REST, Excel, PDF, CSV, JSON, Classeur, SDK cloud"
description: "Documentation de l'API de fractionnement par lots Aspose.Cells Cloud, qui permet de diviser des fichiers de classeurs en plusieurs formats tels que PDF, CSV ou JSON. Inclut les détails de la requête, des exemples de commandes cURL et l'utilisation du SDK dans divers langages de programmation."
weight: 100
---

Cette API REST permet d’effectuer un **fractionnement par lots** des fichiers éligibles.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/split
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type               | Emplacement (Chemin/Requête/Chaîne/Corps HTTP) | Description                                     |
|------------------|--------------------|--------------------------------------------------|-------------------------------------------------|
| BatchSplitRequest| BatchSplitRequest  | corps                                            | Payload de la requête contenant les options de fractionnement. |

### Propriétés de **BatchSplitRequest**

| Nom               | Type                | Description                                                  | Notes        |
|-------------------|---------------------|--------------------------------------------------------------|--------------|
| SourceFolder      | string              | Dossier contenant le fichier source.                         | [optionnel]  |
| SourceStorage     | string              | Nom du stockage où réside le fichier source.                | [optionnel]  |
| MatchCondition    | MatchConditionRequest | Conditions utilisées pour sélectionner les fichiers à diviser. | [optionnel]  |
| Format            | string              | Format de sortie souhaité (par ex. pdf, csv).               | [optionnel]  |
| FromIndex         | integer             | Index de départ des pages à diviser.                         | [optionnel]  |
| ToIndex           | integer             | Index de fin des pages à diviser.                            | [optionnel]  |
| OutFolder         | string              | Dossier de destination pour les fichiers divisés.           | [optionnel]  |
| SaveOptions       | SaveOptions         | Options supplémentaires pour l’enregistrement de la sortie.| [optionnel]  |

### Propriétés de **MatchConditionRequest**

| Nom                  | Type       | Description                                   | Notes        |
|----------------------|------------|-----------------------------------------------|--------------|
| RegexPattern         | string     | Expression régulière pour faire correspondre les noms de fichiers. | [optionnel]  |
| FullMatchConditions  | string[]   | Liste des conditions de correspondance exacte.| [optionnel]  |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description                                      |
|------------------|------|--------------------------------------------------|
| data             | file | Contenu binaire du fichier de classeur à créer. |

### **Réponse**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**Codes de statut HTTP**

| Code | Signification                     | Quand renvoyé                                |
|------|-----------------------------------|----------------------------------------------|
| 200 OK | Classeur créé avec succès         | Flux normal                                  |
| 201 Created | Classeur créé (réponse alternative) | Lorsque l’API renvoie un statut de création |
| 400 Bad Request | Paramètres invalides            | Erreur côté client                           |
| 401 Unauthorized | Jeton manquant ou invalide     | Erreur d’authentification                    |
| 409 Conflict | Fichier existant et `isWriteOver=false` | Conflit avec un fichier existant         |


## Comment utiliser l’API PostBatchSplit à l’aide des SDK

### Spécification de l’API PostBatchSplit

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la meilleure façon d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur vos tâches de fractionnement. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
---