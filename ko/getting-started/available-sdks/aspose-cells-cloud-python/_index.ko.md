---
title: "Aspose.Cells Cloud SDK for Python: 변환, 병합, 분할, 보호, 검색, 바꾸기 등"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud SDK for Python: 변환, 병합, 분할, 보호, 검색, 바꾸기 등"
linktitle: "Aspose.Cells Cloud SDK for Python"
type: docs
url: /available-sdks/aspose-cells-cloud-python/
description: "Aspose.Cells Cloud SDK for Python은 Office 설치 없이 클라우드에서 Excel 파일을 생성, 변환, 병합, 분할, 보호, 검색, 바꾸기 및 조작할 수 있도록 해주는 크로스플랫폼 유창한 API를 제공합니다."
weight: 30
keywords: ["Aspose.Cells", "Python SDK", "Excel", "클라우드 API", "Excel을 PDF로 변환", "Excel 병합", "워크북 분할", "워크시트 보호", "검색 및 바꾸기", "REST API"]
---

이 SDK는 오픈소스이며 MIT 라이선스를 따릅니다. Aspose.Cells Cloud의 Python 라이브러리 소스 코드는 [여기](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python)에서 확인할 수 있습니다.

# **Aspose.Cells Cloud SDK for Python 사용 방법**

Aspose.Cells Cloud SDK for Python은 파이썬 프로그래밍 언어를 사용해 마이크로소프트 Excel 파일을 조작하고 처리할 수 있도록 해주는 강력한 라이브러리입니다. 이 SDK를 사용하면 로컬 머신에 추가 소프트웨어나 의존성 없이 클라우드에서 Excel 문서를 생성, 편집 및 변환할 수 있습니다.

이 글에서는 Aspose.Cells Cloud SDK for Python을 사용해 일반적인 작업을 수행하는 방법을 살펴보겠습니다. 예를 들어, 새로운 Excel 워크북 생성, 셀에 데이터 삽입, 수정된 워크북을 클라우드에 저장 등이 있습니다.

## 시작하기

Aspose.Cells Cloud SDK for Python을 사용하기 전에 개발 환경을 설정하고 필요한 의존성을 설치해야 합니다. Aspose 웹사이트의 [해당 문서](https://docs.aspose.cloud/cells/quickstart/)를 참고해 클라이언트 ID와 클라이언트 시크릿을 발급받으세요.

## Aspose.Cells Cloud Python 패키지 설치 방법

다음 명령어를 사용해 Aspose.Cells Cloud SDK for Python을 설치할 수 있습니다:

```bash

    pip3 install AsposeCellsCloud
  
 ```

## Python 패키지를 사용해 Xlsx를 PDF로 변환하는 방법

- Aspose.Cells Cloud 라이브러리 불러오기
  프로젝트에 Aspose.Cells Cloud Python SDK에서 필요한 패키지를 먼저 불러옵니다.
- 자격 증명으로 API 클라이언트 구성
  고유한 클라이언트 ID와 클라이언트 시크릿을 사용해 API 클라이언트를 인증합니다.
- 변환 매개변수 준비
  변환 작업에 필요한 매개변수를 정의합니다. 이는 소스 파일 이름, 원하는 출력 형식, 저장소 폴더 경로 등을 포함합니다.
- 워크북 변환 실행
  PostConvertWorkbook 메서드를 호출해 변환 프로세스를 실행하고 응답을 처리합니다.

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_AvailableSDKs.py" >}}