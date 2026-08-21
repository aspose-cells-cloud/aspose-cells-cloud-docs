---
title: "API de copie de fichiers Aspose.Cells Cloud – Une interface pour la copie rapide et les opérations en lot de fichiers Excel dans le cloud"
second_title: "Document"
articleTitle: "Solution de gestion de fichiers Excel en cloud – Explication détaillée de la fonctionnalité de copie en lot de l’API Aspose.Cells Copy File"
linktype: "docs"
url: /fr/copy-file/
keywords: "Aspose.Cells, API CopyFile, copie de fichier Excel, stockage cloud, API REST"
description: "Découvrez comment utiliser l’API CopyFile d’Aspose.Cells Cloud pour dupliquer efficacement des fichiers Excel et les gérer entre différents emplacements de stockage."
weight: 100
---

L’**API copyFile** permet aux utilisateurs de dupliquer un fichier Excel depuis un chemin source vers un chemin de destination, en prenant en charge diverses options de stockage.

## **API Excel : Copie de fichier**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête de l’API **copyFile**

| Nom du paramètre | Type   | Emplacement (Chemin / Chaîne de requête / Corps HTTP) | Description                                                    |
| ---------------- | ------ | ----------------------------------------------------- | -------------------------------------------------------------- |
| srcPath          | String | Chemin                                                | Le chemin source du fichier à copier.                          |
| destPath         | String | Chaîne de requête                                     | Le chemin de destination où le fichier sera enregistré.       |
| srcStorageName   | String | Chaîne de requête                                     | Le nom du stockage source.                                     |
| destStorageName  | String | Chaîne de requête                                     | Le nom du stockage de destination.                             |
| versionId        | String | Chaîne de requête                                     | ID de version facultatif du fichier à copier.                  |

### **Réponse**

L’opération ne renvoie aucun contenu en cas de succès. Les codes d’état HTTP typiques sont les suivants :

**Codes d’état HTTP**

| Code | Signification         | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête      | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT non valide ou manquant.                                |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille.          |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                    |

## Comment utiliser l’API de copie de fichier avec les SDK ?

### Spécification de l’API de copie de fichier

La [spécification de l’API de copie de fichier](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile) fournit une interface de programmation accessible publiquement pour réaliser des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage" \
     -H "Authorization: Bearer VOTRE_JETON_D_ACCÈS" \
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

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant ainsi de convertir les données de tables de feuilles de calcul en images avec un minimum de code. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

---