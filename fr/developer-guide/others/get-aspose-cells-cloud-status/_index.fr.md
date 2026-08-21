---
title: "Aspose.Cells Cloud Web API – Obtenir l’état du service Aspose Cells Cloud"
second_title: "Document"
articleTitle: "Obtenir l’état du service Aspose.Cells Cloud"
linktitle: "Obtenir l’état du service Aspose.Cells Cloud"
type: docs
url: /fr/get-aspose-cells-cloud-status/
keywords: "Aspose.Cells, API Cloud, Vérification de santé, Excel, REST"
description: "Surveiller en temps réel l’état de santé du service Aspose.Cells Cloud."
weight: 100
---

Obtenez l’état de santé du service Aspose.Cells Cloud en temps réel.

**Conditions préalables :** Pour appeler cette API, vous devez obtenir un jeton d’accès Bearer à l’aide de vos identifiants client Aspose Cloud. Incluez ce jeton dans l’en-tête `Authorization` sous la forme `Bearer {access_token}`.

## **Obtenir l’état du service Aspose.Cells Cloud**

### **API Web**

Le point de terminaison utilise la méthode HTTP **GET** et ne nécessite pas de corps de requête.

```
GET https://api.aspose.cloud/v4.0/cells
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                     |
| ---------------- | ------ | ----------------------------------------------------- | ----------------------------------------------- |
| Authorization    | String | En-tête                                               | Jeton Bearer pour l’authentification (obligatoire). |
| format           | String | Chaîne de requête                                      | Format souhaité pour la réponse, par exemple `json`. |

### **Réponse**

```json
{
  "status": "OK",
  "service": "Aspose.Cells Cloud",
  "timestamp": "2026-07-06T12:34:56Z"
}
```

**Schéma de la réponse**

| Champ       | Type              | Description                                     |
| ----------- | ----------------- | ----------------------------------------------- |
| status      | string            | État de santé du service (`OK`, `Dégradé`, etc.). |
| service     | string            | Nom du service.                                 |
| timestamp   | string (ISO‑8601) | Heure de la vérification d’état.                |

L’API renvoie une charge utile JSON standard contenant l’**état** actuel de santé du service Aspose.Cells Cloud.

**Codes d’état HTTP**

- **200 OK** – Le service est sain et la réponse contient les informations d’état.
- **401 Non autorisé** – Jeton d’authentification manquant ou invalide.
- **503 Service non disponible** – Le service est actuellement hors ligne pour maintenance ou rencontre des problèmes.

## Comment utiliser l’API Obtenir l’état du service Aspose.Cells Cloud avec les SDK

### **Spécification OpenAPI**

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/#/CellsStatusController/GetAsposeCellsCloudStatus) définit une interface de programmation accessible publiquement qui permet d’effectuer directement des interactions REST depuis un navigateur web.

### **Utiliser les SDK Aspose.Cells Cloud**

L’utilisation d’un SDK simplifie l’intégration et réduit la quantité de code répétitif. Le SDK gère les détails sous-jacents, vous permettant ainsi d’obtenir l’état d’exécution du service Aspose.Cells Cloud avec un minimum d’efforts. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.