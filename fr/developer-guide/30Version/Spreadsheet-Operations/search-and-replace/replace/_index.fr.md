---
title: "Remplacer du texte dans des fichiers Excel"
second_title: "Document"
linktitle: "Remplacement sans utiliser de stockage"
type: docs
url: /replace/
keywords: "remplacement de texte Excel, Aspose.Cells Cloud, API REST, remplacement dans feuille de calcul, API, remplacement de texte dans fichier Excel"
description: "Utilisez l’API REST Aspose.Cells Cloud pour remplacer du texte existant par de nouvelles valeurs dans des fichiers Excel. Prend en charge les SDK pour C#, Java, Python, Node.js, PHP, Ruby, Go et Perl."
weight: 80
---


## API REST

Cette API REST permet de remplacer des données dans des fichiers Excel.

```bash
POST https://api.aspose.cloud/v3.0/cells/replace
```

### Sécurité et authentification

Les API REST Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement           | Description                                           |
| ---------------- | ------ | --------------------- | ----------------------------------------------------- |
| **file**         | file   | formData (multipart)  | Fichier Excel à traiter.                              |
| **text**         | string | query                 | Chaîne de texte à remplacer.                          |
| **newtext**      | string | query                 | Texte de remplacement.                                |
| **password**     | string | query                 | Mot de passe pour un classeur protégé (facultatif).  |
| **sheetname**    | string | query                 | Nom de la feuille de calcul cible (facultatif).      |

### **Réponse**

```json
{
  "Status":"OK",
  "Code":200,
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

| Code | Signification               | Description                                                |
|------|-----------------------------|------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT non valide ou manquant.                          |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la taille limite.           |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur.                              |

## Comment utiliser l’API PostReplace avec les SDK

### Spécification de l’API PostReplace

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostReplace) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/replace?text=1&newtext=aspose.cells.cloud" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxx1",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxx2",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}