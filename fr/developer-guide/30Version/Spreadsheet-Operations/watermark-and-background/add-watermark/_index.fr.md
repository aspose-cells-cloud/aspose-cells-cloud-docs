---
title: "Ajouter une filigrane aux fichiers Excel"
second_title: "Document"
linktitle: "Ajouter une filigrane aux fichiers Excel"
type: docs
url: /add-watermark-into-excel-files/
aliases: [/watermark/]
keywords: "ajouter une filigrane à Excel, Aspose.Cells Cloud, API REST, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Découvrez comment ajouter une filigrane textuelle aux classeurs Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut un exemple cURL, les paramètres requis et les détails de la réponse."
weight: 39
ArticleTitle: "Ajouter une filigrane aux fichiers Excel – Documentation Aspose.Cells Cloud"
---

Cette API REST ajoute une **filigrane** aux fichiers Excel.

**Prérequis :** Vous devez obtenir un jeton d’accès JWT valide et vous assurer que le fichier Excel est dans un format pris en charge (par exemple, `.xlsx`, `.xls`).  
**Contexte :** Une filigrane est un texte semi-transparent superposé à chaque feuille de calcul afin d’indiquer la propriété ou le caractère confidentiel du document.

## API PostWatermark

```http
POST https://api.aspose.cloud/v3.0/cells/watermark
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une authentification basée sur <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement                     | Description                                                  |
| ---------------- | ------ | ------------------------------- | ------------------------------------------------------------ |
| `file`           | fichier | formData (corps multipart)      | Le fichier Excel auquel la filigrane sera appliquée.       |
| `text`           | chaîne  | query                           | Le texte de la filigrane à afficher.                         |
| `color`          | chaîne  | query                           | La couleur de la filigrane au format hexadécimal ARGB (par exemple, `004433ff`). |

### **Réponse**

La réponse JSON contient un tableau **Files** (Fichiers). Pour chaque objet fichier :

- **Filename** – nom du classeur traité.  
- **FileSize** – taille du fichier en octets.  
- **FileContent** – contenu de l’ fichier Excel filigrané encodé en Base64 ; décodez-le pour obtenir le fichier effectif.

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[nom_fichier1]",
            "Filesize" : [taille_fichier],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[nom_fichier2]",
            "Filesize" : [taille_fichier],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[nom_fichier3]",
            "Filesize" : [taille_fichier],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**Codes d’état HTTP**

| Code | Signification               | Description                                                  |
|------|-----------------------------|--------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Demande incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille. |
| 500  | Erreur interne du serveur    | Erreur inattendue du serveur. |

## Comment utiliser l’API PostWatermark à l’aide des SDK

### Spécification de l’API PostWatermark

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostWatermark) définit une interface de programmation publiquement accessible et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour appeler les services web Aspose.Cells. L’exemple ci-dessous montre une requête complète, incluant l’en-tête d’authentification requis. Remplacez `<your-jwt-token>` par un jeton d’accès JWT valide obtenu à partir du point d’authentification Aspose.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/watermark?text=aspose.cells.cloud&color=004433ff" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample_watermarked.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer. Un SDK masque les détails de bas niveau, vous permettant ainsi de vous concentrer sur votre logique métier. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWatermark.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWatermark.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWatermark.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWatermark.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWatermark.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWatermark.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWatermark.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWatermark.go" >}}

{{< /tab >}}

{{< /tabs >}}
---