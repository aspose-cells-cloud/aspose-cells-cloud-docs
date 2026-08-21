---
title: "Enregistrer un classeur Excel – API Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Enregistrer sous"
type: docs
url: /save-an-excel-file-as-other-formats-files/
aliases:
  - /convert-excel-workbook-to-different-file-formats/
  - /saveas-other-formats/
keywords: "Aspose Cells, Excel, Enregistrer sous, PDF, CSV, JSON, Markdown, API REST"
description: "Enregistrez des classeurs Excel au format PDF, CSV, JSON, Markdown et d'autres formats à l'aide de l'API REST Aspose.Cells Cloud."
weight: 30
---

Cette API REST vous permet **d'enregistrer** un fichier Excel dans différents formats.  
Avant d'appeler ce point de terminaison, assurez-vous de disposer d'un jeton d'accès OAuth 2.0 valide et que le classeur source est stocké dans votre espace de stockage Aspose Cloud.

**Prérequis**  
1. Obtenez un jeton d'accès JWT et incluez-le dans l'en-tête `Authorization: Bearer <token>` de chaque requête.  
2. Téléversez le classeur source vers l'espace de stockage Aspose Cloud (ou confirmez qu'il existe déjà).  
3. Connaître le nom de l'espace de stockage et le chemin du dossier contenant le classeur.

## API PostWorkbookSaveAs

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/saveAs
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification par jeton JWT</a>.

### **Paramètre de chemin**

| Nom du paramètre | Type   | Description                           |
| ---------------- | ------ | ------------------------------------- |
| name             | string | Nom du fichier Excel.                 |

### **Paramètre de requête**

| Nom du paramètre      | Type   | Description                                                                                              |
| --------------------- | ------ | -------------------------------------------------------------------------------------------------------- |
| newfilename           | string | Nom du nouveau fichier à enregistrer.                                                                   |
| isAutoFitRows         | string | Si `true`, ajuste automatiquement la hauteur de toutes les lignes du classeur. Par défaut : `false`.    |
| isAutoFitColumns      | string | Si `true`, ajuste automatiquement la largeur des colonnes du classeur. Par défaut : `false`.            |
| folder                | string | Dossier contenant le classeur original.                                                                  |
| storageName           | string | Nom de l'espace de stockage où se trouve le fichier source.                                             |
| outStorageName        | string | Nom de l'espace de stockage où le fichier de sortie sera enregistré.                                    |
| checkExcelRestriction | bool   | Indique s’il faut appliquer les restrictions Excel lors de la modification des cellules ou des objets associés. |
| region                | string | Paramètres régionaux appliqués au classeur.                                                             |
| pageWideFitOnPerSheet | bool   | Ajuste la largeur de page à chaque feuille de calcul lors de la conversion.                             |
| pageTallFitOnPerSheet | bool   | Ajuste la hauteur de page à chaque feuille de calcul lors de la conversion.                             |
| sheetName             | string | Nom de la feuille de calcul à convertir.                                                                |
| pageIndex             | string | Index de la page à convertir dans la feuille spécifiée (nécessite `sheetName`).                         |
| onePagePerSheet       | bool   | Lors de la conversion au format PDF, génère une page par feuille de calcul.                             |

### **Paramètre du corps de la requête**

| Nom du paramètre | Type   | Description                                                   |
| ---------------- | ------ | ------------------------------------------------------------- |
| SaveOptions      | Object | Options d'enregistrement fournies dans la deuxième partie de la requête multipart. |

**Exemple de corps de requête (partie JSON de la requête multipart)**

```json
{
  "SaveOptions": {
    "SaveFormat": "pdf",
    "CompressionLevel": 9
  }
}
```

### Réponse

L'API renvoie un objet `SaveResponse`.

```json
{
  "Status": "OK",
  "Code": 200,
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  }
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                       |
|------|-----------------------------|-------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l'opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                   |
| 413  | Charge utile trop grande     | Le fichier téléversé dépasse la taille maximale autorisée.       |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                        |

## Comment utiliser l'API PostWorkbookSaveAs avec les SDK

### Spécification de l'API PostWorkbookSaveAs

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser **cURL** pour accéder facilement aux services web Aspose.Cells. L'exemple ci-dessous montre comment appeler l'API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" \
  -H "accept: multipart/form-data" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L'utilisation d'un SDK est le moyen le plus efficace d'accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}

Pour d'autres scénarios de conversion, consultez les guides [Convertir Excel en PDF](/convert-excel-to-pdf/) et [Exporter Excel en CSV](/export-excel-to-csv/).