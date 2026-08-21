---
title: "Verrouiller en masse des fichiers Excel"
second_title: "Document"
type: docs
url: /batch/lock
keywords: "verrouillage en masse, Excel, Aspose.Cells, API Cloud, feuille de calcul, protection de fichiers"
description: "L’API Aspose.Cells Cloud permet de verrouiller en masse plusieurs fichiers Excel. Utilisez le point de terminaison REST ou l’un des SDK pris en charge (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, etc.) pour verrouiller les fichiers en lot."
weight: 100
---

Cette API REST permet de **verrouiller en masse** les fichiers Excel éligibles.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/lock
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.


### Paramètres de la requête

| Nom du paramètre | Type               | Emplacement | Description                                |
|------------------|--------------------|-------------|--------------------------------------------|
| BatchLockRequest | BatchLockRequest   | corps       | Corps JSON contenant les paramètres de verrouillage. |

#### Propriétés de **BatchLockRequest**

| Nom              | Type                     | Description                                                   | Notes    |
|------------------|--------------------------|---------------------------------------------------------------|----------|
| SourceFolder     | string                   | Dossier contenant les fichiers Excel sources.                 | facultatif |
| MatchCondition   | MatchConditionRequest    | Conditions utilisées pour sélectionner les fichiers à verrouiller. | facultatif |
| Password         | string                   | Mot de passe à appliquer aux fichiers verrouillés.           | facultatif |
| OutFolder        | string                   | Dossier de destination des fichiers verrouillés.             | facultatif |

#### Propriétés de **MatchConditionRequest**

| Nom                | Type      | Description                                            | Notes    |
|--------------------|-----------|--------------------------------------------------------|----------|
| RegexPattern       | string    | Expression régulière pour faire correspondre les noms de fichiers. | facultatif |
| FullMatchConditions| string[]  | Correspondances exactes de noms de fichiers à verrouiller. | facultatif |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description                                    |
| ---------------- | ---- | ---------------------------------------------- |
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
| 200 OK | Classeur créé avec succès   | Déroulement normal                      |
| 201 Created | Classeur créé (réponse alternative) | Lorsque l’API renvoie un statut de création |
| 400 Bad Request | Paramètres invalides | Erreur côté client                      |
| 401 Unauthorized | Jeton manquant ou invalide | Erreur d’authentification              |
| 409 Conflict | Fichier existant et `isWriteOver=false` | Conflit avec un fichier existant      |

## Comment utiliser l’API PostBatchLock à l’aide des SDK

### Spécification de l’API PostBatchLock

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchLock) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment appeler l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/lock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}"
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

L’utilisation d’un SDK est le moyen le plus rapide de développer. Un SDK abstrait les détails de bas niveau afin que vous puissiez vous concentrer sur vos tâches de verrouillage. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchLock.go" >}}

{{< /tab >}}

{{< /tabs >}}