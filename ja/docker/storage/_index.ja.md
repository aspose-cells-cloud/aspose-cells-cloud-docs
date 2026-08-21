---
title: "Aspose.Cells Cloud Docker コンテナ用ストレージ位置の設定方法"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud Docker コンテナストレージの設定"
linktitle: "コンテナストレージ"
type: docs
url: /ja/docker/storage/
description: "JSON、PowerShell、または Bash を使用して Aspose.Cells Cloud Docker コンテナのストレージ位置を設定します。"
weight: 30
keywords: "Aspose.Cells, Docker, コンテナストレージ, JSON 設定, PowerShell, Bash"
---

**概要**: 本ガイドでは、Windows および Linux 上で JSON 設定ファイルおよび Docker run コマンドを使用して、Aspose.Cells Cloud Docker コンテナのストレージ位置を設定する方法を説明します。

## デフォルトのストレージ設定 ##

**前提条件**: Docker Engine 20.10 以降がインストールされており、有効な Aspose.Cells Cloud ライセンスキー (`LicensePublicKey` および `LicensePrivateKey`) を所有していること、また、ストレージ用に使用するホストフォルダ（Windows の場合は `c:/data`、Linux の場合は `/data` など）が適切な権限で存在していることを確認してください。

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```json
{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "c:/data"
    }
  ]
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "/data"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## デフォルトの配置場所 ##

- **Windows**

```powershell
c:\app\storageResource.json
```

- **Linux**

```bash
/app/storageResource.json
```

## カスタムストレージの設定 ##

Aspose.Cells Cloud データ用に別のフォルダを使用する必要がある場合、カスタムストレージプロファイルを指定してください。

```bash
docker run -d \
  -v c:/data:c:/data \   # ホストフォルダをコンテナストレージとしてマウント
  -p 47900:5000 \        # API ポートをマッピング
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=c:/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

*Linux の例*:

```bash
docker run -d \
  -v /data:/data \       # ホストフォルダをコンテナストレージとしてマウント
  -p 47900:5000 \        # API ポートをマッピング
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

**参考ドキュメント** :

- [Aspose.Cells Cloud Docker コンテナの実行方法](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
- [Docker コンテナの機能](https://docs.aspose.cloud/cells/docker/container-features/)
- [Aspose.Cells Cloud Docker イメージのダウンロード](https://docs.aspose.cloud/cells/docker/download-image/)
- [コンテナタグの管理](https://docs.aspose.cloud/cells/docker/manage-tags/)