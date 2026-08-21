---
title: "Travail avec les commentaires Excel"
second_title: "Document"
linktitle: "Commentaires"
type: docs
url: /fr/comments/
aliases: [  /fr/working-with-comments/ ]
keywords: "Aspose.Cells Cloud, API des commentaires Excel, commentaires de feuille de calcul, API REST"
description: "Découvrez comment ajouter, récupérer, mettre à jour et supprimer des commentaires Excel à l’aide de l’API REST Aspose.Cells Cloud v3.0, avec des exemples de code, les prérequis et la gestion des erreurs."
weight: 100
ArticleTitle: "Travail avec les commentaires Excel – Guide de l’API Aspose.Cells Cloud"
---

Lors de la création d’un classeur Excel, les utilisateurs peuvent ajouter des commentaires pour diverses raisons. Une utilisation courante consiste à expliquer une formule dans une cellule, notamment lorsque le fichier sera partagé avec d’autres personnes. Les commentaires peuvent également servir de rappels, de notes destinées aux collaborateurs ou d’outils de référence croisée avec d’autres classeurs. Une fois un commentaire ajouté, Excel permet aux utilisateurs de redimensionner, de modifier la forme et de mettre en forme la zone de commentaire selon leur style préféré. Maîtriser la gestion des commentaires aide les utilisateurs à tirer pleinement parti de cette fonctionnalité.

**Prérequis**

- Un compte actif Aspose.Cells Cloud.  
- Un **jeton d’accès** valide obtenu via OAuth 2.0.  
- Version de l’API **v3.0** (les points de terminologie utilisés dans ce guide appartiennent à cette version).  
- Facultatif : le SDK Aspose.Cells pour votre langage préféré afin de simplifier la construction des requêtes.

**Version**

Les exemples ci-dessous ciblent l’**API REST Aspose.Cells Cloud v3.0**. Les futures versions de l’API peuvent introduire des paramètres supplémentaires ou modifier la structure des réponses ; consultez toujours la référence API la plus récente pour obtenir des détails à jour.

**Ajouter un commentaire**

Pour ajouter un commentaire, envoyez une requête **POST** vers le point de terminaison suivant :

```
POST https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
Content-Type: application/json
```

**Paramètres de chemin**

| Paramètre | Type   | Obligatoire | Description                              |
|-----------|--------|-------------|------------------------------------------|
| `file`    | string | Oui         | Nom du fichier de classeur (y compris l’extension). |
| `sheet`   | string | Oui         | Nom de la feuille de calcul dans laquelle le commentaire sera ajouté. |

**Schéma du corps de la requête**

| Champ      | Type   | Obligatoire | Description                              |
|------------|--------|-------------|------------------------------------------|
| `CellName` | string | Oui         | Adresse en notation A1 (par exemple, **B2**). |
| `Comment`  | string | Oui         | Texte du commentaire à stocker. |
| `Author`   | string | Non         | Nom de l’auteur du commentaire. |

**Exemple de corps de requête**

```json
{
  "CellName": "B2",
  "Comment": "Revue nécessaire",
  "Author": "Jean Dupont"
}
```

**Exemple de réponse réussie** (`200 OK`)

```json
{
  "Code": 200,
  "Status": "OK",
  "Comment": {
    "CellName": "B2",
    "Author": "Jean Dupont",
    "HtmlComment": "Revue nécessaire",
    "Note": "Revue nécessaire"
  }
}
```

**Codes d’erreur courants**

| Code | Signification                              |
|------|--------------------------------------------|
| 400  | Adresse de cellule invalide ou corps de requête incorrect |
| 401  | Non autorisé – jeton manquant ou invalide |
| 404  | Classeur ou feuille de calcul introuvable |

**Récupérer les commentaires**

Récupérer tous les commentaires d’une feuille de calcul :

```
GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**Paramètres de chemin**

| Paramètre | Type   | Obligatoire | Description                              |
|-----------|--------|-------------|------------------------------------------|
| `file`    | string | Oui         | Nom du fichier de classeur. |
| `sheet`   | string | Oui         | Nom de la feuille de calcul. |

**Exemple de réponse**

```json
{
  "Code": 200,
  "Status": "OK",
  "Comments": [
    {
      "CellName": "A1",
      "Author": "Alice",
      "HtmlComment": "Valeur initiale",
      "Note": "Valeur initiale"
    },
    {
      "CellName": "B2",
      "Author": "Jean Dupont",
      "HtmlComment": "Revue nécessaire",
      "Note": "Revue nécessaire"
    }
  ]
}
```

**Mettre à jour un commentaire**

Pour modifier un commentaire existant, envoyez une requête **PUT**. Le commentaire est identifié par son **index** dans la collection de commentaires de la feuille de calcul (indexation à partir de 0).

```
PUT https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
Content-Type: application/json
```

**Paramètres de chemin**

| Paramètre      | Type   | Obligatoire | Description |
|----------------|--------|-------------|-------------|
| `file`         | string | Oui         | Nom du fichier de classeur. |
| `sheet`        | string | Oui         | Nom de la feuille de calcul. |
| `commentIndex` | int    | Oui         | Index à partir de zéro du commentaire à mettre à jour. |

**Schéma du corps de la requête**

| Champ     | Type   | Obligatoire | Description |
|-----------|--------|-------------|-------------|
| `Comment` | string | Oui         | Nouveau texte du commentaire. |
| `Author`  | string | Non         | Nom de l’auteur mis à jour (facultatif). |

**Exemple de corps de requête**

```json
{
  "Comment": "Texte de note mis à jour",
  "Author": "Jean Dupont"
}
```

La réponse suit la même structure que celle de la réponse **Ajouter un commentaire**.

**Supprimer un commentaire**

Supprimer un seul commentaire à l’aide de son index :

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
```

**Paramètres de chemin**

| Paramètre      | Type   | Obligatoire | Description |
|----------------|--------|-------------|-------------|
| `file`         | string | Oui         | Nom du fichier de classeur. |
| `sheet`        | string | Oui         | Nom de la feuille de calcul. |
| `commentIndex` | int    | Oui         | Index à partir de zéro du commentaire à supprimer. |

Une suppression réussie renvoie :

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Supprimer tous les commentaires**

Pour effacer tous les commentaires d’une feuille de calcul :

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**Paramètres de chemin**

| Paramètre | Type   | Obligatoire | Description |
|-----------|--------|-------------|-------------|
| `file`    | string | Oui         | Nom du fichier de classeur. |
| `sheet`   | string | Oui         | Nom de la feuille de calcul. |

**Conseils pour la gestion des erreurs**

- **404 Not Found** – Vérifiez que l’identifiant du classeur, le nom de la feuille de calcul et l’index du commentaire sont corrects.  
- **400 Bad Request** – Vérifiez la syntaxe JSON et les champs obligatoires (`CellName`, `Comment`).  
- **429 Too Many Requests** – Mettez en œuvre une backoff exponentielle et respectez l’en-tête `Retry-After`.

**Résumé**

- Les commentaires Excel permettent [d’ajouter une note ou d’expliquer une formule dans une cellule](/cells/comments/add/).  
- Excel offre la flexibilité de [modifier](/cells/comments/update/), [supprimer](/cells/comments/delete/) et [afficher](/cells/comments/get/) ou [masquer](/cells/comments/update/) les commentaires sur une feuille de calcul.  
- Les utilisateurs peuvent également [redimensionner](/cells/comments/update/) et [déplacer](/cells/comments/update/) la zone de commentaire.  

Pour en savoir plus sur le travail avec d’autres éléments de feuille de calcul, consultez le guide sur [le travail avec les cellules](/cells/working-with-cells/).