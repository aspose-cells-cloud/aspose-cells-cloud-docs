---
title: Obtenez Cells Propriété
type: docs
url: /fr/get-cells-properties/
weight: 130
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Obtenir les propriétés Cells
---
Ce REST API indique comment utiliser `get a specific cell` dans un fichier Excel.

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| Nom du document.|
| nom de la feuille| chaîne| chemin| Nom de la feuille de calcul.|
| nom de cellule ou de méthode| chaîne| chemin|Nom de la cellule ou de la méthode. (Valeur du nom de la méthode : firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn et cellName.)|
| dossier| chaîne| requête| Dossier du document.|
| nom de stockage| chaîne| requête| nom de stockage.|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

### **Famille de SDK Cloud**

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

### **Comment obtenir une cellule spécifique**

- [Obtenir des données de cellule à partir d'une feuille de calcul](/cells/fr/get-cell-data-from-a-worksheet/)
- [Feuille de travail « Obtenir la première cellule de Excel »](/cells/fr/get-first-cell-from-excel-worksheet/)
- [Obtenir la dernière cellule de la feuille de calcul Excel](/cells/fr/get-last-cell-of-excel-worksheet/)
- [Obtenir MaxRow à partir de la feuille de calcul Excel](/cells/fr/get-maxrow-from-excel-worksheet/)
- [Obtenir MaxDataRow à partir de la feuille de calcul Excel](/cells/fr/get-maxdatarow-from-excel-worksheet/)
- [Obtenir MaxColumn à partir de la feuille de calcul Excel](/cells/fr/get-maxcolumn-from-excel-worksheet/)
- [Obtenir MaxDataColumn à partir de la feuille de calcul Excel](/cells/fr/get-maxdatacolumn-from-excel-worksheet/)
- [Obtenir MinRow à partir de la feuille de calcul Excel](/cells/fr/get-minrow-from-excel-worksheet/)
- [Obtenir MinDataRow à partir de la feuille de calcul Excel](/cells/fr/get-mindatarow-from-excel-worksheet/)
- [Obtenir MinColumn à partir de la feuille de calcul Excel](/cells/fr/get-mincolumn-from-excel-worksheet/)
- [Obtenir MinDataColumn à partir de la feuille de calcul Excel](/cells/fr/get-mindatacolumn-from-excel-worksheet/)
