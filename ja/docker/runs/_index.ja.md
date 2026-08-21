---
title: "Aspose.Cells Cloud Docker コンテナの実行方法"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud Docker コンテナの実行方法"
linktype: "コンテナ実行"
type: docs
url: /run-aspose-cells-cloud-docker-container/
description: "Windows Server 2022 上で Aspose.Cells Cloud を Docker コンテナとして起動する方法を学びましょう。トライアルモード、従量課金モード、ライセンス課金モード、ストレージ設定、ヘルスチェックのためのステップバイステップのコマンドを解説します。"
weight: 30
keywords: "Aspose.Cells, Docker, Windows Server 2022, トライアルモード, 従量課金, ライセンス課金, ストレージ設定"
---

Aspose.Cells Cloud Docker は、Aspose.Cells Cloud API をローカルまたはプライベートクラウド上で実行可能な、すぐに使えるコンテナイメージを提供します。このガイドでは、**トライアル**、**従量課金**、**ライセンス課金**の3つの一般的なライセンスモードでコンテナを起動する方法を示し、さらに**アクセストークン**を使用するバリエーションも含まれています。すべてのコマンドは Windows Server 2022 上の PowerShell 用に記述されています。Linux を使用する場合はボリュームパスを適宜変更してください。

**前提条件**

- Docker Engine 20.10 以降がインストール・実行されていること。  
- PowerShell 5.1 または PowerShell 7+ が利用可能であること。  
- コンテナ内ポート 5000 をホストポート 47900 にマッピングし、ホスト側のファイアウォールがポート 47900 の受信トラフィックを許可していること。  
- 従量課金またはライセンス課金モードの場合は、`LicensePublicKey`、`LicensePrivateKey`、ライセンスファイルのいずれか、またはアクセストークンモードの場合は `AccessToken` を準備しておくこと。  
- コンテナのストレージとしてマウントするローカルフォルダ（例: `C:\data`）。

**クイックスタート（トライアルモード）**

以下のコマンドを実行して、コンテナをトライアルモードで起動します：

```powershell
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

## トライアルモードで Aspose.Cells Cloud Docker コンテナを実行する

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

コンテナはフォアグラウンドで実行され、ホストポート **47900**（コンテナ内部のポート **5000** に転送）でリッスンします。

## 従量課金モードで Aspose.Cells Cloud Docker コンテナを実行する

```powershell
# Windows Server 2022
# 従量課金モード: LicensePublicKey と LicensePrivateKey を環境変数として設定
# ストレージフォルダをバインド（ホスト → コンテナ）
#   -v c:/data:c:/data
# API がシステムフォントにアクセスできるよう、Windows のフォントフォルダもバインド
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicensePublicKey=yourLicensePublicKey `
  -e LicensePrivateKey=yourLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

コンテナはデタッチドモード（`-d`）で実行されます。起動後、サービスにアクセス可能であることを確認できます：

```powershell
curl http://localhost:47900/v3.0/health
```

**`storageResource.json` のサンプル**

```json
{
  "default": {
    "type": "Local",
    "rootFolder": "c:/data"
  }
}
```

## ライセンス課金モードで Aspose.Cells Cloud Docker コンテナを実行する

```powershell
# Windows Server 2022
# ライセンス課金モード: LicenseFile 環境変数でライセンスファイルを指定
# ストレージフォルダをバインド（ホスト → コンテナ）
#   -v c:/data:c:/data
# Windows のフォントフォルダをバインド
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicenseFile=c:/data/aspose.cells.lic `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

## アクセストークンを使用して Aspose.Cells Cloud Docker コンテナを実行する

```powershell
# Windows Server 2022
# アクセストークンモード: AccessToken とオプションで従量課金用キーを設定
# ストレージフォルダをバインド
#   -v c:/data:c:/data
# Windows のフォントフォルダをバインド
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e AccessToken=ace8955d11cf82e9189ea349976da6f `
  -e LicensePublicKey=yourLicensePublicKey `
  -e LicensePrivateKey=yourLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

コンテナ起動後、前述のヘルスチェックコマンドでサービスが正常に動作していることを確認してください。

## 参考ドキュメント

- [Aspose.Cells Cloud Docker コンテナのストレージ設定方法](https://docs.aspose.cloud/cells/docker/storage/)

---

### トラブルシューティング

- **ヘルスチェックが失敗する場合** – ファイアウォールでポート 47900 がブロックされていないか、コンテナが実行中（`docker ps`）であるかを確認してください。  
- **ライセンスエラーが発生する場合** – `LicensePublicKey`、`LicensePrivateKey`、または `LicenseFile` の値が正しいこと、および環境変数に余分な空白が含まれていないことを確認してください。  
- **ストレージにアクセスできない場合** – ホストフォルダ（`c:/data`）が存在し、Docker がそのフォルダに対して読み書きの権限を持っていることを確認してください。

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud Docker コンテナの実行方法",
  "description": "Windows Server 2022 上で Aspose.Cells Cloud を Docker コンテナとして起動するためのステップバイステップガイド。トライアルモード、従量課金、ライセンス課金、アクセストークンモードに対応しています。",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "url": "https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/",
  "keywords": "Aspose.Cells, Docker, Windows Server 2022, トライアルモード, 従量課金, ライセンス課金, ストレージ設定"
}
</script>