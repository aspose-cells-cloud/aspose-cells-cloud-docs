---
title: "Aspose.Cells Cloud Docker 이미지 태그"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud Docker 이미지 태그"
linktitle: "이미지 태그"
type: docs
url: /docker/tag-list/
description: "Windows Server(2016~2022) 및 Linux용 최신 Aspose.Cells Cloud Docker 이미지 태그를 확인하세요. 풀(pull) 명령어, 아키텍처 세부 정보 및 업그레이드 참고 사항을 한 곳에서 확인하세요."
weight: 30
keywords:
  - "Aspose.Cells Cloud Docker 이미지 태그"
  - "Docker 풀 명령어"
  - "Windows Server Docker 태그"
  - "Linux Docker 태그"
  - "Aspose.Cells Cloud"
---

Aspose.Cells Cloud는 Windows Server(2016, 2019, 2022) 및 Linux용으로 즉시 실행 가능한 Docker 이미지를 제공합니다.  
각 이미지는 제품 릴리스 및 대상 운영 체제를 식별하는 **태그**로 버전이 지정됩니다.  
아래 태그를 사용하여 필요한 정확한 이미지를 풀(pull)하고, 빠른 시작을 위해 제공되는 풀 및 실행 예제를 참조하세요.

*최종 업데이트: 2026-07-01*

**필수 조건:** Docker Engine 20.10 이상이 설치되어 있고, 유효한 Aspose.Cells Cloud 라이선스 키가 있어야 합니다. 해당 이미지는 지정된 Windows Server 버전 또는 Linux x64용으로 빌드되었습니다.

## Windows Server 2016 이미지 ##

태그 | 아키텍처 | Dockerfile | 비고
---|---|---|---
✅ `ltsc2016.23.5.0` | x64 | Dockerfile은 공개되지 않음 – 빌드 세부 정보는 [릴리스 노트](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2016)를 참조하세요. | Windows Server 2016에 대한 더 이상의 새 태그는 예정되어 있지 않으며, 이는 최종 릴리스 버전입니다.

```bash
docker pull aspose/cells:ltsc2016.23.5.0
docker run -d --name cells-ws2016 -p 8080:80 aspose/cells:ltsc2016.23.5.0
```

추가 자료: [Docker 다운로드](/cells/docker/downloads/), [릴리스 노트](/cells/release-notes/), [필수 조건](/cells/docker/prerequisites/).  
자세한 내용은 [Docker 개요](/cells/docker/)를 참조하세요.

## Windows Server 2019 이미지 ##

태그 | 아키텍처 | Dockerfile | 비고
---|---|---|---
✅ `ltsc2019.25.10.0` | x64 | Dockerfile은 공개되지 않음 – 빌드 세부 정보는 [릴리스 노트](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2019)를 참조하세요. | —
```bash
docker pull aspose/cells:ltsc2019.25.10.0
docker run -d --name cells-ws2019 -p 8080:80 aspose/cells:ltsc2019.25.10.0
```

추가 자료: [Docker 다운로드](/cells/docker/downloads/), [릴리스 노트](/cells/release-notes/), [필수 조건](/cells/docker/prerequisites/).  
자세한 내용은 [Docker 개요](/cells/docker/)를 참조하세요.

## Windows Server 2022 이미지 ##

태그 | 아키텍처 | Dockerfile | 비고
---|---|---|---
✅ `ltsc2022.25.10.0` | x64 | Dockerfile은 공개되지 않음 – 빌드 세부 정보는 [릴리스 노트](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2022)를 참조하세요. | —
```bash
docker pull aspose/cells:ltsc2022.25.10.0
docker run -d --name cells-ws2022 -p 8080:80 aspose/cells:ltsc2022.25.10.0
```

추가 자료: [Docker 다운로드](/cells/docker/downloads/), [릴리스 노트](/cells/release-notes/), [필수 조건](/cells/docker/prerequisites/).  
자세한 내용은 [Docker 개요](/cells/docker/)를 참조하세요.

## Linux 이미지 ##

태그 | 아키텍처 | Dockerfile | 비고
---|---|---|---
✅ `linux.25.10.0` | x64 | Dockerfile은 공개되지 않음 – 빌드 세부 정보는 [릴리스 노트](https://github.com/aspose-cells/dockerfiles/tree/main/linux)를 참조하세요. | —
```bash
docker pull aspose/cells:linux.25.10.0
docker run -d --name cells-linux -p 8080:80 aspose/cells:linux.25.10.0
```

추가 자료: [Docker 다운로드](/cells/docker/downloads/), [릴리스 노트](/cells/release-notes/), [필수 조건](/cells/docker/prerequisites/).  
자세한 내용은 [Docker 개요](/cells/docker/)를 참조하세요.

**버전 변경 로그**

태그 | 변경 사항
---|---
`ltsc2016.23.5.0` | Windows Server 2016용 최종 릴리스; 보안 패치 및 성능 개선 포함.
`ltsc2019.25.10.0` | Aspose.Cells 25.10.0으로 업데이트됨; 새로운 수식 지원 및 버그 수정 추가.
`ltsc2022.25.10.0` | 2019 태그와 동일하며, Windows Server 2022 런타임에 최적화됨.
`linux.25.10.0` | Aspose.Cells 25.10.0 기반 Linux 이미지; 업데이트된 종속성 및 Linux 전용 최적화 포함.
---