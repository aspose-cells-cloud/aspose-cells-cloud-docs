---
title: "Décrypter un classeur Excel"
second_title: "Document"
linktitle: "Décrypter un fichier Excel"
type: docs
url: /excel-file-decrypt/
aliases: [/decrypt-excel-workbooks/, /workbook/decrypt/]
keywords: "Aspose.Cells, décryptage Excel, API REST, SDK cloud"
description: "Découvrez comment décrypter un classeur Excel à l'aide de l'API REST Aspose.Cells Cloud. Inclut les paramètres requis, un exemple cURL, des exemples de code SDK et des détails sur la gestion des erreurs."
ArticleTitle: "Comment décrypter un classeur Excel à l'aide de l'API Aspose.Cells Cloud"
weight: 50
---

**Conditions préalables**

- Un jeton d'accès JWT valide.
- Le classeur doit être uploadé vers le stockage Aspose Cloud et son chemin spécifié dans le paramètre de requête `folder`.

## API DeleteDecryptWorkbook

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de requête

| Nom du paramètre | Type   | Description                                           |
| ---------------- | ------ | ----------------------------------------------------- |
| folder           | string | Chemin du dossier contenant le classeur original.     |
| storageName      | string | Nom du stockage dans lequel réside le classeur.       |

### Paramètre du corps de la requête

| Nom du paramètre | Type                      | Description                                       |
| ---------------- | ------------------------- | ------------------------------------------------- |
| encryption       | WorkbookEncryptionRequest | Paramètres de chiffrement requis pour le décryptage. |

### WorkbookEncryptionRequest

| Nom du paramètre | Type    | Description                                                                                              |
| ---------------- | ------- | -------------------------------------------------------------------------------------------------------- |
| EncryptionType   | string  | Algorithme de chiffrement (`XOR`, `Compatible`, `EnhancedCryptographicProviderV1`, `StrongCryptographicProvider`). |
| KeyLength        | integer | Longueur de la clé de chiffrement en bits.                                                               |
| Password         | string  | Mot de passe utilisé pour le décryptage.                                                                 |

### Réponse

```json
{
  "Status":"OK",
  "Code":200
}
```

**Exemples de réponses d’erreur**

```json
{
  "Code": "400",
  "Message": "Paramètres de requête invalides."
}
```

```json
{
  "Code": "401",
  "Message": "Échec de l'authentification. Jeton JWT invalide ou manquant."
}
```

```json
{
  "Code": "413",
  "Message": "Charge utile trop volumineuse. Le fichier uploadé dépasse la taille autorisée."
}
```

```json
{
  "Code": "500",
  "Message": "Erreur interne du serveur. Veuillez réessayer ultérieurement."
}
```

**Codes de statut HTTP**

| Code | Signification              | Description                                          |
|------|----------------------------|------------------------------------------------------|
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l'opération. |
| 400  | Demande incorrecte         | Paramètres manquants ou invalides (par ex. type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT invalide ou manquant.                      |
| 413  | Charge utile trop volumineuse | Le fichier uploadé dépasse la limite de taille.    |
| 500  | Erreur interne du serveur  | Erreur serveur inattendue.                           |

## Comment utiliser l'API DeleteDecryptWorkbook avec les SDK

### Spécification de l'API DeleteDecryptWorkbook

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook) définit une interface de programmation publiquement accessible et vous permet d'effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser **cURL** pour accéder facilement aux services web Aspose.Cells. L'exemple suivant montre comment appeler l'API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 1280, "Password": "aspose"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

### Utiliser les SDK Aspose.Cells Cloud

L'utilisation d'un SDK est le moyen optimal d'accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDecryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDecryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDecryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDecryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDecryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDecryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDecryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDecryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}