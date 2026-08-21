---
title: "Obtenir MaxRow à partir d'une feuille de calcul Excel"
type: docs
url: /get-maxrow-from-excel-worksheet/
weight: 40
ArticleTitle: "Récupérer le numéro de ligne maximal dans une feuille de calcul Excel – API Aspose.Cells Cloud"
keywords: "Aspose.Cells, Excel, MaxRow, API REST, SDK cloud, classeur, feuille de calcul, GetMaxRow"
description: "Découvrez comment récupérer le numéro de ligne maximal d'une feuille de calcul dans un fichier Excel à l'aide de l'API REST Aspose.Cells Cloud. Inclut la syntaxe de requête, le schéma de réponse, les exemples de SDK et les notes d'utilisation."
---

Cet appel REST renvoie le **numéro de ligne maximal** dans une feuille de calcul Excel lorsque le paramètre `cellOrMethodName` est défini sur `maxrow`.

- **Exemple cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxrow" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxRow": 1048576
}
```

{{< /tab >}}

{{< /tabs >}}

- **Utiliser les SDK Aspose.Cells Cloud**

L'utilisation d'un SDK constitue la méthode la plus efficace pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur la logique de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "afcfd72b172e9c3e2d283a9ac059c8c7" >}}

{{< /tab >}}

{{< /tabs >}}

**Référence de l'API**

| Élément | Détails |
|--------|---------|
| **Méthode** | `GET` |
| **Point de terminaison** | `/cells/{fileName}/worksheets/{sheetName}/cells/maxrow` |
| **Paramètres de chemin** | `fileName` – nom du fichier Excel (obligatoire) <br> `sheetName` – nom de la feuille de calcul (obligatoire) |
| **Paramètres de requête** | `folder` – chemin du dossier dans le stockage (facultatif) <br> `storageName` – nom du stockage (facultatif) |
| **Réponse en cas de succès** | `200 OK` <br> ```json { "MaxRow": entier } ``` |
| **Réponses d’erreur** | `400 Bad Request` – paramètres invalides <br> `401 Unauthorized` – échec d’authentification <br> `404 Not Found` – fichier ou feuille de calcul introuvable |

**Prérequis**

- Un jeton d'authentification valide Aspose Cloud.  
- Le classeur cible doit être téléchargé dans le stockage Aspose Cloud ou accessible via une URL publique.  

**Notes**

- Cette opération est disponible à partir de la version **v3.0** de l'API.  
- La valeur renvoyée `MaxRow` correspond à l'index le plus élevé de ligne utilisée (basé sur 1). Pour une feuille de calcul vide, la valeur est généralement `1`.  

Les exemples de SDK suivants illustrent comment invoquer cette opération dans différents langages de programmation.