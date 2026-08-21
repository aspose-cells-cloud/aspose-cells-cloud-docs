---
title: "Supprimer toutes les images d'une feuille de calcul Excel"
second_title: "Document"
linktitle: "Effacer"
type: docs
url: /fr/pictures/clear/
aliases: [  /fr/delete-all-pictures-from-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, supprimer toutes les images, feuille de calcul, API REST, effacer les images"
description: "Découvrez comment supprimer toutes les images d'une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud, avec des exemples utilisant cURL et les SDK."
weight: 60
ArticleTitle: "Comment supprimer toutes les images d'une feuille de calcul Excel avec Aspose.Cells Cloud"
---

Cette API REST supprime **toutes** les images d'une feuille de calcul.

**Conditions préalables**  
- Un compte Aspose.Cells Cloud actif avec un jeton d'accès OAuth 2.0 valide.  
- La version 3.0 (ou ultérieure) de l'API est requise ; les versions antérieures sont obsolètes.  
- Le fichier Excel cible doit être stocké dans un emplacement de stockage pris en charge (par défaut ou personnalisé).

**Compatibilité des versions**  
Le point de terminaison respecte la spécification de l'API Cells Cloud 3.0. Assurez-vous que vos bibliothèques clientes et les URL de requête ciblent `api.aspose.cloud/v3.0`.

## API DeleteWorksheetPictures

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                         |
| ---------------- | ------ | ----------- | --------------------------------------------------- |
| name             | string | Path        | Nom du fichier Excel.                              |
| sheetName        | string | Path        | Nom de la feuille de calcul contenant les images. |
| folder           | string | Query       | Dossier dans lequel le fichier est stocké.         |
| storageName      | string | Query       | Nom du service de stockage.                        |

### Réponses d’erreur

| Code HTTP | Description                                                             |
| --------- | ----------------------------------------------------------------------- |
| 401       | Non autorisé – jeton manquant ou invalide.                             |
| 404       | Non trouvé – le fichier, la feuille de calcul ou l’index de saut de page spécifié n'existe pas. |
| 400       | Requête incorrecte – syntaxe de requête mal formée ou paramètres invalides. |
| 500       | Erreur interne du serveur – une condition inattendue s'est produite.   |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/DeleteWorksheetPictures) définit une interface de programmation accessible publiquement et permet d'effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l'outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L'exemple suivant montre comment appeler l'API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/pictures" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
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

## Famille de SDK Cloud

Utiliser un SDK est le moyen le plus rapide de développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPictures.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPictures.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPictures.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPictures.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPictures.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPictures.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPictures.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPictures.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Notes :** L'opération DELETE ne prend pas en charge la pagination et est soumise aux limites de débit standard des API Aspose.Cells Cloud (par défaut : 100 requêtes par minute). Ajustez en conséquence la logique de votre client.

**Voir aussi** :  
- [/pictures/delete/](../delete/) – Supprimer une image spécifique d'une feuille de calcul.  
- [/pictures/add/](../add/) – Ajouter une image à une feuille de calcul.  
---