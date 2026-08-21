---
title: "Aspose.Cells Cloud AI – Décomposition des tâches, traduction de feuilles de calcul et de fichiers texte"
second_title: "Document"
ArticleTitle: "Améliorez vos compétences en IA : découvrez la traduction Excel, la décomposition des tâches et bien plus encore"
linktype: "AI"
type: docs
url: /fr/ai/
keywords: "Aspose.Cells, Cloud AI, traduction Excel, décomposition des tâches, API REST"
description: "Découvrez Aspose.Cells Cloud AI pour décomposer des tâches, traduire des classeurs Excel et des fichiers texte. Inclut les points de terminaison REST, du code d’exemple et les meilleures pratiques."
weight: 20
---

Aspose.Cells Cloud AI propose trois services puissants alimentés par l’IA qui simplifient la manipulation des données Excel et des fichiers texte : **Décomposer la tâche utilisateur**, **Traduire la feuille de calcul** et **Traduire le fichier texte**. Ces API permettent aux développeurs de décomposer de manière programmatique des objectifs utilisateur complexes en étapes concrètes, de traduire des classeurs entiers ou des fichiers texte simples, et d’intégrer les résultats dans leurs applications personnalisées. Utilisez les points de terminaison ci-dessous pour commencer rapidement, et consultez les spécifications détaillées de demande/réponse fournies pour chaque service.

- **[Décomposer la tâche utilisateur](https://docs.aspose.cloud/cells/decompose-user-task/)** – Convertissez les objectifs utilisateur en plans d’action séquentiels à l’aide d’Aspose.Cells Cloud AI.  
  - **Méthode de requête :** `POST`  
  - **URL du point de terminaison :** `https://api.aspose.cloud/v4.0/cells/ai/decompose-task`  
  - **En-têtes :** `Authorization: Bearer <access_token>`, `Content-Type: application/json`  
  - **Corps de la demande (JSON) :**  
    ```json
    {
      "task": "Générer un rapport de ventes trimestriel avec des graphiques et des tableaux croisés dynamiques"
    }
    ```  
  - **Réponse :** Renvoie le fichier de feuille de calcul contenant la liste des tâches en tant que fichier téléchargeable.  
  - **Codes de statut :** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`  
  - **Conditions préalables :** Un jeton d’accès valide avec la portée **CellsAI**.  
  - **Exemple de réponse (extrait JSON) :**  
    ```json
    {
      "fileId": "12345abcde",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/12345abcde"
    }
    ```  
  - **Notes :** Le classeur généré inclut une feuille nommée **TaskList** contenant les étapes ordonnées. Limite de débit : 100 requêtes par minute.

- **[Traduire la feuille de calcul](https://docs.aspose.cloud/cells/translate-spreadsheet/)** – Traduisez une feuille de calcul entière à l’aide d’Aspose.Cells Cloud AI.  
  - **Méthode de requête :** `POST`  
  - **URL du point de terminaison :** `https://api.aspose.cloud/v4.0/cells/ai/translate-spreadsheet`  
  - **En-têtes :** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **Paramètres de la demande :**  
    - `file` – Le fichier Excel à traduire (données binaires).  
    - `targetLanguage` – Code de langue ISO (par exemple, `fr`, `de`).  
  - **Réponse :** Renvoie le classeur traduit en tant que fichier téléchargeable.  
  - **Codes de statut :** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **Conditions préalables :** Jeton d’accès avec la portée **CellsAI** et quota de stockage suffisant.  
  - **Exemple de réponse (extrait JSON) :**  
    ```json
    {
      "translatedFileId": "f9d8c7b6",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/f9d8c7b6"
    }
    ```  
  - **Notes :** Toutes les valeurs de cellules, commentaires et noms de feuilles sont traduits. Limite de débit : 100 requêtes par minute.

- **[Traduire le fichier texte](https://docs.aspose.cloud/cells/translate-text-file/)** – Traduisez un fichier texte entier à l’aide d’Aspose.Cells Cloud AI.  
  - **Méthode de requête :** `POST`  
  - **URL du point de terminaison :** `https://api.aspose.cloud/v4.0/cells/ai/translate-text`  
  - **En-têtes :** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **Paramètres de la demande :**  
    - `file` – Le fichier texte à traduire (données binaires).  
    - `targetLanguage` – Code de langue ISO (par exemple, `es`, `ja`).  
  - **Réponse :** Renvoie le fichier texte traduit.  
  - **Codes de statut :** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **Conditions préalables :** Jeton d’accès valide avec la portée **CellsAI**.  
  - **Exemple de réponse (extrait JSON) :**  
    ```json
    {
      "translatedFileId": "a1b2c3d4",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/a1b2c3d4"
    }
    ```  
  - **Notes :** Prend en charge les fichiers texte simples encodés en UTF‑8 d’une taille maximale de 5 Mo. Limite de débit : 100 requêtes par minute.