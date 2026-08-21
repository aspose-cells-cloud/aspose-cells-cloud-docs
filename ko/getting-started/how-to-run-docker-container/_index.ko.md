---
title: "Aspose.Cells Cloud Docker 컨테이너 실행 – 풀링, 설정 및 시작"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud Docker 컨테이너 실행 방법"
LinkTitle: "Docker 컨테이너"
type: docs
url: /getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: "Windows 또는 Linux에서 Aspose.Cells Cloud Docker 컨테이너를 풀링하고, 설정하며 실행하는 방법을 알아보세요. Docker‑Compose YAML, 라이선스 설정, 포트 매핑, 문제 해결 팁이 포함됩니다."
weight: 100
keywords:
  - "Aspose.Cells Cloud Docker"
  - "Docker 컨테이너"
  - "Docker Compose"
  - "라이선스 키"
  - "Excel"
  - "스프레드시트"
  - "클라우드 API"
  - "Docker"
  - "Aspose Cells"
  - "API"
---

Docker 기술은 경량 컨테이너를 사용하여 애플리케이션 배포를 자동화하기 위해 설계되었습니다. 개발자는 Docker 컨테이너를 사용하여 애플리케이션과 모든 라이브러리 및 종속성을 함께 묶어 단일 패키지로 배포할 수 있습니다.

Aspose.Cells Cloud 팀은 Docker 사용자를 지원하기 위해 <a href="https://hub.docker.com/r/aspose/cells-cloud" target="_blank" rel="noopener noreferrer">Docker Hub</a>에 Docker 컨테이너를 게시했습니다.

**사전 요구 사항** – Docker Engine ≥ 20.x가 설치되어 있고, 운영 체제(Windows 10/Server 2019/2022 또는 지원되는 Linux 배포판)가 요구 사항을 충족하는지 확인하세요. 라이선스 모드로 실행하려면 선택적으로 라이선스 키를 제공할 수 있습니다.

- Docker Engine ≥ 20.x 설치됨  
- 지원되는 OS (Windows 10/Server 2019/2022 또는 Linux 배포판)  
- 라이선스 모드를 위한 선택적 라이선스 키  

## 컨테이너 설정

### 필수 볼륨

| 컨테이너 내 마운트 경로 | 설명 |
| :--- | :--- |
| C:\fonts | 문서 렌더링에 사용될 글꼴 폴더 |
| C:\data | 파일 저장 폴더 |

**Linux/macOS 대안** – 컨테이너 내에서 `/fonts` 및 `/data`를 사용하고, 컨테이너 실행 시 호스트 디렉터리(예: `/home/user/fonts`, `/home/user/data`)와 매핑하세요.

### 매개변수

| 이름 | 설명 |
| :--- | :--- |
| LicensePublicKey | 라이선스의 공개 키 |
| LicensePrivateKey | 라이선스의 비공개 키 |

**License** 매개변수를 생략하면 애플리케이션은 평가판 모드로 실행됩니다.

### 1. Aspose.Cells Cloud 이미지 풀링

```bash
# 특정 버전의 Aspose.Cells Cloud 이미지 풀링
docker pull aspose/cells-cloud:25.9.0
```

```powershell
# Windows Server 2019용 Aspose.Cells Cloud 이미지 풀링
docker pull aspose/cells-cloud:ltsc2019.25.9.0

# Windows Server 2022용 Aspose.Cells Cloud 이미지 풀링
docker pull aspose/cells-cloud:ltsc2022.25.9.0

# Windows 11용 Aspose.Cells Cloud 이미지 풀링
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

> **참고:** 항상 최신 릴리스를 받으려면 `latest` 태그를 풀링할 수도 있습니다: `docker pull aspose/cells-cloud:latest`.

### 2. Docker‑Compose 도구용 설정

**docker‑compose.yml** 파일에 다음 설정을 기술할 수 있습니다:

```yaml
AsposeCellsCloud:
  image: aspose/cells-cloud:25.9.0
  ports: ["5000:80"]   # 호스트 5000 → 컨테이너 80
  volumes:
    - "C:/Windows/Fonts:C:/Windows/Fonts"
    - "c:/data:c:/data"
  environment:
    LicensePublicKey: "yourPublicKey"
    LicensePrivateKey: "yourPrivateKey"
```

> **참고:** 포트 매핑 `5000:80`은 API가 `http://localhost:5000`에서 접근 가능함을 의미합니다.

### 3. 명령줄을 사용하여 Docker 컨테이너 실행

```bash
docker run \
  -e "LicensePublicKey=yourPublicKey" \
  -e "LicensePrivateKey=yourPrivateKey" \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 5000:80 \
  aspose/cells-cloud:25.9.0
```

**문제 해결:**  
- **포트 충돌:** 호스트의 5000 포트가 사용 중이지 않은지 확인하거나, 사용되지 않는 포트로 매핑을 변경하세요.  
- **라이선스 로드 실패:** 공개 키 및 비공개 키가 환경 변수로 올바르게 전달되었는지, 또는 파일로 마운트되었는지 확인하세요.  
- **글꼴 누락:** 문서가 잘못된 글꼴로 렌더링되는 경우, 글꼴 디렉터리가 올바르게 마운트되었고 필요한 글꼴 파일이 포함되어 있는지 확인하세요.

**관련 리소스:**  
- <a href="/cells/api/">API 레퍼런스</a> | <a href="/cells/license/">라이선스 활성화 가이드</a> | <a href="/cells/getting-started/">시작 가이드 개요</a>

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "Run Aspose.Cells Cloud Docker Container",
  "step": [
    {
      "@type": "HowToStep",
      "url": "#1-pull-asposecells-cloud-image",
      "name": "Docker 이미지 풀링",
      "text": "필요한 이미지를 다운로드하려면 `docker pull aspose/cells-cloud:<version>`을 실행하세요."
    },
    {
      "@type": "HowToStep",
      "url": "#2-configurations-for-docker-compose-tool",
      "name": "docker‑compose 파일 생성",
      "text": "`docker‑compose.yml`에서 이미지, 포트, 볼륨 및 라이선스 환경 변수를 정의하세요."
    },
    {
      "@type": "HowToStep",
      "url": "#3-run-a-docker-container-using-the-command-line",
      "name": "컨테이너 실행",
      "text": "적절한 환경 변수, 볼륨 마운트 및 포트 매핑과 함께 `docker run`을 실행하세요."
    }
  ]
}
```