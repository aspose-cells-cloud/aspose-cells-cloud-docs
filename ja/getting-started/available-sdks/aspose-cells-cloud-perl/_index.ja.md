---
title: "Aspose.Cells Cloud SDK for Perl – 変換、結合、分割、保護など"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud SDK for Perl – 変換、結合、分割、保護など"
linktitle: "Aspose.Cells Cloud SDK for Perl"
type: docs
url: /available-sdks/aspose-cells-cloud-perl/
description: "Aspose.Cells Cloud Perl SDK を探索する – Office をインストールせずに Excel ファイルを作成・変換・結合・分割・保護・検索・置換できるクロスプラットフォームライブラリ。インストールガイド、コード例、API リファレンスを含む。"
weight: 30
keywords: "Perl, Aspose.Cells Cloud, Excel SDK, 変換, PDF, API, Excel 操作, Perl SDK, クラウド Excel 処理"
---

_最終更新日: 2026年7月30日_

この SDK はオープンソースであり、MIT ライセンスの下で提供されています。Aspose.Cells Cloud の Perl ライブラリのソースコードは[こちら](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl)からアクセスできます。

# **Perl による Aspose.Cells Cloud ライブラリの使用方法**

Aspose.Cells Cloud SDK for Perl は、Perl プログラミング言語を使用して Microsoft Excel ファイルを操作・処理できる強力なライブラリです。この SDK を使用すると、ローカルマシンに追加のソフトウェアや依存関係をインストールすることなく、クラウド上で Excel ドキュメントを作成・編集・変換できます。

この記事では、Aspose.Cells Cloud SDK for Perl を使用して、新しい Excel ワークブックの作成、セルへのデータ挿入、変更済みワークブックをクラウドに保存するなど、一般的なタスクを実行する方法について説明します。

## はじめに

**Perl** 用 Aspose.Cells Cloud SDK の使用を開始する前に、開発環境をセットアップし、必要な依存関係をインストールする必要があります。Aspose.Cells Cloud のクライアント ID とクライアントシークレットを取得するには、Aspose のウェブサイトにある**[Aspose.Cells Cloud クイックスタートガイド](https://docs.aspose.cloud/cells/quickstart/)** を参照してください。

## Aspose.Cells Cloud 用 Perl パッケージのインストール方法

**前提条件**  
- Perl 5.10 以降  
- CPAN（Comprehensive Perl Archive Network）がインストールされていること  
- 有効な Aspose.Cells Cloud のクライアント ID およびクライアントシークレット  

以下のコマンドで Aspose.Cells Cloud SDK for Perl をインストールできます：

```perl
perl -MCPAN -e shell
install AsposeCellsCloud::CellsApi
```

## Perl パッケージを使用して Xlsx をその他の形式に変換する方法

- **Aspose.Cells Cloud ライブラリのインポート**  
  プロジェクトに Aspose.Cells Cloud Perl SDK から必要なパッケージをインポートすることから始めます。

- **資格情報による API クライアントの設定**  
  固有のクライアント ID とクライアントシークレットを使用して API クライアントを認証します。

- **変換パラメータの準備**  
  変換タスクのパラメータ（ソースファイル名、出力形式、ストレージフォルダのパスなど）を定義します。

- **ワークブック変換の実行**  
  `PostConvertWorkbook` メソッドを使用して変換処理を実行し、レスポンスを処理します。

以下に `PostConvertWorkbook` 操作の簡潔なリファレンスを示します：

| HTTP メソッド | エンドポイント                             | 必須パラメータ                               | サンプルリクエスト（Perl）                                                                                   | サンプルレスポンス（JSON）                             | 考えられるステータスコード             |
|-------------|------------------------------------------|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------|-----------------------------------|
| POST        | `/cells/convert`                         | `file`（ソースワークブック）、`outputFormat`、`storage` | ```perl\nmy $result = $api_instance->post_convert_workbook({ file => 'Book1.xlsx', outputFormat => 'pdf', storage => 'MyStorage' });\n``` | `{ "File": "Book1.pdf", "Url": "https://.../Book1.pdf" }` | 200 OK、400 Bad Request、401 Unauthorized、500 Server Error |

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_AvailableSDKs.pl" >}}
---