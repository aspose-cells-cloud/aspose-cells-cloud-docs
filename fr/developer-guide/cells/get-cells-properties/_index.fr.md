---
title: Obtenir la propriété Cells
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
 
| Le nom du paramètre| Taper| Chemin/chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| Nom du document.|
| NomFeuille| chaîne| chemin| Nom de la feuille de calcul.|
| cellOrMethodNamecellOrMethodName| chaîne| chemin| Le nom de la cellule ou de la méthode. (Valeur du nom de la méthode : firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn et cellName.)|
| dossier| chaîne| mettre en doute| Dossier du document.|
| nom_stockage| chaîne| mettre en doute| nom de stockage.|
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.


- **Comment obtenir une cellule spécifique**

   - [Obtenir des données de cellule à partir d'une feuille de calcul](/cells/fr/get-cell-data-from-a-worksheet/)
   - [Obtenir la première cellule de la feuille de calcul Excel](/cells/fr/get-first-cell-from-excel-worksheet/)
   - [Obtenir la dernière cellule de la feuille de calcul Excel](/cells/fr/get-last-cell-of-excel-worksheet/)
   - [Obtenir MaxRow à partir de la feuille de calcul Excel](/cells/fr/get-maxrow-from-excel-worksheet/)
   - [Obtenir MaxDataRow à partir de la feuille de calcul Excel](/cells/fr/get-maxdatarow-from-excel-worksheet/)
   - [Obtenir MaxColumn à partir de la feuille de calcul Excel](/cells/fr/get-maxcolumn-from-excel-worksheet/)
   - [Obtenir MaxDataColumn à partir de la feuille de calcul Excel](/cells/fr/get-maxdatacolumn-from-excel-worksheet/)
   - [Obtenir MinRow à partir de la feuille de calcul Excel](/cells/fr/get-minrow-from-excel-worksheet/)
   - [Obtenir MinDataRow à partir de la feuille de calcul Excel](/cells/fr/get-mindatarow-from-excel-worksheet/)
   - [Obtenir MinColumn à partir de la feuille de calcul Excel](/cells/fr/get-mincolumn-from-excel-worksheet/)
   - [Obtenir MinDataColumn à partir de la feuille de calcul Excel](/cells/fr/get-mindatacolumn-from-excel-worksheet/)
