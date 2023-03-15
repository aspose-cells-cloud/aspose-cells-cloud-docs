---
title: Переместить папку
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/folder/move/
keywords: Learn how to move folder with Aspose Cells Cloud REST API
description: Узнайте, как переместить папку с Aspose Cells Cloud REST API SDK, поддерживающим различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и swift.
weight: 100
---
Этот REST API указывает `move folder`
 
## РСЕТ API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| srcPath| нить| путь| Путь к папке для перемещения, например, «/folder»|
| путь назначения| нить| запрос| Путь к папке назначения для перемещения, например, «/dst»|
| srcStorageName| нить| запрос| Имя исходного хранилища|
| destStorageName| нить| запрос| Имя целевого хранилища|

 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder" \
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
 
 Использование SDK — лучший способ ускорить разработку. SDK позаботится о низкоуровневых деталях и позволит вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) полный список Aspose.Cells Cloud SDK.
 
В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с помощью различных SDK.
 
 