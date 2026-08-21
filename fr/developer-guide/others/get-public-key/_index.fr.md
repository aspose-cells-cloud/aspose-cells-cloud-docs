---
title: "API Cloud Aspose.Cells – Obtenir la clé publique (v4.0) | Documentation REST"
second_title: "Document"
ArticleTitle: "Obtenir la clé publique"
linktitle: "Obtenir la clé publique"
type: docs
url: /fr/get-public-key/
keywords: "Aspose.Cells, clé publique, RSA, API, cloud"
description: "Récupérer la clé publique RSA utilisée pour chiffrer les données avec Aspose.Cells Cloud. Inclut l’endpoint, les paramètres, un exemple de requête/réponse, les codes de statut et des exemples d’utilisation des SDK."
weight: 100
---

Cette API permet de récupérer la clé publique issue d’un algorithme de chiffrement asymétrique.

**Résumé rapide :** Utilisez l’API Aspose.Cells « Obtenir la clé publique » pour obtenir la clé publique RSA (2048 bits) nécessaire au chiffrement des données lors de l’utilisation de fichiers Excel dans le cloud. L’endpoint renvoie la clé au format JSON et est sécurisé via OAuth 2.0.

## **API Obtenir la clé publique**

**Conditions préalables :**  
Obtenez d’abord un jeton d’accès OAuth 2.0 valide incluant le scope `Cells.Read` avant d’appeler cet endpoint.

### **API Web**

```
GET https://api.aspose.cloud/v4.0/cells/publickey
```

**Exemple de requête (cURL)**

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/publickey" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement | Description                                                                     |
| ---------------- | ------ | ----------- | ------------------------------------------------------------------------------- |
| Authorization    | string | En-tête     | Jeton « Bearer » pour l’authentification OAuth2 (obligatoire).                 |
| Accept           | string | En-tête     | Format de réponse souhaité, par ex. `application/json` (facultatif, JSON par défaut). |

### **Réponse**

```json
{
  "Code": 200,
  "Status": "OK",
  "CellsCloudPublicKey": {
    "PublicKey": "MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAr...",
    "Algorithm": "RSA",
    "KeySize": 2048
  }
}
```

**Codes de statut HTTP**

| Code | Signification           | Description                                                     |
| ---- | ----------------------- | --------------------------------------------------------------- |
| 200  | OK                      | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte      | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé            | Jeton JWT invalide ou manquant.                                |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille maximale autorisée. |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                    |

## Comment utiliser l’API « Obtenir la clé publique » à l’aide des SDK

### **Spécification OpenAPI**

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) définit une interface de programmation publiquement accessible, vous permettant d’effectuer directement des interactions REST depuis votre navigateur web.

### **Utiliser les SDK Aspose.Cells Cloud**

L’utilisation des SDK est la méthode recommandée pour accélérer le développement. Les SDK gèrent les détails sous-jacents, vous permettant de simplement implémenter l’obtention de la clé publique pour les cells avec un minimum de code.  
Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Voici des exemples concrets pour les langages les plus courants :

---