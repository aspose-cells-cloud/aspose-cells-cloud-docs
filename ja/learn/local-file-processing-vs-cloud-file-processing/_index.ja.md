---
title: "Aspose.Cells Cloudにおけるローカルファイル処理とクラウドファイル処理の違いとは？"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloudにおけるローカルファイル処理とクラウドファイル処理の違いとは？"
linktitle: "ローカルファイル処理 vs. クラウドファイル処理"
type: docs
url: /learn/local-file-processing-vs-cloud-file-processing/
description: "Aspose.Cells Cloudのローカルファイル処理とクラウドファイル処理を比較：ストレージ、コスト、セキュリティ、および一般的な利用シナリオ。ワークフローに適したアプローチを理解しましょう。"
keywords: "Aspose.Cells Cloud、ローカルファイル処理、クラウドファイル処理、スプレッドシート変換、API"
weight: 10
---

ローカルファイル処理とクラウドファイル処理は、異なるデータ管理パラダイムであり、ファイルストレージインフラストラクチャ、ビジネス処理、アクセス方法、コスト構造、セキュリティ、および適用シナリオにおいて顕著な違いがあります。両者の主な違いは以下の通りです。

**前提条件：** 例を使用する前に、有効なAspose.Cells Cloudアカウント、最新バージョンのSDKがインストールされており、認証用のClient IdとClient Secretが準備できていることを確認してください。

## 1. ファイル保存場所とインフラストラクチャ

- ローカルファイル：

  - ファイルは、ユーザーが所有または管理する物理デバイス（例：個人用コンピュータのハードドライブ、内部サーバー、外部ハードドライブなど）に保存されます。**Cells Cloudクライアントを、任意のローカルストレージデバイス上に存在するファイルに対して直接指定できます。**
  - ユーザーはハードウェアの物理的制御を完全に持ちます。
  - インフラストラクチャの購入、保守、アップグレード、および廃止は、ユーザーまたはその組織の責任となります。

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest

# CellsApiを初期化
api = CellsApi('YourCellsCloudClientId', 'YourCellsCloudClientSecret')

# ローカルExcelファイルをPDFに変換
api.convert_spreadsheet(
    ConvertSpreadsheetRequest('D:\\Data\\BookSales.xlsx', "pdf"),
    local_outpath="BookSales.pdf"
)
```

**APIリファレンス – スプレッドシートの変換**

| メソッド                | HTTP動詞 | エンドポイント        | パラメータ（キー）                                 | レスポンス            |
|-----------------------|-----------|---------------------|--------------------------------------------------|----------------------|
| `convert_spreadsheet` | POST      | `/cells/convert`    | `inputFile` – ソースファイルのパス<br>`format` – 変換先フォーマット（例：`pdf`） | `200 OK` – 変換成功<br>`400 Bad Request` – 無効なパラメータ<br>`401 Unauthorized` – 認証失敗 |

- クラウドファイル：

  - ファイルは、サードパーティのクラウドサービスプロバイダー（Asposeクラウドストレージ、Dropbox、AWS、Google Cloud、Microsoft Azure）が運営するリモートデータセンターに保存されます。**AWS、Dropbox、Google Cloud、Microsoft AzureはすべてAsposeクラウドストレージに接続可能です。**
  - ユーザーは、基盤となるハードウェアの場所や保守状況に関係なく、インターネット経由でこれらのファイルにアクセスします。
  - インフラストラクチャはクラウドサービスプロバイダーの責任であり、ユーザーは必要に応じてそれを使用します。

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import (
    UploadFileRequest,
    ExportSpreadsheetAsFormatRequest,
    SaveSpreadsheetAsRequest,
)

# CellsApiを初期化
api = CellsApi('YourCellsCloudClientId', 'YourCellsCloudClientSecret')

# ローカルファイルをクラウドストレージにアップロード
api.upload_file(
    UploadFileRequest(
        "D:\\Data\\EmployeeSalesSummary.xlsx",
        "PythonSDK/EmployeeSalesSummary.xlsx"
    )
)

# クラウドファイルを指定したフォーマットでローカルストレージにエクスポート
api.export_spreadsheet_as_format(
    ExportSpreadsheetAsFormatRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder="PythonSDK"
    ),
    local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf"
)

# リモートフォルダを定義（必要に応じて実際のフォルダ名に置き換えてください）
RemoteFolder = "PythonSDK"

# Cells Cloud上のExcelファイルを、Cells Cloud上で別のフォーマットのファイルとして保存
api.save_spreadsheet_as(
    SaveSpreadsheetAsRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder=RemoteFolder
    )
)
```

**APIリファレンス – クラウドファイル操作**

| メソッド                     | HTTP動詞 | エンドポイント                     | パラメータ（キー）                                                                                 | レスポンス                                    |
|----------------------------|-----------|------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| `upload_file`              | PUT       | `/cells/storage/file`        | `localPath` – ローカルファイルのパス<br>`remotePath` – クラウドストレージ内での保存先            | `200 OK` – アップロード成功<br>`401 Unauthorized` |
| `export_spreadsheet_as_format` | POST      | `/cells/{name}/export`       | `name` – クラウドファイル名<br>`format` – 変換先フォーマット（例：`pdf`）<br>`folder` – オプションのフォルダ | `200 OK` – エクスポート成功<br>`400 Bad Request` |
| `save_spreadsheet_as`      | POST      | `/cells/{name}/saveas`       | `name` – クラウドファイル名<br>`format` – 変換先フォーマット<br>`folder` – 保存先フォルダ            | `200 OK` – 保存成功<br>`401 Unauthorized` |

## 2. ビジネス処理

ローカルファイル処理でもクラウドファイル処理でも、すべてのビジネス処理はCells Cloudサーバー内で完了するため、**インターネット接続が必要です**。

## 3. データアクセス

- ローカルファイル処理：

  - アクセスは通常、デバイス自体に限定されます。
  - 複数人での共同作業が困難です。
  - 機器や作業場所を変更する際に不便です。

- クラウドファイル処理：

  - インターネット接続が可能な限り、いつでもどこでも（コンピュータ、スマートフォン、タブレットなど）任意のデバイスからファイルにアクセスできます。
  - 自然に複数人によるリアルタイム共同編集をサポートし、複数のユーザーが同時に同じドキュメントを編集でき、システムが自動的にバージョン管理を行います。
  - 移動性が高く、柔軟なオフィスサポートおよびリモートワークが可能です。

## 4. コスト構造とセキュリティ

- ローカルファイル：

  - 初期段階で高額な設備投資が必要であり、その後も運用保守に追加コストがかかります。
  - 物理的セキュリティとネットワークセキュリティは、ユーザー自身が管理します。

- クラウドファイル：

  - 初期投資は低く、主に運用費として必要であり、使用量に応じた従量課金方式です。
  - セキュリティとデータ整合性はクラウドサービスプロバイダーの責任となります。

## 5. 適用シナリオ

- ローカルファイル：ファイル操作はローカルでのみ実行可能です。  
- クラウドファイル：ファイル操作はローカルまたはクラウド上で実行可能です。  

**注意事項／制限事項：** APIはクラウド処理用に最大200 MBのファイルをサポートしており、変換可能なフォーマットはドキュメントに記載されているものに限られます。ネットワーク遅延により、大規模なスプレッドシートの処理時間が影響を受ける可能性があります。

_最終更新日：2026年7月30日_