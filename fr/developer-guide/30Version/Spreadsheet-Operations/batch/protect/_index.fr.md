---
title: "Protéger par lots des fichiers Excel"
second_title: "Document"
type: docs
url: /fr/batch/protect
keywords: "Protéger par lots des fichiers Excel, Aspose Cells Cloud, API REST, protection Excel, protection par lots"
description: "Découvrez comment utiliser l’API REST Aspose.Cells Cloud pour protéger par lots plusieurs fichiers Excel. Inclut les détails de la requête, un exemple cURL et des exemples de code SDK pour divers langages."
weight: 100
---

Cette API REST permet la **protection par lots** des fichiers Excel éligibles.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/protect
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre      | Type                | Emplacement | Description                                                                                              |
|-----------------------|---------------------|-------------|----------------------------------------------------------------------------------------------------------|
| batchProtectRequest   | BatchProtectRequest | body        | Charge utile JSON spécifiant le dossier source, les conditions de correspondance, le type de protection, le mot de passe et le dossier de sortie. |

### Propriétés de BatchProtectRequest

| Nom               | Type                     | Description                                                                                 | Notes        |
|-------------------|--------------------------|---------------------------------------------------------------------------------------------|--------------|
| SourceFolder      | string                   | Dossier contenant les fichiers Excel sources.                                               | facultatif   |
| MatchCondition    | MatchConditionRequest   | Critères utilisés pour sélectionner les fichiers à protéger.                                | facultatif   |
| ProtectionType    | string                   | Type de protection à appliquer (par ex. `All`, `ReadOnly`).                                 | facultatif   |
| Password          | string                   | Mot de passe à définir pour les fichiers protégés.                                          | facultatif   |
| OutFolder         | string                   | Dossier de destination pour les fichiers protégés.                                          | facultatif   |

### Propriétés de MatchConditionRequest

| Nom                 | Type       | Description                                   | Notes        |
|---------------------|------------|-----------------------------------------------|--------------|
| RegexPattern        | string     | Expression régulière utilisée pour faire correspondre les noms de fichiers. | facultatif   |
| FullMatchConditions | string[]   | Liste des conditions exactes de nom de fichier. | facultatif   |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description                                    |
|------------------|------|------------------------------------------------|
| data             | file | Contenu binaire du fichier classeur à créer.   |

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

| Code | Signification               | Quand renvoyé                           |
|------|-----------------------------|-----------------------------------------|
| 200 OK | Classeur créé avec succès   | Fluide normal                           |
| 201 Created | Classeur créé (réponse alternative) | Lorsque l’API renvoie un statut « créé » |
| 400 Bad Request | Paramètres non valides | Erreur côté client                      |
| 401 Unauthorized | Jeton manquant ou non valide | Erreur d’authentification              |
| 409 Conflict | Fichier existant et `isWriteOver=false` | Conflit avec un fichier existant       |

## Comment utiliser l’API PostProtectConvert à l’aide des SDK

### Spécification de l’API PostProtectConvert

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/PostProtectConvert) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/protect" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\",\"ProtectionType\":\"All\"}"
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

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}