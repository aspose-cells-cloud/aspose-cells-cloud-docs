---
title: "Aspose.Cells Cloud Docker 이미지 다운로드"  
second_title: "문서"  
ArticleTitle: "Aspose.Cells Cloud Docker 이미지 다운로드"  
linktitle: "이미지 다운로드"  
type: docs  
url: /ko/docker/downloads/
description: "Windows Server 2016/2019 및 Linux용 최신 Aspose.Cells Cloud Docker 이미지를 다운로드하세요. 로컬에서 컨테이너를 실행하기 위한 단계별 설명, 사전 조건 및 보안 팁을 따르세요."  
weight: 30  
keywords: "Aspose.Cells, 클라우드, Docker, 컨테이너, 이미지, 다운로드, Windows Server, Linux, REST API"  
---  

## 개요  

`aspose/cells-cloud` – **Aspose.Cells Cloud** REST API를 호스팅하는 공식 Docker 이미지입니다. 이 이미지를 사용하면 Aspose의 퍼블릭 클라우드 서비스에 의존하지 않고 온라인 또는 프라이빗 클라우드 환경에서 스프레드시트 처리 엔진을 컨테이너 내에서 실행할 수 있습니다.  

**최종 업데이트:** 2026-06-30  

**빠른 시작 체크리스트**

- Docker 엔진 버전이 20.10 이상인지 확인하세요.  
- 운영 체제에 맞는 적절한 이미지를 풀하세요(아래 섹션 참조).  
- `ASPOSE_CLIENT_ID` 및 `ASPOSE_CLIENT_SECRET` 환경 변수를 설정하세요.  
- 컨테이너를 실행할 때 포트 8080을 내부 포트 80에 매핑하세요.  

---  

## 사전 조건  

| 요구 사항 | 세부 정보 |
|-----------|-----------|
| **Docker 엔진** | 호스트 운영 체제에 Docker 20.10 이상이 설치되어 있어야 합니다. |
| **운영 체제** | Windows Server 2016, Windows Server 2019 또는 최신 Linux 배포판. |
| **Docker Hub 접근 권한** | 활성 Docker Hub 계정(선택 사항이지만 프라이빗 이미지를 풀할 경우 권장됨). 프라이빗 저장소에서 풀할 필요가 있다면 `docker login`을 실행하세요. |
| **Aspose Cloud 자격 증명** | `ASPOSE_CLIENT_ID` 및 `ASPOSE_CLIENT_SECRET` – Aspose Cloud 대시보드에서 획득하세요. |

> **팁:** `docker --version` 명령으로 Docker 설치를 확인하세요.  

---  

## Windows Server 2016  

```powershell
docker pull aspose/cells-cloud:ltsc2016.21.9
```

---  

## Windows Server 2019  

```powershell
docker pull aspose/cells-cloud:ltsc2019.21.9
```

---  

## Linux  

```sh
docker pull aspose/cells-cloud:linux.21.9
```

---  

## 컨테이너 실행  

```sh
docker run -d \
  -e ASPOSE_CLIENT_ID=YOUR_CLIENT_ID \
  -e ASPOSE_CLIENT_SECRET=YOUR_CLIENT_SECRET \
  -p 8080:80 \
  --name aspose-cells \
  aspose/cells-cloud:ltsc2019.21.9
```

* **환경 변수** – `ASPOSE_CLIENT_ID` 및 `ASPOSE_CLIENT_SECRET`은 API에서 필요한 자격 증명을 제공합니다.  
* **포트 매핑** – 컨테이너는 포트 80을 노출하며, 서비스에 접근하려면 호스트 포트(예: 8080)에 매핑해야 합니다.  
* **백그라운드 실행(`-d`)** – 컨테이너를 백그라운드에서 실행합니다.  

---  

## 버전 관리 및 업데이트  

| OS | 태그 | 릴리스 날짜 | 최신 버전 받는 방법 |
|----|------|--------------|---------------------|
| Windows Server 2016 | `ltsc2016.21.9` | 2026-06-30 | `docker pull aspose/cells-cloud:ltsc2016.latest` |
| Windows Server 2019 | `ltsc2019.21.9` | 2026-06-30 | `docker pull aspose/cells-cloud:ltsc2019.latest` |
| Linux | `linux.21.9` | 2026-06-30 | `docker pull aspose/cells-cloud:linux.latest` |

> **참고:** 태그 `21.9`는 현재 안정 릴리스입니다. 최신 버전을 확인하려면 `latest` 태그를 사용하거나 [Aspose.Cells Cloud 릴리스 노트](/cells/release-notes/)를 참조하세요.  

---  

## 검증 및 보안  

* **이미지 다이제스트 확인**  

  ```sh
  docker image inspect aspose/cells-cloud:ltsc2019.21.9 --format='{{.RepoDigests}}'
  ```

* **취약성 스캔**(권장)  

  ```sh
  trivy image aspose/cells-cloud:ltsc2019.21.9
  ```

* **모범 사례** – Docker를 최신 상태로 유지하고, 필요한 최소 권한만 부여하여 컨테이너를 실행하며, 알려진 CVE에 대해 이미지를 정기적으로 스캔하세요.  

* **구조화된 데이터(JSON-LD) 예제**  

  ```html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "Aspose.Cells Cloud Docker Image",
    "operatingSystem": "Windows Server 2016/2019, Linux",
    "softwareVersion": "21.9",
    "downloadUrl": "https://hub.docker.com/r/aspose/cells-cloud",
    "offers": {
      "price": "0",
      "priceCurrency": "USD"
    }
  }
  </script>
  ```

---  

## 일반적인 문제 및 문제 해결  

| 증상 | 가능한 원인 | 해결 방법 |
|------|-------------|-----------|
| `docker: command not found` | Docker가 설치되지 않았거나 PATH가 설정되지 않음 | Docker를 설치하고 터미널을 다시 시작하세요. |
| 이미지 풀 시 인증 실패 | 누락되거나 잘못된 `docker login` | 유효한 Docker Hub 자격 증명으로 `docker login`을 실행하세요. |
| 컨테이너가 즉시 종료됨 | 필수 환경 변수 누락 | **컨테이너 실행** 섹션에 나온 대로 `ASPOSE_CLIENT_ID` 및 `ASPOSE_CLIENT_SECRET`을 제공하세요. |
| 호스트에서 포트 충돌 | 호스트 포트가 이미 사용 중 | 다른 호스트 포트를 선택하세요(예: `-p 8081:80`). |

---  

## 추가 정보  

* [Aspose.Cells Cloud API 문서](/cells/cloud/api/)  
* [Aspose.Cells Cloud 릴리스 노트](/cells/release-notes/) – 버전 21.9 및 이후 버전의 자세한 변경 로그.  
* [Aspose.Cells Docker 컨테이너 기능](/cells/docker/features/)  
* [Aspose.Cells Docker 이미지 태그 목록](/cells/docker/tag-list/)  

---  

*Aspose Cloud 엔지니어링 팀이 작성.*