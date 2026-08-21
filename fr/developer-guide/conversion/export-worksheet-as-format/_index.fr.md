---
title: "Exporter une feuille de calcul – Aspose.Cells Cloud API v4 (PDF, PNG, SVG, CSV)"
second_title: "Document"
ArticleTitle: "Comment exporter une feuille de calcul de classeur distant vers un autre format : guide pas à pas"
linktype: "Exporter une feuille de calcul"
type: docs
url: /fr/export-worksheet-as-format/
keywords: "Aspose Cells, exporter une feuille de calcul, API cloud, PDF, PNG, CSV, conversion Excel"
description: "Convertir une feuille de calcul stockée dans Aspose.Cells Cloud en PDF, PNG, SVG, CSV ou d'autres formats via une seule requête GET. Inclut des exemples de code en C#, Java, Python, et plus encore."
weight: 100
---

Exporter une feuille de calcul ou classeur cloud vers un fichier d’un autre format à l’aide de l’API Web Aspose.Cells Cloud.

## **Exporter une feuille de calcul vers un format – API**

### API Web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de la requête**

| Nom du paramètre   | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                        |
| :----------------- | :----- | :---------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | String | Chemin                                                | (Obligatoire) Le nom du fichier classeur à récupérer.                                                                                              |
| **worksheet**      | String | Chemin                                                | (Obligatoire) La feuille de calcul spécifique à convertir.                                                                                        |
| **format**         | String | Chaîne de requête                                     | (Obligatoire) Le format de sortie souhaité (par exemple, `png`, `pdf`, `svg`).                                                                    |
| **folder**         | String | Chaîne de requête                                     | (Facultatif) Le chemin du dossier dans lequel le classeur est stocké. La valeur par défaut est `null`.                                            |
| **storageName**    | String | Chaîne de requête                                     | (Facultatif) Le nom du stockage cloud personnalisé. Utilise le stockage par défaut si omis.                                                       |
| **outPath**        | String | Chaîne de requête                                     | (Facultatif) Le chemin du dossier de sortie. La valeur par défaut est `null`.                                                                     |
| **outStorageName** | String | Chaîne de requête                                     | (Facultatif) Le nom du stockage pour le fichier de sortie.                                                                                        |
| **fontsLocation**  | String | Chaîne de requête                                     | (Facultatif) Spécifier des polices personnalisées si nécessaire.                                                                                  |
| **region**         | String | Chaîne de requête                                     | (Facultatif) Paramètre de région/langue du classeur (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement localisé. |
| **password**       | String | Chaîne de requête                                     | (Facultatif) Le mot de passe pour accéder au fichier de classeur.                                                                                |

### **Réponse**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Codes d’état HTTP**

| Code | Signification            | Description                                                    |
| ---- | ------------------------ | -------------------------------------------------------------- |
| 200  | OK                       | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte       | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé             | Jeton JWT invalide ou manquant.                                |
| 413  | Payload trop volumineux  | Le fichier téléchargé dépasse la taille limite.              |
| 500  | Erreur interne du serveur| Erreur serveur inattendue.                                     |

## **Dans quel cas utiliser l’API d’exportation d’une feuille de calcul vers un autre format ?**

- **Migration de systèmes hérités** – Convertir des milliers de fichiers XLS hérités en XLSX pour les systèmes modernes.
- **Standardisation d’archivage** – Normaliser divers formats de classeurs (XLS, XLSM, ODS, CSV) vers un seul format pour l’archivage.
- **Interopérabilité avec suites bureautiques** – Convertir des fichiers Excel vers des formats compatibles avec LibreOffice, Google Sheets ou Apple Numbers.
- **Normalisation des sources de données** – Convertir divers formats de classeurs en CSV ou JSON pour ingestion dans une base de données.
- **Publication web** – Convertir des modèles financiers en HTML pour affichage sur le web.

## Pourquoi utiliser l’API d’exportation d’une feuille de calcul vers un autre format ?

- **Prise en charge multi-langages des SDK** – Fournit des bibliothèques client pour plusieurs langages de programmation, permettant aux développeurs d’appeler l’API directement depuis leur environnement préféré.
- **Conversion directe sans téléchargement intermédiaire** – Permet de convertir une feuille de calcul stockée dans le stockage cloud vers le format demandé, sans avoir à télécharger puis réuploade le fichier.
- **Extraction des données uniquement** – Renvoie le contenu de la feuille de calcul dans le format sélectionné, sans préserver le style visuel.

## Comment utiliser l’API d’exportation d’une feuille de calcul vers un format à l’aide des SDK ?

### Spécification de l’API d’exportation d’une feuille de calcul vers un format

La [spécification de l’API d’exportation d’une feuille de calcul vers un format](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportWorksheetAsFormat) fournit une interface de programmation publiquement accessible permettant d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et permet d’exporter une feuille de calcul vers un fichier d’un autre format à l’aide d’un code court.  
Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}