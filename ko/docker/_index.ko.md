---
title: "Aspose.Cells Cloud Docker 운영 매뉴얼: Aspose.Cells Cloud 애플리케이션을 자체 사설 인프라에 배포하기"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud Docker 운영 매뉴얼"
linktitle: "Docker"
type: docs
url: /ko/docker-developer-guide/
aliases: [  /ko/docker/ , /ko/docker/run/ ]
description: "Aspose.Cells Cloud를 Docker 컨테이너로 사설 또는 온프레미스 인프라에 배포하여 Aspose의 퍼블릭 클라우드를 사용하지 않고도 스프레드시트 처리(Excel, PDF, CSV, JSON, Markdown)를 수행할 수 있습니다."
keywords:
  [
    "Aspose.Cells Cloud",
    "Docker",
    "Docker Image",
    "Spreadsheet API",
    "Excel",
    "PDF",
    "CSV",
    "JSON",
    "Markdown",
    "Private Cloud",
    "Deployment",
  ]
weight: 30
---

Aspose.Cells Cloud는 Excel과 같은 형식의 파일 생성, 편집, 변환 및 조작을 지원하는 클라우드 기반 스프레드시트 처리 서비스입니다. Docker 배포를 통해 독립적인 서비스 환경으로 빠르게 구축할 수 있어 의존성 관리 및 크로스 플랫폼 배포 과정을 간소화합니다.

이 매뉴얼은 환경 준비부터 서비스 검증까지 전체 운영 절차를 상세히 안내합니다.

## 환경 준비

Aspose.Cells Cloud Docker 컨테이너를 배포하기 전에, 로컬 환경이 다음 의존성 요구 사항을 충족하는지 확인해야 합니다. 그렇지 않으면 누락된 구성 요소로 인해 배포가 실패할 수 있습니다.

### 기본 의존성 구성 요소

- **Docker Engine:** 컨테이너 런타임 핵심 엔진으로, 컨테이너 생성 및 관리를 담당합니다. 최소 버전 요구 사항은 **18.09.0**입니다.
- **운영체제:** Docker를 지원하는 주요 운영체제

  | 운영체제 유형 | 버전                      |
  | :------------ | :------------------------ |
  | Windows       | Windows 10/11             |
  | Windows Server| 2016 / 2019 / 2022        |
  | Linux         | CentOS 7+ / Ubuntu 20.04+ |

- **하드웨어 자원:** 서비스가 안정적으로 실행되도록 하여 자원 부족으로 인한 충돌을 방지합니다.
  - CPU: 2코어 이상
  - 메모리: 4GB 이상
  - 디스크: 10GB 이상의 여유 공간

### 주요 사전 조건

- **Aspose 라이선스:** Aspose 공식 계정을 등록하여 유효한 라이선스를 획득해야 합니다(평가판 또는 상용 버전 신청 가능). 라이선스가 없을 경우 서비스 기능이 제한될 수 있습니다. 자세한 내용은 [라이선스](https://purchase.aspose.com/buy) 페이지를 참조하십시오.
- **네트워크 연결:** Docker Hub에 접근 가능하도록 배포 환경의 네트워크가 설정되어 있어야 합니다(이미지를 풀기 위해).

## Aspose.Cells Cloud Docker 이미지 획득

Aspose.Cells Cloud 이미지는 Docker Hub에 호스팅되어 있으며, 수동 빌드 없이 `docker pull` 명령으로 직접 풀할 수 있습니다.

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

## Aspose.Cells Cloud Docker 컨테이너 실행

### 실행 매개변수

| 이름                        | 설명                                                                 | 비고                                                         |
| --------------------------- | -------------------------------------------------------------------- | ------------------------------------------------------------ |
| LicensePublicKey            | Metered 과금 모드 사용 시 라이선스의 공개 키를 설정합니다.          | Metered 과금 모드를 사용하는 경우에만 유효합니다.            |
| LicensePrivateKey           | Metered 과금 모드 사용 시 라이선스의 비공개 키를 설정합니다.         | Metered 과금 모드를 사용하는 경우에만 유효합니다.            |
| storagesCredentialsFilePath | 스토리지 설정 파일 경로입니다. 기본 파일은 `./storageResource.json`입니다. |                                                              |
| LicenseFile                 | LicenseFile 과금 모드 사용 시 라이선스 파일을 설정합니다.            | LicenseFile 과금 모드를 사용하는 경우에만 유효합니다.        |
| AccessToken                 | API에 접근하기 위한 토큰입니다.                                      | 비어 있을 경우 토큰 인증이 필요 없습니다.                     |

### 실행 명령어

평가판 모드로 컨테이너를 실행하는 것은 다음과 같이 간단합니다:

```bash
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

모든 기능을 사용하려면 [Metered 라이선스](https://purchase.aspose.com/faqs/licensing/metered/)를 획득하고, 파일 저장소를 위해 호스트 폴더를 마운트해야 합니다. 이 경우 실행 명령은 다음과 같습니다:

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

### API 참조 – Aspose.Cells Cloud Docker

- `<https://hostname:port/swagger>`
- `<https://hostname:port/swagger/ui/index.html>`

### 포트 노출

| 포트 | 설명                                      | 필수 여부 |
| ---- | ----------------------------------------- | --------- |
| 5000 | 문서 렌더링에 사용되는 글꼴 폴더           | true      |

### 필수 볼륨 마운트

| 컨테이너 내 마운트 경로 | 설명                                      | 필수 여부 | 비고                                                         |
| ----------------------- | ----------------------------------------- | --------- | ------------------------------------------------------------ |
| C:\fonts                | 문서 렌더링에 사용되는 글꼴 폴더           | false     | 글꼴 누락으로 인한 스프레드시트/Excel 문제를 해결합니다.     |
| C:\data                 | 파일 저장 폴더                             | false     | 저장 공간을 확보하여 파일 관리 및 접근을 용이하게 합니다.     |

## 참고 문서

- [Aspose.Cells Cloud Docker 컨테이너 핵심 기능](https://docs.aspose.cloud/cells/docker-container-features/)
- [Aspose.Cells Cloud Docker 컨테이너 스토리지 설정 방법](https://docs.aspose.cloud/cells/docker/storage/)
- [Aspose.Cells Cloud Docker 컨테이너 실행 방법](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)