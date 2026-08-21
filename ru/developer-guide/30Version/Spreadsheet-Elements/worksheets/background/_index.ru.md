---
title: "Добавление или удаление фонового изображения листа — Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Фон"
type: docs
url: /worksheets/background/
keywords: "Aspose.Cells Cloud, фон листа, Excel API, добавление фонового изображения, удаление фонового изображения листа, примеры SDK"
description: "Узнайте, как добавить или удалить фоновое изображение на листе Excel с помощью REST API Aspose.Cells Cloud. Включает синтаксис запроса, примеры SDK для Java, .NET, Python, PHP и обработку ошибок."
weight: 20
ArticleTitle: "Добавление или удаление фонового изображения листа с помощью Aspose.Cells Cloud API"
---

## Работа с фоном листа Excel

**Обзор:** Фон листа — это изображение, отображаемое за ячейками листа, полезное для брендинга или визуальных подсказок. Aspose.Cells Cloud API позволяет программно добавлять или удалять это фоновое изображение.

**Необходимые условия:**  
- Действующий токен доступа Aspose.Cells Cloud (OAuth 2.0).  
- Рабочая книга Excel, хранящаяся в облаке.  
- Файл изображения (PNG, JPEG, BMP) для фона.

- **Добавление фона** — задать фоновое изображение на листе. Подробное руководство см. в статье [Как задать фон листа Excel](/cells/worksheets/background/add/).  
- **Удаление фона** — удалить существующее фоновое изображение с листа. Подробное руководство см. в статье [Как удалить фон листа Excel](/cells/worksheets/background/delete/).

Использование фонового изображения листа может улучшить брендинг, выделить важные разделы или предоставить визуальные подсказки конечным пользователям. Aspose.Cells Cloud API позволяет просто и удобно задавать или очищать фоновое изображение непосредственно из вашего приложения.

### Справочник по API

| Операция | HTTP-метод | Конечная точка | Параметры пути | Тело запроса | Ответ при успешном выполнении |
|----------|------------|---------------|----------------|--------------|-------------------------------|
| Добавить фон | PUT | `/cells/{name}/worksheets/{sheetName}/background` | `name` — имя файла рабочей книги<br>`sheetName` — целевой лист | Файл изображения (PNG, JPEG, BMP) в формате multipart/form‑data | `200 OK` — фон применён |
| Удалить фон | DELETE | `/cells/{name}/worksheets/{sheetName}/background` | `name` — имя файла рабочей книги<br>`sheetName` — целевой лист | *нет* | `200 OK` — фон удалён |

#### Пример (SDK для Java)

```java
// Добавить фоновое изображение
CellsApi cellsApi = new CellsApi("client_id", "client_secret");
File image = new File("path/to/background.png");
cellsApi.putWorksheetBackground("Book1.xlsx", "Sheet1", image, null);

// Удалить фоновое изображение
cellsApi.deleteWorksheetBackground("Book1.xlsx", "Sheet1", null);
```

#### Пример (SDK для Python)

```python
import asposecellscloud
api = asposecellscloud.CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")

# Добавить фон
with open("background.png", "rb") as img:
    api.put_worksheet_background("Book1.xlsx", "Sheet1", img)

# Удалить фон
api.delete_worksheet_background("Book1.xlsx", "Sheet1")
```

Дополнительные примеры на других языках (C#, PHP, Ruby) приведены в документации SDK.

**См. также**  
- Дополнительные сведения об управлении листами в целом: [Обзор листов](/cells/worksheets/).  
- Как выполнить аутентификацию в Aspose.Cells Cloud: [Руководство по аутентификации API](/cells/authentication/).  
- Другие элементы электронных таблиц: диаграммы, таблицы, формулы — см. [Раздел элементов электронных таблиц](/cells/elements/).
---