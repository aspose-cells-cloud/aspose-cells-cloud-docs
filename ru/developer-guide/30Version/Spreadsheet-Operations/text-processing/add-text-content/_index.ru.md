---
title: "Добавление текста в Excel: эффективное внесение данных с помощью веб-API электронных таблиц"
second_title: "Документ"
linktitle: "Добавление текста"
type: docs
url: /ru/excel-add-text/
keywords: "Excel, Aspose.Cells, добавление текста, API электронных таблиц, REST API, Office Cloud, вставка текста, API Excel"
description: "Добавляет текст в заданное место электронной таблицы Excel с помощью API Aspose.Cells Cloud."
weight: 100
---

Добавляет текстовое содержимое в заданное место внутри электронной таблицы. Требуется объект, определяющий добавляемый текст и место вставки.

## **Excel API: PostAddTextContent**

```
POST http://api.aspose.cloud/v3.0/cells/addtext
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/ru/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Описание функции**

Этот метод безопасно добавляет новый текст в указанные ячейки, поддерживая несколько режимов вставки и обработку форматов.

- **Добавление текста в начало выбранных ячеек**  
  Добавляет текст в начало всех выбранных ячеек, обеспечивая единообразие при вводе данных. Идеально подходит для добавления общих идентификаторов или меток, таких как коды товаров, категории или префиксы.

- **Вставка символов до или после определённого текста**  
  Размещает символы до или после целевого текста в выбранных ячейках, позволяя легко создавать структурированный и организованный контент.

- **Добавление одинакового текста в конец каждой выбранной ячейки**  
  Добавляет идентичный текст в конец нескольких ячеек за одну операцию, упрощая ввод данных и гарантируя единообразный внешний вид.

- **Вставка текста до или после заданного количества символов**  
  Вставляет текст после определённого количества символов от начала или конца каждой ячейки целевого диапазона. Типичные сценарии использования: форматирование кодов, временных меток или пользовательских разделителей.

### **Параметры запроса**

| Имя параметра | Тип  | Местоположение | Описание                                                                 |
|---------------|------|----------------|---------------------------------------------------------------------------|
| addTextOptions| Класс| Body           | Определяет текстовое содержимое и позицию, куда должен быть добавлен текст. |

### **Ответ**

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "Содержимое файла: base64_кодированная_строка"
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                              |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK (ОК)                     | Фильтр применён успешно; ответ содержит данные о операции. |
| 400 | Bad Request (Неверный запрос)| Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано)| Неверный или отсутствующий JWT-токен.                 |
| 413 | Payload Too Large (Слишком большой полезный груз)| Загруженный файл превышает лимит размера.             |
| 500 | Internal Server Error (Внутренняя ошибка сервера)| Непредвиденная ошибка сервера.                        |

## Как использовать API PostAddTextContent с SDK

### Спецификация API PostAddTextContent

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/TextProcessingController/PostAddTextContent) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия прямо из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Использование SDK — наиболее эффективный способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostAddTextContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostAddTextContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostAddTextContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostAddTextContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostAddTextContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostAddTextContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostAddTextContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostAddTextContent.go" >}}
{{</ tab>}}
{{< /tabs >}}