---
title: "Assemblage de données pour la création d’un rapport Excel"
second_title: "Document"
linktitle: "Assemblage des données"
type: docs
url: /assembly-data-for-the-creation-of-an-excel-report/
aliases: [/assembly/]
keywords: "Aspose.Cells, rapport Excel, assemblage de données, API cloud, REST, SDK, cURL, PDF, ODS"
description: "Découvrez comment utiliser l’API Aspose.Cells Cloud d’assemblage pour intégrer des données dans des rapports Excel (XLSX, PDF, ODS). Inclut l’URL du point d’accès, les paramètres, un exemple cURL, du code SDK, un guide d’authentification et la gestion des erreurs."
weight: 40
---

Cette API REST permet d’assembler des données **dans** un fichier Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/assembly
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête


| Nom du paramètre | Type   | Emplacement                | Description                                                                 |
|------------------|--------|----------------------------|-----------------------------------------------------------------------------|
| file             | fichier | formData (corps multipart) | Le fichier de feuille de calcul à télécharger.                             |
| DataSource       | chaîne  | chaîne de requête          | Identifiant de la source de données fournissant les données à assembler.   |
| format           | chaîne  | chaîne de requête          | Format de sortie souhaité (par exemple, `xlsx`, `pdf`).                    |

### **Réponse**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nom du fichier2]",
    "Filesize" : [taille du fichier],
    "FileContent" : "[Base64String]"
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                               |
|------|-----------------------------|---------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                           |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille.                      |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur.                                             |

## Comment utiliser l’API PostAssemble avec les SDK

### Spécification de l’API PostAssemble

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostAssemble) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/assembly?DataSource=ds&format=pdf" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F 'template=@template.xlsx' \
  -F 'data=@data.json'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "rapport1",
      "FileSize": 274022,
      "FileContent": "-----ChaîneBase64--------"
    },
    {
      "Filename": "rapport2",
      "FileSize": 274022,
      "FileContent": "-----ChaîneBase64--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer avec l’API. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAssemble.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAssemble.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAssemble.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAssemble.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAssemble.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAssemble.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAssemble.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAssemble.go" >}}

{{< /tab >}}

{{< /tabs >}}