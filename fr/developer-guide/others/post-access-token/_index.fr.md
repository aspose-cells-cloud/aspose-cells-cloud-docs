---
title: Aspose.Cells Cloud Web API - Token d'accès post
second_title: Documen
ArticleTitle: Get Access Token with Client ID and Secre
linktitle: Toke d'accès post
type: docs
url: /fr/post-access-token/
keywords: Access Token, Aspose Cloud, API Authentication, OAuth, REST API, Excel, Office Cloud, Token Managemen
description: Récupérez un jeton d'accès à l'aide du jeton d'accès Cloud Cells API, qui agit comme un service proxy transmettant les demandes des utilisateurs au serveur d'authentification Cloud Aspose et renvoie le jeton d'accès résultant au client en toute sécurité
weight: 100
kwords: Excel, Office Cloud, REST API, Authentification, Gestion des jetons, Intégration middleware, Sécurisé API, Aspose Clou
---
Récupérez un jeton d'accès à l'aide du jeton Cloud Get Cells API avec l'ID client et le secret.

## **Jeton d'accès postal API**

```
POST http://api.aspose.cloud/v4.0/cells/connect/token
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| ID client| chaîne| requête| ID client|
| Secret client| chaîne| requête| Secret client|

### **Réponse**

```json
 [
        {
          "Name": "String",
          "DataType": {
            "Identifier": "String",
            "Name": "string"
          }
        }
  ]
```

## Comment utiliser la clé publique Get API avec les SDK

### Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) définit une interface de programmation accessible au public, vous permettant d'effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

Utiliser le SDK est le meilleur moyen d'accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant d'implémenter facilement l'obtention d'un jeton d'accès pour les cellules avec un minimum de code.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) Pour obtenir la liste complète des SDK Cloud Aspose.Cells.nt. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :
