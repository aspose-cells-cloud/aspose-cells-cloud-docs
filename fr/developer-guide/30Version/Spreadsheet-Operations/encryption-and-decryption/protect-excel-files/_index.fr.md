---
title: "Protéger des fichiers Excel"
second_title: "Document"
linktitle: "Chiffrer des classeurs Excel"
type: docs
url: /protect-excel-files/
aliases:
  [
    /protect/without-storage/,
    /protect/without-using-storage/,
    /protect/without-using-storage/,
  ]
keywords: "Aspose.Cells, API de protection Excel, chiffrer un classeur Excel, sécurité des feuilles de calcul dans le cloud, API REST"
description: "Utilisez l’API REST Aspose.Cells Cloud pour protéger vos fichiers Excel. Ce guide explique comment chiffrer des classeurs via HTTP POST, cURL et les SDK pour plusieurs langages de programmation, en 2026."
weight: 40
---

Cette API REST permet de protéger des fichiers Excel.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/protect
```

### Sécurité et authentification

Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement              | Description                                    |
| ---------------- | ------ | ------------------------ | ---------------------------------------------- |
| file             | fichier | formData (corps)         | Fichier à télécharger                          |
| password         | chaîne  | chaîne de requête (`password`) | Mot de passe utilisé pour protéger le classeur |

### Réponse

```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename": "nom de fichier protégé : sample1.xlsx",
      "FileSize": taille,
      "FileContent": "-----Chaîne Base64 de sample1-----"
    },
    {
      "Filename": "nom de fichier protégé : sample2.xlsx",
      "FileSize": taille,
      "FileContent": "-----Chaîne Base64 de sample2-----"
    }
  ]
}
```

**Codes de statut HTTP**

| Code | Signification              | Description                                                           |
|------|----------------------------|-----------------------------------------------------------------------|
| 200  | OK                         | Le filtre a été appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte         | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la taille maximale autorisée. |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur. |

## Comment utiliser l’API PostProtect avec les SDK

### Spécification de l’API PostProtect

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostProtect) définit une interface de programmation publiquement accessible, vous permettant d’interagir directement avec l’API REST depuis un navigateur web.

Vous pouvez également utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/protect?password=MySecretPwd" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F 'file1=@sample1.xlsx' \
  -F 'file2=@sample2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "sample1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Chaîne Base64 de sample1-----"
    },
    {
      "Filename": "sample2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Chaîne Base64 de sample2-----"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### **Gestion des erreurs**

– L’API peut renvoyer les codes de statut suivants :

| Code HTTP | Signification                                | Exemple de charge utile d’erreur JSON                     |
| --------- | -------------------------------------------- | --------------------------------------------------------- |
| 400       | Requête incorrecte (par exemple, fichier manquant) | `{"Code":400,"Message":"Le fichier est obligatoire."}`   |
| 401       | Non autorisé (jeton invalide ou manquant)   | `{"Code":401,"Message":"Jeton d’accès invalide."}`        |
| 403       | Interdit (permissions insuffisantes)        | `{"Code":403,"Message":"Accès refusé."}`                  |
| 500       | Erreur interne du serveur                   | `{"Code":500,"Message":"Erreur inattendue du serveur."}`  |

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer. Un SDK gère les détails de bas niveau, afin que vous puissiez vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}