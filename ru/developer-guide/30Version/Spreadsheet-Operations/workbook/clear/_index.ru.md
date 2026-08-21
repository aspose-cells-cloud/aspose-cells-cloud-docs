---
title: "Очистка объектов в файле Excel"
second_title: "Документ"
linktitle: "Очистка"
type: docs
url: /ru/clear/
aliases: [  /ru/clearobjects/ ]
keywords: "Aspose.Cells, Excel, очистка объектов, REST API, облачный SDK, удаление комментариев, удаление диаграмм"
description: "Используйте облачное REST API Aspose.Cells для удаления комментариев, диаграмм, фигур и других объектов из рабочей книги Excel. Поддерживает множество SDK и возвращает очищенный файл в формате Base64."
weight: 39
---

Это REST API очищает объекты в файле Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/clearobjects
```

### Параметры запроса

| Параметр   | Тип    | Местоположение | Обязательный | Значение по умолчанию | Допустимые значения                                                                                                                                                                                    | Описание                                       |
| ---------- | ------ | -------------- | ------------ | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------- |
| file       | файл   | form‑data      | Да           | —                     | —                                                                                                                                                                                                      | Файл Excel для загрузки                        |
| objecttype | строка | query          | Нет          | —                     | `duplicaterows`, `blankcolumns`, `blankrows`, `formula`, `content`, `style`, `chart`, `comment`, `picture`, `shape`, `listobject`, `hyperlink`, `oleobject`, `pivottable`, `validation`, `background` | Типы объектов для очистки (через запятую)     |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostClearObjects) определяет публично доступное программное интерфейсное решение и позволяет выполнять взаимодействие по REST напрямую из веб‑браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб‑сервисам Aspose.Cells. Пример ниже показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/clearobjects?objecttype=comment" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'xxxxx1=@xxxx1.xlsx' \
  -F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "file2",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK скрывает низкоуровневые детали и позволяет сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells представлен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют, как вызывать веб‑сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearObjects.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearObjects.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearObjects.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearObjects.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearObjects.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearObjects.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearObjects.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearObjects.go" >}}

{{< /tab >}}

{{< /tabs >}}