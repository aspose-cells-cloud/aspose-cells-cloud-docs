---
title: Переместить файл
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/file/move/
keywords: Learn how to download file with Aspose Cells Cloud REST API
description: Узнайте, как загрузить файл с помощью Aspose Cells Cloud REST API SDK, поддерживающего различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 100
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdwon, Переместить файл
---
Этот REST API указывает на `move file`.
 
## РСЕТ API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| исходный путь| нить| путь|Путь к исходному файлу, например «/src.ext».|
| путь назначения| нить| запрос| Путь к целевому файлу, например «/dest.ext».|
| имя_источника_хранилища| нить| запрос| Имя исходного хранилища|
| destStorageName| нить| запрос| Имя целевого хранилища|
| идентификатор версии| нить| запрос| Идентификатор версии файла для перемещения|
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/File/MoveFile) определяет общедоступный интерфейс программирования и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для легкого доступа к веб-службам Aspose.Cells. В следующем примере показано, как позвонить на Cloud API с помощью cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/move/Book2.xlsx?destPath=MoveBook2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Семейство облачных SDK
 
 Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для получения полного списка Aspose.Cells Cloud SDK.
 
Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:
 
 
