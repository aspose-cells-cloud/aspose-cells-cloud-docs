﻿---
title: Получить файл
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/folder/get-files/
keywords: Learn how to get files from folder with Aspose Cells Cloud REST API
description: Узнайте, как получить файл из папки с помощью Aspose Cells Cloud REST API SDK, поддерживающего различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 100
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdwon, Получить файлы
---
Этот REST API указывает на `get files`.
 
## РСЕТ API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| путь| нить| путь| Путь к папке, например «/folder»|
| имя_хранилища| нить| запрос| Имя хранилища|
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) определяет общедоступный интерфейс программирования и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для легкого доступа к веб-службам Aspose.Cells. В следующем примере показано, как позвонить на Cloud API с помощью cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 0,
      "Path": "string"
    }
  ]
}
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Семейство облачных SDK
 
 Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для получения полного списка Aspose.Cells Cloud SDK.
 
Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:
 
 
 
 

