---
title: "API Aspose.Cells Cloud CopyFolder – Copie rapide de dossiers dans le cloud"
second_title: "Document"
ArticleTitle: "Solution de gestion de fichiers Excel en ligne – Explication détaillée de la fonction de copie en masse de l’API Aspose.Cells Copy Folder"
linktype: "docs"
url: /fr/copy-folder/
keywords: "Copier dossier, Aspose.Cells Cloud, API REST, Stockage cloud, Gestion de feuilles de calcul"
description: "Découvrez comment copier des dossiers dans le stockage Aspose.Cells Cloud via un seul appel REST. Inclut l’endpoint, les paramètres, les exemples de requêtes, les codes d’erreur et les exemples de SDK."
weight: 100
---

L’API **CopyFolder** duplique un dossier existant dans le stockage Aspose.Cells Cloud. Cette fonctionnalité est utile pour créer des sauvegardes, réorganiser des données ou préparer une hiérarchie de dossiers pour un traitement ultérieur, sans avoir à déplacer manuellement les fichiers.

## **API Excel : Copier un dossier**

### API Web

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### L’API CopyFolder accepte les paramètres suivants

| Nom du paramètre  | Obligatoire | Type   | Emplacement (Chemin/Requête) | Description                                                          |
| ------------------ | ----------- | ------ | ---------------------------- | -------------------------------------------------------------------- |
| `srcPath`          | Oui         | String | Chemin                       | Le chemin du dossier source à copier.                               |
| `destPath`         | Oui         | String | Requête                      | Le chemin où le nouveau dossier sera créé.                          |
| `srcStorageName`   | Non         | String | Requête                      | Le nom du stockage contenant le dossier source.                     |
| `destStorageName`  | Non         | String | Requête                      | Le nom du stockage de destination où le dossier doit être copié.   |

### Exemple de réponse

Un appel réussi renvoie le code **HTTP 200** avec un corps JSON vide :

```json
{}
```

**Exemple de requête cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy" \
     -H "Authorization: Bearer {access_token}"
```

**Codes de statut HTTP**

| Code | Signification         | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête      | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT invalide ou manquant.                                   |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite.                |
| 500  | Erreur interne du serveur | Erreur inattendue sur le serveur.                                |

## Spécification OpenAPI

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels vers l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy
Authorization: Bearer {access_token}
Content-Type: application/json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

Utiliser un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{</tab>}}
{{< /tabs >}}