---
title: "Remove a Particular Document Property"
type: docs
url: /remove-a-particular-document-property/
weight: 50
---

## **Introduction**
This example shows how to remove a particular property from a Excel Workbook using Aspose.Cells Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.

## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/documentproperties/{propertyName}|DELETE|Remove a particular property|[DeleteDocumentProperty](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperty)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" -H "accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

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

        "Value": "",

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

        "Value": "14.0300",

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
## **SDK Source**
The Aspose.Cells Cloud SDKs can be downloaded from the following page: [Available SDKs](/cells/available-sdks/)
### **SDK Examples**
{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Examples-DotNET-CSharp-Document-Properties-RemoveParticularProperty-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "af3fea45644d431483f6df52cf3bfe26" "Examples-Java-properties-RemoveParticularProperty-remove-particular-property.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "3c5c9f9fff9898bb8251aa7ee9191641" "Examples-Ruby-Document-delete_document_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "5161752550311c9baf73ffa0a811ea0b" "RemoveParticularDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Document-Properties-RemoveParticularProperty-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cloud" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-properties-RemoveParticularProperty-remove-particular-property.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Document-Properties-RemoveParticularProperty-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cloud" "998e9933fd0e00942039175ebc85a76f" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cloud" "1d4dd557dfa1834527376159043d428b" >}}

{{< /tab >}}

{{< /tabs >}}
