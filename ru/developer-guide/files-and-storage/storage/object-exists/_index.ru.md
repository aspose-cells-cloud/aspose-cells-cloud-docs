﻿---
title: Объект существует
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/storage/object-exists/
keywords: Learn how to check object exist with Aspose Cells Cloud REST API
description: Узнайте, как проверить существование объекта с помощью Aspose Cells Cloud REST API SDK, поддерживающего различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 100
kwords: Excel, Office Облако, REST API, электронная таблица, PDF, CSV, Json, Markdwon, объект существует
---
Этот REST API указывает на проверку `file or folder exists`.
 
## РСЕТ API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/exist/{path}
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| путь| нить| путь| Путь к файлу или папке, например «/file.ext» или «/folder».|
| имя_хранилища| нить| запрос| Имя хранилища|
| идентификатор версии| нить| запрос| Идентификатор версии файла|

 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) определяет общедоступный интерфейс программирования и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для легкого доступа к веб-службам Aspose.Cells. В следующем примере показано, как позвонить на Cloud API с помощью cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName21="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
  "Exists": true,
  "IsFolder": false
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Семейство облачных SDK
 
 Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для получения полного списка Aspose.Cells Cloud SDK.
 
Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:
 
 
