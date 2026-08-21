---
title: "Réparer des fichiers Excel"
second_title: "Document"
type: docs
linktitle: "Réparer des fichiers Excel"
url: /repair-excel-files/
keywords: "Aspose Cells, API de réparation Excel, XLSX corrompu, récupération de feuille de calcul, API cloud"
description: "Utilisez l’API REST Aspose.Cells Cloud pour réparer des fichiers Excel corrompus (XLS, XLSX, XLSM, XLSB, ODS). Téléchargez un ou plusieurs fichiers, choisissez le format de sortie, et recevez les fichiers réparés au format Base64. Aucune installation requise."
weight: 39
---

Cette API REST vous permet de **réparer** des fichiers Excel.

- Réparez les formats XLS, XLSX, XLSM, XLSB, ODS et d’autres formats de feuilles de calcul.
- Prend en charge le téléchargement de plusieurs fichiers en une seule requête.

Aspose.Cells Cloud Réparation Excel permet de récupérer les données à partir de fichiers Excel corrompus en ligne, sans aucune installation. Les fichiers Excel corrompus posent problème car ils ne peuvent pas être ouverts. Vous pouvez essayer l’application Aspose.Cells Cloud Réparation Excel pour récupérer les données à partir de tels fichiers.

## API REST

L’endpoint **Réparer des fichiers Excel** répare les fichiers de feuilles de calcul corrompus et renvoie le contenu réparé.


```bash
POST https://api.aspose.cloud/v3.0/cells/repair
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement                   | Description |
|------------------|--------|-------------------------------|-------------|
| file             | fichier | formData (multipart)          | Fichier à télécharger |
| format           | chaîne  | query                         | Format de sortie souhaité. Si omis (null), le format de sortie est celui du fichier d’entrée par défaut. |

### **Réponse**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nom de fichier combiné]",
    "Filesize" : [taille du fichier],
    "FileContent" : "[ChaîneBase64]"
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande     | Le fichier téléversé dépasse la taille limite. |
| 500  | Erreur interne du serveur   | Erreur inattendue côté serveur. |

## Comment utiliser l’API PostRepair avec les SDK

### Spécification de l’API PostRepair

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/repair" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F 'file1=@fichier1.xlsx' \
  -F 'file2=@fichier2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "fichier1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----ChaîneBase64--------"
    },
    {
      "Filename": "fichier2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----ChaîneBase64--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

En cas de succès, le service renvoie HTTP 200 avec une charge utile JSON contenant un tableau `Files`. En cas d’erreur, l’API utilise les codes de statut HTTP standards :

- **400 Mauvaise requête** – Paramètres invalides ou fichier non récupérable.  
- **401 Non autorisé** – Jeton JWT manquant ou invalide.  
- **413 Charge utile trop grande** – Le fichier téléversé dépasse la taille autorisée.  
- **500 Erreur interne du serveur** – Échec inattendu côté serveur.

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur vos tâches de projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}
---