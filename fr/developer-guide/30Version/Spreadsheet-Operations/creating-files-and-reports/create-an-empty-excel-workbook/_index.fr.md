---
title: "Créer un classeur Excel vide"
second_title: "Document"
linktitle: "Classeur vide"
type: docs
url: /fr/create-an-empty-excel-file/
aliases:
  [
    /create-an-empty-excel-workbook/,
    /workbook/new/,
    /workbook/create/empty-workbook/,
  ]
keywords: "Aspose.Cells, Cloud, Excel, classeur vide, API REST, SDK"
description: "Découvrez comment créer un classeur Excel vide à l’aide de l’API REST Aspose.Cells Cloud. Inclut des exemples en cURL et en SDK."
weight: 20
ArticleTitle: "Créer un classeur Excel vide à l’aide de l’API Aspose.Cells Cloud"
---

Cet API REST permet de créer un **classeur vide**.

## API PutWorkbookCreate

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de requête

| Nom du paramètre | Type    | Description                                                  |
| ---------------- | ------- | ------------------------------------------------------------ |
| templateFile     | string  | Chemin d’accès vers un classeur modèle à utiliser comme base (facultatif). |
| dataFile         | string  | Chemin d’accès vers un fichier de données pour remplir le classeur (facultatif). |
| isWriteOver      | boolean | `true` pour écraser un fichier existant ; `false` sinon.     |
| folder           | string  | Dossier de destination pour le classeur créé (facultatif).   |
| storageName      | string  | Nom du service de stockage à utiliser.                       |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description                                 |
| ---------------- | ---- | ------------------------------------------- |
| data             | file | Contenu binaire du fichier classeur à créer. |

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

| Code | Signification                        | Conditions de retour                            |
|------|--------------------------------------|-------------------------------------------------|
| 200 OK | Classeur créé avec succès            | Déroulement normal                              |
| 201 Created | Classeur créé (réponse alternative) | Lorsque l’API renvoie un statut de création    |
| 400 Bad Request | Paramètres non valides            | Erreur côté client                              |
| 401 Unauthorized | Jeton manquant ou non valide      | Erreur d’authentification                       |
| 409 Conflict | Fichier existant et `isWriteOver=false` | Conflit avec un fichier existant               |

## Comment utiliser l’API PutWorkbookCreate avec les SDK

### Spécification de l’API PutWorkbookCreate

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder aux services web Aspose.Cells. Incluez l’en-tête `Authorization` avec un jeton d’accès OAuth2/JWT valide. Pour un classeur vide, le corps de la requête est facultatif ; si vous devez télécharger un fichier, ajoutez `--data-binary @empty.xlsx`, comme indiqué ci-dessous.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
# Créer un classeur vide nommé newworkbook.xlsx
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?isWriteOver=false" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     --data-binary @empty.xlsx   # Omettez cette ligne pour un classeur véritablement vide
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```
{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la meilleure méthode pour accélérer le développement. Un SDK masque les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreateEmpty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreateEmpty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreateEmpty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreateEmpty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreateEmpty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreateEmpty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreateEmpty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreateEmpty.go" >}}

{{< /tab >}}

{{< /tabs >}}
---