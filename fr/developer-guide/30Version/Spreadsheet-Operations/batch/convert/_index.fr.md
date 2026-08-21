---
title: "Conversion en lot de fichiers Excel"
second_title: "Document"
type: docs
url: /batch/convert
keywords: "conversion en lot, Excel, Aspose.Cells Cloud, API REST, PDF, CSV, JSON, Markdown, feuille de calcul"
description: "Découvrez comment utiliser l'API Aspose.Cells Cloud pour convertir en lot plusieurs fichiers Excel dans des formats tels que PDF, CSV, JSON ou Markdown. Ce guide inclut les détails des points de terminaison REST, les paramètres de requête, un exemple cURL et des extraits de code SDK pour divers langages."
weight: 100
---

Cette API REST permet la **conversion en lot** des fichiers éligibles.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/convert
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre     | Type   | Emplacement | Description                                           |
|----------------------|--------|-------------|-------------------------------------------------------|
| **batchConvertRequest** | objet | corps       | Corps de la requête contenant les paramètres de conversion. |

#### Propriétés de BatchConvertRequest

| Nom                | Type                | Description                                           | Notes |
|--------------------|---------------------|-------------------------------------------------------|-------|
| **SourceFolder**   | chaîne              | Chemin vers le dossier contenant les fichiers Excel sources. | [facultatif] |
| **MatchCondition** | MatchConditionRequest | Conditions utilisées pour sélectionner les fichiers à convertir. | [facultatif] |
| **Format**         | chaîne              | Format cible de la conversion (par ex., `pdf`, `csv`). | [facultatif] |
| **OutFolder**      | chaîne              | Dossier de destination où les fichiers convertis seront enregistrés. | [facultatif] |
| **SaveOptions**    | SaveOptions         | Options supplémentaires contrôlant la manière dont les fichiers sont enregistrés. | [facultatif] |

#### Propriétés de MatchConditionRequest

| Nom                     | Type       | Description                                          | Notes |
|-------------------------|------------|------------------------------------------------------|-------|
| **RegexPattern**        | chaîne     | Expression régulière utilisée pour filtrer les noms de fichiers. | [facultatif] |
| **FullMatchConditions** | chaîne[]   | Liste des conditions exactes de nom de fichier pour la correspondance. | [facultatif] |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description                                    |
| ---------------- | ---- | ---------------------------------------------- |
| data             | fichier | Contenu binaire du classeur à créer.          |
  
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

| Code | Signification                     | Quand renvoyé                           |
|------|-----------------------------------|-----------------------------------------|
| 200 OK | Classeur créé avec succès         | Déroulement normal                      |
| 201 Created | Classeur créé (réponse alternative) | Lorsque l'API renvoie un statut « créé » |
| 400 Bad Request | Paramètres invalides             | Erreur côté client                      |
| 401 Unauthorized | Jeton manquant ou invalide       | Erreur d'authentification               |
| 409 Conflict | Fichier existant et `isWriteOver=false` | Conflit avec un fichier existant        |

## Comment utiliser l'API PostBatchConvert avec les SDK

### Spécification de l'API PostBatchConvert

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/PostBatchConvert) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/convert" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\",\"SaveOptions\":{\"SaveFormat\":\"pdf\",\"CalculateFormula\":true,\"EnableHTTPCompression\":true,\"OnePagePerSheet\":true,\"CreateDirectory\":false,\"Compliance\":\"None\"}}"
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

L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur vos tâches de projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Batch-Convet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Batch-Convet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-Batch-Convet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Batch-Convet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Batch-Convet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Batch-Convet.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Batch-Convet.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d763dc80b0aff6275403dc1d82ad59a5" "Examples-Batch-Convet.go" >}}

{{< /tab >}}

{{< /tabs >}}