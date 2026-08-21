---
title: "Aspose.Cells Cloud – Vérifier la santé du service (API)"
second_title: "Document"
ArticleTitle: "Vérification de la santé du service Aspose.Cells Cloud"
linktitle: "Vérifier la santé du service cloud"
type: docs
url: /check-cloud-service-health/
keywords: "Aspose.Cells Cloud, vérification de la santé de l’API, statut REST, surveillance des services cloud"
description: "Surveillez en temps réel la santé d’Aspose.Cells Cloud. Découvrez le point de terminaison GET /v4.0/cells/status/check, ses paramètres, le format de réponse et des exemples d’implémentation via les SDK."
weight: 100
---

Vérifiez l’état de santé des services Aspose.Cells Cloud.

**Conditions préalables**  
Pour appeler ce point de terminaison, vous devez disposer d’un jeton d’accès Aspose Cloud valide. Obtenez ce jeton enregistrant une application dans le tableau de bord Aspose Cloud, puis en utilisant votre *client-id* et *client-secret* pour solliciter un jeton *Bearer* via le point de terminaison OAuth2. Incluez ce jeton dans l’en-tête `Authorization`, comme indiqué ci-dessous.

## **Vérifier la santé du service cloud**

### **API Web**

```http
GET https://api.aspose.cloud/v4.0/cells/status/check
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Paramètre     | Type   | Obligatoire | Description                                                       |
| ------------- | ------ | ----------- | ----------------------------------------------------------------- |
| Authorization | header | Oui         | Jeton *Bearer* pour l’authentification (`Authorization: Bearer <jeton>`). |
| detail        | query  | Non         | Définir sur `true` pour inclure des informations détaillées sur les composants. |
| Accept        | header | Non         | Format de réponse souhaité ; la valeur par défaut est `application/json`. |

### **Réponse**

En cas de succès, le service renvoie une charge utile JSON.

```json
{
  "status": "OK",
  "service": "Cells",
  "timestamp": "{{timestamp}}",
  "components": {
    "api": "Opérationnel",
    "storage": "Opérationnel",
    "database": "Opérationnel"
  }
}
```

**Codes de statut HTTP**

| Code | Signification          | Description                                                  |
| ---- | ---------------------- | ------------------------------------------------------------ |
| 200  | OK                     | Le service est en bon état ; voir l’exemple JSON ci-dessus. |
| 401  | Non autorisé           | Jeton d’authentification invalide ou manquant.              |
| 503  | Service indisponible   | Le service est actuellement défaillant ou en maintenance.   |
| 4xx  | Erreur client          | Paramètres de requête incorrects ou requête mal formée.     |
| 5xx  | Erreur serveur         | Échec inattendu du serveur ; réessayez ultérieurement.      |

## Comment utiliser l’API de statut Aspose.Cells Cloud avec les SDK

### **Spécification OpenAPI**

<a href="https://reference.aspose.cloud/cells/#/CellsStatusController/CheckCloudServiceHealth" target="_blank" rel="noopener noreferrer">Spécification OpenAPI</a> définit une interface de programmation publiquement accessible et permet d’effectuer directement des interactions REST depuis un navigateur web.

### **Utiliser les SDK Aspose.Cells Cloud**

L’utilisation d’un SDK constitue la méthode optimale pour accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant ainsi de mettre en œuvre une vérification de la santé du service Cells avec un minimum de code.  
Consultez le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Ci-dessous figurent des extraits d’exemple illustrant comment appeler le point de terminaison de vérification de la santé à l’aide des SDK les plus courants.