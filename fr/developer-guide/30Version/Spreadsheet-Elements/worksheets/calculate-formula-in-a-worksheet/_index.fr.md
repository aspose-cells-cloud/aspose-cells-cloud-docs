---
title: "Calculer une formule dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Calculer"
type: docs
url: /fr/worksheets/calculate-formula/
aliases: [  /fr/calculate-formula-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, calcul de formule, API REST, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift"
description: "Calculer les formules dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Prend en charge plusieurs SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift) avec des exemples prêts à l’emploi."
weight: 20
ArticleTitle: "Calculer une formule dans une feuille de calcul Excel – Documentation Aspose.Cells Cloud"
---

Cette API REST renvoie la **valeur calculée d’une formule** dans une feuille de calcul. Elle permet d’**évaluer directement une formule Excel** depuis votre application.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/formulaResult
```

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                          |
| ---------------- | ------ | ----------- | ---------------------------------------------------- |
| name             | string | path        | Nom du fichier Excel.                                |
| sheetName        | string | path        | Nom de la feuille de calcul contenant la formule.    |
| formula          | string | query       | Formule à évaluer (par exemple, `SUM(A5:A10)`).      |
| folder           | string | query       | Dossier dans lequel le document est stocké.          |
| storageName      | string | query       | Nom du service de stockage (le cas échéant).         |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetCalculateFormula) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

### Authentification

Toutes les requêtes doivent inclure un **jeton Bearer JWT valide** dans l’en-tête `Authorization` :

```
Authorization: Bearer <votre_jeton_jwt>
```

Vous pouvez obtenir un jeton en suivant le flux OAuth 2.0 décrit dans le guide d’authentification d’Aspose.Cells Cloud.

### Codes d’état de réponse possibles

| Code | Description                                           |
|------|-------------------------------------------------------|
| 200  | Requête réussie ; la valeur de la formule est renvoyée. |
| 400  | Requête incorrecte – paramètres manquants ou invalides. |
| 401  | Non autorisé – jeton JWT invalide ou manquant.        |
| 404  | Non trouvé – le fichier ou la feuille de calcul spécifié n’existe pas. |
| 500  | Erreur interne du serveur – condition inattendue sur le serveur. |

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour appeler facilement les services web Aspose.Cells Cloud. L’exemple ci-dessous montre comment demander le résultat d’une formule avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet2/formulaResult?formula=SUM(A5:A10)" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton_jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Value": {
    "Value": "0"
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour intégrer l’API. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "d1a2b3c4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a1b2c3d4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "b1c2d3e4f5g67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c1d2e3f4g5h67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "d1e2f3g4h5i67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e1f2g3h4i5j67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f1g2h3i4j5k67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "g1h2i3j4k5l67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

**Voir aussi :**  
- [Obtenir une feuille de calcul](https://docs.aspose.cloud/cells/worksheets/get-worksheet/)  
- [Mettre à jour une feuille de calcul](https://docs.aspose.cloud/cells/worksheets/update-worksheet/)  
- [Calculer toutes les formules](https://docs.aspose.cloud/cells/worksheets/calculate-all-formulas/)  
---