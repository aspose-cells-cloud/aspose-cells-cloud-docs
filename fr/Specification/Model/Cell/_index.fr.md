---
title: Cellule
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/cell/
description: "Aspose.Cells Spécification du modèle Cloud : Cell. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
weight: 50
---
## **cellule**

 

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Nom| Chaîne| Vrai| FAUX|| Obtient le nom de la cellule.|
| Rangée| Entier| Vrai| FAUX|| Obtient le numéro de ligne (base zéro) de la cellule.|
| Colonne| Entier| Vrai| FAUX|| Obtient le numéro de colonne (base zéro) de la cellule.|
| Valeur| Chaîne| Vrai| FAUX|| Obtient la valeur contenue dans cette cellule.|
| Taper| Chaîne| Vrai| FAUX|| Représente le type de valeur de cellule.|
|Formule| Chaîne| Vrai| FAUX|| Obtient ou définit une formule du .|
| EstFormule| Booléen| Vrai| FAUX|| Représente si la cellule spécifiée contient une formule.|
| Estfusionné| Booléen| Vrai| FAUX|| Vérifie si une cellule fait partie d'une plage fusionnée ou non.|
| EstArrayHeader| Booléen| Vrai| FAUX|| Indique que la formule de la cellule est une formule matricielle et qu'il s'agit de la première cellule du tableau.|
| EstDansArray| Booléen| Vrai| FAUX|| Indique si la formule de cellule est une formule matricielle.|
| EstErrorValue| Booléen| Vrai| FAUX|| Vérifie si la valeur de cette cellule est une erreur.|
| EstDansTable| Booléen| Vrai| FAUX|| Indique si cette cellule fait partie de la formule du tableau.|
| EstStyleSet| Booléen| Vrai| FAUX|| Indique si le style de la cellule est défini. Si renvoie false, cela signifie que cette cellule a un format de cellule par défaut.|
| Chaîne HTML| Chaîne| Vrai| FAUX|| Obtient et définit la chaîne HTML qui contient des données et certains formats dans cette cellule.|
| Style| Classe : LinkElement| Vrai| FAUX|||
| Feuille de travail| Chaîne| Vrai| FAUX|| Obtient la feuille de calcul parent.|
| lien| Classe : Lien| Vrai| FAUX|||

**Nom du parent** : (LinkElement)[linkelement]