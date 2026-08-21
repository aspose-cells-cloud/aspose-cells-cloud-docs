---
title: "Удаление фонового изображения на листе Excel"
second_title: "Документ"
linktitle: "Удалить"
type: docs
url: /ru/worksheets/background/delete/
aliases: [  /ru/delete-background-or-watermark-of-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Удаление фонового изображения листа, Excel, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Используйте Aspose.Cells Cloud REST API для удаления фонового изображения листа Excel. SDK доступны для C#, Java, PHP, Ruby, Node.js, Python, Perl и Go."
weight: 210
ArticleTitle: "Удаление фонового изображения на листе Excel с использованием Aspose.Cells Cloud API"
---

Этот REST API удаляет фоновое изображение листа.

**Необходимые условия:** Рабочая книга должна быть сохранена в облачном хранилище Aspose, а также у вас должен быть действующий JWT-токен доступа для аутентификации.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **Параметры запроса**

| Имя параметра | Тип   | Местоположение | Описание                                                |
|---------------|-------|---------------|---------------------------------------------------------|
| name          | string | path          | Имя файла Excel.                                        |
| sheetName     | string | path          | Имя листа, у которого удаляется фоновое изображение.   |
| folder        | string | query         | Папка в хранилище, где находится файл.                  |
| storageName   | string | query         | Имя хранилища (если отличается от хранилища по умолчанию). |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetBackground) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Все запросы требуют действительного JWT-токена. Получите токен через OAuth2 endpoint, как описано в руководстве по аутентификации.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/WorkSheetBackground_Sample_Test_Book.xls/worksheets/Sheet1/background" \
  -X DELETE \
  -H "Content-Type: application/json" \
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

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                  |
|-----|-----------------------------|-----------------------------------------------------------|
| 200 | OK (OK)                     | Фильтр успешно применён; ответ содержит подробную информацию о выполнении операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или неверны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Неверный или отсутствующий JWT-токен.                     |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает допустимый размер.            |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                            |

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали и позволяет сосредоточиться на задачах вашего проекта. Ознакомьтесь со [списком репозитория GitHub](https://github.com/aspose-cells-cloud) для получения полного списка SDK Aspose.Cells Cloud.

Приведённые ниже примеры кода демонстрируют, как осуществлять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}
---