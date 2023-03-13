---
title: Protégez un Workboo Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Protec
type: docs
url: /fr/workbook/protect/
aliases: [/protect-excel-workbooks/]
keywords: Protect Excel files
description: Aspose.Cells Cloud REST API prend en charge la protection des fichiers Excel. SDK prend en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift
weight: 30
---
Ce REST API protège un Excel `workbook`.

**Paramètre de requête**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
|dossier|chaîne|Dossier de classeur d'origine.|
|nom_stockage|chaîne|Nom de stockage.|

**Paramètre de corps de requête**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
|protection|WorkbookProtectionRequestWorkbookProtectionRequest||

**WorkbookProtectionRequestWorkbookProtectionRequest**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
|Type de protection|chaîne|TOUT/CONTENU/AUCUN/OBJETS/SCÉNARIOS/STRUCTURE/FENÊTRES|
|Mot de passe|chaîne||



## REPOS API

|**API**|**Taper**|**Description**|**Lien fanfaron**|
|:- |:- |:- |:- |
|/cellules/{nom}/protection|POSTE|Protéger un document|[PostProtectDocument](https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument)|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.

 Vous pouvez utiliser**cURL** outil de ligne de commande pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"ProtectionType\": \"all\", \"Password\": \"aspose\"}"

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

## Famille SDK Cloud

 L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Référentiel GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookPostProtectDocument.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-workbook-ProtectWorkbook-protect-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostProtectDocument-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Document-protect_document-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ProtectExcelWorkbooks.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-ProtectWorkbook-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-ProtectWorkbook-protect-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example-encrypt-with-password.go" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-ProtectWorkbook-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "81821b7ead61ba5371d2b1130aba0c2f" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "5a57805e300750236fa567e015f1677b" >}}

{{< /tab >}}

{{< /tabs >}}
