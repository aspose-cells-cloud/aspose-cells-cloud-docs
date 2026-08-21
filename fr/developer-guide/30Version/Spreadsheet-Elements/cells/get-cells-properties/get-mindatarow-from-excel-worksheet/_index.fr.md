---
title: "Obtenir MinDataRow à partir d'une feuille Excel"
type: docs
url: /fr/get-mindatarow-from-excel-worksheet/
weight: 90
keywords: "Aspose Cells, MinDataRow, API Excel, SDK cloud"
description: "Récupérer l'index de la première ligne contenant des données dans une feuille à l’aide de l’API Aspose.Cells Cloud v3.0. Inclut le modèle de requête, les paramètres, un exemple cURL, un exemple de réponse, les codes de statut HTTP et des extraits de SDK."
ArticleTitle: "Obtenir MinDataRow à partir d'une feuille Excel – Aspose.Cells Cloud API"
---

L'endpoint **Get MinDataRow** de l'**API Aspose.Cells Cloud v3.0** renvoie l'index de la première ligne contenant des données dans une feuille spécifiée. Cette opération nécessite un jeton d'accès valide (authentification Bearer) ainsi que le paramètre de requête `cellOrMethodName` défini sur `mindatarow`.

**Version de l’API : 3.0**

### Exemple cURL

La requête utilise la méthode HTTP GET. Remplacez les placeholders `{fileName}` et `{sheetName}` par les noms réels du classeur et de la feuille de calcul.

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/mindatarow?cellOrMethodName=mindatarow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**Paramètres de la requête**

| Paramètre          | Emplacement | Type   | Obligatoire | Description                                               |
|--------------------|-------------|--------|-------------|-----------------------------------------------------------|
| `fileName`         | Chemin      | string | Oui         | Nom du classeur Excel (avec extension).                  |
| `sheetName`        | Chemin      | string | Oui         | Nom de la feuille de calcul à l’intérieur du classeur.   |
| `cellOrMethodName` | Requête     | string | Oui         | Doit être défini sur `mindatarow` pour exécuter cette opération. |

**Exemple de réponse**

```json
{
  "MinDataRow": 5
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                              |
|------|-----------------------------|----------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                          |
| 413  | Charge utile trop grande    | Le fichier envoyé dépasse la limite de taille.          |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur.                        |

### Exemples de SDK

L'utilisation d'un SDK est la méthode la plus rapide pour développer. Un SDK gère les détails de bas niveau, afin que vous puissiez vous concentrer sur la logique de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "85f2a886ba296b8abf640c0638b4eec1" >}}

{{< /tab >}}

{{< /tabs >}}

**Voir aussi**

- [Obtenir MaxDataRow](https://docs.aspose.cloud/cells/fr/get-maxdatarow-from-excel-worksheet/)
- [Obtenir MinColumn](https://docs.aspose.cloud/cells/fr/get-mincolumn-from-excel-worksheet/)
- [Obtenir MaxColumn](https://docs.aspose.cloud/cells/fr/get-maxcolumn-from-excel-worksheet/)