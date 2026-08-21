---
title: "Effacer les liens hypertexte"
type: docs
url: /hyperlinks/clear/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, effacer les liens hypertexte, supprimer les liens hypertexte, API REST, feuille de calcul, SDK"
description: "Découvrez comment supprimer tous les liens hypertexte d'une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud ou de l'un des SDK pris en charge (C#, Java, Python, Node.js, Go, PHP, Ruby, Perl, etc.)."
weight: 40
ArticleTitle: "Effacer les liens hypertexte – Documentation de l'API Aspose.Cells Cloud"
---

Cette API REST supprime **tous les liens hypertexte** d'une feuille de calcul Excel.

## Sécurité et authentification
Les API Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                  |
| ---------------- | ------ | ----------- | -------------------------------------------- |
| name             | string | path        | Le nom du fichier Excel.                     |
| sheetName        | string | path        | Le nom de la feuille de calcul.              |
| folder           | string | query       | Le dossier contenant le document.            |
| storageName      | string | query       | Le nom du service de stockage.               |

### Réponses d’erreur

| Code HTTP | Raison                                                   | Corps d’exemple                                                                 |
| --------- | -------------------------------------------------------- | ------------------------------------------------------------------------------- |
| **400**   | Requête incorrecte – paramètres manquants ou non valides. | `{ "Code":"400", "Message":"Valeur de paramètre non valide." }`                |
| **401**   | Non autorisé – jeton JWT manquant ou non valide.         | `{ "Code":"401", "Message":"Le jeton d’accès est manquant ou non valide." }`   |
| **404**   | Introuvable – classeur ou feuille de calcul inexistante. | `{ "Code":"404", "Message":"Fichier introuvable." }`                           |
| **500**   | Erreur interne du serveur – défaillance serveur inattendue. | `{ "Code":"500", "Message":"Une erreur inattendue s’est produite." }`         |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlinks) définit une interface de programmation publiquement accessible, vous permettant d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour appeler les services web Aspose.Cells. L’exemple ci-dessous montre comment supprimer tous les liens hypertexte d’une feuille de calcul.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
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

## Famille de SDK Cloud

L’utilisation d’un SDK accélère le développement en gérant les détails de bas niveau pour vous. Pour obtenir la liste complète des SDK Aspose.Cells Cloud, rendez-vous sur le [dépôt GitHub](https://github.com/aspose-cells-cloud).

Les exemples de code suivants montrent comment supprimer les liens hypertexte d’une feuille de calcul à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}