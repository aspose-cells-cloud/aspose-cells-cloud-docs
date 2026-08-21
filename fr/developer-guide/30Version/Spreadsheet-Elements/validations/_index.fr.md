---
title: "Travail avec la validation de données Excel"
second_title: "Document"
linktype: "Validations"
type: docs
url: /fr/validations/fr/
keywords: "validation de données Excel, Aspose.Cells Cloud, API REST, feuille de calcul, cloud bureautique"
description: "Découvrez comment ajouter, récupérer, mettre à jour, supprimer et effacer des règles de validation de données Excel de manière programmatique à l’aide de l’API REST Aspose.Cells Cloud. Inclut des exemples pour .NET, Java, Python et PHP."
weight: 100
ArticleTitle: "Travail avec la validation de données Excel - Documentation de l’API Aspose.Cells Cloud"
---

La validation de données Excel est une fonctionnalité de Microsoft Excel permettant de contrôler ce qu’un utilisateur peut saisir dans une cellule d’une feuille de calcul. Elle permet par exemple de limiter les entrées à une plage de dates spécifique, à des nombres entiers uniquement, ou encore de créer des listes déroulantes permettant d’économiser de l’espace et d’afficher des valeurs dans une seule cellule. Vous pouvez également définir un message personnalisé s’affichant lorsqu’un utilisateur saisit une valeur incorrecte ou un format non valide.

Par exemple, un utilisateur peut spécifier une réunion prévue entre 9 h 00 et 18 h 00.

La validation de données peut être utilisée pour garantir qu’une valeur est un nombre positif, une date comprise entre le 15 et le 30 d’un mois, une date survenant dans les 30 jours à venir, ou encore une entrée textuelle contenant moins de 25 caractères, etc.

### Résumé de l’API

| Opération | Méthode HTTP | Endpoint | Description |
|-----------|-------------|----------|-------------|
| Ajout | POST | `/cells/{file}/worksheets/{sheet}/validations` | Créer une règle de validation |
| Récupération | GET | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Récupérer une règle spécifique |
| Tout récupérer | GET | `/cells/{file}/worksheets/{sheet}/validations` | Lister toutes les règles |
| Mise à jour | PUT | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Modifier une règle |
| Suppression | DELETE | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Supprimer une règle |
| Effacer | POST | `/cells/{file}/worksheets/{sheet}/validations/clear` | Supprimer toutes les règles |

## Travail avec les validations sur un fichier Excel

- [Comment ajouter une règle de validation à une feuille de calcul Excel](/cells/validations/add/fr/)
- [Comment récupérer une règle de validation à partir d’une feuille de calcul Excel](/cells/validations/get/fr/)
- [Comment récupérer toutes les règles de validation à partir d’une feuille de calcul Excel](/cells/validations/get-all/fr/)
- [Comment supprimer une règle de validation à partir d’une feuille de calcul Excel](/cells/validations/delete/fr/)
- [Comment effacer toutes les règles de validation à partir d’une feuille de calcul Excel](/cells/validations/clear/fr/)
- [Comment mettre à jour une règle de validation sur une feuille de calcul Excel](/cells/validations/update/fr/)
---