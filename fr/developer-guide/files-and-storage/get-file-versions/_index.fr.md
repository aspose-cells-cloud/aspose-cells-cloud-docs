---
title: "API Aspose.Cells Cloud Get File Versions – Récupération rapide de l’historique des versions de fichiers"
second_title: "Document"
ArticleTitle: "Gestion Excel basée sur le cloud – Récupérez rapidement l’historique des versions de fichiers dans Aspose.Cells Cloud"
linktitle: "Obtenir les versions de fichier"
type: docs
url: /fr/get-file-versions/
keywords: "API Aspose Cells, versions de fichiers, gestion des versions de feuilles de calcul, API de stockage cloud, REST, historique de fichiers Excel"
description: "Obtenez une liste complète de l’historique des versions pour tout fichier Excel stocké dans Aspose.Cells Cloud. Prend en charge la sélection de stockage, l’authentification et les codes d’erreur détaillés."
weight: 100
---

Récupérez une liste complète des enregistrements de version pour une feuille de calcul spécifique stockée dans Aspose.Cells Cloud. Ce point de terminaison permet aux développeurs de suivre les modifications, d’auditer les modifications apportées et de mettre en œuvre des flux de travail de gestion des versions directement depuis le stockage cloud.

L’API **GetFileVersions** renvoie tous les enregistrements de version pour une feuille de calcul spécifiée stockée dans Aspose.Cells Cloud. Elle vous permet de conserver un historique complet des modifications pour chaque fichier.

## **API Excel : Obtenir les versions de fichier**

### API Web

```
GET https://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Les paramètres de requête de l’API **GetFileVersions** sont les suivants

| Nom du paramètre | Type   | Emplacement | Description                                                                                           |
| ---------------- | ------ | ----------- | ----------------------------------------------------------------------------------------------------- |
| `path`           | String | Path        | **Obligatoire.** Chemin complet du fichier dont les versions sont récupérées.                        |
| `storageName`    | String | Query       | Facultatif. Nom du stock contenant le fichier. Si omis, le stock par défaut est utilisé.             |

### **Réponse**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Contient une liste des versions de fichier pour le document spécifié."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": ["Une collection de détails sur les versions de fichier."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

En cas de succès, l’API renvoie **HTTP 200 OK** accompagné d’une charge utile JSON contenant le tableau `Value` d’objets de version de fichier, comme illustré ci-dessus.

**Codes d’état HTTP**

| Code | Signification             | Description                                                    |
| ---- | ------------------------- | -------------------------------------------------------------- |
| 200  | OK                        | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte        | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé              | Jeton JWT invalide ou manquant.                                |
| 413  | Charge utile trop grande   | Le fichier téléchargé dépasse la limite de taille.            |
| 500  | Erreur interne du serveur  | Erreur serveur inattendue.                                     |

## Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions) fournit une interface de programmation complète pour exécuter des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/version/MyFolder/MyFile.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "VersionId": "1",
      "IsLatest": false,
      "ModifiedDate": "2024-01-15T12:34:56Z",
      "Size": 10240
    },
    {
      "VersionId": "2",
      "IsLatest": true,
      "ModifiedDate": "2024-03-01T08:22:10Z",
      "Size": 10300
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK simplifie le développement en masquant les complexités de bas niveau, ce qui permet aux développeurs de se concentrer sur les fonctionnalités essentielles. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment interagir avec les services web Aspose.Cells dans divers langages de programmation :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{</tab>}}
{{< /tabs >}}

---