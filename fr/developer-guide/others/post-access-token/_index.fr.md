---
title: "Aspose.Cells Cloud Web API - Post Access Token"
second_title: "Document"
ArticleTitle: "Obtenir un jeton d'accès avec l'ID client et le secret"
linktitle: "Post Access Token"
type: docs
url: /post-access-token/
keywords: "Aspose.Cells, Cloud, Jeton d'accès, OAuth2, API, Authentification, REST, Excel, Office Cloud"
description: "Obtenir un jeton d'accès OAuth2 pour Aspose.Cells Cloud en appelant le point de terminaison POST /cells/connect/token avec votre ID client et votre secret."
weight: 100
---

Récupérer un jeton d'accès à l'aide de l'API Cells Cloud Get Token avec un ID client et un secret.

## API Post Access Token

Avant d'appeler le point de terminaison, assurez-vous d'avoir :

* Un compte Aspose Cloud enregistré.  
* Un **ID client** et un **Secret client** générés dans le portail Aspose Cloud.  

### Web API

```
POST https://api.aspose.cloud/v4.0/cells/connect/token
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement                        | Description                                                 |
| ---------------- | ------ | ---------------------------------- | ----------------------------------------------------------- |
| grant_type       | string | corps (encodé en url-form)         | Valeur fixe `client_credentials` requise pour OAuth.       |
| client_id        | string | corps (encodé en url-form)         | L'identifiant client qui vous a été attribué.               |
| client_secret    | string | corps (encodé en url-form)         | Le secret associé à l'ID client.                            |

**Exemple de requête (cURL)**  

```bash
curl -X POST "https://api.aspose.cloud/v4.0/cells/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=VOTRE_ID_CLIENT&client_secret=VOTRE_SECRET_CLIENT"
```

### Réponse

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

**Codes de statut HTTP**

| Code | Signification              | Description                                                    |
|------|----------------------------|----------------------------------------------------------------|
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l'opération. |
| 400  | Mauvaise requête           | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT invalide ou manquant.                               |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la limite de taille.           |
| 500  | Erreur interne du serveur  | Erreur inattendue du serveur.                                 |

**Exemple de gestion d'erreur**

```json
{
  "error": "invalid_client",
  "error_description": "L'authentification client a échoué."
}
```

## Comment utiliser l'API Get public key à l'aide des SDK

### Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) définit une interface de programmation accessible publiquement, vous permettant d'effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L'utilisation d’un SDK est le moyen le plus rapide de débuter. Le SDK abstrait les détails HTTP sous-jacents, vous permettant d'obtenir un jeton d'accès pour Cells avec un minimum de code.

Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :
---