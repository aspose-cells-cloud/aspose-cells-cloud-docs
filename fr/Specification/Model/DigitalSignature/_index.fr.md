---
title: Signature numérique
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/digitalsignature/
description: "Aspose.Cells Spécification du modèle Cloud : DigitalSignature. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
weight: 50
---
## **signature numérique**

 Signature au dossier.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| commentaires| Chaîne| Vrai| FAUX|| Le but de la signature.|
| Heure de signature| Chaîne| Vrai| FAUX|| L'heure à laquelle le document a été signé.|
| Identifiant| Chaîne| Vrai| FAUX|| Spécifie un GUID qui peut être référencé avec le GUID de la ligne de signature stockée dans le contenu du document. La valeur par défaut est Guid vide (tous les zéros).|
| Mot de passe| Chaîne| Vrai| FAUX|| Spécifie le texte de la signature réelle dans la signature numérique. La valeur par défaut est Vide.|
| Image|Tableau<Byte> | Vrai| FAUX|| Spécifie une image pour la signature numérique. La valeur par défaut est nulle.|
| ID du fournisseur| Chaîne| Vrai| FAUX|| Spécifie l'ID de classe du fournisseur de signature. La valeur par défaut est Guid vide (tous les zéros).|
| Est valable| Booléen| Vrai| FAUX||Si cette signature numérique est valide et que le document n'a pas été falsifié, cette valeur sera vraie.|
| XAdESType| Chaîne| Vrai| FAUX|| Type XAdES. La valeur par défaut est Aucun (XAdES est désactivé).|

