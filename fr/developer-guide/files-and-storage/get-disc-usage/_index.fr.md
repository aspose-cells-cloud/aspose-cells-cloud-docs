---
title: "Aspose.Cells Cloud API – Obtenir l’utilisation du disque | Métriques de stockage en temps réel"
second_title: "Document"
ArticleTitle: "Solution de gestion de fichiers Excel basée dans le cloud – Interface pour récupérer rapidement l’utilisation du disque dans le cloud."
linktype: "Obtenir l’utilisation du disque"
type: docs
url: /fr/get-disk-usage/
keywords: "Aspose Cells, API Cloud, Utilisation du disque, Métriques de stockage, Excel, REST"
description: "Récupérez l’utilisation du disque en temps réel pour Aspose.Cells Cloud. Découvrez le point de terminaison GET /v4.0/cells/storage/disk, l’authentification requise et la réponse d’exemple."
weight: 100
---

L’opération **Obtenir l’utilisation du disque** renvoie des métriques de stockage en temps réel pour votre compte Aspose.Cells Cloud. Utilisez ce point de terminaison pour surveiller l’espace disque consommé et l’espace disque total.

- Récupère l’utilisation actuelle du disque pour l’API Excel dans l’environnement Aspose Cloud.
- Permet aux développeurs de surveiller la quantité de stockage consommée par leurs applications.
- Permet une gestion proactive des limites de stockage et du contrôle des coûts.

## API Excel : GetDiskUsage

### API Web

```http
GET https://api.aspose.cloud/v4.0/cells/storage/disk
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                                | Obligatoire |
| ---------------- | ------ | ----------- | ---------------------------------------------------------- | ----------- |
| storageName      | String | Query       | Le nom du stockage pour lequel récupérer l’utilisation. | Facultatif  |

### **Réponse**

```json
{
  "Name": "DiskUsage",
  "Description": ["Classe contenant les informations sur l’espace disque."],
  "Type": "Classe",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "UsedSize",
      "Description": ["Quantité d’espace disque utilisée par l’application."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    },
    {
      "Name": "TotalSize",
      "Description": ["Espace disque total disponible."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    }
  ]
}
```

**Codes d’état HTTP**

| Code | Signification        | Description                                                     |
| ---- | -------------------- | --------------------------------------------------------------- |
| 200  | OK                   | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte   | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé         | Jeton JWT invalide ou manquant.                                 |
| 413  | Charge utile trop grande | Le fichier envoyé dépasse la limite de taille.                |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                  |

## Spécification OpenAPI

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetDiskUsage) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/disk?storageName=MyStorage" \
     -H "Authorization: Bearer VOTRE_JETON_D_ACCÈS"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 10737418240
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la meilleure façon d’accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetDiskUsage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetDiskUsage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetDiskUsage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetDiskUsage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetDiskUsage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetDiskUsage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetDiskUsage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetDiskUsage.go" >}}
{{</tab>}}
{{< /tabs >}}