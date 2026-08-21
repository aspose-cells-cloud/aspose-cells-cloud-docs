---
title: "Supprimer un filtre d'une feuille Excel – API Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Supprimer un filtre"
type: docs
url: /fr/delete-filter/
aliases: [  /fr/delete-a-filter-for-a-filter-column/ , /fr/delete-auto-filter/ ]
keywords: "Aspose.Cells Cloud supprimer filtre, Excel, API REST, SDK"
description: "Découvrez comment supprimer un filtre automatique d'une feuille Excel à l'aide de l'API REST Aspose.Cells Cloud, de cURL et des SDK (C#, Java, Python, etc.). Inclut l'URL du point de terminaison, les paramètres, l'authentification et des exemples de code."
weight: 100
---

## API REST

Cette API REST supprime un **filtre automatique** sur une feuille Excel.

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre         | Type    | Emplacement | Obligatoire ? | Description                                                                                              |
| ------------------------ | ------- | ----------- | ------------- | -------------------------------------------------------------------------------------------------------- |
| **name**                 | string  | Path        | Oui           | Nom du classeur.                                                                                         |
| **sheetName**            | string  | Path        | Oui           | Nom de la feuille de calcul.                                                                             |
| **range**                | string  | Query       | Non           | Plage de cellules à laquelle le filtre s'applique (par exemple, `A1:C10`).                               |
| **fieldIndex**           | integer | Query       | Oui           | Index à base zéro de la colonne à laquelle le filtre est appliqué.                                       |
| **dateTimeGroupingType** | string  | Query       | Non           | Mode de regroupement des valeurs de date/heure : `Day` (jour), `Hour` (heure), `Minute` (minute), `Month` (mois), `Second` (seconde) ou `Year` (année). |
| **year**                 | integer | Query       | Non           | Composante année pour le regroupement par date.                                                          |
| **month**                | integer | Query       | Non           | Composante mois pour le regroupement par date.                                                           |
| **day**                  | integer | Query       | Non           | Composante jour pour le regroupement par date.                                                           |
| **hour**                 | integer | Query       | Non           | Composante heure pour le regroupement par date.                                                          |
| **minute**               | integer | Query       | Non           | Composante minute pour le regroupement par date.                                                         |
| **second**               | integer | Query       | Non           | Composante seconde pour le regroupement par date.                                                        |
| **matchBlanks**          | boolean | Query       | Non           | `true` / `false` – indique si les cellules vides sont incluses dans le filtre.                          |
| **refresh**              | boolean | Query       | Non           | `true` / `false` – indique s’il faut actualiser la feuille de calcul après suppression.                 |
| **folder**               | string  | Query       | Non           | Dossier d'origine du classeur.                                                                           |
| **storageName**          | string  | Query       | Non           | Nom du stockage.                                                                                         |

### **Réponse**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre supprimé avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                             |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la taille maximale autorisée.                |
| 500  | Erreur interne du serveur    | Erreur serveur inattendue.                                                  |

## Comment utiliser l'API DeleteWorksheetFilter avec les SDK

### Spécification de l’API DeleteWorksheetFilter

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&dateTimeGroupingType=Year" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L'utilisation d'un SDK est la méthode la plus efficace pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

---