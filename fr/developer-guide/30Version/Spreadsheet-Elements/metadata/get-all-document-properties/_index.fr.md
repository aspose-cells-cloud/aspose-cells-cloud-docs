---
title: Obtenir toutes les propriétés du document
second_title: Documen
linktitle: Obtenez tout
type: docs
url: /fr/document-properties/get-all/
aliases: [/get-all-document-properties/]
keywords: Get properties from excel files
description: Aspose.Cells Cloud REST API prend en charge l'obtention de propriétés à partir de fichiers Excel. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 25
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Obtenir toutes les propriétés du document
---
Ce REST API indique de lire les propriétés du document.

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/documentproperties
 
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| Le nom du document.|
| dossier| chaîne| requête| Le dossier de documents.|
| nom de stockage| chaîne| requête| nom de stockage.|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperties) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{

  "DocumentProperties": {

    "DocumentPropertyList": [

      {

        "Name": "Title",

        "Value": "",

        "BuiltIn": "True",

        "link": {

          "Href": "/Title",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "Subject",

        "Value": "",

        "BuiltIn": "True",

        "link": {

          "Href": "/Subject",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "Author",

        "Value": "",

        "BuiltIn": "True",

        "link": {

          "Href": "/Author",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "Keywords",

        "Value": "",

        "BuiltIn": "True",

        "link": {

          "Href": "/Keywords",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "Comments",

        "Value": "",

        "BuiltIn": "True",

        "link": {

          "Href": "/Comments",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "LastSavedBy",

        "Value": "",

        "BuiltIn": "True",

        "link": {

          "Href": "/LastSavedBy",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "CreateTime",

        "Value": "6/5/2015 6:17:20 PM",

        "BuiltIn": "True",

        "link": {

          "Href": "/CreateTime",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "LastSavedTime",

        "Value": "9/27/2019 9:09:43 PM",

        "BuiltIn": "True",

        "link": {

          "Href": "/LastSavedTime",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "Category",

        "Value": "",

        "BuiltIn": "True",

        "link": {

          "Href": "/Category",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "NameOfApplication",

        "Value": "Microsoft Excel",

        "BuiltIn": "True",

        "link": {

          "Href": "/NameOfApplication",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "Version",

        "Value": "16.0300",

        "BuiltIn": "True",

        "link": {

          "Href": "/Version",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "Security",

        "Value": "0",

        "BuiltIn": "True",

        "link": {

          "Href": "/Security",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "ScaleCrop",

        "Value": "False",

        "BuiltIn": "True",

        "link": {

          "Href": "/ScaleCrop",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "Template",

        "Value": "",

        "BuiltIn": "True",

        "link": {

          "Href": "/Template",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "Manager",

        "Value": "",

        "BuiltIn": "True",

        "link": {

          "Href": "/Manager",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "Company",

        "Value": "",

        "BuiltIn": "True",

        "link": {

          "Href": "/Company",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "Name": "LinksUpToDate",

        "Value": "False",

        "BuiltIn": "True",

        "link": {

          "Href": "/LinksUpToDate",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      }

    ],

    "link": {

      "Href": "/test.xlsx/documentproperties",

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

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperties.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperties.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperties.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperties.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperties.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperties.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperties.go" >}}

{{< /tab >}}

{{< /tabs >}}
