---
title: "Exporter un graphique Excel – API Aspose.Cells Cloud"
second_title: "Document"
description: "Convertir un graphique à partir d’un classeur Excel stocké dans le cloud en PDF, PNG, SVG ou d’autres formats à l’aide d’un seul appel REST."
ArticleTitle: "Comment convertir une feuille de calcul locale en fichier PDF : guide étape par étape"
linktitle: "Convertir une feuille en PDF"
type: docs
url: /export-chart-as-format/
keywords: "Aspose.Cells Cloud, exporter un graphique, API, PDF, PNG, SVG, Excel, REST, conversion cloud"
weight: 100
---

Exportez un graphique contenu dans un classeur stocké dans Aspose Cloud Storage vers un autre format de fichier (PDF, PNG, SVG, etc.) sans télécharger le fichier source.

## API ExportChartAsFormat

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### 📦 Paramètres de la requête

| Nom                  | Type    | Emplacement | Obligatoire | Description                                                              |
| -------------------- | ------- | ----------- | ----------- | ------------------------------------------------------------------------ |
| **name**             | string  | chemin      | oui         | Nom du fichier du classeur.                                              |
| **worksheet**        | string  | chemin      | oui         | Nom de la feuille de calcul contenant le graphique.                     |
| **chartIndex**       | integer | chemin      | oui         | Index à base zéro du graphique à exporter.                              |
| **format**           | string  | paramètre   | oui         | Format de sortie souhaité (par exemple, `png`, `pdf`, `svg`).           |
| **folder**           | string  | paramètre   | non         | Chemin du dossier où le classeur est stocké (par défaut : racine).      |
| **storageName**      | string  | paramètre   | non         | Nom personnalisé du stockage ; omettre pour utiliser le stockage par défaut. |
| **outPath**          | string  | paramètre   | non         | Chemin du dossier où le fichier converti sera enregistré.              |
| **outStorageName**   | string  | paramètre   | non         | Nom du stockage pour le fichier de sortie.                              |
| **fontsLocation**    | string  | paramètre   | non         | Chemin d’un dossier contenant des polices personnalisées.               |
| **region**           | string  | paramètre   | non         | Paramètre régional (par exemple, `en-US`, `fr-FR`).                     |
| **password**         | string  | paramètre   | non         | Mot de passe pour ouvrir un classeur protégé.                           |

### **Réponse**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**Codes de statut HTTP**

| Code | Signification             | Description                                                             |
| ---- | ------------------------- | ----------------------------------------------------------------------- |
| 200  | OK                        | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé              | Jeton JWT invalide ou manquant.                                         |
| 413  | Charge utile trop grande  | Le fichier téléchargé dépasse la limite de taille.                    |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                           |

## Comment utiliser l’API Export Chart as Format avec les SDK ?

### Spécification de l’API Export Chart as Format

La [spécification de l’API Export Chart as Format](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportChartAsFormat) fournit une interface de programmation publiquement accessible et permet des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}?format={format}" \
  -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (encodé en Base64)",
  "contentType": "type MIME",
  "fileDownloadName": "nom de fichier facultatif"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant de convertir des données de tableur en fichier PDF avec un minimum de code. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

---