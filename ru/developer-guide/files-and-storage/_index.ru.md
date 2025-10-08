---
title: Файлы и хранение
second_title: Documen
type: docs
url: /ru/files-and-storage/
aliases: [/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: Aspose Cells Cloud file storage, upload, download, delete, move, copy file
description: Полное руководство по использованию Aspose Cells Cloud для хранения файлов, включая загрузку, скачивание и управление файлами. Поддержка SDK для различных языков программирования, таких как Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 100
kwords: Aspose Cells, Облачное хранилище, REST API, Управление файлами, Excel, PDF, CSV, JSON, Markdow
---
 Aspose.Cells Cloud предоставляет комплексные вспомогательные функции для работы с файлами, загруженными в Aspose.Cells Cloud Storage или любое другое облачное хранилище по вашему выбору. За помощью в настройке стороннего хранилища обращайтесь к[Aspose Темы справки Cloud UI](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**Aspose.Cells Cloud предлагает ряд API для операций с файлами, папками и хранилищами.**

## **Как загрузить файл**

### Загрузить файл API Информация

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| путь| нить| путь|Путь к загружаемому файлу, включая имя файла и расширение (например, /file.ext или /Folder 1/file.ext). Если содержимое состоит из нескольких частей и путь не содержит имени файла, он пытается извлечь его из параметра имени файла в заголовке Content-Disposition.|
| файл| Файл| formData| Файл для загрузки|
| имя_хранилища| нить| запрос| Имя хранилища|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/File/UploadFile) определяет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

### Пример загрузки файла

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-d {"File":{}}
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
} 
```

{{< /tab >}}
{{< /tabs >}}

## **Как скачать файл**

### Скачать файл API Информация

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| путь| нить| путь| Путь к файлу (например, '/folder/file.ext')|
| имя_хранилища| нить| запрос| Имя хранилища|
| versionId| нить| запрос| Идентификатор версии файла для загрузки|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/File/DownloadFile) определяет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

### Пример загрузки файла

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="13" tabName13="Request" tabName14="Response" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```bash
{
    Stream
}
```

{{< /tab >}}
{{< /tabs >}}

## **Как удалить файл**

### Удалить файл API Информация

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| путь| нить| путь| Путь к файлу (например, '/folder/file.ext')|
| имя_хранилища| нить| запрос| Имя хранилища|
| versionId| нить| запрос| Идентификатор версии файла для удаления|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/File/DeleteFile) определяет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="15" tabName15="Request" tabName16="Response" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/book12.xlsx" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Как скопировать файл**

### Копировать файл API Информация

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| srcPath| нить| путь| Путь к исходному файлу (например, '/folder/file.ext')|
|destPath| нить| запрос| Путь к файлу назначения|
| srcStorageName| нить| запрос| Имя исходного хранилища|
| destStorageName| нить| запрос| Имя целевого хранилища|
| versionId| нить| запрос| Идентификатор версии файла для копирования|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/File/CopyFile) определяет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

### Пример копирования файла

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="17" tabName17="Request" tabName18="Response" >}}

{{< tab tabNum="17" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/copy/Book1.xlsx?destPath=Book2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Как переместить файл**

### Переместить файл API Информация

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| srcPath| нить| путь| Путь к исходному файлу (например, '/src.ext')|
|destPath| нить| запрос| Путь к файлу назначения (например, '/dest.ext')|
| srcStorageName| нить| запрос| Имя исходного хранилища|
| destStorageName| нить| запрос| Имя целевого хранилища|
| versionId| нить| запрос| Идентификатор версии файла для перемещения|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/File/MoveFile) определяет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

### Пример перемещения файла

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

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

## **Как создать папку**

### Создать папку API Информация

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| путь| нить| путь|Путь к создаваемой папке (например, «папка_1/папка_2/') |
| имя_хранилища| нить| запрос| Имя хранилища|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) определяет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

### Пример создания папки

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="3" tabName3="Request" tabName4="Response" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

## **Как получить файлы в папке**

### Получить файлы API Информация

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| путь| нить| путь| Путь к папке (например, «/folder»)|
| имя_хранилища| нить| запрос| Имя хранилища|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) определяет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

### Пример получения файлов

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="5" tabName5="Request" tabName6="Response" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

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

## **Как удалить папку**

### Удалить папку API Информация

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| путь| нить| путь| Путь к папке (например, «/folder»)|
| имя_хранилища| нить| запрос| Имя хранилища|
| рекурсивный| булев| запрос|ЛОЖЬ|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) определяет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

### Пример удаления папки

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="7" tabName7="Request" tabName8="Response" >}}

{{< tab tabNum="7" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Как скопировать папку**

### Копировать папку API Информация

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| srcPath| нить| путь| Путь к исходной папке (например, '/src')|
|destPath| нить| запрос| Путь к папке назначения (например, '/dst')|
| srcStorageName| нить| запрос| Имя исходного хранилища|
| destStorageName| нить| запрос| Имя целевого хранилища|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) определяет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

### Пример копирования папки

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="21" tabName21="Request" tabName22="Response" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Как переместить папку**

### Переместить папку API Информация

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| srcPath| нить| путь| Путь к папке для перемещения (например, '/folder')|
|destPath| нить| запрос| Путь к папке назначения для перемещения (например, '/dst')|
| srcStorageName| нить| запрос| Имя исходного хранилища|
| destStorageName| нить| запрос| Имя целевого хранилища|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) определяет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

### Пример перемещения папки

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="23" tabName23="Request" tabName24="Response" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="24" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Как проверить наличие хранилища**

### Хранилище существует API Информация

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя_хранилища| нить| путь| Имя хранилища|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) определяет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

### Пример наличия хранилища

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="33" tabName33="Request" tabName34="Response" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```bash
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **Как проверить существование файла или папки**

### Объект существует API Информация

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| путь| нить| путь| Путь к файлу или папке (например, «/file.ext» или «/folder»)|
| имя_хранилища| нить| запрос| Имя хранилища|
| versionId| нить| запрос| Идентификатор версии файла|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) определяет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

### Пример существования объекта

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="37" tabName37="Request" tabName38="Response" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```bash
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **Как получить информацию об использовании диска**

### Получить информацию об использовании диска API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/disc
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя_хранилища| нить| запрос| Имя хранилища|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) определяет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

### Получить пример использования диска

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="40" tabName40="Request" tabName41="Response" >}}

{{< tab tabNum="40" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/disc" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```bash
{
  "UsedSize": 0,
  "TotalSize": 0
}
```

{{< /tab >}}
{{< /tabs >}}

## **Как получить версии файла**

### Получить информацию о версиях файлов API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| путь| нить| путь| Путь к файлу (например, '/file.ext')|
| имя_хранилища| нить| запрос| Имя хранилища|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) определяет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

### Пример получения версий файла

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="46" tabName46="Request" tabName47="Response" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="47" >}}

```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 0,
      "Path": "string",
      "VersionId": "string",
      "IsLatest": true
    }
  ]
} 
```

{{< /tab >}}
{{< /tabs >}}
