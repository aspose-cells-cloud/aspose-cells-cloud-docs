---
title: Enregistrer sous Excel
second_title: Documen
linktitle: Enregistrer un
type: docs
url: /fr/save-an-excel-file-as-other-formats-files/
aliases: [/convert-excel-workbook-to-different-file-formats/, /saveas-other-formats/]
keywords: Save excel files as kinds of format files
description: Aspose.Cells Cloud REST API prend en charge l'enregistrement de fichiers Excel sous différents formats. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 30
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Enregistrer sous Excel
---
Ce REST API indique le fichier Excel `save` comme un fichier de format différent.

**Paramètre de chemin**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
|nom|chaîne| Le nom du fichier.|

**Paramètre de requête**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
|nouveau nom de fichier|chaîne| nouveau nom de fichier|
|isAutoFitRows|chaîne| Ajuste automatiquement toutes les lignes de ce classeur. La valeur par défaut est « false ».|
|isAutoFitColumns|chaîne| Ajuste automatiquement la largeur des colonnes de ce classeur. La valeur par défaut est « false ».|
|dossier|chaîne|Classeur original.|
|nom de stockage|chaîne| Le nom du stockage où se trouve le fichier.|
|outStorageName|chaîne| Le nom du stockage où se trouve le fichier enregistré.|
|vérifierExcelRestriction|booléen| Vérifiez si la restriction du fichier Excel est vérifiée lorsque l'utilisateur modifie les objets liés aux cellules.|
|région|chaîne| Les paramètres régionaux du classeur.|
|pageWideFitOnPerSheet|booléen| La page s'adapte à la largeur de la feuille de calcul.|
|pageTallFitOnPerSheet|booléen| La page haute tient sur la feuille de calcul.|
|nom de la feuille|chaîne| Convertissez la feuille de calcul spécifiée.|
|pageIndex|chaîne| Convertissez la page spécifiée de la feuille de calcul, sheetName est requis.|
|une page par feuille|booléen| Lors de la conversion au format PDF, une page par feuille.|

**Paramètre du corps de la requête**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
|Options de sauvegarde| Objet|Option d'enregistrement pour enregistrer dans la deuxième partie du contenu en plusieurs parties.|

## RESTE API

|**API**|**Taper**|**Description**|**Lien vers la ressource**|
|:- |:- |:- |:- |
|/cellules/{nom}/enregistrer sous|POSTE|Exporter le classeur au format|[PostDocumentEnregistrer sous](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

 Vous pouvez utiliser**cURL** Outil en ligne de commande pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le cloud API avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" -H "accept: multipart/form-data" 

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
  "SaveResult": {
    "SourceDocument": {
      "Href": "test.xlsx",
      "Rel": null,
      "Title": null,
      "Type": null
    },
    "DestDocument": {
      "Href": "test.pdf",
      "Rel": null,
      "Title": null,
      "Type": null
    },
    "AdditionalItems": []
  },
  "Code": 200,
  "Status": "OK"
}

```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

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
