---
title: "Modifier la protection par mot de passe d’un classeur Excel"
second_title: "Document"
linktitle: "Modifier le mot de passe d’un fichier Excel"
type: docs
url: /fr/workbook/password/modify/
aliases:
  - /set-modify-password-of-excel-workbooks/
  - /workbook/modify-password/
keywords: "mot de passe Excel, Aspose.Cells Cloud, protection en écriture, API REST, modifier le mot de passe du classeur"
description: "Modifier le mot de passe de protection en écriture d’un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut des exemples en cURL et en SDK."
weight: 100
ArticleTitle: "Modifier la protection par mot de passe d’un classeur Excel – Aspose.Cells Cloud"
---

Cet **API REST modifie le mot de passe de protection en écriture** d’un classeur Excel existant.

La mise à jour programmatique du mot de passe de protection en écriture vous permet de renouveler ou de remplacer les mots de passe sans télécharger le fichier. C’est particulièrement pratique lors de la gestion de classeurs sécurisés stockés dans le stockage Aspose.Cells Cloud.

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### Sécurité et authentification

Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                      |
| ---------------- | ------ | ----------- | ------------------------------------------------ |
| **name**         | string | path        | Nom du classeur Excel (obligatoire).             |
| **password**     | string | body (JSON) | Nouveau mot de passe de protection en écriture à définir (obligatoire). |
| **folder**       | string | query       | Dossier facultatif où le classeur est stocké.    |
| **storageName**  | string | query       | Nom facultatif du service de stockage.           |

### Réponse

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise demande            | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT non valide ou manquant. |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille. |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue. |

## Comment utiliser l’API PutDocumentProtectFromChanges avec les SDK

### Spécification de l’API PutDocumentProtectFromChanges

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutDocumentProtectFromChanges) définit l’interface de programmation publiquement accessible qui vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. La commande cURL ci-dessous montre comment appeler l’API Cloud.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/writeProtection?folder=Samples&storageName=Default" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -d '{ "Password": "aspose" }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus rapide de développer. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutDocumentProtectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutDocumentProtectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutDocumentProtectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutDocumentProtectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutDocumentProtectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutDocumentProtectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutDocumentProtectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutDocumentProtectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}