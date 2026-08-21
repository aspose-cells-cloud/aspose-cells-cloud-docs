---
title: "Aspose.Cells Cloud Docker 컨테이너 스토리지 위치 설정 방법"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud Docker 컨테이너 스토리지 설정"
linktype: "컨테이너 스토리지"
type: docs
url: /ko/docker/storage/
description: "JSON, PowerShell 또는 Bash를 사용하여 Aspose.Cells Cloud Docker 컨테이너의 스토리지 위치를 설정하는 방법을 안내합니다."
weight: 30
keywords: "Aspose.Cells, Docker, 컨테이너 스토리지, JSON 설정, PowerShell, Bash"
---

**요약**: 이 가이드는 Windows 및 Linux 환경에서 JSON 설정 파일과 Docker run 명령을 사용하여 Aspose.Cells Cloud Docker 컨테이너의 스토리지 위치를 설정하는 방법을 설명합니다.

## 기본 스토리지 설정 ##

**사전 조건**: Docker Engine 20.10+가 설치되어 있고, 유효한 Aspose.Cells Cloud 라이선스 키(`LicensePublicKey` 및 `LicensePrivateKey`)를 보유하고 있으며, 스토리지로 사용할 호스트 폴더(예: Windows의 경우 `c:/data`, Linux의 경우 `/data`)가 적절한 권한으로 존재하는지 확인하십시오.

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

## 기본 위치 ##

- **windows**

```powershell
c:\app\storageResource.json
```

- **linux**

```bash
/app/storageResource.json
```

## 사용자 정의 스토리지 설정 ##

Aspose.Cells Cloud 데이터를 위해 다른 폴더를 사용하려는 경우, 사용자 정의 스토리지 프로필을 지정합니다.

```bash
docker run -d \
  -v c:/data:c:/data \   # 호스트 폴더를 컨테이너 스토리지로 마운트
  -p 47900:5000 \        # API 포트 매핑
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=c:/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

*Linux 예시*:

```bash
docker run -d \
  -v /data:/data \   # 호스트 폴더를 컨테이너 스토리지로 마운트
  -p 47900:5000 \    # API 포트 매핑
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

**참조 문서**:

- [Aspose.Cells Cloud Docker 컨테이너 실행 방법](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
- [Docker 컨테이너 기능](https://docs.aspose.cloud/cells/docker/container-features/)
- [Aspose.Cells Cloud Docker 이미지 다운로드](https://docs.aspose.cloud/cells/docker/download-image/)
- [컨테이너 태그 관리](https://docs.aspose.cloud/cells/docker/manage-tags/)