---
title: "Remplacer du texte dans un classeur Excel"
second_title: "Document"
linktitle: "Remplacer dans le classeur"
type: docs
url: /fr/workbook/replace-text/
aliases: [  /fr/replace-text-in-a-workbook/ ]
weight: 60
keywords: "Aspose.Cells Cloud, Remplacer du texte, Classeur Excel, XLSX, ODS, API REST, Feuille de calcul, SDK"
description: "Remplacer du texte dans des classeurs Excel (XLS, XLSX, XLSM, XLSB) et des classeurs OpenDocument Spreadsheet (ODS) à l’aide de l’API REST Aspose.Cells Cloud. Disponible via cURL et une large gamme de SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, etc.)."
---

Cette API REST permet de remplacer du texte dans un classeur Excel.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/replaceText
```
### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                              |
| ---------------- | ------ | ----------- | -------------------------------------------------------- |
| name             | string | path        | Nom du fichier du classeur.                              |
| sheetName        | string | path        | Nom de la feuille de calcul dans laquelle la substitution a lieu. |
| oldValue         | string | query       | Texte à remplacer.                                       |
| newValue         | string | query       | Texte qui remplacera l’ancienne valeur.                  |
| folder           | string | query       | Chemin du dossier contenant le classeur.                 |
| storageName      | string | query       | Nom du service de stockage dans lequel réside le classeur. |

### **Réponse**

```json
{
    "Status":"OK",
    "Code":200,
      "Workbook": {
    "FileName": "test.xlsx",
    "Links": [
      {
        "Href": "/test.xlsx",
        "Rel": "self",
        "Title": null,
        "Type": null
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Télécharger au format CSV",
        "Type": "text/csv"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Télécharger au format HTML",
        "Type": "text/html"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Télécharger au format ODS",
        "Type": "application/vnd.oasis.opendocument.spreadsheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Télécharger au format PDF",
        "Type": "application/pdf"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Télécharger au format texte délimité par tableaux",
        "Type": "text/plain"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Télécharger au format TIFF",
        "Type": "image/tiff"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Télécharger au format Microsoft Excel 2003",
        "Type": "application/vnd.ms-excel"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Télécharger au format Microsoft Excel 2007",
        "Type": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Télécharger au format XPS",
        "Type": "application/vnd.ms-xpsdocument"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "/worksheets",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "/defaultstyle",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "/documentproperties",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Names": {
      "link": {
        "Href": "/names",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Settings": {
      "link": {
        "Href": "/settings",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "IsWriteProtected": "False",
    "IsProtected": "False",
    "IsEncryption": "false",
    "Password": null
  }
}
```

**Codes d’état HTTP**

| Code | Signification               | Description                                                 |
|------|-----------------------------|-------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                             |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la limite de taille.         |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur.                               |

## Comment utiliser l’API PostReplace avec les SDK

### Spécification de l’API PostReplace

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetTextReplace) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour appeler facilement les services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer une requête avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/replaceText?oldValue=a&newValue=a12" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Matches": 26,
  "Workbook": {
    "link": {
      "Href": "/test.xlsx",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour intégrer cette fonctionnalité. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookTextReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookTextReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookTextReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookTextReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookTextReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookTextReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookTextReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookTextReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}