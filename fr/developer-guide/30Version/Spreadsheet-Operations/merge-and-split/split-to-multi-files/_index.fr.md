---
title: "Diviser un fichier Excel en plusieurs fichiers"
second_title: "Document"
linktitle: "Diviser des fichiers Excel multipages"
type: docs
url: /fr/split-an-excel-file-to-multi-files/
aliases: [  /fr/split-excel-workbooks/ , /fr/workbook/split/ ]
keywords: "Aspose.Cells, Cloud, Excel, Diviser, API, PDF, CSV, JSON"
description: "Utilisez l’API REST Aspose.Cells Cloud pour diviser des classeurs Excel multi-feuilles en fichiers séparés. Prend en charge les formats de sortie tels que PDF, CSV et JSON, et est accessible via des SDK pour Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby et Swift."
weight: 32
ArticleTitle: "Diviser un fichier Excel en plusieurs fichiers - Documentation Aspose.Cells Cloud"
---

L’API REST Aspose.Cells Cloud permet de diviser des classeurs Excel multi-feuilles en fichiers distincts.

**Prérequis**  
Avant d’appeler l’API, vous devez obtenir un jeton JWT valide et l’inclure dans l’en-tête `Authorization` de chaque requête. Consultez le [guide d’authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) pour plus de détails.

## API PostSplit

```http
POST https://api.aspose.cloud/v3.0/cells/split
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                                    |
|------------------|--------|-------------|----------------------------------------------------------------|
| file             | file   | formData    | Le classeur Excel à télécharger.                              |
| format           | string | query       | Format de sortie souhaité (par exemple, `pdf`, `csv`, `json`).|
| password         | string | query       | Mot de passe pour un classeur chiffré (facultatif).           |
| from             | integer| query       | Index de la première feuille à inclure (indexation à 1).      |
| to               | integer| query       | Index de la dernière feuille à inclure (inclusif).            |

### **Réponse**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[nom_fichier1]",
            "Filesize" : [taille_fichier],
            "FileContent" : "[Base64String]"
        },
        {
            "Filename" : "[nom_fichier2]",
            "Filesize" : [taille_fichier],
            "FileContent" : "[Base64String]"
        },
        {
            "Filename" : "[nom_fichier3]",
            "Filesize" : [taille_fichier],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                     |
|------|-----------------------------|-----------------------------------------------------------------|
| 200  | OK                          | Le filtre a été appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Demande incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                 |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille.             |
| 500  | Erreur interne du serveur    | Erreur inattendue côté serveur.                                 |

## Comment utiliser l’API PostSplit avec les SDK

### Spécification de l’API PostSplit

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostSplit) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

**Codes de statut HTTP**

| Code | Signification               | Description                                                     |
|------|-----------------------------|-----------------------------------------------------------------|
| 200  | OK                          | Le classeur a été divisé avec succès ; la réponse contient la liste des fichiers. |
| 400  | Demande incorrecte          | Paramètres manquants ou non valides (par exemple, format non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                 |
| 500  | Erreur interne du serveur    | Une erreur inattendue s’est produite côté serveur.             |

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/split?format=pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton_jwt>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' \
# Remplacez xxxxx1.xlsx et xxxxx2.xlsx par les chemins vers vos fichiers Excel
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
    "Files": [
        {
            "Filename": "xxxxx_feuille1.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        },
        {
            "Filename": "xxxxx_feuille2.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        }
        …
    ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}