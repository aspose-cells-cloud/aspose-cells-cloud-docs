---
title: "Compresser et réparer des fichiers Excel"
second_title: "Document"
type: docs
url: /fr/compress-and-repair-excel-files/
linktitle: "Compresser et réparer"
keywords: "Aspose.Cells, compression Excel, réparation Excel, API cloud, réduire la taille des fichiers Excel, restaurer un classeur corrompu, compresser un fichier Excel, réparer un classeur Excel"
description: "Découvrez comment compresser des classeurs Excel volumineux et réparer des fichiers corrompus à l’aide de l’API Aspose.Cells Cloud. Exemples détaillés étape par étape, langages pris en charge et bonnes pratiques."
weight: 100
ArticleTitle: "Compresser et réparer des fichiers Excel – API Aspose.Cells Cloud"
---

Compresser un classeur Excel permet de réduire sa taille en supprimant les styles, images et chaînes partagées inutilisés, tandis que la réparation restaure l’intégrité des classeurs corrompus. L’API Aspose.Cells Cloud fournit des points d’accès dédiés à ces deux opérations.

- **[Compresser les données d’un fichier Excel](https://docs.aspose.cloud/cells/compress-excel-files/).**
- **[Réparer des fichiers Excel](https://docs.aspose.cloud/cells/repair-excel-files/).**

**API Compresser un classeur**  
L’opération **Compresser** utilise une simple requête POST. Voici la spécification complète de la requête/réponse :

| Méthode | Point d’accès | Paramètres requis | Corps de la requête | Exemple de réponse | Codes de statut typiques |
|--------|---------------|-------------------|---------------------|-------------------|--------------------------|
| POST   | `/cells/compress` | `file` (binaire) – le classeur à compresser ; `outPath` optionnel (chaîne) – chemin de destination | *Aucun* (le fichier est envoyé en tant que multipart/form‑data) | `{ "compressedSize": 12456, "originalSize": 45678 }` | `200 OK`, `400 Bad Request`, `401 Unauthorized` |

**API Réparer un classeur**  
L’opération **Réparer** utilise également une requête POST. Sa spécification est la suivante :

| Méthode | Point d’accès | Paramètres requis | Corps de la requête | Exemple de réponse | Codes de statut typiques |
|--------|---------------|-------------------|---------------------|-------------------|--------------------------|
| POST   | `/cells/repair` | `file` (binaire) – le classeur corrompu ; `outPath` optionnel (chaîne) – emplacement où enregistrer le fichier réparé | *Aucun* (le fichier est envoyé en tant que multipart/form‑data) | `{ "isRepaired": true, "message": "Workbook repaired successfully." }` | `200 OK`, `400 Bad Request`, `415 Unsupported Media Type` |

Ces tableaux fournissent aux développeurs les informations essentielles pour appeler directement les API sans avoir à consulter ailleurs.

**Ressources supplémentaires**  
- Consultez le guide complet **[Compresser des fichiers Excel](/compress-excel-files/)** pour des options avancées, telles que la suppression des lignes et colonnes inutilisées.  
- Consultez la documentation **[Réparer des fichiers Excel](/repair-excel-files/)** pour obtenir des conseils de dépannage et des explications sur les codes d’erreur.  
- Explorez d’autres opérations connexes telles que **[Obtenir les informations sur le fichier](/file-info/)** et **[Opérations sur les feuilles de calcul](/spreadsheet-operations/)** afin d’approfondir votre compréhension de l’API Aspose.Cells Cloud.