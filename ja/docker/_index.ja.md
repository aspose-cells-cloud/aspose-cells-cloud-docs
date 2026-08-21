---
title: "Aspose.Cells Cloud Docker 操作マニュアル：Aspose.Cells Cloud アプリケーションを独自のプライベートインフラストラクチャ上にホスト"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud Docker 操作マニュアル"
linktype: "docs"
url: /ja/docker-developer-guide/
aliases: [  /ja/docker/ , /ja/docker/run/ ]
description: "Aspose.Cells Cloud を Docker コンテナとしてプライベートまたはオンプレミスのインフラストラクチャ上にデプロイし、Aspose のパブリッククラウドを使用せずにスプレッドシート処理（Excel、PDF、CSV、JSON、Markdown）を実行可能にします。"
keywords:
  [
    "Aspose.Cells Cloud",
    "Docker",
    "Docker イメージ",
    "スプレッドシート API",
    "Excel",
    "PDF",
    "CSV",
    "JSON",
    "Markdown",
    "プライベートクラウド",
    "デプロイ",
  ]
weight: 30
---

Aspose.Cells Cloud は、Excel などの形式のファイルの作成・編集・変換・操作をサポートするクラウドベースのスプレッドシート処理サービスです。Docker を利用することで、独立したサービス環境を迅速に構築でき、依存関係の管理やクロスプラットフォームへのデプロイプロセスを簡素化できます。

本マニュアルでは、環境準備からサービス検証に至るまでの全操作手順を詳細に解説します。

## 環境の準備

Aspose.Cells Cloud Docker コンテナをデプロイする前に、以下の依存関係要件をローカル環境が満たしていることを確認してください。これにより、不足コンポーネントによるデプロイ失敗を回避できます。

### 基本的な依存コンポーネント

- **Docker Engine:** コンテナの実行・管理を行うコアエンジン。最低バージョンは **18.09.0** が必要です。
- **オペレーティングシステム:** Docker をサポートする主要な OS

  | OS タイプ     | バージョン                |
  | :------------ | :------------------------ |
  | Windows       | Windows 10/11             |
  | Windows Server| 2016 / 2019 / 2022        |
  | Linux         | CentOS 7+ / Ubuntu 20.04+ |

- **ハードウェアリソース:** サービスが安定して動作するよう、十分なリソースを確保してください。リソース不足によるクラッシュを防ぐため、以下を推奨します。
  - CPU: 2 コア以上
  - メモリ: 4 GB 以上
  - ディスク: 空き容量 10 GB

### 主な前提条件

- **Aspose ライセンス:** Aspose 公式アカウントに登録し、有効なライセンスを取得してください（トライアル版または商用版のいずれかを選択可能）。ライセンスがない場合、サービスの機能が制限される可能性があります。詳しくは [ライセンス](https://purchase.aspose.com/buy) ページをご参照ください。
- **ネットワーク接続:** Docker Hub にアクセスできること（イメージのプルに必要）を確認してください。

## Aspose.Cells Cloud Docker イメージの取得

Aspose.Cells Cloud イメージは Docker Hub 上にホストされており、`docker pull` コマンドで直接プル可能で、手動でのビルドは不要です。

```bash
# Linux
docker pull aspose/cells-cloud:linux.22.2.0
docker pull aspose/cells-cloud:latest
```

```powershell
# Windows
docker pull aspose/cells-cloud:ltsc2019.25.9.0
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

## Aspose.Cells Cloud Docker コンテナの実行

### 実行パラメータ

| 名前                        | 説明                                                                 | 備考                                         |
| --------------------------- | -------------------------------------------------------------------- | -------------------------------------------- |
| LicensePublicKey            | メーターブリッジング課金モードを使用する場合のライセンス公開鍵を設定 | メーターブリッジング課金モードの場合のみ有効 |
| LicensePrivateKey           | メーターブリッジング課金モードを使用する場合のライセンス秘密鍵を設定 | メーターブリッジング課金モードの場合のみ有効 |
| storagesCredentialsFilePath | ストレージ設定ファイルのパス。既定ファイルは `./storageResource.json` |                                              |
| LicenseFile                 | ライセンスファイル課金モードを使用する場合のライセンスファイルを設定 | ライセンスファイル課金モードの場合のみ有効   |
| AccessToken                 | API アクセス用のトークン                                             | 空の場合、トークン認証は不要                 |

### 実行コマンド

トライアルモードでの実行は非常にシンプルです：

```bash
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

全機能を有効にするには、[メーターライセンス](https://purchase.aspose.com/faqs/licensing/metered/)を取得し、ホスト側のフォルダをファイルストレージ用にマウントします。その場合の実行コマンドは以下の通りです：

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows
docker run -d \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2022.25.9.0
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux
docker run -d \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:linux.25.9.0
```

{{< /tab >}}

{{< /tabs >}}

### API リファレンス – Aspose.Cells Cloud Docker

- `<https://hostname:port/swagger>`
- `<https://hostname:port/swagger/ui/index.html>`

### ポート公開

| ポート | 説明                         | 必須 |
| ---- | ---------------------------- | ---- |
| 5000 | 文書レンダリング用フォントのフォルダ | はい   |

### 必須ボリューム

| コンテナ内マウントパス | 説明                         | 必須 | 備考                                       |
| -------------------- | ---------------------------- | ---- | ------------------------------------------ |
| C:\fonts             | 文書レンダリング用フォントのフォルダ | いいえ | フォント不足によるスプレッドシート/Excel 問題を解決 |
| C:\data              | ファイルストレージフォルダ       | いいえ | ストレージ容量拡張、ファイル管理・アクセス容易化 |

## 参考ドキュメント

- [Aspose.Cells Cloud Docker コンテナのコア機能](https://docs.aspose.cloud/cells/docker-container-features/)
- [Aspose.Cells Cloud Docker コンテナのストレージ設定方法](https://docs.aspose.cloud/cells/docker/storage/)
- [Aspose.Cells Cloud Docker コンテナの実行方法](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)