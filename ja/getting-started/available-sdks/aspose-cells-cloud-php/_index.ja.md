---
title: "Aspose.Cells Cloud PHP SDK – Excel ファイルの変換、結合、分割、保護"  
second_title: "ドキュメント"  
ArticleTitle: "Aspose.Cells Cloud PHP SDK – Excel ファイルの変換、結合、分割、保護"  
linktitle: "Aspose.Cells Cloud PHP SDK"  
type: docs  
url: /available-sdks/aspose-cells-cloud-php/  
description: "Aspose.Cells Cloud PHP SDK (v24.3) をダウンロード。Composer によるインストール方法、認証、XLSX を PDF/CSV に変換する方法、ワークブックの結合、シートの保護など、Office をインストールせずに実行する方法を学びましょう。"  
keywords: "Aspose.Cells, Cloud, PHP, SDK, Excel, 変換, 結合, 分割, 保護"  
weight: 30  
---  

この SDK はオープンソースであり、MIT ライセンスの下で提供されています。Aspose.Cells Cloud の PHP ライブラリのソースコードは<a href="https://github.com/aspose-cells-cloud/aspose-cells-cloud-php" target="_blank" rel="noopener noreferrer">こちら</a>からアクセスできます。

# **Aspose.Cells Cloud SDK for PHP の使用方法**

Aspose.Cells Cloud SDK for PHP は、**PHP プログラミング言語**を使用して Microsoft Excel ファイルを操作・処理できる強力なライブラリです。この SDK を使用すると、ローカルマシンに追加のソフトウェアや依存関係をインストールすることなく、クラウド上で Excel ドキュメントを作成・編集・変換できます。

本記事では、Aspose.Cells Cloud SDK for PHP を使用して、新しい Excel ワークブックの作成、セルへのデータ挿入、および変更後のワークブックをクラウドに保存するなど、一般的なタスクの実行方法を紹介します。

## はじめに

**PHP** 用 Aspose.Cells Cloud SDK の使用を開始する前に、開発環境を設定し、必要な依存関係をインストールする必要があります。Aspose Cloud のクライアント ID とクライアント シークレットを取得するには、Aspose のウェブサイトにある<a href="https://docs.aspose.cloud/cells/quickstart/" target="_blank" rel="noopener noreferrer">記事</a>を参照してください。

**前提条件**

- PHP 7.4 以降  
- 開発マシンに Composer がインストール済み  
- 有効な Aspose Cloud のクライアント ID およびクライアント シークレット  
- Aspose Cloud ストレージ場所 (デフォルトまたはカスタム) へのアクセス権  

## PHP パッケージのインストール方法

Aspose.Cells Cloud SDK for PHP をインストールできます。手順は以下の通りです。

- `composer.json` ファイルに Aspose.Cells Cloud を依存関係として追加します。

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- Composer を実行して SDK をインストールします。

   ```bash
   composer install
   ```

- PHP コードに Composer のオートローダーを読み込みます。

   ```php
   require 'vendor/autoload.php';
   ```

## PHP パッケージを使用して Xlsx をその他の形式に変換する方法

- Aspose.Cells Cloud ライブラリのインポート  
  まず、Aspose.Cells Cloud PHP SDK から必要なパッケージをプロジェクトにインポートします。

- 資格情報を使用して API クライアントを設定  
  固有のクライアント ID とクライアント シークレットを使用して、API クライアントを認証します。

- 変換パラメータの準備  
  変換タスクのパラメータを定義します。これには、ソースファイル名、希望の出力形式、ストレージフォルダのパスが含まれます。

- ワークブックの変換を実行  
  `PostConvertWorkbook` メソッドを呼び出して変換プロセスを実行し、応答を処理します。

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}

### `PostConvertWorkbook` の API リファレンス

| パラメータ       | 説明                                           | 型     | 必須   |
|----------------|-----------------------------------------------|--------|--------|
| `file`         | ソース Excel ファイル名 (例: `sample.xlsx`)。    | 文字列 | はい   |
| `format`       | 出力形式 (`pdf`、`csv`、`png` など)。            | 文字列 | はい   |
| `storage`      | ソースファイルが配置されているストレージ名またはフォルダパス。 | 文字列 | いいえ |
| `outPath`      | 変換後のファイルをストレージ内に直接保存するためのオプションのパス。 | 文字列 | いいえ |

**HTTP メソッド:** POST  
**エンドポイント:** `/cells/convert/{format}`  

**応答例 (JSON)**  

```json
{
  "status": "OK",
  "url": "https://api.aspose.cloud/v3.0/cells/convert/output.pdf"
}
```

**ステータスコード**

- `200` – 変換成功。  
- `400` – 不正なリクエスト (パラメータが不足しているか無効です)。  
- `401` – 認証失敗。  
- `500` – サーバーエラー。  
---