---
title: "Récupérer les métadonnées à partir de fichiers Excel"
second_title: "Document"
linktitle: "Récupération sans utiliser le stockage"
type: docs
url: /fr/metadata/get/
keywords: "Aspose.Cells, Excel, métadonnées, REST API, SDK cloud"
description: "Récupérer les métadonnées intégrées ou personnalisées à partir de classeurs Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut le format de la requête, les paramètres, le code d’exemple des SDK et la gestion des erreurs."
weight: 23
ArticleTitle: "Récupérer les métadonnées à partir de fichiers Excel – API Aspose.Cells Cloud"
---

Cette API REST permet de récupérer des **métadonnées** à partir d’un ou plusieurs fichiers Excel.  
La requête doit inclure un en‑tête `Authorization: Bearer <jeton_d’accès>` obtenu via le flux d’octroi d’accès OAuth 2.0 (client_credentials).

**Conditions préalables** : Pour appeler ce point de terminaison, vous devez disposer d’un jeton d’accès valide obtenu auprès du point de terminaison de jetons OAuth 2.0 d’Aspose Cloud. Exemple de requête curl permettant d’obtenir un jeton :

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=<votre_id_client>&client_secret=<votre_secret_client>"
```

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/get
```

### Paramètre de requête

| Nom du paramètre | Type   | Description                                                                 |
| ---------------- | ------ | --------------------------------------------------------------------------- |
| type             | string | `ALL` / `BuiltIn` / `Custom` – spécifie quels groupes de métadonnées doivent être retournés. |

### Paramètre du corps de la requête

| Nom du paramètre | Type      | Description                                                        |
| ---------------- | --------- | ------------------------------------------------------------------ |
| fichier Excel    | fichier de données | Le fichier Excel fourni en tant que première partie de la requête multipart. |

### Réponse

```json
[
  {
    "Name": "Author",
    "Value": "Jean Dupont",
    "BuiltIn": true,
    "IsReadOnly": false
  },
  {
    "Name": "CustomProp1",
    "Value": "Valeur personnalisée",
    "BuiltIn": false,
    "IsReadOnly": false
  }
]
```

| Code | Signification                 | Quand                                           |
| ---- | ----------------------------- | ----------------------------------------------- |
| 200  | Succès                        | Métadonnées retournées.                         |
| 400  | Requête incorrecte            | Fichier manquant ou requête invalide.           |
| 401  | Non autorisé                  | Jeton invalide ou manquant.                     |
| 404  | Non trouvé                    | Fichier spécifié introuvable.                   |
| 500  | Erreur interne du serveur     | Échec inattendu du serveur.                     |

L’API renvoie ces codes de statut HTTP standard accompagnés, le cas échéant, d’un objet JSON de réponse d’erreur.

### Famille de SDK Cloud

L’utilisation d’un SDK accélère le développement en gérant les détails de bas niveau. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}