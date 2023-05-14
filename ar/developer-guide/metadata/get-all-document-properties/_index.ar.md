---
title: Get All Document Propertie
second_title: Aspose.Cells Cloud Documen
linktitle: Get al
type: docs
url: /ar/document-properties/get-all/
aliases: [/get-all-document-properties/]
keywords: Get properties from excel files
description: Aspose.Cells Cloud REST API support getting properties from excel files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift
weight: 25
---
This REST API indicates to read document properties.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/documentproperties
 
```
The request parameters are: 
 
|Parameter Name |Type |Path/Query String/HTTPBody |Description|
|:- |:- |:- |:- |
|name |string |path |The document name. |
|folder |string |query |The document folder. |
|storageName |string |query |storage name. |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperties) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

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

## Cloud SDK Family
 
Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
 
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Go" tabName10="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Document-Properties-GetAllProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-properties-GetAllProperties-get-all-document-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Document-read_document_properties-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetAllDocumentProperties.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Document-Properties-GetAllProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-properties-GetAllProperties-get-all-document-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "5f24423a3e2baa1f81d494ae28b7f236" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8b6b3b09a51ee508082813294346e672" >}}

{{< /tab >}}

{{< /tabs >}}
