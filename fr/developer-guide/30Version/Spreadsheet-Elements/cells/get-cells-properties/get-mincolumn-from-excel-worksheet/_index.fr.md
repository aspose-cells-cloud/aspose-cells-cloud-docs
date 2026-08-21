---
title: "Obtenir MinColumn à partir d'une feuille Excel"
type: docs
url: /get-mincolumn-from-excel-worksheet/
weight: 100
keywords: Excel, Aspose.Cells Cloud, REST API, Get MinColumn, Worksheet, SDK, Cloud API
description: Récupérer l'index minimal de colonne contenant des données dans une feuille d’un fichier Excel via l’API REST Aspose.Cells Cloud.
ArticleTitle: "Obtenir MinColumn à partir d'une feuille Excel - Aspose.Cells Cloud API"
---

Cet API REST renvoie l'index minimal de colonne contenant des données dans une feuille Excel lorsque le paramètre `cellOrMethodName` est défini sur `mincolumn`.

- **Exemple cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mincolumn" \
     -H "Authorization: Bearer <VOTRE_JETON_D’ACCÈS>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**Détails de la requête**

| Paramètre | Type | Obligatoire | Description |
|-----------|------|-------------|-------------|
| `cellOrMethodName` | string | Oui | Valeur fixe `mincolumn` indiquant l’opération à effectuer. |
| `folder` | string | Non | Chemin vers le dossier contenant le classeur (si différent de la racine). |
| `storageName` | string | Non | Nom du stockage Aspose Cloud à utiliser. |

**Détails de la réponse**

L’API renvoie un objet JSON contenant une seule propriété :

```json
{
  "MinColumn": entier   // Index de la colonne la plus à gauche contenant des données (indexé à partir de zéro).
}
```

Codes d’état HTTP typiques :

- **200 OK** – Requête réussie, renvoie la valeur `MinColumn`.  
- **401 Unauthorized** – Jeton d’authentification manquant ou invalide.  
- **404 Not Found** – Le classeur, la feuille ou la plage de cellules spécifiée n’existe pas.  
- **500 Internal Server Error** – Erreur serveur inattendue.

- **Utiliser les SDK Aspose.Cells Cloud**

L’utilisation d’un SDK constitue la méthode la plus efficace pour développer. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur la logique métier de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "108bf3803d41abd988a29cdbd39aee44" >}}

{{< /tab >}}

{{< /tabs >}}