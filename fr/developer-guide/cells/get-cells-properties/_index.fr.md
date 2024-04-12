---
title: Obtenez la propriété Cells
type: docs
url: /fr/get-cells-properties/
weight: 130
---
Ce REST API indique comment `get a specific cell` dans un fichier Excel.

## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```
 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| Nom du document.|
| Nom de la feuille| chaîne| chemin| Nom de la feuille de calcul.|
| celluleOuNoMéthode| chaîne| chemin|Le nom de la cellule ou de la méthode. (Valeur du nom de la méthode : firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn et cellName.)|
| dossier| chaîne| requête| Dossier du document.|
| Nom de stockage| chaîne| requête| nom de stockage.|
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement depuis un navigateur Web.


- **Comment obtenir une cellule spécifique**

   - [Obtenir des données cellulaires à partir d'une feuille de calcul](/cells/fr/get-cell-data-from-a-worksheet/)
   - [Obtenir la première cellule de la feuille de calcul Excel](/cells/fr/get-first-cell-from-excel-worksheet/)
   - [Obtenir la dernière cellule de la feuille de calcul Excel](/cells/fr/get-last-cell-of-excel-worksheet/)
   - [Obtenez MaxRow à partir de la feuille de calcul Excel](/cells/fr/get-maxrow-from-excel-worksheet/)
   - [Obtenez MaxDataRow à partir de la feuille de calcul Excel](/cells/fr/get-maxdatarow-from-excel-worksheet/)
   - [Obtenez MaxColumn à partir de la feuille de calcul Excel](/cells/fr/get-maxcolumn-from-excel-worksheet/)
   - [Obtenez MaxDataColumn à partir de la feuille de calcul Excel](/cells/fr/get-maxdatacolumn-from-excel-worksheet/)
   - [Obtenez MinRow à partir de la feuille de calcul Excel](/cells/fr/get-minrow-from-excel-worksheet/)
   - [Obtenez MinDataRow à partir de la feuille de calcul Excel](/cells/fr/get-mindatarow-from-excel-worksheet/)
   - [Obtenez MinColumn à partir de la feuille de calcul Excel](/cells/fr/get-mincolumn-from-excel-worksheet/)
   - [Obtenez MinDataColumn à partir de la feuille de calcul Excel](/cells/fr/get-mindatacolumn-from-excel-worksheet/)
