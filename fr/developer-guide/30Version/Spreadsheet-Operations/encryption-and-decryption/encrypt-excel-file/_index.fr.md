---
title: "Chiffrer un classeur Excel à l’aide de l’API Aspose.Cells Cloud – Exemples rapides cURL et SDK"
second_title: "Document"
linktitle: "Chiffrer un fichier Excel"
type: docs
url: /fr/excel-file-encrypt/
aliases: [  /fr/encrypt-excel-workbooks/ , /fr/workbook/encrypt/ ]
keywords: "Aspose Cells chiffrer classeur, API de chiffrement Excel, API REST, cURL, .NET, Java, Python, PHP, Ruby, Node.js, Go, Perl"
description: "Découvrez comment chiffrer un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut la commande cURL, des exemples de code SDK (C#, Java, Python, …), les paramètres requis et la gestion des erreurs."
weight: 20
ArticleTitle: "Chiffrer un classeur Excel avec l’API Aspose.Cells Cloud – Exemples cURL et SDK"
---

Cette API REST chiffre un **classeur** Excel.

**Prérequis :** Vous devez disposer d’un jeton JWT valide et avoir chargé le classeur dans un emplacement de stockage avant d’appeler ce point de terminaison.

## API PostEncryptDocument

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de requête**

| Nom du paramètre | Type   | Obligatoire | Description                              |
| ---------------- | ------ | ----------- | ---------------------------------------- |
| folder           | string | ✗           | Chemin du dossier contenant le classeur original. |
| storageName      | string | ✗           | Nom du stockage à utiliser.              |

### **Paramètre du corps de la requête**

| Nom du paramètre | Type                      | Obligatoire | Description                              |
| ---------------- | ------------------------- | ----------- | ---------------------------------------- |
| encryption       | WorkbookEncryptionRequest | ✓           | Paramètres de chiffrement pour le classeur. |

#### **WorkbookEncryptionRequest**

| Nom du paramètre | Type    | Obligatoire | Description                                                                                      |
| ---------------- | ------- | ----------- | ------------------------------------------------------------------------------------------------ |
| EncryptionType   | string  | ✓           | Algorithme de chiffrement. Voir le tableau ci-dessous pour les valeurs prises en charge et leur signification. |
| KeyLength        | integer | ✗           | Longueur de la clé de chiffrement en bits (ignorée pour `XOR` et `Compatible`).                 |
| Password         | string  | ✓           | Mot de passe utilisé pour le chiffrement.                                                       |

#### **Valeurs possibles pour EncryptionType**

| Valeur                            | Description                                        |
| --------------------------------- | -------------------------------------------------- |
| `XOR`                             | Algorithme XOR simple (obsolète, sécurité faible). |
| `Compatible`                      | Chiffrement compatible Excel 97‑2003 (40 bits).    |
| `EnhancedCryptographicProviderV1` | AES‑128 avec hachage SHA‑1.                        |
| `StrongCryptographicProvider`     | AES‑256 avec hachage SHA‑512 (le plus sécurisé).   |

### Réponse

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification              | Description                                                                  |
|------|----------------------------|------------------------------------------------------------------------------|
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte         | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT invalide ou manquant.                                              |
| 413  | Charge utile trop volumineuse | Le fichier chargé dépasse la taille maximale autorisée.                   |
| 500  | Erreur interne du serveur  | Erreur serveur inattendue.                                                   |

## Comment utiliser l’API PostEncryptDocument avec les SDK

### Spécification de l’API PostEncryptDocument

La <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument" rel="noopener noreferrer">Spécification OpenAPI</a> définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
# Chiffre le classeur "test.xlsx" à l’aide de l’algorithme XOR (clé 128‑bits) et du mot de passe "mateen".
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 128, "Password": "mateen"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**Réponses d’erreur possibles**

| Statut HTTP | Code                | Message                                             |
| ----------- | ------------------- | --------------------------------------------------- |
| 400         | BadRequest          | Paramètres manquants ou non valides.                |
| 401         | Unauthorized        | Le jeton d’authentification est absent ou non valide. |
| 403         | Forbidden           | Permissions insuffisantes pour accéder au stockage. |
| 500         | InternalServerError | Erreur serveur inattendue.                          |

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau, ce qui vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostEncryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostEncryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostEncryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostEncryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostEncryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostEncryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostEncryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostEncryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---