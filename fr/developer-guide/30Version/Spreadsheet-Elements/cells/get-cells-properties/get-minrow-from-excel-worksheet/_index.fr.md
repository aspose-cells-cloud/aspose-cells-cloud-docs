---
title: "Obtenir MinRow à partir d’une feuille Excel – Référence de l’API Aspose.Cells Cloud"
type: docs
url: /fr/get-minrow-from-excel-worksheet/
weight: 80
keywords: "Aspose.Cells, GetMinRow, feuille Excel, API REST, index de ligne minimale, SDK cloud"
description: "Découvrez comment récupérer l’index de ligne minimal d’une feuille à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut une requête cURL complète avec authentification, le schéma de réponse et des exemples de SDK pour plusieurs langages."
ArticleTitle: "Obtenir MinRow à partir d’une feuille Excel – Référence de l’API Aspose.Cells Cloud"
---

Cette API REST renvoie l’index de ligne minimal dans une feuille Excel lorsque le paramètre `cellOrMethodName` est défini sur `minrow`. L’endpoint peut être utilisé pour déterminer la première ligne non vide (indexée à partir de zéro) dans une feuille donnée.

- **Exemple cURL :**

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/minrow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "MinRow": 0
}
```

{{< /tab >}}

{{< /tabs >}}

**Requête**

```
GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/minrow
```

| Propriété          | Type   | Obligatoire | Description                                            |
|--------------------|--------|-------------|--------------------------------------------------------|
| `fileName`         | string | Oui         | Nom du classeur (par exemple, `myWorkbook.xlsx`).     |
| `sheetName`        | string | Oui         | Feuille cible (par exemple, `Sheet1`).                |
| `cellOrMethodName` | string | Oui         | Valeur fixe `minrow`.                                  |
| `folder`           | string | Non         | Chemin du dossier dans le stockage cloud.             |
| `storageName`      | string | Non         | Nom du stockage utilisé si ce n’est pas le stockage par défaut. |

**Réponse**

Le service renvoie un objet JSON contenant la propriété `MinRow`, indiquant l’index de la première ligne non vide (indexée à partir de zéro).

| Code HTTP | Signification                                     |
|-----------|---------------------------------------------------|
| 200       | Succès – charge utile JSON avec `MinRow`.        |
| 401       | Non autorisé – jeton invalide ou manquant.       |
| 404       | Classeur ou feuille introuvable.                 |
| 500       | Erreur interne du serveur.                       |

La valeur `MinRow` est utile lorsqu’il s’agit de localiser rapidement le début des données dans une feuille.

- **Utiliser les SDK Aspose.Cells Cloud**

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9497c39cde5cecb6709ff5feb2ab2b8" >}}

{{< /tab >}}

{{< /tabs >}}