---
title: "Aspose.Cells Trim Content API — удаление пробелов и разрывов строк из Excel"
second_title: "Документ"
linktype: "Trim Content"
type: docs
url: /ru/spreadsheet-trim-content/
keywords: "Aspose.Cells, Trim Content API, очистка данных Excel, удаление пробелов в Excel, удаление разрывов строк, очистка данных в электронных таблицах"
description: "Используйте API PostTrimContent Aspose.Cells Cloud для автоматической очистки лишних пробелов, разрывов строк и нежелательных символов из ячеек Excel. Изучите конечную точку, формат запроса, примеры кода и обработку ошибок."
weight: 100
---

## **Web-API для Excel: PostTrimContent**

API **PostTrimContent** обрабатывает и обрезает содержимое в заданном диапазоне электронной таблицы. Он удаляет лишние пробелы, разрывы строк и другие ненужные символы из содержимого выбранных ячеек, что делает его полезным для очистки введённых данных и обеспечения единообразного форматирования электронных таблиц.

```http
POST https://api.aspose.cloud/v3.0/cells/trimcontent
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.


### **Описание функции**

- **Эффективность** — обрезка содержимого только в пределах заданного диапазона, что экономит время и ресурсы за счёт исключения ненужных операций по всему листу.
- **Гибкость** — позволяет пользователю задать точный диапазон ячеек для обработки, что соответствует различным наборам данных и требованиям.
- **Целостность данных** — удаляет лишние пробелы и разрывы строк, способствуя поддержанию согласованных и надёжных данных для анализа и отчётности.
- **Простота использования** — простая интеграция с минимальной настройкой, подходит как для разработчиков, так и для конечных пользователей.

### **Параметры запроса**

| Имя параметра      | Тип   | Расположение | Описание                                                                 |
|--------------------|-------|-------------|--------------------------------------------------------------------------|
| trimContentOptions | Класс | Body        | Параметры, определяющие, как следует обрезать содержимое (например, целевой диапазон, режим обрезки). |

### **Ответ**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[имя объединённого файла]",
    "Filesize" : [размер файла],
    "FileContent" : "[Base64String]"
}
```

**HTTP-коды состояния**

| Код  | Значение                    | Описание                                                      |
|------|-----------------------------|---------------------------------------------------------------|
| 200  | OK (OK)                     | Фильтр применён успешно; ответ содержит сведения об операции. |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен.                |
| 413  | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает лимит размера.                    |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                               |
## Как использовать API PostRemoveCharacters с SDK

### Спецификация API PostRemoveCharacters

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/TextProcessingController/PostTrimContent) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostTrimContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostTrimContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostTrimContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostTrimContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostTrimContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostTrimContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostTrimContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostTrimContent.go" >}}
{{</ tab>}}
{{< /tabs >}}

_Последнее обновление: 30.03.2026_