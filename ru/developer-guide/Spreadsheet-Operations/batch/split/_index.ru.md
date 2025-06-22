---
title: Пакетное разделение
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/batch/split
keywords: Batch split Excel file
description: Aspose.Cells Cloud API поддерживает пакетное разделение файлов. SDK поддерживает различные языки разработки. Они включают Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift
weight: 100
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Пакетное разделение
---
Этот REST API указывает на `batch split` соответствующего файла.

## РЕТ API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/split
 
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
|BatchSplitRequest|| тело||

**Свойства BatchSplitRequest**

Имя | Тип | Описание | Примечания
------------ | ------------- | ------------- | -------------
 SourceFolder | string | | [необязательно]SourceStorage | string | | [необязательно]MatchCondition | MatchConditionRequest | | [необязательно]Format | string | | [необязательно]FromIndex | integer | | [необязательно]ToIndex | integer | | [необязательно]OutFolder | string | | [необязательно]SaveOptions | SaveOptions | | [необязательно]**Свойства MatchConditionRequest**

Имя | Тип | Описание | Примечания
------------ | ------------- | ------------- | -------------
 RegexPattern | string | | [необязательно]FullMatchConditions | string[]| | [необязательно][Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать командную строку cURL для легкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}" 
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
 
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет вам сосредоточиться на ваших разделенных задачах. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
