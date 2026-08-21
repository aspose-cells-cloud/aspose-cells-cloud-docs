---
title: "Supprimer une image d'une feuille de calcul Excel – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Supprimer"
type: docs
url: /fr/pictures/delete/
aliases: [  /fr/delete-a-specific-picture-from-excel-worksheet/ ]
keywords: "Aspose.Cells, API cloud, supprimer une image, feuille de calcul Excel, REST"
description: "Supprimer une image d'une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Découvrez le point de terminaison DELETE, les paramètres requis, l’authentification, les codes d’erreur et les exemples de code."
weight: 50
ArticleTitle: "Supprimer une image d'une feuille de calcul Excel – Aspose.Cells Cloud API"
---

Cette API REST permet de supprimer une image d'une feuille de calcul Excel.

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Obligatoire | Description                                           |
| ---------------- | ------- | ----------- | ----------- | ----------------------------------------------------- |
| name             | string  | path        | Oui         | Le nom du fichier du classeur.                        |
| sheetName        | string  | path        | Oui         | Le nom de la feuille de calcul contenant l’image.    |
| pictureIndex     | integer | path        | Oui         | L’index de l’image à supprimer (indexation à partir de 0). |
| folder           | string  | query       | Non         | Le dossier dans lequel le classeur est stocké.       |
| storageName      | string  | query       | Non         | Le nom du service de stockage (facultatif).          |

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer cet appel avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Exemple d’en-têtes de réponse**

| En-tête         | Valeur                        |
|-----------------|------------------------------|
| Content-Type    | application/json             |
| Content-Length  | (variable)                   |
| Date            | (date du serveur)            |

{{< /tab >}}

{{< /tabs >}}

### Gestion des erreurs

| Code HTTP | Signification                                                     | Exemple de charge utile d’erreur                                           |
| --------- | ----------------------------------------------------------------- | -------------------------------------------------------------------------- |
| 200       | Image supprimée avec succès.                                      | `{ "Code": 200, "Status": "OK" }`                                          |
| 400       | Requête incorrecte – paramètres non valides.                      | `{ "Code": 400, "Message": "pictureIndex invalide." }`                    |
| 401       | Non autorisé – jeton manquant ou non valide.                      | `{ "Code": 401, "Message": "Le jeton d'accès est manquant ou invalide." }` |
| 404       | Introuvable – le classeur, la feuille de calcul ou l’image n’existe pas. | `{ "Code": 404, "Message": "Ressource introuvable." }`                    |
| 500       | Erreur interne du serveur.                                        | `{ "Code": 500, "Message": "Erreur serveur inattendue." }`                |

## Famille de SDK Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}