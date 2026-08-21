---
title: "Aspose.Cells Cloud PHP SDK – Excel 파일 변환, 병합, 분할, 보호"  
second_title: "문서"  
ArticleTitle: "Aspose.Cells Cloud PHP SDK – Excel 파일 변환, 병합, 분할, 보호"  
linktitle: "Aspose.Cells Cloud PHP SDK"  
type: docs  
url: /ko/available-sdks/aspose-cells-cloud-php/
description: "Aspose.Cells Cloud PHP SDK(v24.3) 다운로드. Composer를 통한 설치 방법, 인증, XLSX를 PDF/CSV로 변환, 워크북 병합, 시트 보호 등 다양한 기능을 살펴보세요. Office 설치 없이 모두 가능합니다."  
keywords: "Aspose.Cells, 클라우드, PHP, SDK, Excel, 변환, 병합, 분할, 보호"  
weight: 30  
---  

이 SDK는 오픈소스이며 MIT 라이선스가 부여됩니다. Aspose.Cells Cloud용 PHP 라이브러리 소스 코드는 <a href="https://github.com/aspose-cells-cloud/aspose-cells-cloud-php" target="_blank" rel="noopener noreferrer">여기</a>에서 확인할 수 있습니다.

# **Aspose.Cells Cloud PHP SDK 사용 방법**

Aspose.Cells Cloud PHP SDK는 **PHP 프로그래밍 언어**를 사용해 마이크로소프트 Excel 파일을 조작하고 처리할 수 있는 강력한 라이브러리입니다. 이 SDK를 사용하면 로컬 머신에 추가 소프트웨어나 의존성 없이 클라우드에서 Excel 문서를 생성, 편집 및 변환할 수 있습니다.

이 문서에서는 Aspose.Cells Cloud PHP SDK를 사용해 일반적인 작업을 수행하는 방법을 살펴보겠습니다. 예를 들어 새로운 Excel 워크북 생성, 셀에 데이터 삽입, 수정된 워크북을 클라우드에 저장하는 등의 작업을 수행합니다.

## 시작하기 전에

Aspose.Cells Cloud SDK를 **PHP**에서 사용하기 전에 개발 환경을 설정하고 필요한 의존성을 설치해야 합니다. Aspose 웹사이트의 <a href="https://docs.aspose.cloud/cells/quickstart/" target="_blank" rel="noopener noreferrer">문서</a>를 참조해 클라이언트 ID와 클라이언트 시크릿을 발급받으세요.

**필수 조건**

- PHP 7.4 이상  
- 개발 머신에 Composer 설치됨  
- 유효한 Aspose Cloud 클라이언트 ID 및 클라이언트 시크릿  
- Aspose Cloud 스토리지 위치(기본 또는 사용자 지정) 접근 권한  

## Aspose.Cells Cloud용 PHP 패키지 설치 방법

Aspose.Cells Cloud PHP SDK를 설치할 수 있습니다. 아래는 설치 단계입니다.

- `composer.json` 파일에 Aspose.Cells Cloud를 의존성으로 추가합니다:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- Composer를 실행해 SDK를 설치합니다:

   ```bash
   composer install
   ```

- PHP 코드에서 Composer의 autoloader를 포함시킵니다:

   ```php
   require 'vendor/autoload.php';
   ```

## PHP 패키지를 사용해 Xlsx를 다른 형식으로 변환하는 방법

- Aspose.Cells Cloud 라이브러리 임포트  
  먼저 프로젝트에 Aspose.Cells Cloud PHP SDK에서 필요한 패키지를 임포트합니다.

- 자격 증명으로 API 클라이언트 구성  
  고유한 클라이언트 ID와 클라이언트 시크릿을 사용해 API 클라이언트를 인증합니다.

- 변환 파라미터 준비  
  변환 작업에 필요한 파라미터를 정의합니다. 예: 원본 파일 이름, 원하는 출력 형식, 스토리지 폴더 경로 등.

- 워크북 변환 실행  
  `PostConvertWorkbook` 메서드를 호출해 변환 작업을 실행하고 응답을 처리합니다.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}

### `PostConvertWorkbook` API 참조

| 파라미터       | 설명                                             | 타입   | 필수 여부 |
|----------------|--------------------------------------------------|--------|-----------|
| `file`         | 원본 Excel 파일 이름(예: `sample.xlsx`).         | string | 예         |
| `format`       | 원하는 출력 형식(`pdf`, `csv`, `png` 등).         | string | 예         |
| `storage`      | 원본 파일이 위치한 스토리지 이름 또는 폴더 경로. | string | 아니오     |
| `outPath`      | 선택적으로, 변환된 파일을 스토리지에 직접 저장할 경로. | string | 아니오     |

**HTTP 메서드:** POST  
**엔드포인트:** `/cells/convert/{format}`  

**응답 예시(JSON)**  

```json
{
  "status": "OK",
  "url": "https://api.aspose.cloud/v3.0/cells/convert/output.pdf"
}
```

**상태 코드**

- `200` – 변환 성공.  
- `400` – 잘못된 요청(누락되거나 유효하지 않은 파라미터).  
- `401` – 인증 실패.  
- `500` – 서버 오류.  
---