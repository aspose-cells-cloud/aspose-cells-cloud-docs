---
title: Скачать файл
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/file/download/
keywords: Learn how to download file with Aspose Cells Cloud REST API
description: Узнайте, как загрузить файл с Aspose Cells Cloud REST API SDK, поддерживающим различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и swift.
weight: 100
---
Этот REST API указывает на `download file`.
 
## РСЕТ API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/file/{path}
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| путь| нить| путь| Путь к файлу, например, '/folder/file.ext'|
| имя_хранилища| нить| запрос| Имя хранилища|
| идентификатор версии| нить| запрос| Идентификатор версии файла для загрузки|
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/File/DownloadFile) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash

{
    Stream
}

```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Семейство облачных SDK
 
 Использование SDK — лучший способ ускорить разработку. SDK позаботится о низкоуровневых деталях и позволит вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) полный список Aspose.Cells Cloud SDK.
 
В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с помощью различных SDK.
 
 
 
 

