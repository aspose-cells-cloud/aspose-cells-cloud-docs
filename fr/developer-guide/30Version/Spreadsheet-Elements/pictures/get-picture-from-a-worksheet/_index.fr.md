---
title: "Obtenir toutes les images d'une feuille de calcul Excel"
second_title: "Document"
linktype: "get-all"
type: docs
url: /fr/pictures/get-all/
aliases: [/get-picture-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, feuille de calcul Excel, API d'images, obtenir toutes les images, API REST, SDK"
description: "Récupérer tous les objets image d'une feuille de calcul Excel via l'API REST Aspose.Cells Cloud."
ArticleTitle: "Obtenir toutes les images d'une feuille de calcul Excel - Aspose.Cells Cloud API"
weight: 10
---

Cet API REST récupère toutes les informations relatives aux images d'une feuille de calcul Excel.

**Prérequis**  
Avant d’appeler ce point de terminaison, assurez-vous d’avoir :

- Un jeton d’accès JWT Aspose Cloud valide.  
- Le fichier Excel cible téléchargé dans le stockage sélectionné.  
- Le nom correct du stockage (si vous utilisez un stockage personnalisé).  
- Le nom de la feuille de calcul contenant les images.

## API GetWorksheetPictures

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

**Remarque :** Utilisez HTTPS (TLS 1.2 ou version ultérieure) lors de l’appel à l’API et incluez un jeton JWT valide dans l’en-tête `Authorization`.

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une authentification basée sur <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                           |
| ---------------- | ------ | ----------- | ----------------------------------------------------- |
| name             | string | path        | Le nom du fichier Excel.                             |
| sheetName        | string | path        | Le nom de la feuille de calcul contenant les images. |
| folder           | string | query       | Le chemin du dossier où le fichier est stocké.      |
| storageName      | string | query       | Le nom du service de stockage.                       |

### Réponses d’erreur

| Code HTTP | Description                                                                      |
| --------- | -------------------------------------------------------------------------------- |
| 401       | Non autorisé – jeton manquant ou non valide.                                    |
| 404       | Introuvable – le fichier, la feuille de calcul ou l’indice de saut de page spécifié n’existe pas. |
| 400       | Requête incorrecte – syntaxe mal formée ou paramètres invalides.                |
| 500       | Erreur interne du serveur – une condition inattendue s’est produite.            |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPictures) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Pictures": {
    "PictureList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet2/pictures",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Réponse de succès** – Un appel réussi renvoie le code HTTP 200 avec une charge utile JSON contenant un objet `Pictures` listant le lien de ressource de chaque image.

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen optimal d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}

Vous pouvez télécharger les SDK directement depuis leurs gestionnaires de packages respectifs (par exemple, NuGet pour .NET, Maven Central pour Java, Composer pour PHP, npm pour Node.js, PyPI pour Python, CPAN pour Perl, et les modules Go pour Go).  

*Voir également :* Ajouter une image, Supprimer une image, Mettre à jour les propriétés d'une image.