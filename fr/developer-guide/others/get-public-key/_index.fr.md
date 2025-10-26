---
title: Aspose.Cells Cloud WEb API - Obtenir une clé publique
second_title: Documen
ArticleTitle: Get Public Ke
linktitle: Obtenir des clés publiques
type: docs
url: /fr/get-public-key/
keywords: asymmetric encryption, public key retrieval, REST API, Excel API, security, data encryption, API integratio
description: Récupérer une clé publique asymétrique pour un cryptage sécurisé des données
weight: 100
kwords: chiffrement asymétrique, clé publique, REST API, Excel API, sécurité, chiffrement des données, intégration API, JSON, documentation API
---
Récupère la clé publique à partir d'un algorithme de chiffrement asymétrique.

## **Obtenir la clé publique API**

```
GET http://api.aspose.cloud/v4.0/cells/publickey
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|||||

### **Réponse**

```json
{
  "Name": "CellsCloudPublicKeyResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "CellsCloudPublicKey",
      "DataType": {
        "Identifier": "Class",
        "Reference": "CellsCloudPublicKey",
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

## Comment utiliser la clé publique Get API avec les SDK

### Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) définit une interface de programmation accessible au public, vous permettant d'effectuer des interactions REST directement depuis votre navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

Utiliser le SDK est le meilleur moyen d'accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant d'implémenter facilement l'obtention de la clé publique pour les cellules avec un minimum de code.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment interagir avec les services Web Aspose.Cells à l'aide de divers SDK :
