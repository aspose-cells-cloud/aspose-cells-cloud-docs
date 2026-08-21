---
title: "Démarrage avec l'API Aspose.Cells Cloud – Traitement de fichiers Excel en 3 étapes simples"
second_title: "Document"
ArticleTitle: "Démarrage avec Aspose.Cells Cloud"
linktype: "Démarrage"
type: docs
url: /getting-started/
description: "Découvrez comment télécharger, convertir et télécharger des fichiers Excel à l'aide de l'API REST Aspose.Cells Cloud en trois étapes simples. Inclut des exemples de code cURL."
weight: 10
keywords: "Aspose.Cells Cloud, API Excel, conversion de feuilles de calcul, Excel vers PDF, feuille de calcul cloud, API Aspose.Cells Cloud"
---

- [Vue d'ensemble](/cells/overview/)
- [Guide de démarrage rapide](/cells/quickstart/)
- [SDK disponibles](/cells/available-sdks/)
- [Plateformes prises en charge](/cells/supported-platforms/)
- [Formats de fichiers pris en charge](/cells/supported-file-formats/)
- [Évaluer Aspose.Cells Cloud](/cells/evaluate-aspose-cells/)
- [Formule tarifaire](/cells/pricing-plan/)
- [Assistance technique](/cells/technical-support/)
- [Comment exécuter un conteneur Docker](/cells/how-to-run-docker-container/)

**Guide de démarrage**

Avant de commencer, assurez-vous de disposer d'une **clé API Aspose Cloud** et d'un **nom de stockage** valides. Ces identifiants sont requis pour toutes les appels API ultérieurs.

**Étape 1 : Télécharger un fichier Excel**  
Téléchargez votre classeur source vers le stockage Aspose Cloud.

```curl
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/{path}" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/octet-stream" \
     --data-binary @sample.xlsx
```

*Corps de la requête* : Le fichier est envoyé en tant que flux binaire (`application/octet‑stream`).  
*Paramètres requis* :

- `path` – chemin de stockage où le fichier sera enregistré (par ex., `dossier/sample.xlsx`).

**Étape 2 : Convertir le classeur en PDF**  
Envoyez une requête de conversion une fois le fichier stocké.

```curl
curl -X POST "https://api.aspose.cloud/v4.0/cells/{name}/saveas?format=pdf&outPath={outputPath}" \
     -H "Authorization: Bearer {access_token}"
```

*Paramètres requis* :

- `name` – nom du classeur téléchargé (par ex., `sample.xlsx`).
- `format` – format cible (`pdf`).
- `outputPath` – chemin de stockage du fichier converti (par ex., `dossier/result.pdf`).

*Exemple de charge utile de réponse* (JSON) :

```json
{
  "status": "OK",
  "outputPath": "folder/result.pdf"
}
```

**Étape 3 : Télécharger le PDF converti**  
Récupérez le PDF résultant depuis le stockage.

```curl
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/{outputPath}" \
     -H "Authorization: Bearer {access_token}" \
     -o result.pdf
```

*Paramètres requis* :

- `outputPath` – chemin du PDF généré à l’étape précédente.

**Résumé des exemples de requête et de réponse**

| Opération | Méthode HTTP | Point de terminaison (exemple) | Paramètres | Statut de succès |
|-----------|-------------|-------------------------------|------------|------------------|
| Télécharger | PUT         | /cells/storage/file/{path} | `path` (emplacement de stockage) | 200 OK |
| Convertir | POST        | /cells/{name}/saveas?format=pdf&outPath={outputPath} | `name`, `format`, `outPath` | 200 OK |
| Télécharger | GET         | /cells/storage/file/{outputPath} | `outputPath` | 200 OK |

**Codes d’erreur courants**

- **400 Bad Request** – Paramètres manquants ou invalides.  
- **401 Unauthorized** – Jeton d’accès invalide ou manquant.  
- **404 Not Found** – Le fichier ou le chemin spécifié n’existe pas.  
- **500 Internal Server Error** – Erreur serveur inattendue ; réessayez ou contactez le support.  
---