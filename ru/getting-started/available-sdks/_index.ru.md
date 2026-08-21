---
title: "Доступные SDK для Aspose.Cells Cloud"
second_title: "Документ"
ArticleTitle: "Доступные SDK для Aspose.Cells Cloud: C#, Java, PHP, Python, Ruby, Node.js, Go, Perl"
LinkTitle: "Доступные SDK"
type: docs
url: /ru/available-sdks/
description: "Ознакомьтесь с SDK для Aspose.Cells Cloud на C#, Java, PHP, Python, Ruby, Node.js, Go и Perl. Создавайте, преобразуйте и анализируйте файлы Excel в облаке с помощью недорогих кроссплатформенных API."
weight: 30
keywords: "SDK для Aspose.Cells Cloud, C#, Java, PHP, Python, Ruby, Node.js, Go, Perl, Excel, облачный API"
---

# **Почему стоит использовать SDK для Aspose.Cells Cloud**

## **Кроссплатформенная совместимость**

SDK для Aspose.Cells Cloud предоставляет надёжную и стабильную библиотеку для множества языков программирования. Он обеспечивает разработчикам надёжную кроссплатформенную поддержку, упрощая интеграцию в системах Windows, Linux или macOS.

## **Эффективная обработка Excel и богатый функционал**

SDK для Aspose.Cells Cloud позволяет разработчикам эффективно работать с файлами Excel в облаке — считывать, записывать, изменять и преобразовывать их, не устанавливая локально никакое программное обеспечение Microsoft Office. SDK предоставляет обширный набор API и функций для выполнения сложных операций с Excel, таких как расчёт формул, создание диаграмм, условное форматирование и многое другое, удовлетворяя разнообразные потребности разработчиков.

## **Простота интеграции**

SDK предоставляет лаконичный и понятный API, позволяющий разработчикам быстро интегрировать его в существующие проекты, сокращая время и стоимость разработки.

## **Снижение затрат**

Использование SDK для Aspose.Cells Cloud позволяет снизить операционные расходы вашей компании, избавляя от необходимости приобретать и обслуживать дорогостоящее локальное ПО Microsoft Office или серверное оборудование.

### Обзор SDK

<table>
<thead>
<tr>
<th>Язык</th>
<th>Последняя версия</th>
<th>Установка</th>
<th>Пример быстрого старта</th>
</tr>
</thead>
<tbody>
<tr>
<td>C#</td>
<td>23.12</td>
<td><code>dotnet add package Aspose.Cells-Cloud</code></td>
<td>
<pre><code class="language-csharp">var api = new CellsApi("clientId", "clientSecret");
var result = api.ConvertSpreadsheet(new ConvertSpreadsheetRequest("sample.xlsx", "pdf"));</code></pre>
</td>
</tr>
<tr>
<td>Java</td>
<td>23.12</td>
<td><code>mvn dependency:copy -Dartifact=aspose:aspose-cells-cloud:23.12</code></td>
<td>
<pre><code class="language-java">CellsApi api = new CellsApi("clientId", "clientSecret");
ConvertSpreadsheetRequest request = new ConvertSpreadsheetRequest();
request.setSpreadsheet("Book1.xlsx");
request.setFormat("pdf");
File result = api.ConvertSpreadsheetRequest(request);</code></pre>
</td>
</tr>
<tr>
<td>PHP</td>
<td>23.12</td>
<td><code>composer require aspose/cells-cloud-sdk</code></td>
<td>
<pre><code class="language-php">$instance = new CellsApi(getenv("CellsCloudClientId"), getenv("CellsCloudClientSecret"));
$convertSpreadsheetRequest = new ConvertSpreadsheetRequest();
$convertSpreadsheetRequest->setSpreadsheet($EmployeeSalesSummaryXlsx);
$convertSpreadsheetRequest->setFormat("pdf");
$instance->convertSpreadsheet($convertSpreadsheetRequest, "export-out1.pdf");</code></pre>
</td>
</tr>
<tr>
<td>Python</td>
<td>23.12</td>
<td><code>pip install aspose-cells-cloud</code></td>
<td>
<pre><code class="language-python">instance = CellsApi(os.getenv('CellsCloudClientId'), os.getenv('CellsCloudClientSecret'))
instance.convert_spreadsheet(ConvertSpreadsheetRequest('EmployeeSalesSummary.xlsx', 'pdf'), local_outpath="EmployeeSalesSummary.pdf")</code></pre>
</td>
</tr>
<tr>
<td>Ruby</td>
<td>23.12</td>
<td><code>gem install aspose_cells_cloud</code></td>
<td>
<pre><code class="language-ruby">@instance = AsposeCellsCloud::CellsApi.new(ENV['CellsCloudClientId'], ENV['CellsCloudClientSecret'])
request = AsposeCellsCloud::ConvertSpreadsheetRequest.new(:Spreadsheet=>'EmployeeSalesSummary.xlsx', :format=>'pdf')
response = @instance.convert_spreadsheet(request)</code></pre>
</td>
</tr>
<tr>
<td>Node.js</td>
<td>23.12</td>
<td><code>npm install asposecellscloud</code></td>
<td>
<pre><code class="language-javascript">const cellsApi = new CellsApi(process.env.CellsCloudClientId, process.env.CellsCloudClientSecret, "v4.0", process.env.CellsCloudApiBaseUrl);
var request = new model.ConvertSpreadsheetRequest();
request.spreadsheet = "Book1.xlsx";
request.format = "pdf";
return cellsApi.convertSpreadsheet(request).then((result) => {
    expect(result.response.statusCode).to.equal(200);
});</code></pre>
</td>
</tr>
<tr>
<td>Go</td>
<td>23.12</td>
<td><code>go get github.com/aspose/cells-cloud-go/v2</code></td>
<td>
<pre><code class="language-go">instance := NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"))
convertedData, httpResponse, err := instance.ConvertSpreadsheet(&amp;ConvertSpreadsheetRequest{Spreadsheet: employeeSalesSummaryXlsx, Format: "pdf"})</code></pre>
</td>
</tr>
</tbody>
</table>

**Необходимые условия** – .NET 6+ / Java 8+ / PHP 7.4+ / Python 3.7+ / Ruby 2.6+ / Node 12+ / Go 1.16+ / Perl 5.30+. Также потребуется действующий идентификатор клиента и секретный ключ клиента Aspose Cloud.

**Пример запроса и ответа API** — преобразование рабочей книги Excel в PDF:

```json
{
  "Input": "EmployeeSalesSummary.xlsx",
  "OutputFormat": "pdf"
}
```

SDK являются открытыми и размещены на GitHub; вы можете скопировать репозиторий (fork) или внести в них свой вклад:

- C#: https://github.com/aspose-cells-cloud/aspose-cells-cloud-csharp  
- Java: https://github.com/aspose-cells-cloud/aspose-cells-cloud-java  
- PHP: https://github.com/aspose-cells-cloud/aspose-cells-cloud-php  
- Python: https://github.com/aspose-cells-cloud/aspose-cells-cloud-python  
- Ruby: https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby  
- Node.js: https://github.com/aspose-cells-cloud/aspose-cells-cloud-node  
- Go: https://github.com/aspose-cells-cloud/aspose-cells-cloud-go  
- Perl: https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl  

В целом, использование SDK для Aspose.Cells Cloud даёт множество преимуществ: кроссплатформенная совместимость, эффективная обработка файлов Excel, богатый функционал, защита безопасности и конфиденциальности, высокая масштабируемость, простота интеграции, поддержка сообщества и документация, а также снижение затрат. Эти преимущества делают SDK идеальным выбором для разработчиков, работающих с файлами Excel.

# **Сценарии применения**

## **Автоматизация обработки электронных таблиц**

- С помощью SDK для Aspose.Cells Cloud разработчики могут писать сценарии автоматизации для пакетной обработки файлов электронных таблиц, таких как Excel.  
- Автоматизированные задачи могут включать импорт/экспорт данных, форматирование, расчёты по формулам, создание диаграмм и др.

## **Обработка и анализ данных в облаке**

- Благодаря облачному сервису Aspose.Cells можно обрабатывать большие объёмы данных электронных таблиц, не нагружая локальные вычислительные ресурсы.  
- Это особенно подходит для сценариев, требующих сложного анализа данных, добычи данных или генерации отчётов.

## **Кроссплатформенная совместимость**

- Благодаря кроссплатформенной природе SDK, Aspose.Cells Cloud позволяет легко реализовать обработку электронных таблиц на различных операционных системах и архитектурах.  
- Особенно подходит для сценариев, требующих поддержки нескольких ОС, например: серверные части веб-приложений, настольные и мобильные приложения.

## **Интеграция и расширение API**

- SDK для Aspose.Cells Cloud можно интегрировать в существующие API, предоставляя обработку электронных таблиц как часть сервиса.  
- Подходит для создания корпоративных приложений, платформ SaaS или предоставления API-сервисов.

## **Совместная работа и обмен документами**

- С помощью SDK для Aspose.Cells Cloud можно реализовать совместное редактирование электронных таблиц несколькими пользователями в режиме онлайн.  
- Пользователи могут в режиме реального времени редактировать, комментировать и обмениваться файлами электронных таблиц в облаке, повышая эффективность командной работы.

## **Миграция и трансформация данных**

- Когда требуется миграция данных из других форматов или систем, SDK для Aspose.Cells Cloud может выступать в роли моста для преобразования данных.  
- Данные в других форматах можно преобразовать в формат Excel для последующего анализа и обработки.

## **Автоматическая генерация отчётов**

- Выполнение сценариев по расписанию позволяет автоматически генерировать периодические отчёты или информационные панели (дашборды) с помощью SDK для Aspose.Cells Cloud.  
- Это полезно для организаций, которым требуется регулярный мониторинг бизнес-показателей, продаж или финансовых данных.

## **Интеграция в процессы CI/CD**

- Интеграция SDK для Aspose.Cells Cloud в процессы непрерывной интеграции и доставки (CI/CD) позволяет автоматически проверять корректность данных в электронных таблицах.  
- Это помогает убедиться, что изменения в коде не нарушают целостность и форматирование данных электронных таблиц.

## **Создание пользовательских приложений для электронных таблиц**

- С помощью SDK для Aspose.Cells Cloud можно создавать пользовательские приложения для электронных таблиц, отвечающие специфическим бизнес-требованиям.  
- Например, разрабатывать приложения для обработки форм, инструменты управления финансовыми данными и др.

# **Преимущества SDK**

Наши SDK полностью протестированы и готовы к работе «из коробки». Они являются открытыми и распространяются под лицензией MIT, поэтому вы можете использовать и настраивать их совершенно бесплатно.