﻿---
title: Установите конкретное свойство документа
second_title: Aspose.Cells Cloud Documen
linktitle: Обновление
type: docs
url: /ru/document-properties/update/
aliases: [/set-a-particular-document-property/]
keywords: Update properties from excel files
description: Aspose.Cells Cloud REST API поддерживает обновление свойств из файлов Excel. SDK поддерживает различные языки разработки. Они включают Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift
weight: 30
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Установка определенного свойства документа
---
Этот REST API указывает на свойство документа `set/create`.

## РЕТ API

```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
 
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь| Название документа.|
| Имясвойства| нить| путь| Имя свойства.|
| свойство|| тело| с новой стоимостью недвижимости.|
| папка| нить| запрос| Папка с документами.|
| имя_хранилища| нить| запрос| имя хранилища.|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать командную строку cURL для легкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author"  \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d "{ \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" }, \"Name\": \"author\", \"Value\": \"aspose\", \"BuiltIn\": \"string\"}"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

  "Code": 200,

  "Status": "Created"

}

```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}
