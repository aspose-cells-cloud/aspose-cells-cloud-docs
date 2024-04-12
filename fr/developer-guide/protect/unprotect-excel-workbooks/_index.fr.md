---
title: Déprotéger un classeur Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Non protégé
type: docs
url: /fr/workbook/unprotect/
aliases: [/unprotect-excel-workbooks/]
keywords: REST API, spreadsheets, excel, merg
description: "Cells.Cloud API pour Excel fonctionner : protéger un classeur Excel"
weight: 60
---
Ce REST API dé-protège un Excel `workbook`.

**Paramètre de requête**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
|dossier|chaîne|Dossier de classeur d'origine.|
|Nom de stockage|chaîne|Nom de stockage.|

**Paramètre du corps de la demande**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
|protection|Demande de protection du classeur||

**Demande de protection du classeur**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
|Type de protection|chaîne|TOUS/CONTENU/AUCUN/OBJETS/SCÉNARIOS/STRUCTURE/FENÊTRES|
|Mot de passe|chaîne||


## REPOS API

|**API**|**Taper**|**Description**|**Lien fanfaron**|
|:- |:- |:- |:- |
|/cellules/{nom}/protection|SUPPRIMER|Déprotéger un document|[SupprimerUnProtectDocument](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectDocument)|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectDocument) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement depuis un navigateur Web.

 Vous pouvez utiliser**cURL** outil de ligne de commande pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection" -H "accept: application/json"  -H "Content-Type: application/json" -d "{ \"ProtectionType\": \"all\", \"Password\": \"aspose\"}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code":"200",

  "Status":"OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d’accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Java" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookDeleteUnProtectDocument.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-DeleteUnProtectDocument-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Document-unprotect_document-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-workbook-UnprotectWorkbook-unprotect-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnProtectExcelWorkbooks.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-UnprotectWorkbook-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-UnprotectWorkbook-unprotect-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-UnprotectWorkbook-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e70e326db37cfb9a80aadf9d795687c5" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "a856eb7506ccc320def87e055b177ca5" >}}

{{< /tab >}}

{{< /tabs >}}
