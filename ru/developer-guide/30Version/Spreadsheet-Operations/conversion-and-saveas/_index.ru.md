---
title: "Преобразование файла Excel в другой формат или сохранение его иным способом."
second_title: "Документ"
linktitle: "Преобразование и Сохранить как"
type: docs
url: /ru/conversion-and-save-as/
aliases: [  /ru/convert-excel/ , /ru/convert/ ]
keywords: "Aspose.Cells, API для преобразования Excel, преобразование Excel в PDF, Excel в CSV, Excel в JSON, облачное преобразование электронных таблиц"
description: "Узнайте, как с помощью Aspose.Cells Cloud REST API преобразовывать рабочие книги Excel в PDF, CSV, JSON, HTML и более 15 других форматов. Включает сведения об эндпоинтах, примеры команд cURL и фрагменты кода для Java, .NET, Python и других языков."
weight: 30
ArticleTitle: "Преобразование файлов Excel в PDF, CSV, JSON и другие форматы с помощью Aspose.Cells Cloud"
---

Если вы изначально создали файл Excel в определённом формате — например, [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) или [CSV](https://docs.fileformat.com/spreadsheet/csv/) — вам может пригодиться возможность преобразовать файл Excel в другой формат, чтобы использовать специальные функции. Например, преобразование Excel в [PDF](https://docs.fileformat.com/pdf/) защищает его содержимое от несанкционированных изменений и облегчает чтение и распространение.

**Необходимые условия**  
Перед вызовом API для преобразования получите токен доступа OAuth 2.0 от Aspose Cloud и убедитесь, что рабочая книга хранится в облачном хранилище Aspose Cloud (или передаётся в теле запроса для эндпоинта преобразования PUT).

Преобразование документов — сложный процесс. Множество факторов влияет на его сложность и должны учитываться при трансформации. Обеспечение точного и профессионального качества преобразования между форматами Excel — ключевая особенность Aspose.Cells Cloud.

Сервис одинаково хорошо работает для преобразования документов любого формата. Вы можете как импортировать, так и экспортировать документы в следующих форматах:

**Поддерживаемые форматы**  
- Импорт/Экспорт: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/)
- Только экспорт: [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/)

### API для преобразования

| API                         | Описание                                                                 |
| :-------------------------- | :---------------------------------------------------------------------- |
| `GET /cells/{name}`         | Извлекает рабочую книгу Excel из облачного хранилища и преобразует её в указанный формат. |
| `PUT /cells/convert`        | Преобразует рабочую книгу Excel, переданную в теле запроса, в указанный выходной формат. |
| `POST /cells/{name}/saveAs` | Сохраняет существующую рабочую книгу Excel в другом формате непосредственно в облачное хранилище. |

**Детали API**

- **GET /cells/{name}**  
  - **Параметры пути:** `name` — имя файла рабочей книги (обязательный параметр).  
  - **Параметры запроса:** `format` — целевой формат (например, pdf, csv, json); `storage` — имя облачного хранилища (необязательный); `folder` — путь к папке внутри хранилища (необязательный).  
  - **Ответ:** Поток данных преобразованной рабочей книги; `Content-Type` соответствует целевому формату.  
  - **Коды состояния:** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

- **PUT /cells/convert**  
  - **Тело запроса:** multipart/form‑data, содержащее исходный файл рабочей книги (`file`) и обязательное поле `format`, указывающее желаемый выходной формат.  
  - **Ответ:** Бинарный поток преобразованного файла.  
  - **Коды состояния:** 200 OK, 400 Bad Request, 401 Unauthorized, 500 Internal Server Error.  

- **POST /cells/{name}/saveAs**  
  - **Параметры пути:** `name` — имя существующей рабочей книги.  
  - **Параметры запроса:** `format` — целевой формат; `outPath` — путь назначения в облачном хранилище (необязательный); `storage` — имя хранилища (необязательный).  
  - **Ответ:** Объект JSON с результатом операции и путём сохранённого файла. Пример ответа:  

    ```json
    {
      "status": "OK",
      "code": 200,
      "message": "Файл успешно сохранён.",
      "path": "Converted/MyWorkbook.pdf"
    }
    ```  

  - **Коды состояния:** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

**Пример cURL для преобразования в PDF**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx?format=pdf" \
  -H "Authorization: Bearer {access_token}" \
  -o MyWorkbook.pdf
```

**Фрагмент кода SDK для Java (GET /cells/{name})**

```java
CellsApi apiInstance = new CellsApi();
String name = "MyWorkbook.xlsx";
String format = "pdf";
File result = apiInstance.cellsGetWorkbook(name, format, null, null);
result.renameTo(new File("MyWorkbook.pdf"));
```

**Фрагмент кода SDK для .NET (PUT /cells/convert)**

```csharp
var api = new CellsApi();
var file = File.ReadAllBytes("MyWorkbook.xlsx");
var format = "pdf";
var result = api.ConvertWorkbook(new MemoryStream(file), format);
File.WriteAllBytes("MyWorkbook.pdf", result);
```

**Фрагмент кода SDK для Python (POST /cells/{name}/saveAs)**

```python
import asposecellscloud
api = asposecellscloud.CellsApi()
api.post_save_as(name="MyWorkbook.xlsx", format="pdf", out_path="Converted/MyWorkbook.pdf")
```

В следующих статьях подробно описан каждый API и приведены дополнительные примеры cURL и SDK:

- [Преобразование файла Excel в другой формат](/ru/cells/convert-an-excel-file-to-different-formats)
- [Сохранение файла Excel в другом формате](/ru/cells/save-an-excel-file-as-other-formats-files)
- [Преобразование файла Excel в файл CSV](/ru/cells/convert-excel-file-to-csv-file)
- [Преобразование файла Excel в файл DOCX](/ru/cells/convert-excel-file-to-docx-file)
- [Преобразование файла Excel в файл HTML](/ru/cells/convert-excel-file-to-html-file)
- [Преобразование файла Excel в файл JSON](/ru/cells/convert-excel-file-to-json-file)
- [Преобразование файла Excel в файл Markdown](/ru/cells/convert-excel-file-to-markdown-file)
- [Преобразование файла Excel в файл PDF](/ru/cells/convert-excel-file-to-pdf-file)
- [Преобразование файла Excel в файл PNG](/ru/cells/convert-excel-file-to-png-file)
- [Преобразование файла Excel в файл PPTX](/ru/cells/convert-excel-file-to-pptx-file)
- [Преобразование файла Excel в файл SQL](/ru/cells/convert-excel-file-to-sql-file)
- [Преобразование файла Excel в файл TIFF](/ru/cells/convert-excel-file-to-tiff-file)
---