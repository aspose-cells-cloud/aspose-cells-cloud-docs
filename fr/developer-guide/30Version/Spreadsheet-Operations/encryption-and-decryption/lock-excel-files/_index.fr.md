---
title: "Verrouiller des fichiers Excel"
second_title: "Document"
linktitle: "Verrouiller des fichiers Excel"
type: docs
url: /fr/lock-excel-files/
aliases: [  /fr/lock/without-storage/ , /fr/lock/ , /fr/lock/without-using-storage/ ]
keywords: "Verrouiller, Excel, API, Aspose.Cells, Cloud, REST, Classeur, Feuille de calcul, SDK"
description: "Découvrez comment verrouiller des classeurs Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut le point de terminaison HTTPS, l’authentification, la requête cURL, le schéma de réponse et des exemples de code SDK pour C#, Java, Python et plus encore."
ArticleTitle: "Verrouiller des fichiers Excel – Documentation de l’API Aspose.Cells Cloud"
weight: 70
---

**Version de l’API :** v3.0 (version actuelle)

Cette API REST **verrouille** les classeurs Excel.

## API PostLock

```http
POST https://api.aspose.cloud/v3.0/cells/lock
```

**Prérequis** – La requête doit être envoyée via **HTTPS** et inclure un jeton Bearer OAuth 2.0 valide dans l’en-tête `Authorization`.

### Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement                    | Description                                          |
| ---------------- | ------ | ------------------------------ | ---------------------------------------------------- |
| file             | fichier | données de formulaire (corps multipart) | Le classeur Excel à télécharger et verrouiller.   |
| password         | chaîne  | chaîne de requête              | Mot de passe pour le classeur (facultatif).         |

La <a href="https://apireference.aspose.cloud/cells/#/LightCells/PostLock" target="_blank" rel="noopener noreferrer">Spécification OpenAPI</a> définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment **appeler** l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/lock?password=123456" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

*Vous pouvez télécharger un classeur d’exemple — [Sample.xlsx](https://example.com/Sample.xlsx) — afin de tester la requête.*

**Remarque :** L’API prend en charge des fichiers dont la taille maximale est de 100 Mo ; des charges utiles plus importantes peuvent entraîner une réponse HTTP 413 (Payload Too Large).

### **Détails de la réponse**

| Champ         | Type             | Description                                               |
| ------------- | ---------------- | --------------------------------------------------------- |
| Filename      | chaîne           | Nom du classeur verrouillé renvoyé par le service.       |
| FileSize      | entier           | Taille du fichier verrouillé, en octets.                  |
| FileContent   | chaîne (Base64)  | Le classeur verrouillé encodé en chaîne Base64.           |

Pour récupérer le classeur verrouillé, décodez la valeur `FileContent` depuis Base64 et enregistrez-le en utilisant le `Filename` fourni dans la réponse.

### **Gestion des erreurs**

– L’API renvoie des codes d’état HTTP standard (par ex. `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`) accompagnés d’un objet erreur JSON contenant les champs `Code` et `Message`.

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la meilleure façon d’accélérer le développement. Un SDK abstractise les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostLock.go" >}}

{{< /tab >}}

{{< /tabs >}}