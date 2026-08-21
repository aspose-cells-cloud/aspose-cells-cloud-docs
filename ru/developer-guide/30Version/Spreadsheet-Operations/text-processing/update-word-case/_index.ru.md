---
title: "Aspose.Cells – API обновления регистра слов"
second_title: "Документ"
linktype: "Документация"
type: docs
url: /ru/post-update-word-case/
keywords: "Aspose.Cells, API обновления регистра слов, преобразование регистра текста, Excel, CSV, Google Таблицы, REST API"
description: "Преобразуйте регистр текста в файлах Excel, CSV или Google Таблиц с помощью API обновления регистра слов из Aspose.Cells Cloud. Поддерживает верхний/нижний регистр, заглавные буквы в начале каждого слова и капитализацию первой буквы."
weight: 100
ArticleTitle: "Aspose.Cells – Документация по API обновления регистра слов"
---

**Версия API:** 3.0

Управление несогласованным регистром текста в электронных таблицах (Excel, Google Таблицы, CSV) может быть утомительным, особенно при работе с большими наборами данных. **Web-API PostUpdateWordCase** автоматизирует преобразование регистра текста, обеспечивая чистые и стандартизированные данные с минимальными усилиями.


## **Web-API Excel – API обновления регистра слов**

```http
POST https://api.aspose.cloud/v3.0/cells/updatewordcase
```
### **Безопасность и аутентификация**

Web-API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/ru/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Описание функции**

Web-API PostUpdateWordCase решает распространённую проблему несогласованного регистра текста в электронных таблицах, которая может существенно повлиять на анализ и обработку данных. Это API автоматизирует преобразование регистра, гарантируя, что ваши данные будут чистыми, стандартизированными и готовыми к дальнейшей обработке или анализу.

- **Автоматизированное преобразование регистра**
  - **Верхний регистр → нижний регистр** – преобразует все заглавные буквы в строчные.
  - **Нижний регистр → верхний регистр** – преобразует все строчные буквы в заглавные.
  - **Заглавная первая буква** – делает заглавной первую букву каждого слова.
  - **Регистр заголовка** – преобразует текст в регистр заголовка, где первая буква каждого основного слова становится заглавной.

- **Поддержка нескольких форматов** – API работает с широким спектром форматов электронных таблиц, включая Excel, OpenOffice, JSON, CSV и другие. Это делает его подходящим для различных задач обработки данных.

### **Параметры запроса**

| Имя параметра    | Тип   | Расположение | Описание                                                                                                               |
| ----------------- | ------ | ------------ | ------------------------------------------------------------------------------------------------------------------------- |
| `wordCaseOptions` | объект | Тело запроса | Параметры, определяющие желаемое преобразование регистра, включая исходный диапазон, тип целевого регистра и дополнительные настройки. |

**Схема `wordCaseOptions`**

```json
{
  "Range": "A1:B10", // диапазон в стиле Excel для обработки (обязательный)
  "CaseType": "Upper", // перечисление: Upper, Lower, Capitalize, Title (обязательный)
  "IgnoreBlank": true // логическое значение, необязательный — при значении true пустые ячейки остаются без изменений
}
```

**Пример тела запроса**

```json
{
  "Range": "A1:B10",
  "CaseType": "Upper",
  "IgnoreBlank": true
}
```

- **Range** – диапазон ячеек, к которому будет применено преобразование регистра (например, `A1:C5`).
- **CaseType** – тип преобразования регистра. Допустимые значения: `Upper`, `Lower`, `Capitalize`, `Title`.
- **IgnoreBlank** – если `true`, пустые ячейки игнорируются; по умолчанию — `false`.

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

- **Filename** – имя обработанного файла.
- **FileSize** – размер файла в байтах.
- **FileContent** – содержимое преобразованного файла в формате Base64.

**Коды HTTP-статуса**

| Код | Значение                     | Описание                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Фильтр успешно применён; ответ содержит детали операции. |
| 400  | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized                | Недействительный или отсутствующий JWT-токен. |
| 413  | Payload Too Large           | Загруженный файл превышает лимит размера. |
| 500  | Internal Server Error       | Непредвиденная ошибка сервера. |

## Как использовать API PostUpdateWordCase с SDK

### Спецификация API PostUpdateWordCase

Спецификация <a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostUpdateWordCase" target="_blank" rel="noopener noreferrer">OpenAPI</a> определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud см. в <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозитории GitHub</a>.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostUpdateWordCase.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostUpdateWordCase.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostUpdateWordCase.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostUpdateWordCase.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostUpdateWordCase.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostUpdateWordCase.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostUpdateWordCase.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostUpdateWordCase.go" >}}
{{</ tab>}}
{{</ tabs >}}
---