---
title: "Установка фонового изображения на лист Excel"
ArticleTitle: "Установка фонового изображения на лист Excel – Руководство по API Aspose.Cells Cloud"
second_title: "Документ"
linktitle: "Добавить"
type: docs
url: /ru/worksheets/background/add/
aliases: [  /ru/set-background-or-watermark-for-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel, лист, фон, REST API, SDK, добавить изображение"
description: "Узнайте, как добавить фоновое изображение (PNG, JPEG, BMP) на лист Excel с помощью REST API Aspose.Cells Cloud. Включает endpoint, необходимые параметры, шаги аутентификации, пример cURL и примеры кода SDK."
weight: 180
---

Этот REST API добавляет фоновое изображение на лист.

## Безопасность и аутентификация
Aspose.Cells Cloud API защищены и требуют [аутентификации с использованием токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **Параметры запроса**

| Имя параметра | Тип   | Расположение | Описание                                                       |
| ------------- | ----- | ------------ | -------------------------------------------------------------- |
| name          | string | path        | Имя файла книги Excel.                                         |
| sheetName     | string | path        | Имя листа, на который будет применено изображение.            |
| imageFile     | file   | body        | Бинарный файл изображения (PNG, JPEG, BMP и др.) для установки в качестве фона. |
| folder        | string | query       | Папка в хранилище, где находится файл книги.                   |
| storageName   | string | query       | Имя хранилища Aspose Cloud.                                    |

**Поддерживаемые форматы и ограничения**

- Поддерживаемые расширения изображений: **PNG, JPEG, BMP, GIF**.
- Максимальный размер файла: **5 МБ**.
- Изображение повторяется (заливается тайлом), чтобы заполнить весь фон листа.

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetBackground) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/background" \
  -X PUT \
  -F "imageFile=@Creative.jpg" \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

_Возможные ответы об ошибках_

| HTTP-код | Описание                                                   |
| -------- | ---------------------------------------------------------- |
| 400      | Неверный запрос — отсутствуют или некорректны параметры.    |
| 401      | Неавторизовано — недействительный или просроченный токен JWT. |
| 404      | Не найдено — файл книги или лист не существует.             |
| 500      | Внутренняя ошибка сервера — непредвиденное состояние сервера. |

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}