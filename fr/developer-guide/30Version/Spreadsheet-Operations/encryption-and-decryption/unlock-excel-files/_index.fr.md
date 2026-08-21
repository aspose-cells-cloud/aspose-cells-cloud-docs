---
title: "Déverrouiller des fichiers Excel"
second_title: "Document"
linktitle: "Déverrouiller des fichiers Excel"
type: docs
url: /unlock-excel-files/
aliases: [/unlock/without-storage/, /unlock/, /unlock/without-using-storage/]
keywords: "Déverrouiller Excel, Aspose.Cells Cloud, API REST, Déverrouillage Excel, classeur protégé par mot de passe, SDK, C#, Java, Python, Node.js, Go, PHP, Ruby, Swift"
description: "L’API REST Aspose.Cells Cloud fournit un point de terminaison pour déverrouiller des fichiers Excel protégés par mot de passe. Des SDK sont disponibles pour de nombreux langages de programmation, notamment Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby et Swift."
ArticleTitle: "Déverrouiller des fichiers Excel à l’aide de l’API REST Aspose.Cells Cloud"
weight: 70
---

Cette API REST permet de déverrouiller des fichiers Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/unlock
```

### Sécurité et authentification

Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement             | Description                                          |
|------------------|--------|-------------------------|------------------------------------------------------|
| file             | fichier| formData (corps HTTP)   | Fichier à télécharger                                |
| password         | string | chaîne de requête       | Mot de passe pour déverrouiller le fichier (le cas échéant) |

### Réponse

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                |
|------|-----------------------------|------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite. |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur. |

## Comment utiliser l’API PostUnlock avec les SDK

### Spécification de l’API PostUnlock

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostUnlock) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/unlock?password=123456" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----ChaîneBase64--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----ChaîneBase64--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen idéal pour accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

**Remarques**  
- L’API permet de déverrouiller plusieurs fichiers Excel en une seule requête ; chaque fichier est retourné dans le tableau `Files` de la réponse.  
- Assurez-vous que la version de votre SDK correspond à la version de l’API (`v3.0`) afin d’éviter des problèmes de compatibilité.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}