---
---
title: "Supprimer des caractères par position"
ArticleTitle: "Supprimer des caractères par position – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Supprimer des caractères par position"
type: docs
url: /cells/content/remove/characters-by-position
aliases: []
keywords: "Aspose.Cells, Supprimer des caractères, API"
description: "Supprime des caractères des cellules par position dans une feuille de calcul."
weight: 100
---

## Supprimer des caractères par position avec les services web Aspose.Cells Cloud

Supprime des caractères dans chaque cellule de la plage cible par position (les N premiers/derniers caractères, avant/après une sous-chaîne ou entre deux délimiteurs), tout en conservant les formules, le formatage et la validation des données.

### Point de terminaison de l’API web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre          | Type    | Emplacement (chemin/chaîne de requête/ Corps HTTP) | Description                                                                                                          |
|---------------------------|---------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Spreadsheet               | Fichier | FormData                                            | Télécharger le fichier de feuille de calcul.                                                                        |
| theFirstNCharacters       | Entier  | Chaîne de requête                                    | Spécifier la suppression des N premiers caractères des cellules sélectionnées. Facultatif.                         |
| theLastNCharacters        | Entier  | Chaîne de requête                                    | Spécifier la suppression des N derniers caractères des cellules sélectionnées. Facultatif.                          |
| allCharactersBeforeText   | Chaîne  | Chaîne de requête                                    | Supprimer le texte situé avant une sous-chaîne spécifiée. Facultatif.                                               |
| allCharactersAfterText    | Chaîne  | Chaîne de requête                                    | Supprimer le texte situé après une sous-chaîne spécifiée. Facultatif.                                               |
| caseSensitive             | Booléen | Chaîne de requête                                    | Affecte le mode `Substring` et `CustomChars` lorsqu’activé. Facultatif.                                             |
| worksheet                 | Chaîne  | Chaîne de requête                                    | Spécifier la feuille de calcul de la feuille de calcul. Facultatif.                                                |
| range                     | Chaîne  | Chaîne de requête                                    | Spécifier la plage de la feuille de calcul (par ex., `A1:B10`). Facultatif.                                        |
| outPath                   | Chaîne  | Chaîne de requête                                    | (Facultatif) Le chemin du dossier où le classeur est stocké. La valeur par défaut est null. Facultatif.           |
| outStorageName            | Chaîne  | Chaîne de requête                                    | Nom du stockage pour le fichier de sortie. Facultatif.                                                             |
| region                    | Chaîne  | Chaîne de requête                                    | Paramètre de région/langue de la feuille de calcul (par ex., `en-US`, `fr-FR`). Facultatif.                        |
| password                  | Chaîne  | Chaîne de requête                                    | Mot de passe pour ouvrir le fichier de feuille de calcul. Facultatif.                                              |

### Paramètre du corps de la requête

| Nom du paramètre | Type  | Description                     |
| ---------------- | ----- | ------------------------------- |
| Spreadsheet      | Fichier | Télécharger le fichier de feuille de calcul. |

### **Réponse**

```json
{
  "status": "OK",
  "message": "Les caractères ont été supprimés avec succès.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

**Codes d’état de la réponse**

| Code | Signification         | Description                                                                 |
|------|-----------------------|-----------------------------------------------------------------------------|
| 200  | OK                    | L’opération s’est terminée avec succès et le fichier traité est renvoyé.   |
| 400  | Mauvaise requête      | La requête est mal formée ou contient des paramètres invalides.            |
| 401  | Non autorisé          | L’authentification a échoué ou le jeton JWT est manquant/ invalide.        |
| 413  | Charge utile trop grande | La taille du fichier téléchargé dépasse la limite autorisée.             |
| 500  | Erreur interne du serveur | Une erreur inattendue s’est produite côté serveur.                      |

## Comment utiliser la fonctionnalité de suppression des caractères par position avec les SDK

### Spécification de la fonctionnalité de suppression des caractères par position

La [spécification de l’API Supprimer des caractères par position](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPosition) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells Cloud. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position?theFirstNCharacters=5&worksheet=Sheet1&range=A1%3AB10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "status": "OK",
  "message": "Les caractères ont été supprimés avec succès.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose Cells Cloud

L’utilisation d’un SDK est le moyen le plus rapide d’accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose Cells Cloud à l’aide de divers SDK :
`[TBD]`
---