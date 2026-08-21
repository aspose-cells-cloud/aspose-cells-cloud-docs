---
title: "Importer des données sans utiliser de stockage – API Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Importer des données sans stockage"
type: docs
url: /import/without-using-storage/
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: "Aspose.Cells, API Cloud, importer des données sans stockage, API d'import Excel, import REST"
description: "Découvrez comment importer des données sans stockage dans un classeur Excel à l’aide de l’API Aspose.Cells Cloud. Inclut le format de requête, les paramètres, un exemple cURL, du code SDK et la gestion des erreurs."
weight: 10
ArticleTitle: "Importer des données sans utiliser de stockage – API Aspose.Cells Cloud"
---

L’importation de données Excel peut être complexe car de nombreux facteurs influencent le résultat. Tous ces facteurs doivent être pris en compte pendant le processus d’**import**. Aspose.Cells Cloud simplifie l’importation de divers formats et types de données dans un fichier Excel avec une qualité professionnelle.

Cette API REST permet d’**importer des données** dans un fichier Excel.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une authentification basée sur <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type          | Emplacement  | Description                                                                                                                                     |
| ---------------- | ------------- | ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| file             | fichier       | formData     | Le fichier Excel à télécharger.                                                                                                                 |
| ImportOption     | ImportOption  | corps JSON   | Objet JSON définissant les données à importer, leur type (par exemple, `IntArray`, `DoubleArray`, `StringArray`) et leur position dans la feuille de calcul. |

Les paramètres **ImportOption** sont décrits dans la **référence des options d’importation** [/cells/import/#import-data-option-parameter](/cells/import/#import-data-option-parameter).

**Prérequis :**  
Un jeton JWT valide doit être généré au préalable, et la taille du fichier ne doit pas dépasser la limite du service (généralement 100 Mo). Les formats de fichier pris en charge incluent XLS, XLSX, CSV et ODS. Assurez-vous que le SDK approprié est installé si vous préférez un accès programmatique.

### Réponse

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codes d’état HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                             |
| 413  | Charge utile trop grande     | Le fichier téléversé dépasse la limite de taille.                          |
| 500  | Erreur interne du serveur    | Erreur inattendue du serveur.                                               |

**Notes :**  
Lors de l’envoi de la requête, l’en-tête `Content-Type: multipart/form-data` est automatiquement défini par l’option `-F`. Pour les charges utiles volumineuses, envisagez de compresser les données avant l’import et mettez en place une logique de reprise en cas d’erreurs transitoires.

## Comment utiliser l’API PostImportData avec les SDK

### Spécification de l’API PostImportData

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/import" \
  -X POST \
  -H "Authorization: Bearer <jeton_jwt>" \
  -F "file=@fichier.xlsx" \
  -F "ImportOption={\"Data\":[1,2,4],\"DestinationWorksheet\":\"Feuil1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"ImportDataType\":\"IntArray\"}"
```

*L’option `-F` définit automatiquement `Content-Type: multipart/form-data`.*  

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status":"OK",
  "Code":200
}
```

{{< /tab >}}

{{< /tabs >}}


### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostImportData.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostImportData.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostImportData.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostImportData.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostImportData.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostImportData.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostImportData.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostImportData.go" >}}

{{< /tab >}}

{{< /tabs >}}