---
title: "Créer un dossier – API Aspose.Cells Cloud | Gestion du stockage Excel"
second_title: "Document"
articleTitle: "Créer un dossier – API Aspose.Cells Cloud"
linktitle: "Créer un dossier"
type: docs
url: /fr/create-folder/
keywords: "Aspose.Cells, API Cloud, Créer un dossier, Gestion du stockage, Excel"
description: "Créez un nouveau dossier dans le stockage cloud d'Aspose.Cells via une simple requête PUT. Voir le format de la requête, les paramètres, la réponse et la gestion des erreurs."
weight: 100
---

L'opération **createFolder** crée un nouveau dossier à l'emplacement spécifié dans le stockage cloud utilisé par l'API Excel. Cela est essentiel pour organiser les fichiers et maintenir une hiérarchie de répertoires structurée.

## **API Excel : Créer un dossier**

### API Web

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête de l’API **createFolder**

| Nom du paramètre | Type   | Emplacement | Obligatoire | Valeur par défaut | Description                                                                 |
| ---------------- | ------ | ----------- | ----------- | ----------------- | --------------------------------------------------------------------------- |
| `path`           | String | Path        | Oui         | –                 | Le chemin du dossier à créer (par exemple, `monDossier/sousDossier`).      |
| `storageName`    | String | Query       | Non         | –                 | Le nom du stockage à utiliser. Si omis, le stockage par défaut est appliqué. |

### Description de la réponse

```json
{}
```

L’opération ne renvoie aucun contenu en cas de succès. Les codes d'état HTTP typiques sont les suivants :

**Codes d'état HTTP**

| Code HTTP | Statut HTTP           | Description                                                                 |
| --------- | --------------------- | --------------------------------------------------------------------------- |
| 200       | OK                    | L'API Web a été appelée avec succès ; la réponse contient les détails de l'opération. |
| 400       | Mauvaise requête      | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401       | Non autorisé          | Jeton JWT invalide ou manquant.                                             |
| 413       | Charge utile trop grande | Le fichier téléchargé dépasse la limite de taille.                        |
| 500       | Erreur interne du serveur | Erreur inattendue du serveur.                                              |

## Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/monDossier/sousDossier" \
     -H "Authorization: Bearer {jeton_acces}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{</tab>}}
{{< /tabs >}}