---
title: "ConvertRangeToPdf"
ArticleTitle: "Convertir une plage en PDF – API Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /cells/convert/range/pdf
aliases: []
keywords: "Aspose.Cells, convertir une plage en PDF, API"
description: "Convertit une plage spécifiée d’un classeur en PDF à l’aide d’Aspose.Cells Cloud."
weight: 1
---

## ConvertRangeToPdf des services web Aspose.Cells Cloud

Convertit une plage d’un classeur stocké localement en fichier PDF.

### Point de terminaison de l’API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                              |
|------------------|--------|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Fichier | FormData                                               | Télécharger le fichier de classeur.                                                                                                                      |
| worksheet        | Chaîne  | Chaîne de requête                                      | Nom de la feuille de calcul.                                                                                                                             |
| range            | Chaîne  | Chaîne de requête                                      | Zone de cellules (ex. A1:C10)                                                                                                                            |
| outPath          | Chaîne  | Chaîne de requête                                      | (Facultatif) Chemin du dossier où le classeur est stocké. La valeur par défaut est null.                                                               |
| outStorageName   | Chaîne  | Chaîne de requête                                      | Nom du stockage pour le fichier de sortie.                                                                                                              |
| fontsLocation    | Chaîne  | Chaîne de requête                                      | Utiliser des polices personnalisées.                                                                                                                     |
| AutoRowsFit      | Booléen | Chaîne de requête                                      | (Facultatif) Ajuste automatiquement la hauteur de toutes les lignes dans les feuilles de calcul.                                                        |
| AutoColumnsFit   | Booléen | Chaîne de requête                                      | (Facultatif) Ajuste automatiquement la largeur de toutes les colonnes dans les feuilles de calcul.                                                      |
| region           | Chaîne  | Chaîne de requête                                      | Paramètre de région/langue du classeur (ex. `fr-FR`, `en-US`). Affecte le formatage des nombres, l’analyse des dates et le comportement localisé.     |
| password         | Chaîne  | Chaîne de requête                                      | Mot de passe requis pour ouvrir le fichier de classeur.                                                                                                 |

### Paramètre du corps de la requête

| Nom du paramètre | Type   | Description                   |
|------------------|--------|-------------------------------|
| Spreadsheet      | Fichier | Télécharger le fichier de classeur. |

### **Réponse**

```json
{
  "file": "<contenu binaire du PDF>"
}
```

**Codes de statut de la réponse**

| Code | Signification          | Description                                                                 |
|------|------------------------|-----------------------------------------------------------------------------|
| 200  | OK                     | Conversion réussie ; renvoie le flux binaire du fichier PDF généré.        |
| 400  | Mauvaise requête       | URL non valide.                                                             |
| 401  | Non autorisé           | L’authentification a échoué ou aucune information d’identification n’a été fournie. |
| 413  | Charge utile trop grande | La taille du fichier téléchargé dépasse la limite autorisée.              |
| 500  | Erreur interne du serveur | Une anomaly est survenue lors de l’extraction des données de conversion.   |

## Comment utiliser ConvertRangeToPdf avec les SDK

### Spécification de ConvertRangeToPdf

La [spécification de l’API ConvertRangeToPdf](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPdf) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose Cells Cloud. L’exemple suivant montre comment effectuer des appels à l’API cloud avec cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<contenu binaire du PDF>"
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose Cells Cloud à l’aide de divers SDK :

```csharp
// Exemple de code SDK pour C#
var apiInstance = new ConversionApi();
var file = File.OpenRead("sample.xlsx");
var result = apiInstance.ConvertRangeToPdf(file, "Sheet1", "A1:C10", outPath: null, outStorageName: null, fontsLocation: null, autoRowsFit: null, autoColumnsFit: null, region: null, password: null);
File.WriteAllBytes("output.pdf", result);
```

```java
// Exemple de code SDK pour Java
ConversionApi api = new ConversionApi();
File file = new File("sample.xlsx");
byte[] result = api.convertRangeToPdf(file, "Sheet1", "A1:C10", null, null, null, null, null, null, null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Exemple de code SDK pour Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    result = api_instance.convert_range_to_pdf(f, worksheet="Sheet1", range="A1:C10")
    with open("output.pdf", "wb") as out_file:
        out_file.write(result)
```

```javascript
// Exemple de code SDK pour JavaScript/Node.js
const fs = require('fs');
const { ConversionApi } = require('asposecellscloud');
const apiInstance = new ConversionApi();

let file = fs.createReadStream('sample.xlsx');
apiInstance.convertRangeToPdf(file, { worksheet: 'Sheet1', range: 'A1:C10' })
    .then((result) => {
        fs.writeFileSync('output.pdf', result);
    })
    .catch((error) => console.error(error));
```

`[TBD]`
---