---
title: "Операции с электронными таблицами"
second_title: "Документ"
type: docs
url: /ru/spreadsheet-operations/
keywords: "Aspose Cells Cloud, Excel API, операции с электронными таблицами, автонастройка размеров, пакетная обработка, защита файлов, преобразование, импорт и экспорт, обработка текста"
description: "Узнайте, как выполнять операции с электронными таблицами — автонастройку размеров, пакетное преобразование, защиту, объединение и поиск с заменой — с помощью REST API Aspose.Cells Cloud. Приведены краткие примечания по использованию и примеры кода."
weight: 100
ArticleTitle: "Операции с электронными таблицами – Руководство по API Aspose.Cells Cloud"
---

Операции с электронными таблицами содержат краткое руководство по наиболее распространённым действиям, которые можно выполнять с книгами Excel с помощью **Aspose.Cells Cloud** (версия 3.0). Независимо от того, нужно ли вам автоматически подогнать ширину столбцов и высоту строк, выполнить пакетную обработку файлов, защитить листы или манипулировать текстом, REST API предоставляет специализированные конечные точки, доступные из языков программирования, таких как Python, C# и Java. В приведённом ниже списке содержатся ссылки на подробную документацию по каждой операции, а также краткие примечания, помогающие быстро начать работу.

**Необходимые условия**: Для вызова этих конечных точек необходимо иметь действующий ключ API Aspose.Cells Cloud и передавать заголовок `Authorization` в формате (`Bearer <access-token>`). Примеры предполагают использование API версии v3.0.

- **[Параметры автонастройки размеров](/ru/cells/auto-fitter-options/)** – Автоматическая корректировка ширины столбцов и высоты строк. `POST /cells/{file}/worksheets/{sheet}/autoFitColumns`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/autoFitColumns
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "autoFitOptions": {
      "autoFitType": "All",
      "autoFitMergedCells": true
    }
  }
  ```
- **[Пакетная обработка файлов Excel: преобразование, блокировка, защита, разбиение и снятие блокировки](/ru/cells/batch/)** – Выполнение массовых действий (преобразование, блокировка, защита, разбиение, снятие блокировки) над до 100 файлов за один запрос. `POST /cells/batch`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/batch
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "tasks": [
      { "file": "Book1.xlsx", "action": "convert", "format": "pdf" },
      { "file": "Book2.xlsx", "action": "protect", "password": "Secret123" }
    ]
  }
  ```
- **[Сжатие и восстановление файлов Excel](/ru/cells/compress-and-repair-excel-files/)** – Снижение размера файла и устранение структурных проблем. `POST /cells/{file}/compressAndRepair`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/compressAndRepair
  Authorization: Bearer {access-token}
  ```
- **[Преобразование файла Excel в другой формат или сохранение в другом виде](/ru/cells/conversion-and-save-as/)** – Преобразование Excel в PDF, CSV, HTML и т.д., либо изменение формата выходного файла. `GET /cells/{file}/saveAs`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Financials.xlsx/saveAs?format=pdf
  Authorization: Bearer {access-token}
  ```
- **[Параметры преобразования рабочей книги](/ru/cells/convert-workbook-options/)** – Точная настройка параметров преобразования, включая размер страницы, параметры рендеринга и защиту паролем. `POST /cells/{file}/convert`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/convert
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "format": "pdf",
    "options": {
      "pageSetup": { "orientation": "landscape" },
      "pdfSaveOptions": { "compressImages": true }
    }
  }
  ```
- **[Создание файлов Excel или построение отчётов в Excel](/ru/cells/creating-files-and-reports/)** – Генерация новых книг с нуля или на основе шаблонов. `PUT /cells/{newFile}`  
  ```http
  PUT https://api.aspose.cloud/v3.0/cells/NewReport.xlsx
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "templateFile": "Template.xlsx",
    "dataSource": { "name": "Q1 Sales", "value": 12345 }
  }
  ```
- **[Импорт данных в файлы Excel и экспорт данных из файлов Excel](/ru/cells/data-import-and-export/)** – Загрузка данных из CSV, JSON или баз данных и экспорт данных листов. `POST /cells/{file}/importData`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Orders.xlsx/importData
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "importOptions": {
      "source": "json",
      "jsonData": [{ "OrderId": 1, "Amount": 250.0 }]
    }
  }
  ```
- **[Шифрование, расшифровка и цифровая подпись файлов Excel](/ru/cells/protect/)** – Применение защиты паролем, шифрования или цифровых подписей. `POST /cells/{file}/encrypt`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Sensitive.xlsx/encrypt
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "password": "StrongPass!23",
    "encryptionType": "Standard"
  }
  ```
- **[Информация о файле](/ru/cells/file-info/)** – Получение метаданных, таких как размер, формат и дата создания. `GET /cells/{file}/info`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Archive.xlsx/info
  Authorization: Bearer {access-token}
  ```
- **[Объединение и разбиение файлов Excel](/ru/cells/merge-and-split/)** – Объединение нескольких книг в одну или разбиение книги на отдельные файлы. `POST /cells/merge` / `POST /cells/split`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/merge
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "files": ["Q1.xlsx", "Q2.xlsx"],
    "outputFile": "FullYear.xlsx"
  }
  ```
- **[Поиск и замена текстового содержимого в файлах Excel](/ru/cells/search-and-replace/)** – Поиск и замена строк во всех листах. `POST /cells/{file}/searchReplace`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/searchReplace
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "text": "Draft",
    "newText": "Final",
    "options": { "matchCase": false }
  }
  ```
- **[Обработка текста в Excel: добавление текста, удаление символов, усечение текста, изменение регистра слов и многое другое](/ru/cells/text-processing/)** – Выполнение расширенных операций обработки текста над значениями ячеек. `POST /cells/{file}/textProcessing`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Notes.xlsx/textProcessing
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "trim", "range": "A1:A10" },
      { "type": "toUpper", "range": "B1:B5" }
    ]
  }
  ```
- **[Добавление водяных знаков и установка фонов в файлах Excel](/ru/cells/watermark-and-background/)** – Добавление текстовых или графических водяных знаков и установка фонов листов. `POST /cells/{file}/watermark`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/watermark
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "type": "text",
    "text": "Confidential",
    "fontSize": 36,
    "color": "FF0000"
  }
  ```
- **[Работа с файлами Excel: вычисление формул, автонастройка размеров, очистка объектов и др.](/ru/cells/workbook/)** – Выполнение типовых задач рабочей книги, таких как вычисление формул, очистка объектов и автонастройка размеров. `POST /cells/{file}/workbookOperations`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Analytics.xlsx/workbookOperations
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "calculateFormula" },
      { "type": "clearObjects", "objectType": "charts" }
    ]
  }
  ```