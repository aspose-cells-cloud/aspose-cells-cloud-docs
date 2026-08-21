---
title: "Aspose.Cells Cloud API – Получение изображения из листа"
second_title: "Документ"
linktype: "Документация"
url: /ru/pictures/get/
aliases: [/convert-picture-to-image/]
keywords: "Aspose.Cells, Получение изображения, API, Excel, Облако, REST"
description: "Получите конкретное изображение из листа Excel с помощью REST API Aspose.Cells Cloud. Включает URL-адрес конечной точки, параметры, шаги аутентификации, коды ответов и примеры кода."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – Получение изображения из листа"
---

Этот REST API извлекает изображение по его нулевому индексу из листа Excel.

## REST API

Для вызова этой конечной точки необходимо включить действительный JWT-токен в заголовок **Authorization**. Токены получаются в процессе аутентификации Aspose.Cells Cloud и требуют соответствующих областей доступа к файлу. Подробнее о получении токена см. в общем руководстве по **аутентификации**.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                                                                                           |
| ------------- | ------ | ------------ | ------------------------------------------------------------------------------------------------------------------ |
| name          | string | path         | Имя документа Excel.                                                                                              |
| sheetName     | string | path         | Имя листа.                                                                                                        |
| pictureIndex  | integer| path         | Нулевой индекс изображения.                                                                                       |
| format        | string | query        | Желаемый формат экспорта (например, png, jpg, bmp, gif, tiff). Если не указан, изображение возвращается в исходном формате. |
| folder        | string | query        | Папка, содержащая документ.                                                                                       |
| storageName   | string | query        | Имя хранилища.                                                                                                    |

### Коды ошибок

| HTTP-код | Описание                                                                      |
| -------- | ----------------------------------------------------------------------------- |
| 401      | Неавторизован — отсутствует или недействителен токен.                        |
| 404      | Не найдено — указанный файл, лист или индекс разрыва страницы не существует.  |
| 400      | Неверный запрос — неверный синтаксис запроса или недопустимые параметры.      |
| 500      | Внутренняя ошибка сервера — возникло непредвиденное состояние.                |

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPicture) определяет публично доступное программное интерфейсное решение и позволяет выполнять взаимодействие REST непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует, как вызывать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
# Двоичные данные изображения (PNG), возвращаемые в теле ответа.
# Пример: фрагмент в base64-кодировке
iVBORw0KGgoAAAANSUhEUgAA...
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это самый быстрый способ разработки. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на вашем проекте. Пожалуйста, ознакомьтесь с [репозиторием GitHub](https://github.com/aspose-cells-cloud), чтобы увидеть полный список SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExampleGetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExampleGetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExampleGetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExampleGetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExampleGetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}