---
title: "Set a Particular Document Property"
type: docs
url: /set-a-particular-document-property/
weight: 30
---

## **Introduction**
This example shows you how to set a document property in a Excel Worksheet using Aspose.Cells Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
 
### **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/documentproperties/{propertyName}|PUT|Update a document property|[PutDocumentProperty](https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" -H "accept: application/json" -H "authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYmYiOjE1Njk2MTk0NDUsImV4cCI6MTU2OTcwNTg0NSwiaXNzIjoiaHR0cHM6Ly9hcGkuYXNwb3NlLmNsb3VkIiwiYXVkIjpbImh0dHBzOi8vYXBpLmFzcG9zZS5jbG91ZC9yZXNvdXJjZXMiLCJhcGkucGxhdGZvcm0iLCJhcGkucHJvZHVjdHMiXSwiY2xpZW50X2lkIjoiOWYwYjI2ZDEtMGYxZi00MDNiLTliYTQtMTMzMzk4MGFjNmRiIiwiY2xpZW50X2lkU3J2SWQiOiIiLCJzY29wZSI6WyJhcGkucGxhdGZvcm0iLCJhcGkucHJvZHVjdHMiXX0.at8j6tzptIioEjlSxLX63ouBnmECXvc0NagF9YUi9JU-npyc4dmui_ZhCfQDyYexe8ryFrxF5g_ZP7lhjirvM8p1BJfSR_ferQkk1t-kCS-J4uvjsNzBW0kb9L4sm5u2DWka8-9vGt04psKRALHZRpC7PWBdNJZXYWHpecZXlgUz03PEq_INKbl0fiDZohuKUTrUBa1xNZFdjz3iQoABRP7RmnNPdJrReAL6qZWriVNbPKBaVdMzNPfpRGT07sQa6S-pZvbq-5RiAkwBY9E6IBNwQdN3ykz2W7t8dyH7xFte6WiKERsnjIIhkdp0jjuhaT-F73F5Z1Au38yPZYcXzQ" -H "Content-Type: application/json" -d "{ \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" }, \"Name\": \"author\", \"Value\": \"aspose\", \"BuiltIn\": \"string\"}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "DocumentProperty": {

    "Name": "Author",

    "Value": "aspose",

    "BuiltIn": "True",

    "link": {

      "Href": "/test.xlsx/documentproperties/Author",

      "Rel": "self",

      "Title": null,

      "Type": null

    }

  },

  "Code": 201,

  "Status": "Created"

}

```

{{< /tab >}}

{{< /tabs >}}
## **SDK Source**
The Aspose.Cells Cloud SDKs can be downloaded from the following page: [Available SDKs](/available-sdks/)
## **SDK Examples**
{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Examples-DotNET-CSharp-Document-Properties-SetParticularProperty-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "af3fea45644d431483f6df52cf3bfe26" "Examples-Java-properties-SetParticularProperty-set-particular-property.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "3c5c9f9fff9898bb8251aa7ee9191641" "Examples-Ruby-Document-create_document_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "5161752550311c9baf73ffa0a811ea0b" "SetParticularDocumentProperties.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Document-Properties-SetParticularProperty-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cloud" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-properties-SetParticularProperty-set-particular-property.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Document-Properties-SetParticularProperty-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cloud" "6f152beef44ecbb7776a0f257e12926c" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cloud" "cbfaae84991c29df75197545b87c736d" >}}

{{< /tab >}}

{{< /tabs >}}
