---
title: FormatCondition
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/formatcondition/
description: "Aspose.Cells Spécification du modèle cloud : FormatCondition. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
kwords: Excel, Office, feuille de calcul, Cloud REST API, FormatCondition
weight: 50
---
## **formatCondition**

 Représente la condition de mise en forme conditionnelle.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Priorité| Entier| Vrai| FAUX||Priorité de cette règle de mise en forme conditionnelle. Cette valeur est utilisée pour déterminer quel format doit être évalué et rendu. Les valeurs numériques inférieures ont une priorité plus élevée que les valeurs numériques supérieures, où « 1 » est la priorité la plus élevée.|
| Taper| Chaîne| Vrai| FAUX|| Obtient et définit si le format conditionnel Type.|
| Arrêter si vrai| Booléen| Vrai| FAUX|| Certes, aucune règle de priorité inférieure ne peut être appliquée à cette règle lorsque celle-ci est évaluée comme vraie. S'applique uniquement au Excel 2007 ;|
| Au dessus de la moyenne| Classe : Au-dessus de la moyenne| Vrai| FAUX|| Obtenez l'instance "AboveAverage" de la mise en forme conditionnelle. La règle de l'instance par défaut met en évidence les cellules situées au-dessus de la moyenne pour toutes les valeurs de la plage. Valable uniquement pour le type = AboveAverage.|
| Échelle de couleurs| Classe : Échelle de couleurs| Vrai| FAUX||Obtenez l'instance "ColorScale" de la mise en forme conditionnelle. L'instance par défaut est un 3ColorScale "vert-jaune-rouge". Valable uniquement pour le type = ColorScale.|
| Barre de données| Classe : Barre de données| Vrai| FAUX|| Obtenez l'instance "DataBar" de la mise en forme conditionnelle. La couleur de l'instance par défaut est le bleu. Valable uniquement pour le type DataBar.|
| Formule 1| Chaîne| Vrai| FAUX|| Obtient et définit la valeur ou l'expression associée à la mise en forme conditionnelle.|
| Formule2| Chaîne| Vrai| FAUX|| Obtient et définit la valeur ou l'expression associée à la mise en forme conditionnelle.|
| Jeu d'icônes| Classe : IconSet| Vrai| FAUX|| Obtenez l'instance "IconSet" de la mise en forme conditionnelle. Le IconSetType de l’instance par défaut est TrafficLights31. Valable uniquement pour type = IconSet.|
| Opérateur| Chaîne| Vrai| FAUX|| Obtient et définit le type d'opérateur de format conditionnel.|
| Style| Classe : Style| Vrai| FAUX|| Obtient ou définit le style des plages de cellules mises en forme conditionnellement.|
| Texte| Chaîne| Vrai| FAUX||La valeur du texte dans une règle de mise en forme conditionnelle « le texte contient ». Valable uniquement pour type = containText, notContainsText, BeginsWith et EndsWith. La valeur par défaut est nulle.|
| Période de temps| Chaîne| Vrai| FAUX|| Période de temps applicable dans une règle de formatage conditionnel « date survenant… ». Valable uniquement pour type = timePeriod. La valeur par défaut est TimePeriodType.Today.|
| Top 10| Classe : Top10| Vrai| FAUX|| Obtenez l'instance "Top10" de la mise en forme conditionnelle. La règle de l'instance par défaut met en évidence les cellules dont les valeurs se situent dans la tranche des 10 premières. Valable uniquement pour le type Top10.|
| lien| Classe : Lien| Vrai| FAUX|||

**Nom du parent** : [LienÉlément](/specification/model/linkelement)

**Nom des enfants** : 
	-  [StyleFormatCondition](styleformatcondition) 
