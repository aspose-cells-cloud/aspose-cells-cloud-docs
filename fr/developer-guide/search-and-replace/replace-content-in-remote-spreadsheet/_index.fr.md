---
---
title: "Aspose.Cells Cloud Replace Web API – Mettre à jour le texte dans des classeurs distants"
second_title: "Document"
ArticleTitle: "Remplacement de texte en bloc dans des fichiers Excel cloud – API Rechercher & Remplacer"
linktype: "Remplacer le contenu d'un classeur distant"
type: docs
url: /replace-content-in-remote-spreadsheet/
keywords: "Aspose.Cells Cloud, remplacement de contenu, classeur distant, API rechercher & remplacer, Excel cloud, remplacement de texte en bloc"
description: "Utilisez l’API Rechercher & Remplacer d’Aspose.Cells Cloud pour mettre à jour en bloc le texte dans des classeurs Excel distants. Endpoint HTTPS sécurisé, authentification OAuth2 et exemples d’SDK prêts à l’emploi pour une intégration rapide."
weight: 100
---

Effectuez un remplacement de texte en bloc dans des fichiers Excel distants stockés dans le cloud. Recherchez et mettez à jour efficacement des chaînes de texte spécifiques à l’aide de l’API Rechercher & Remplacer d’Aspose.Cells pour les classeurs cloud.


## **Remplacer le contenu dans l’API de classeur distant**

### **API Web**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                                                                                                                                       |
|------------------|--------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **name**         | String | Path        | Le nom du fichier de classeur stocké dans le stockage cloud à modifier (par ex. `"rapport.xlsx"`).                                                              |
| **searchText**   | String | Query       | La chaîne à localiser dans l’ensemble du classeur. La recherche respecte la casse et s’applique à toutes les feuilles de calcul, sauf si limitée par d’autres paramètres. |
| **replaceText**  | String | Query       | La chaîne qui remplacera chaque occurrence de `searchText`.                                                                                                       |
| **folder**       | String | Query       | Le chemin du dossier dans le stockage cloud contenant le classeur source (par ex. `"/documents/quarterly/"`).                                                    |
| **storageName**  | String | Query       | _(Facultatif)_ Le nom d’un stockage cloud personnalisé (par ex. `"MyS3Bucket"`). S’il est omis, le stockage par défaut configuré pour le compte sera utilisé.   |
| **region**       | String | Query       | _(Facultatif)_ Identifiant de paramètres régionaux pouvant affecter l’encodage des caractères et le comportement de recherche spécifique à la langue (par ex. `"fr-FR"`). |
| **password**     | String | Query       | _(Facultatif)_ Mot de passe permettant d’ouvrir un classeur protégé.                                                                                             |

### Réponse

Une réponse réussie typique renvoie l’état de l’opération et le nombre de remplacements effectués :

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Codes d’erreur

- **400 Bad Request** – URI d’API Aspose.Cells Cloud invalide.
- **401 Unauthorized** – Jeton d’accès OAuth 2.0 manquant ou invalide.
- **404 Not Found** – Le fichier de classeur spécifié est introuvable.
- **500 Server Error** – Une erreur inattendue s’est produite côté serveur pendant le traitement de la requête.

## Quand utiliser l’API Remplacer le contenu dans un classeur distant ?

- **Mise à jour en bloc des fichiers cloud** – Modifiez le contenu de plusieurs fichiers Excel stockés dans un stockage cloud tel qu’AWS S3 ou Azure Blob.
- **Remplissage dynamique de modèles cloud** – Remplissez des modèles de rapports stockés dans le cloud avec des données à jour.
- **Synchronisation inter-régions des fichiers** – Assurez la cohérence des fichiers Excel entre différentes régions de stockage géographique.

## Pourquoi utiliser l’API Remplacer le contenu dans un classeur distant ?

- **Adapté aux développeurs** – Aspose.Cells Cloud fournit des bibliothèques SDK pour de nombreux langages de programmation, réduisant ainsi l’effort de développement par rapport à la création d’une solution personnalisée.
- **Réduction des coûts en main-d’œuvre** – Élimine le besoin de personnel dédié pour consolider manuellement les documents.
- **Paiement à l’usage** – Aucun investissement préalable ; vous ne payez que pour les appels d’API effectivement réalisés.
- **Coûts de maintenance nuls** – Aucun serveur à gérer, aucune mise à jour logicielle à effectuer, aucune préoccupation de compatibilité.
- **Préservation de tous les formatages, formules et graphiques des cellules** – L’opération conserve la mise en page et les calculs du classeur original après remplacement du texte.

## Comment utiliser l’API Remplacer le contenu dans un classeur distant avec les SDK ?

### Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utilisation des SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant ainsi de simplement implémenter le remplacement de contenu dans les classeurs avec un minimum de code. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :


---