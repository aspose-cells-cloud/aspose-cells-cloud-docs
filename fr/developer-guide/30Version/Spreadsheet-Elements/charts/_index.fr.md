---
title: "Travailler avec les graphiques Excel"
second_title: "Document"
linktype: "Graphiques"
type: docs
url: /fr/charts/
aliases: [  /fr/working-with-charts/ ]
keywords: "Aspose, Cells, Excel, graphique, API, REST, Cloud, feuille de calcul"
description: "Découvrez comment gérer les graphiques Excel à l’aide de l’API Aspose.Cells Cloud. Guides pas à pas, exemples de code et gestion des erreurs pour récupérer, ajouter, mettre à jour, supprimer et convertir des graphiques en images."
weight: 100
ArticleTitle: "Travailler avec les graphiques Excel – Documentation Aspose.Cells Cloud"
---

## Travailler avec des graphiques dans un fichier Excel

**Dernière mise à jour :** juillet 2026  

Les graphiques Excel sont des représentations visuelles des données qui aident les utilisateurs à comprendre rapidement les tendances et les motifs.  
L’API Aspose.Cells Cloud permet aux développeurs de manipuler programmatically ces graphiques présents dans des classeurs Excel stockés dans le cloud. Grâce à cette API, vous pouvez récupérer les graphiques existants, en ajouter de nouveaux, modifier leurs propriétés (par exemple titres, axes et légendes), supprimer les graphiques indésirables, et convertir les graphiques en formats d’image pour la production de rapports ou le traitement ultérieur. Les liens suivants vous donnent un accès direct aux pages détaillant chaque opération prise en charge liée aux graphiques.

### Référence rapide

| Opération | Méthode HTTP | Endpoint (modèle) | Documentation |
|-----------|-------------|-------------------|---------------|
| Récupérer un graphique | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Récupérer un graphique à partir d’une feuille de calcul](/cells/get-chart-from-a-worksheet/) |
| Ajouter un graphique | POST | `/cells/{file}/worksheets/{sheet}/charts` | [Ajouter un graphique dans une feuille de calcul](/cells/add-a-chart-in-a-worksheet/) |
| Supprimer tous les graphiques | DELETE | `/cells/{file}/worksheets/{sheet}/charts` | [Supprimer tous les graphiques d’une feuille de calcul](/cells/delete-all-charts-from-a-worksheet/) |
| Supprimer un graphique | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Supprimer un graphique d’une feuille de calcul](/cells/delete-a-chart-from-a-worksheet/) |
| Convertir un graphique en image | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/image` | [Convertir un graphique en image](/cells/convert-chart-to-image/) |
| Récupérer la zone du graphique | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area` | [Récupérer la zone du graphique dans une feuille de calcul](/cells/get-chart-area-from-a-worksheet/) |
| Récupérer le format de remplissage | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area/fillformat` | [Récupérer le format de remplissage de la zone d’un graphique dans une feuille de calcul](/cells/get-fill-format-of-a-chart-area-from-a-worksheet/) |
| Récupérer la légende | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [Récupérer la légende d’un graphique dans une feuille de calcul](/cells/get-chart-legend-from-a-worksheet/) |
| Mettre à jour la légende | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [Mettre à jour la légende d’un graphique dans une feuille de calcul](/cells/update-chart-legend-in-a-worksheet/) |
| Afficher la légende | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/show` | [Afficher la légende d’un graphique dans une feuille de calcul](/cells/show-chart-legend-in-a-worksheet/) |
| Masquer la légende | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/hide` | [Masquer la légende d’un graphique dans une feuille de calcul](/cells/hide-chart-legend-in-a-worksheet/) |
| Récupérer le titre | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Récupérer le titre du graphique depuis une feuille de calcul](/cells/get-chart-title-from-a-worksheet/) |
| Définir le titre | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Définir le titre du graphique dans une feuille de calcul Excel](/cells/set-chart-title-in-excel-worksheet/) |
| Mettre à jour le titre | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Mettre à jour le titre du graphique dans une feuille de calcul Excel](/cells/update-chart-title-in-excel-worksheet/) |
| Supprimer le titre | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Supprimer le titre du graphique dans une feuille de calcul](/cells/delete-chart-title-in-a-worksheet/) |
| Mettre à jour les propriétés du graphique | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Mettre à jour les propriétés du graphique](/cells/charts/properties/update/) |
| Récupérer l’axe des catégories | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [Récupérer l’axe des catégories du graphique](/cells/charts/category-axis/get/) |
| Récupérer l’axe des valeurs | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [Récupérer l’axe des valeurs du graphique](/cells/charts/value-axis/get/) |
| Récupérer le second axe des catégories | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [Récupérer le second axe des catégories du graphique](/cells/charts/second-category-axis/get/) |
| Récupérer le second axe des valeurs | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [Récupérer le second axe des valeurs du graphique](/cells/charts/second-value-axis/get/) |
| Mettre à jour l’axe des catégories | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [Mettre à jour l’axe des catégories du graphique](/cells/charts/category-axis/update/) |
| Mettre à jour l’axe des valeurs | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [Mettre à jour l’axe des valeurs du graphique](/cells/charts/value-axis/update/) |
| Mettre à jour le second axe des catégories | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [Mettre à jour le second axe des catégories du graphique](/cells/charts/second-category-axis/update/) |
| Mettre à jour le second axe des valeurs | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [Mettre à jour le second axe des valeurs du graphique](/cells/charts/second-value-axis/update/) |

- [Récupérer un graphique à partir d’une feuille de calcul](/cells/get-chart-from-a-worksheet/)
- [Ajouter un graphique dans une feuille de calcul](/cells/add-a-chart-in-a-worksheet/)
- [Supprimer tous les graphiques d’une feuille de calcul](/cells/delete-all-charts-from-a-worksheet/)
- [Supprimer un graphique d’une feuille de calcul](/cells/delete-a-chart-from-a-worksheet/)
- [Convertir un graphique en image](/cells/convert-chart-to-image/)
- [Récupérer la zone du graphique dans une feuille de calcul](/cells/get-chart-area-from-a-worksheet/)
- [Récupérer le format de remplissage de la zone d’un graphique dans une feuille de calcul](/cells/get-fill-format-of-a-chart-area-from-a-worksheet/)
- [Récupérer la légende d’un graphique dans une feuille de calcul](/cells/get-chart-legend-from-a-worksheet/)
- [Mettre à jour la légende d’un graphique dans une feuille de calcul](/cells/update-chart-legend-in-a-worksheet/)
- [Afficher la légende d’un graphique dans une feuille de calcul](/cells/show-chart-legend-in-a-worksheet/)
- [Masquer la légende d’un graphique dans une feuille de calcul](/cells/hide-chart-legend-in-a-worksheet/)
- [Récupérer le titre du graphique depuis une feuille de calcul](/cells/get-chart-title-from-a-worksheet/)
- [Définir le titre du graphique dans une feuille de calcul Excel](/cells/set-chart-title-in-excel-worksheet/)
- [Mettre à jour le titre du graphique dans une feuille de calcul Excel](/cells/update-chart-title-in-excel-worksheet/)
- [Supprimer le titre du graphique dans une feuille de calcul](/cells/delete-chart-title-in-a-worksheet/)
- [Mettre à jour les propriétés du graphique](/cells/charts/properties/update/)
- [Récupérer l’axe des catégories du graphique](/cells/charts/category-axis/get/)
- [Récupérer l’axe des valeurs du graphique](/cells/charts/value-axis/get/)
- [Récupérer le second axe des catégories du graphique](/cells/charts/second-category-axis/get/)
- [Récupérer le second axe des valeurs du graphique](/cells/charts/second-value-axis/get/)
- [Mettre à jour l’axe des catégories du graphique](/cells/charts/category-axis/update/)
- [Mettre à jour l’axe des valeurs du graphique](/cells/charts/value-axis/update/)
- [Mettre à jour le second axe des catégories du graphique](/cells/charts/second-category-axis/update/)
- [Mettre à jour le second axe des valeurs du graphique](/cells/charts/second-value-axis/update/)