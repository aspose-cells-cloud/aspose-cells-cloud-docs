---
title: "Travail avec la suppression de lignes dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Supprimer"
type: docs
url: /fr/rows/delete/
keywords: "Aspose.Cells, suppression de ligne, API Excel, REST, cloud, fichier de calcul, Excel, SDK"
description: "Découvrez comment supprimer une ou plusieurs lignes dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut des exemples de code pour Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby et Swift."
weight: 20
ArticleTitle: "Travail avec la suppression de lignes dans une feuille de calcul Excel – Guide de l’API Aspose.Cells Cloud"
---

## Opérations de suppression disponibles

Les exemples ci-dessous montrent comment supprimer une ligne vide unique ou plusieurs lignes dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud.

- [Comment supprimer une ligne vide dans une feuille de calcul Excel](/fr/cells/rows/delete/row/)
- [Comment supprimer plusieurs lignes dans une feuille de calcul Excel](/fr/cells/rows/delete/rows/)

**Référence de l’API**

| Élément                | Détails |
|---------------------|---------------------------------------------------------------|
| **Méthode HTTP**     | DELETE |
| **Point de terminaison**        | `/cells/{fileName}/worksheets/{sheetName}/rows` |
| **Paramètres de chemin**| `fileName` – nom du fichier Excel (obligatoire)<br>`sheetName` – nom de la feuille de calcul (obligatoire) |
| **Paramètres de requête**| `startrow` – index de la première ligne à supprimer (obligatoire)<br>`totalRows` – nombre de lignes à supprimer (obligatoire)<br>`storage` – nom du stockage cloud (facultatif)<br>`folder` – chemin du dossier dans le stockage (facultatif) |
| **Corps de la requête**    | *Aucun* |
| **Exemple de réponse**| ```json<br>{<br>  "Code": 200,<br>  "Status": "OK",<br>  "RowsDeleted": 1<br>}<br>``` |
| **Codes d’état possibles**| 200 OK – lignes supprimées avec succès<br>400 Bad Request – paramètres invalides<br>401 Unauthorized – échec d’authentification<br>404 Not Found – fichier ou feuille de calcul introuvable<br>500 Internal Server Error – problème côté serveur |

**Voir aussi**

- [Ajouter une ligne](/fr/cells/rows/add/)
- [Obtenir une ligne](/fr/cells/rows/get/)
- [Copier une ligne](/fr/cells/rows/copy/)
- [Masquer une ligne](/fr/cells/rows/hide/)
- [Vue d’ensemble des lignes](/fr/cells/rows/)