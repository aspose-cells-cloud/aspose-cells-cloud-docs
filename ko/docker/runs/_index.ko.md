---
title: "Aspose.Cells Cloud Docker 컨테이너 실행 방법"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud Docker 컨테이너 실행 방법"
linktitle: "컨테이너 실행"
type: docs
url: /ko/run-aspose-cells-cloud-docker-container/
description: "Windows Server 2022에서 Docker 컨테이너로 Aspose.Cells Cloud를 실행하는 방법을 배워보세요. 체험 모드, 사용량 기반 과금, 라이선스 과금, 스토리지 설정, 헬스 체크를 위한 단계별 명령어를 제공합니다."
weight: 30
keywords: "Aspose.Cells, Docker, Windows Server 2022, 체험 모드, 사용량 기반 과금, 라이선스 과금, 스토리지 설정"
---

Aspose.Cells Cloud Docker는 로컬 또는 사설 클라우드에서 Aspose.Cells Cloud API를 호스팅할 수 있는 즉시 실행 가능한 컨테이너 이미지를 제공합니다. 이 가이드에서는 세 가지 일반적인 라이선스 모드—**체험 모드**, **사용량 기반 과금**, **라이선스 과금**—로 컨테이너를 시작하는 방법과 액세스 토큰을 사용하는 변형을 설명합니다. 모든 명령어는 Windows Server 2022에서 PowerShell을 기준으로 작성되었으며, Linux 환경에서는 볼륨 경로를 적절히 수정해야 합니다.

**필수 요구 사항**

- Docker Engine 20.10 이상이 설치되어 실행 중인 상태  
- PowerShell 5.1 또는 PowerShell 7+  
- 컨테이너 내부 포트 5000(호스트 포트 47900에 매핑)을 열고, 호스트 방화벽에서 47900 포트로 들어오는 트래픽을 허용해야 함  
- 사용량 기반 과금 또는 라이선스 과금 모드를 사용할 경우, `LicensePublicKey`, `LicensePrivateKey` 또는 라이선스 파일을 준비해 두어야 하며, 토큰 모드를 사용할 경우 `AccessToken`을 준비해야 함  
- 컨테이너의 스토리지로 마운트할 로컬 폴더(예: `C:\data`)

**빠른 시작(체험 모드)**

다음 명령어를 실행하여 체험 모드로 컨테이너를 시작하세요:

```powershell
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

## 체험 모드로 Aspose.Cells Cloud Docker 컨테이너 실행하기

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

컨테이너는 포그라운드(foreground)로 실행되며, 호스트 포트 **47900**에서 수신 대기하며, 이는 컨테이너 내부 포트 **5000**으로 전달됩니다.

## 사용량 기반 과금 모드로 Aspose.Cells Cloud Docker 컨테이너 실행하기

```powershell
# Windows Server 2022
# 사용량 기반 과금 모드: LicensePublicKey 및 LicensePrivateKey를 환경 변수로 설정합니다.
# 스토리지 폴더를 바인딩(호스트 → 컨테이너)
#   -v c:/data:c:/data
# API가 시스템 글꼴에 접근할 수 있도록 Windows 글꼴 폴더를 바인딩합니다.
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

컨테이너는 분리 모드(`-d`)로 실행됩니다. 시작 후 아래 명령어로 서비스가 접근 가능한지 확인할 수 있습니다:

```powershell
curl http://localhost:47900/v3.0/health
```

**`storageResource.json` 샘플**

```json
{
  "default": {
    "type": "Local",
    "rootFolder": "c:/data"
  }
}
```

## 라이선스 과금 모드로 Aspose.Cells Cloud Docker 컨테이너 실행하기

```powershell
# Windows Server 2022
# 라이선스 과금 모드: LicenseFile 환경 변수를 통해 라이선스 파일을 제공합니다.
# 스토리지 폴더를 바인딩(호스트 → 컨테이너)
#   -v c:/data:c:/data
# Windows 글꼴 폴더를 바인딩합니다.
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

## 액세스 토큰으로 Aspose.Cells Cloud Docker 컨테이너 실행하기

```powershell
# Windows Server 2022
# 액세스 토큰 모드: AccessToken과 선택적으로 사용량 기반 과금 키를 설정합니다.
# 스토리지 폴더를 바인딩합니다.
#   -v c:/data:c:/data
# Windows 글꼴 폴더를 바인딩합니다.
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

컨테이너를 시작한 후, 이전에 언급한 헬스 체크 명령어를 사용하여 서비스가 정상 작동하는지 확인하세요.

## 참고 문서

- [Aspose.Cells Cloud Docker 컨테이너 스토리지 설정 방법](https://docs.aspose.cloud/cells/docker/storage/)

---

### 문제 해결

- **헬스 체크 실패** – 포트 47900이 방화벽에 의해 차단되지 않았는지 확인하고, 컨테이너가 실행 중인지(`docker ps`) 확인하세요.  
- **라이선스 오류** – `LicensePublicKey`, `LicensePrivateKey`, 또는 `LicenseFile` 값이 올바른지, 그리고 환경 변수에 불필요한 공백 없이 전달되었는지 확인하세요.  
- **스토리지 접근 불가능** – 호스트 폴더(`c:/data`)가 존재하며, Docker가 이 폴더에 읽기/쓰기 권한을 갖는지 확인하세요.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud Docker 컨테이너 실행 방법",
  "description": "Windows Server 2022에서 Aspose.Cells Cloud를 Docker 컨테이너로 시작하는 단계별 가이드로, 체험 모드, 사용량 기반 과금, 라이선스 과금, 액세스 토큰 모드를 모두 다룹니다.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "url": "https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/",
  "keywords": "Aspose.Cells, Docker, Windows Server 2022, 체험 모드, 사용량 기반 과금, 라이선스 과금, 스토리지 설정"
}
</script>