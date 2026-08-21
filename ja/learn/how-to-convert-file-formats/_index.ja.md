---
title: "Aspose.Cells Cloud を使用してスプレッドシートファイル形式を変換する方法"
linktype: "Aspose.Cells Cloud を使用してスプレッドシートファイル形式を変換する方法"
type: docs
url: /ja/how-to-convert-file-formats
description: "Aspose.Cells Cloud を使用してファイル形式を変換する方法。"
weight: 10
kwords: Excel, Office Cloud, REST API, スプレッドシート, PDF, CSV, JSON, Markdown, Aspose.Cells Cloud でファイル形式を変換する方法
---

## はじめに

Aspose.Cells Cloud スプレッドシート API は、ローカルおよびクラウド上のスプレッドシートファイルを変換するための双方向インターフェースを提供します。Excel（XLS、XLSX）、CSV、HTML、PDF などの形式をサポートし、多様なニーズに対応した簡単な変換を実現します。

### 3つの変換モード・統一されたオブジェクトモデル・全形式カバー

![変換モード](image.png)

## **コア変換マトリクス**

| 変換タイプ             | オブジェクトレベル | 典型的な API                    | 出力形式                       |
|------------------------|--------------------|----------------------------------|--------------------------------|
| **ローカル変換**       | ワークブック       | `ConvertSpreadsheet`            | PDF/XLSX/JSON/.... 30種類以上  |
|                        | シート             | `ConvertWorksheetToImage`       | PNG/JPEG/SVG                   |
|                        |                    | `ConvertWorksheetToPdf`         | PDF                            |
|                        | テーブル           | `ConvertTableToImage`           | PNG/JPEG/SVG/....              |
|                        |                    | `ConvertTableToPdf`             | PDF                            |
|                        |                    | `ConvertTableToCsv`             | CSV                            |
|                        |                    | `ConvertTableToHtml`            | HTML                           |
|                        |                    | `ConvertTableToJson`            | JSON                           |
|                        | 範囲（Range）      | `ConvertRangeToImage`           | PNG/JPEG/SVG/....              |
|                        |                    | `ConvertRangeToPdf`             | PDF                            |
|                        |                    | `ConvertRangeToCsv`             | CSV                            |
|                        |                    | `ConvertRangeToHtml`            | HTML                           |
|                        |                    | `ConvertRangeToJson`            | JSON                           |
|                        | 図表（Chart）      | `ConvertChartToImage`           | PNG/JPEG/SVG/....              |
|                        |                    | `ConvertChartToPdf`             | PDF                            |
| **クラウド変換**       | ワークブック       | `ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... 30種類以上  |
|                        | シート             | `ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... 30種類以上  |
|                        | テーブル           | `ExportTableAsFormat`           | PDF/XLSX/JSON/.... 30種類以上  |
|                        | 範囲（Range）      | `ExportRangeAsFormat`           | PDF/XLSX/JSON/.... 30種類以上  |
|                        | 図表（Chart）      | `ExportChartAsFormat`           | PDF/XLSX/JSON/.... 30種類以上  |
| **クラウド「名前をつけて保存」** | ワークブック       | `SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... 30種類以上  |

### **ローカルファイルの変換**

```csharp
// Cells Cloud API クライアントを取得
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel ファイルの変換**

```c#
// ローカル Excel を PDF に変換
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **Excel 図表を SVG ファイルに変換**

```c#
// ローカル Excel 図表を SVG に変換
cellsApi.ConvertChartToImage(new SDK.Request.ConvertChartToImageRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    chartIndex = 0,
    format = "svg"
}, "EmployeeSalesSummary.svg");

```

- **テーブルを CSV ファイルに変換**

```C#
# Sales シートの販売ログテーブルを CSV に変換
result = api.ConvertTableToCsv( new SDK.Request.ConvertTableToCsvRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    tableName = "SaleLogs",
    format = "csv"
}, "EmployeeSalesLog.csv");

```

### **クラウドファイルの変換**

Aspose Cells Cloud API クライアントの取得も必要です。

```csharp
// Cells Cloud API クライアントを取得
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel を PDF に変換**

```csharp
// クラウド Excel を PDF に変換し、ローカルファイルとして保存
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **Excel シートを PDF に変換**

```csharp
// クラウド Excel シートを PDF に変換し、ローカルファイルとして保存
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

```csharp
// クラウド Excel シートを PDF に変換し、ローカルファイルとして保存
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

## Aspose.Cells Cloud SDK のインストールと初期化

.NET プロジェクトで Aspose.Cells-Cloud NuGet パッケージをインストールするには、NuGet パッケージマネージャコンソールまたは Visual Studio の NuGet パッケージマネージャを使用できます。以下は、パッケージマネージャコンソールを使用してパッケージをインストールする方法です。

```powershell

Install-Package Aspose.Cells-Cloud

```

CellsApi クラスの新しいインスタンスを作成し、クライアント ID とクライアントシークレットで初期化します。以下のコードスニペットの詳細を示します。

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

YOUR_API_KEY、YOUR_APP_SID、YOUR_APP_KEY を実際の API キー、アプリケーション SID、アプリケーションキーに置き換えてください。

## **ファイル形式変換のユースケース**

Aspose Cells Cloud API は、重要なビジネスシナリオ向けにエンタープライズグレードの**スプレッドシート変換**機能を提供します。

1. **Excel → PDF**  
   書式を保持した印刷用レポートを生成します  
2. **スプレッドシート → HTML**  
   インタラクティブなテーブルを Web アプリケーションに埋め込みます  
3. **CSV → Excel (XLSX)**  
   生データを分析可能なワークブックに変換します  
4. **カスタム形式のトランスコード**  
   20種類以上の形式（XLS、XLSB、ODS、FODS、TSV）間で変換します  
![入力形式から出力形式への変換](image-1.png)

## **まとめ：1回の API コールで変換を効率化**

---