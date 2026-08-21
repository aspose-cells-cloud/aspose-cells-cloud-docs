---
title: "Comment ajouter des lignes à une feuille Excel"
second_title: "Document"
linktitle: "Ajouter"
type: docs
url: /fr/rows/add/
keywords: "Aspose.Cells, ajouter des lignes, API Excel, REST, C#, Java, Python, Node.js"
description: "Guide pas à pas pour ajouter une ou plusieurs lignes à une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud, avec des exemples de code en C#, Java, Python et Node.js."
weight: 20
ArticleTitle: "Ajouter des lignes à une feuille Excel à l’aide de l’API Aspose.Cells Cloud – Guide pas à pas"
---

## Comment ajouter des lignes à une feuille Excel

Cet article explique comment insérer une seule ligne vide ou plusieurs lignes dans une feuille existante à l’aide de l’API REST Aspose.Cells Cloud. Assurez-vous d’avoir une clé API valide et le SDK approprié installé avant de continuer.

**Conditions préalables**  
- [ ] Compte Aspose.Cells Cloud avec un abonnement actif.  
- [ ] Clé API / jeton d’accès généré depuis le tableau de bord Aspose Cloud.  
- [ ] L’un des SDK pris en charge (C#, Java, Python, Node.js) installé et configuré.  

**Référence de l’API**  
- **Méthode HTTP :** `POST`  
- **Point de terminaison :** `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/rows`  
- **Paramètres obligatoires dans le chemin :**  
  - `fileName` – Nom du fichier Excel stocké dans le cloud.  
  - `sheetName` – Nom de la feuille de calcul où les lignes seront ajoutées.  
- **Paramètres de requête :**  
  - `startrow` – Index de ligne (à zéro) à partir duquel l’insertion commence.  
  - `totalRows` – Nombre de lignes à insérer.  
  - `folder` – (Facultatif) Chemin du dossier cloud contenant le fichier.  
  - `storage` – (Facultatif) Nom du stockage si un stockage non par défaut est utilisé.  
- **Corps de la requête (exemple JSON) :**  

  ```json
  {
    "startrow": 5,
    "totalRows": 3
  }
  ```

  **Exemple cURL**

  ```bash
  curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/rows?startrow=5&totalRows=3&folder=MyFolder&storage=MyStorage" \
      -H "Authorization: Bearer {access_token}" \
      -H "Content-Type: application/json" \
      -d '{"startrow":5,"totalRows":3}'
  ```

- **Réponse réussie (HTTP 200) :** Renvoie les informations mises à jour de la feuille de calcul, y compris le nouveau nombre de lignes.  

  ```json
  {
    "Code": 200,
    "Status": "OK",
    "Worksheet": {
      "Name": "Sheet1",
      "RowsCount": 30
    }
  }
  ```

- **Exemple de réponse d’erreur (HTTP 400) :**  

  ```json
  {
    "Code": 400,
    "Status": "Bad Request",
    "Message": "Le paramètre startrow est invalide. Il doit s'agir d'un entier non négatif."
  }
  ```

- **Codes d’état :**  

  | Code | Signification                              |
  |------|--------------------------------------------|
  | 200  | Lignes ajoutées avec succès                |
  | 400  | Paramètres invalides ou JSON mal formé    |
  | 401  | Échec de l’authentification                |
  | 404  | Fichier ou feuille de calcul introuvable  |
  | 500  | Erreur serveur                             |

Ci-dessous, des liens directs vers les exemples détaillés pour l’ajout de lignes :

- [Comment ajouter une ligne vide sur une feuille Excel](/cells/rows/add/row/)
- [Comment ajouter plusieurs lignes sur une feuille Excel](/cells/rows/add/rows/)