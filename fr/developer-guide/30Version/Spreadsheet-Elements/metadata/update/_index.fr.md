---
title: "Mettre à jour les métadonnées"
second_title: "Document"
linktitle: "Mise à jour sans utiliser le stockage"
type: docs
url: /fr/metadata/update/
keywords: "métadonnées, Excel, Aspose.Cells Cloud, API REST, mise à jour, classeur"
description: "L'API REST Aspose.Cells Cloud permet de mettre à jour les métadonnées dans des fichiers Excel. Elle prend en charge plusieurs SDK (C#, Java, Python, Ruby, Go, etc.) pour une intégration fluide dans divers langages de programmation."
weight: 35
ArticleTitle: "Mettre à jour les métadonnées – Documentation de l’API Aspose.Cells Cloud"
---

Cette API REST permet de mettre à jour les **métadonnées** dans plusieurs fichiers Excel.

**Prérequis :** Un compte Aspose Cloud actif, un jeton d’accès JWT valide et les fichiers Excel à télécharger.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/update
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre   | Type   | Emplacement       | Description                                            |
| -------------------- | ------ | ----------------- | ------------------------------------------------------ |
| file                 | fichier | formData          | Le fichier Excel à télécharger.                        |
| DocumentProperties   | objet  | Corps HTTP (JSON) | Propriétés du document à définir pour le fichier Excel. |

**Remarques :** Jusqu’à 10 fichiers peuvent être téléchargés en une seule requête. Les formats pris en charge incluent `.xlsx`, `.xls` et `.csv`. La taille totale de la requête ne doit pas dépasser 100 Mo.

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/PostMetadata) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/update" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F 'xxxxx1=@xxxx1.xlsx' \
  -F 'xxxxx2=@xxxx2.xlsx' \
  -d '[{ "name": "test", "value": "test" }]'
```

La requête nécessite un en-tête **Authorization** contenant un jeton JWT en mode Bearer. Assurez-vous que le jeton a été généré à l’aide de vos identifiants client Aspose Cloud.

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Voir aussi :**  
- [Obtenir les métadonnées](/metadata/get/)  
- [Supprimer les métadonnées](/metadata/delete/)  
---