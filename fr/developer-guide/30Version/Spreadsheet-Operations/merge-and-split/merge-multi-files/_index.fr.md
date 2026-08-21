---
title: "Fusionner plusieurs fichiers Excel dans un classeur unique"
second_title: "Document"
linktype: "fusionner-plusieurs-fichiers-excel"
type: docs
url: /merge-multi-files-into-excel/
aliases: [/merge/multi-files/]
keywords: "Aspose.Cells Cloud, fusionner plusieurs fichiers Excel, API REST, fusion de feuilles de calcul, SDK cloud"
description: "Découvrez comment fusionner plusieurs classeurs Excel en un seul fichier à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut l’endpoint HTTPS, la commande cURL, des exemples de SDK, les paramètres requis et les détails de gestion des erreurs."
weight: 32
---

## API REST

Cette API REST permet de fusionner plusieurs fichiers Excel en un seul classeur Excel.

```bash
POST https://api.aspose.cloud/v3.0/cells/merge
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.


### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                                                      | Obligatoire |
| ---------------- | ------- | ----------- | ------------------------------------------------------------------------------------------------ | ----------- |
| files[]          | file    | formData    | Un ou plusieurs classeurs Excel à fusionner. Utilisez `file1`, `file2`, etc. dans la requête. | Oui         |
| format           | string  | query       | Format de sortie souhaité (par exemple, `xlsx`).                                                | Oui         |
| mergeToOneSheet  | boolean | query       | Définir sur `true` pour combiner toutes les feuilles de calcul en une seule feuille ; la valeur par défaut est `false`. | Non      |

### **Réponse**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nom de fichier fusionné]",
    "Filesize" : [taille du fichier],
    "FileContent" : "[Base64String]"
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                             |
| 413  | Payload trop volumineux     | Le fichier téléchargé dépasse la limite de taille.                         |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur.                                               |

## Comment utiliser l’API PostMerge à l’aide des SDK

### Spécification de l’API PostMerge

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostMerge) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/merge?format=xlsx" \
  -X POST \
  -H "Authorization: Bearer <jeton jwt>" \
  -F "file1=@file1.xlsx" \
  -F "file2=@file2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  {
    "Filename": "file1.xlsx",
    "FileSize": 274022,
    "FileContent": "-----ChaineBase64--------"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau, afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Merge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Merge.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Merge.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMerge.py" >}}
{{< /tab >}}

{{< /tabs >}}

---