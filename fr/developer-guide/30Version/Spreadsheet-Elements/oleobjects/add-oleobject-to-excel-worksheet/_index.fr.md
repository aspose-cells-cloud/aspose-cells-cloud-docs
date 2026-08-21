---
title: "Ajouter un objet OLE dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Ajouter un objet OLE"
type: docs
url: /fr/oleobjects/add/
aliases: [  /fr/add-oleobject-to-excel-worksheet/ ]
keywords: "ajouter un objet OLE, Excel, Aspose.Cells Cloud, API REST, SDK"
description: "Utilisez l’API REST Aspose.Cells Cloud pour ajouter des objets OLE aux feuilles de calcul Excel. L’API peut être appelée directement ou via des SDK pour C#, Java, PHP, Ruby, Node.js, Python, Perl et Go."
ArticleTitle: "Ajouter un objet OLE à une feuille de calcul Excel avec l’API Aspose.Cells Cloud"
weight: 20
---

L’API Aspose.Cells Cloud permet la manipulation programmatique de classeurs Excel, notamment la capacité à intégrer directement des objets OLE (par exemple, documents Word, fichiers PDF ou autres fichiers binaires) dans une feuille de calcul.

Cette API REST ajoute un **objet OLE** à une feuille de calcul Excel.

**Prérequis** – Vous devez disposer d’un jeton d’authentification JWT valide, et tous les fichiers sources référencés par `oleFile` ou `imageFile` doivent être préalablement téléchargés dans l’emplacement de stockage spécifié avant d’invoquer le point de terminaison.

## API PutWorksheetOleObject

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                          |
|------------------|---------|-------------|------------------------------------------------------|
| name             | string  | path        | Nom du fichier de classeur.                          |
| sheetName        | string  | path        | Nom de la feuille de calcul.                         |
| oleObject        | object  | body        | Définition de l’objet OLE.                           |
| upperLeftRow     | integer | query       | Index de ligne du coin supérieur gauche (par défaut 0). |
| upperLeftColumn  | integer | query       | Index de colonne du coin supérieur gauche (par défaut 0). |
| height           | integer | query       | Hauteur de l’objet OLE (par défaut 0).               |
| width            | integer | query       | Largeur de l’objet OLE (par défaut 0).               |
| oleFile          | string  | query       | Nom du fichier source OLE.                           |
| imageFile        | string  | query       | Nom du fichier d’image d’aperçu.                     |
| folder           | string  | query       | Dossier contenant le classeur.                       |
| storageName      | string  | query       | Nom du stockage à utiliser.                          |

**Remarques** – `upperLeftRow` et `upperLeftColumn` utilisent un indexation à partir de zéro. Le fichier `oleFile` (et éventuellement `imageFile`) doit déjà exister dans le stockage cible ; sinon, la requête renverra une erreur.

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/PutWorksheetOleObject) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour appeler les services web Aspose.Cells. L’exemple ci-dessous montre comment ajouter un objet OLE à l’aide de cURL. **HTTPS est requis pour tous les appels en production.**

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/oleobjects" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -d '{"ImageSourceFullName":"aspose-logo.png", "IsAutoSize":true, "SourceFullName":"Sample_Book2.xls", "UpperLeftRow":15, "Top":10, "UpperLeftColumn":5, "Left":10, "Width":400, "Height":400}'
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

![Capture d’écran montrant un objet OLE intégré dans une feuille de calcul Excel](/cells/images/ole-object-example.png)

**Codes d’état HTTP possibles**

| Code | Description                                           |
|------|-------------------------------------------------------|
| 200  | Objet OLE ajouté avec succès.                         |
| 400  | Requête incorrecte – paramètres manquants ou invalides. |
| 401  | Non autorisé – jeton JWT invalide ou manquant.        |
| 404  | Introuvable – le classeur, la feuille de calcul ou le fichier source n’existe pas. |
| 500  | Erreur interne du serveur – échec inattendu.          |

Une réponse réussie typique renvoie la charge utile JSON suivante :

```json
{
  "Code": 200,
  "Status": "OK",
  "Data": {
    "OleObjectId": "12345",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Width": 400,
    "Height": 400,
    "SourceFullName": "Sample_Book2.xls",
    "ImageSourceFullName": "aspose-logo.png"
  }
}
```

## Famille de SDK Cloud

L’utilisation d’un SDK accélère le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}