---
title: "Aspose.Cells Cloud API загрузки файлов — интерфейс для быстрой загрузки файлов в облаке"
second_title: "Документ"
ArticleTitle: "Aspose.Cells Cloud API загрузки файлов — интерфейс для быстрой загрузки файлов в облаке"
linktitle: "API загрузки файлов"
type: docs
url: /ru/download-file/
keywords: "Aspose.Cells, API загрузки файлов, облачное хранилище Excel, REST API, загрузка файлов, PDF, CSV, SDK"
description: "Загружайте файлы Excel, PDF, CSV и другие форматы из облачного хранилища Aspose.Cells Cloud с помощью API загрузки файлов (v4.0). Включает endpoint, параметры, данные об аутентификации и примеры кода."
weight: 100
---

**DownloadFile** API позволяет извлекать файлы, хранящиеся в облачном хранилище Aspose.Cells Cloud. API загрузки файлов необходим для прямого получения электронных таблиц Excel, PDF, CSV и других поддерживаемых форматов из облака.

## **Excel API: Загрузка файлов**

### Веб-API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Параметры запроса API **DownloadFile**

| Имя параметра | Тип   | Расположение (Путь / Запрос) | Описание                                                         |
|---------------|-------|------------------------------|------------------------------------------------------------------|
| path          | String| Путь                         | Виртуальный путь к файлу, который вы хотите загрузить.           |
| storageName   | String| Запрос                       | Имя хранилища, из которого будет извлечен файл.                  |
| versionId     | String| Запрос                       | Идентификатор версии файла для загрузки (если применимо).        |

### **Ответ**

API возвращает **поток бинарных данных файла**. Заголовок `Content-Type` соответствует формату файла (например, `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet` для XLSX). JSON-полезная нагрузка не возвращается.

**Коды HTTP-статуса**

| Код | Значение               | Описание                                                       |
|-----|------------------------|----------------------------------------------------------------|
| 200 | OK (ОК)                | Фильтр успешно применён; в ответе содержатся детали операции.  |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или неверны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Неверный или отсутствующий токен JWT.                           |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает лимит размера.                      |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                 |

## Спецификация OpenAPI

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие REST непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells Cloud. Пример ниже показывает, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer ВАШ_ТОКЕН_ДОСТУПА" \
     -H "Accept: application/octet-stream" \
     -o Example.xlsx
```

{{< /tab >}}

{{< tab tabNum="12" >}}

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя работу с низкоуровневыми деталями, позволяя вам сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют выполнение вызовов веб-сервисов Aspose.Cells Cloud с использованием различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{</tab>}}
{{< /tabs >}}