---
title: "Fusionner des feuilles de calcul correspondantes dans un dossier distant"
description: "Combiner des fichiers de feuilles de calcul stockés dans le stockage Aspose Cloud en un seul fichier. Prend en charge plus de 30 formats de sortie tels que PDF, CSV, JSON, XLSX, ODS, XPS, etc."
keywords: "Aspose.Cells, fusionner des feuilles de calcul, dossier distant, API, PDF, CSV, JSON, XLSX, ODS, XPS"
weight: 100
type: docs
url: /merge-spreadsheets-in-remote-folder/
---

Fusionner plusieurs fichiers de feuilles de calcul situés dans un dossier distant du stockage Aspose Cloud en un seul fichier de sortie. L’opération s’exécute entièrement dans le cloud, éliminant ainsi le besoin de télécharger localement les fichiers sources. Plus de 30 formats de sortie sont pris en charge (PDF, CSV, JSON, XLSX, ODS, XPS, …).

## API MergeSpreadsheetsInRemoteFolder

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête <a id="request-parameters"></a>

| Nom                     | Type    | Emplacement | Obligatoire | Description                                                                                          |
| ----------------------- | ------- | ----------- | ----------- | ---------------------------------------------------------------------------------------------------- |
| **folder**              | string  | query       | **Oui**     | Dossier du stockage cloud contenant les feuilles de calcul sources.                                 |
| **fileMatchExpression** | string  | query       | **Oui**     | Modèle pour sélectionner les fichiers (par exemple, `*rapport*.xlsx`). Prend en charge les jokers `*` et `?`. |
| **outFormat**           | string  | query       | **Oui**     | Format de sortie souhaité (`PDF`, `CSV`, `JSON`, `XLSX`, `ODS`, `XPS`, …).                           |
| **mergeInOneSheet**     | boolean | query       | **Oui**     | `true` – toutes les données fusionnées dans une seule feuille de calcul. `false` – chaque fichier source obtient sa propre feuille de calcul. |
| **storageName**         | string  | query       | Non         | Nom personnalisé du stockage ; par défaut, le stockage principal est utilisé si omis.               |
| **outPath**             | string  | query       | Non         | Dossier de destination pour le fichier fusionné. Si omis, le fichier est enregistré dans le dossier source. |
| **outStorageName**      | string  | query       | Non         | Nom du stockage dans lequel le fichier fusionné sera écrit.                                         |
| **fontsLocation**       | string  | query       | Non         | Chemin vers un dossier contenant les polices personnalisées (nécessaire pour l’export PDF/image).    |
| **region**              | string  | query       | Non         | Région (locale) pour le formatage des nombres, dates et devises (par exemple, `fr-FR`, `en-US`).      |
| **password**            | string  | query       | Non         | Mot de passe pour ouvrir toute feuille de calcul source protégée.                                   |

## Exemple de requête (cURL) <a id="request-example"></a>

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

### **Réponse**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

Le fichier peut être téléchargé directement à partir de l’URL `FileUrl` ou enregistré à l’emplacement spécifié par `outPath`.

**Détails de la réponse en cas de succès**

| Code d’état | Type de contenu            | Description                                       |
| ------------ | -------------------------- | ------------------------------------------------- |
| 200 OK       | `application/octet-stream` | Flux binaire du classeur fusionné.               |
| 202 Accepted | `application/json`         | JSON contenant `FileUrl`, `FileName`, etc.       |

**Codes d’état HTTP**

| Code | Signification         | Description                                                   |
| ---- | --------------------- | ------------------------------------------------------------- |
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte    | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT invalide ou manquant.                               |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite.          |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                              |

## Comment utiliser l’API de fusion de feuilles de calcul avec les SDK

### Spécification OpenAPI

La <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder" rel="noopener noreferrer">Spécification OpenAPI</a> fournit une description lisible par machine de l’API, permettant des interactions REST directes.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (encodé en Base64)",
  "contentType": "type MIME",
  "fileDownloadName": "nom de fichier optionnel"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et vous permet d’importer des données dans une feuille de calcul à l’aide de peu de code. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

---