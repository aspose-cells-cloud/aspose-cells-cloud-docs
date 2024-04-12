---
title: PageSetu
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/pagesetup/
description: "Aspose.Cells Spécification du modèle cloud : PageSetup. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
weight: 50
---
## **mise en page**

 

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Noir et blanc| Booléen| Vrai| FAUX|| Représente si les éléments du document seront imprimés en noir et blanc.|
| Marge inférieure| Flottant| Vrai| FAUX|| Représente la taille de la marge inférieure, en unités de centimètres.|
| CentreHorizontalement| Booléen| Vrai| FAUX|| Représente si la feuille est imprimée centrée horizontalement.|
| CentreVerticalement| Booléen| Vrai| FAUX|| Représente si la feuille est imprimée centrée verticalement.|
| Numéro de première page| Entier| Vrai| FAUX|| Représente le numéro de la première page qui sera utilisée lors de l'impression de cette feuille.|
| Ajuster Aux PagesGrandes| Entier| Vrai| FAUX|| Représente le nombre de pages en hauteur sur lequel la feuille de calcul sera mise à l'échelle lors de son impression. La valeur par défaut est 1.|
| Ajuster aux pages larges| Entier| Vrai| FAUX||Représente le nombre de pages de largeur sur lequel la feuille de calcul sera mise à l'échelle lors de son impression. La valeur par défaut est 1.|
| Marge de pied de page| Flottant| Vrai| FAUX|| Représente la distance entre le bas de la page et le pied de page, en unités de centimètres.|
| Marge d'en-tête| Flottant| Vrai| FAUX|| Représente la distance entre le haut de la page et l'en-tête, en unités de centimètres.|
| EstAutoFirstPageNumber| Booléen| Vrai| FAUX|| Indique si le premier numéro de page est automatiquement attribué.|
| IsHFAlignMargins| Booléen| Vrai| FAUX|| Indique si les marges d'en-tête et de pied de page sont alignées avec les marges de la page. Si cette propriété est vraie, l'en-tête et le pied de page gauche seront alignés avec la marge gauche, et l'en-tête et le pied de page droits seront alignés avec la marge droite. Cette option est activée par défaut.|
| EstHFDiffFirst| Booléen| Vrai| FAUX|| True signifie que l'en-tête/pied de page de la première page est différent de celui des autres pages.|
| EstHFDiffOddEven| Booléen| Vrai| FAUX||True signifie que l'en-tête/pied de page des pages impaires est différent des pages impaires.|
| IsHFScaleWithDoc| Booléen| Vrai| FAUX|| Indique si l'en-tête et le pied de page sont mis à l'échelle avec la mise à l'échelle du document. S'applique uniquement au Excel 2007.|
| IsPercentScale| Booléen| Vrai| FAUX|| Si cette propriété est False, les propriétés FitToPagesWide et FitToPagesTall contrôlent la façon dont la feuille de calcul est mise à l'échelle.|
| Marge de gauche| Flottant| Vrai| FAUX|| Représente la taille de la marge gauche, en unités de centimètres.|
| Commande| Chaîne| Vrai| FAUX|| Représente l'ordre que Microsoft Excel utilise pour numéroter les pages lors de l'impression d'une grande feuille de calcul.|
| Orientation| Chaîne| Vrai| FAUX|| Représente l’orientation d’impression de la page.|
| Taille de papier| Chaîne| Vrai| FAUX|| Représente la taille du papier.|
| Zone d'impression| Chaîne| Vrai| FAUX|| Représente la plage à imprimer.|
| ImprimerCommentaires| Chaîne| Vrai| FAUX|| Représente la façon dont les commentaires sont imprimés avec la feuille.|
| Imprimer des copies| Entier| Vrai| FAUX|| Obtenez et définissez le nombre de copies à imprimer.|
| ImprimerBrouillon| Booléen| Vrai| FAUX|| Indique si la feuille sera imprimée sans graphiques.|
| Erreurs d'impression| Chaîne| Vrai| FAUX||Spécifie le type d'erreur d'impression affichée.|
| ImprimerGridlines| Booléen| Vrai| FAUX|| Indique si le quadrillage des cellules est imprimé sur la page.|
| Imprimer les titres| Booléen| Vrai| FAUX|| Indique si les en-têtes de lignes et de colonnes sont imprimés avec cette page.|
| Qualité d'impression| Entier| Vrai| FAUX|| Représente la qualité d’impression.|
| ImprimerTitreColonnes| Chaîne| Vrai| FAUX|| Représente les colonnes contenant les cellules à répéter sur le côté gauche de chaque page.|
| ImprimerTitleRows| Chaîne| Vrai| FAUX|| Représente les lignes contenant les cellules à répéter en haut de chaque page.|
| Marge droite| Flottant| Vrai| FAUX|| Représente la taille de la marge droite, en unités de centimètres.|
| Marge supérieure| Flottant| Vrai| FAUX|| Représente la taille de la marge supérieure, en unités de centimètres.|
| Zoom| Entier| Vrai| FAUX|| Représente le facteur d’échelle en pourcentage. Il devrait être compris entre 10 et 400.|
| Entête| Récipient| Vrai| FAUX|| Représente l'en-tête de la page.|
| Bas de page| Récipient| Vrai| FAUX|| Représente le pied de page.|
| lien| Classe : Lien| Vrai| FAUX|||

**Nom du parent** : (LinkElement)[linkelement]