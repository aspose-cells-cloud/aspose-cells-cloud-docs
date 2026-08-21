---
title: "Aspose.Cells Cloud API – Excel ファイルの変換、結合、分割、保護"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud API – Excel ファイルの変換、結合、分割、保護"
linktitle: "デベロッパー センター"
type: docs
url: /
description: "Aspose.Cells Cloud REST API を使用すると、Excel スプレッドシートの変換、結合、分割、保護、および包括的な処理が可能です。月間 150 回まで無料で API を利用できます。8 言語向けの SDK も提供されています。"
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, スプレッドシート変換, Excel 結合, Excel 分割, Excel 保護, クラウド スプレッドシート SDK, REST API, Excel 処理"
---

## Aspose.Cells Cloud API とは？

Aspose.Cells Cloud API は、クラウドベースのスプレッドシート／Excel サービスの集合です。Office のインストールやサーバー設定は不要で、HTTP リクエストを送信するだけで、あらゆる言語からスプレッドシートの作成・編集・変換・データクリーニング・チャート生成・ピボットテーブル構築・暗号化・分割・結合・透かし追加・デジタル署名適用などが可能です。

## なぜ Aspose.Cells Cloud API を使用するのですか？

- Aspose.Cells Cloud Web API サービスを基に、クラウドストレージ上でスプレッドシートの作成・編集・変換・分析が可能です。  
- Aspose.Cells Cloud Web API サービスを基に、ローカルスプレッドシートファイルの作成・編集・変換・分析が可能です。  
- **xlsx**、**csv**、**ods**、**xlsb** など、30 種類以上のファイル形式をサポートしています。  
- Microsoft Excel に依存せず、Aspose.Cells Cloud Web API を通じてスプレッドシートを直接操作できます。  
- 無料枠では、月間最大 150 回の API コールが利用可能です。  
- 使用量に応じた従量課金制です。  
- **短いコード例**: 1 行で実現できる処理  
  - **XLSX を PDF に変換** → ConvertSpreadsheetToPdf  
  - **ファイル全体の余分なスペースを削除** → TrimSpreadsheetContent  
  - **10 以上のファイルを 1 つのレポートに統合** → MergeSpreadsheets  

## Aspose.Cells Cloud API の使い方

### ステップ 1: **API 認証情報の取得**

- **[Aspose Cloud アカウントを登録](https://dashboard.aspose.cloud/signup)**  
- **[クライアント認証情報の取得](https://dashboard.aspose.cloud/#/applications)**  

### ステップ 2: **SDK を使用してスプレッドシート Web API を呼び出す（推奨）**

SDK を使用すると、認証とリクエスト処理が簡略化され、アクセストークンの自動取得・更新が行われます。

#### **[.NET SDK のインストール（NuGet）](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell
dotnet add package Aspose.Cells-Cloud --version 26.6.0
```

#### 例: **SDK を使用して Excel を PDF に変換**

```csharp
CellsApi cellsApi = new CellsApi(
    Environment.GetEnvironmentVariable("ProductClientId"),
    Environment.GetEnvironmentVariable("ProductClientSecret"));
cellsApi.ConvertSpreadsheet(
    new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" },
    "EmployeeSalesSummary.pdf");
```

#### 解説

- **Spreadsheet**: ローカルストレージにある Excel ファイルの名前  
- **Format**: 変換先の形式（例：pdf、png、csv、json）  
- **Output file**: 指定された名前で、結果のファイルがローカルに保存されます  

## 核心機能

Aspose.Cells Cloud は、エンタープライズレベルのスプレッドシート自動化ニーズに対応するため、以下の主要機能を提供しています：

### **スプレッドシート変換**

- **[スプレッドシートを PDF ファイルに変換](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**  
- **[スプレッドシートのチャートを画像に変換](https://docs.aspose.cloud/cells/convert-chart-to-image/)**  
- **[スプレッドシートを別形式で保存](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**  

### **データ処理**

- **[スプレッドシートの結合](https://docs.aspose.cloud/cells/merge-spreadsheets/)**  
- **[スプレッドシートの分割](https://docs.aspose.cloud/cells/split-spreadsheet/)**  
- **[スプレッドシートの空白行を削除](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**  
- **[スプレッドシートの空白列を削除](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**  
- **[スプレッドシートの内容を置換](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**  

> **注意:** 各エンドポイントの詳細なリクエスト／レスポンススキーマ、HTTP メソッド、クエリパラメーター、およびサンプルレスポンスは、以下リンク先の **Aspose.Cells Cloud スプレッドシート Web API リファレンス** に記載されています。

**エンドポイントのクイックリファレンス**

| 操作 | HTTP メソッド | パス | 必須パラメーター | サンプルレスポンス |
|------|---------------|------|------------------|------------------|
| スプレッドシートの変換 | POST | `/cells/convert` | `Spreadsheet`（ファイル）、`format`（文字列） | バイナリファイル（例：PDF） |
| スプレッドシートの結合 | POST | `/cells/worksheets/merge` | `files`（ファイル一覧） | 結合済みワークブック |
| スプレッドシートの分割 | POST | `/cells/worksheets/split` | `Spreadsheet`（ファイル）、`format`（文字列） | 分割されたファイルのアーカイブ |
| 空白行の削除 | POST | `/cells/worksheets/blankrows/delete` | `Spreadsheet`（ファイル） | 更新されたワークブック |
| コンテンツの置換 | POST | `/cells/replace` | `Spreadsheet`（ファイル）、`oldValue`、`newValue` | 更新されたワークブック |

## サポートされる SDK (**利用可能な SDK**)

- Aspose.Cells Cloud は、主要言語すべてに対応した [SDK](https://github.com/aspose-cells-cloud) を提供しており、すぐに Pull & Code & Ship が可能です：

| 言語 | インストール方法 | GitHub リポジトリー |
|------|----------------|------------------|
| [Java](https://www.oracle.com/java/) | [Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) | [Java SDK GitHub リポジトリー](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
| [.NET](https://dotnet.microsoft.com/) | [NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) | [.NET SDK GitHub リポジトリー](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
| [Python](https://www.python.org/) | [pip](https://pypi.org/project/asposecellscloud/) | [Python SDK GitHub リポジトリー](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
| [Node.js](https://nodejs.org/en) | [npm](https://www.npmjs.com/package/asposecellscloud) | [Node.js SDK GitHub リポジトリー](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
| [PHP](https://www.php.net/) | [Composer](https://packagist.org/packages/aspose/cells-sdk-php) | [PHP SDK GitHub リポジトリー](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
| [GoLang](https://go.dev/) | [Go Modules](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) | [GoLang SDK GitHub リポジトリー](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
| [Ruby](https://www.ruby-lang.org/) | [RubyGems](https://rubygems.org/gems/aspose_cells_cloud) | [Ruby SDK GitHub リポジトリー](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
| [Perl](https://www.perl.org/) | [CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) | [Perl SDK GitHub リポジトリー](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |
| **API エンドポイント** | [Aspose.Cells Cloud スプレッドシート Web API リファレンス](https://reference.aspose.cloud/cells/) |  |

## コード例とオープンソースプロジェクト

すべての SDK はオープンソースであり、豊富なコード例を含んでいます：

- [Java SDK のコード例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)  
- [.NET SDK のコード例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)  
- [Python SDK のコード例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)  
- [Node.js SDK のコード例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)  
- [PHP SDK のコード例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)  
- [Go SDK のコード例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)  
- [Ruby SDK のコード例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)  
- [Perl SDK のコード例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)  
---