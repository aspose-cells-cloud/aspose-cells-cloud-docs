---
title: "Aspose.Cells Cloud SDK for Node.js: 변환, 병합, 분할, 보호, 검색, 바꾸기 등"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud SDK for Node.js: 변환, 병합, 분할, 보호, 검색, 바꾸기 등"
linktype: "Aspose.Cells Cloud SDK for Node.js"
type: docs
url: /ko/available-sdks/aspose-cells-cloud-node/
description: "Aspose.Cells Cloud SDK for Node.js는 진정한 크로스플랫폼 기능을 제공합니다. 단일 import로 윈도우, 리눅스, macOS 개발자들이 동일한 일관된 API를 통해 모든 엑셀 객체를 생성, 변환, 병합, 분할, 보호 및 조작할 수 있으며, Office 설치가 필요 없고 플랫폼별 맞춤 설정도 불필요합니다."
weight: 30
kwords: Node.js, Node.js SDK, Node.js용 엑셀 SDK, Node.js용 클라우드 SDK, REST, 차트, 피벗 테이블, 테이블/목록 개체, 스프레드시트 변환, PDF, CSV, Json, Markdown, 병합, 분할, 보호, 검색, 바꾸기
---

이 SDK는 오픈소스이며 MIT 라이선스하에 배포됩니다. Aspose.Cells Cloud용 Node 라이브러리 소스 코드는 [여기](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node)에서 확인할 수 있습니다.

# **Aspose.Cells Cloud Node 라이브러리 사용 방법**

Aspose.Cells Cloud SDK for Node는 Node 프로그래밍 언어를 사용해 마이크로소프트 엑셀 파일을 조작하고 처리할 수 있는 강력한 라이브러리입니다. 이 SDK를 사용하면 로컬 머신에 추가 소프트웨어나 의존성 없이 클라우드에서 엑셀 문서를 생성, 편집 및 변환할 수 있습니다.

이 글에서는 Aspose.Cells Cloud SDK for Node를 사용해 일반적인 작업을 수행하는 방법을 살펴보겠습니다. 예를 들어 새 엑셀 워크북 생성, 셀에 데이터 삽입, 수정된 워크북을 클라우드에 저장하기 등입니다.

## 시작하기

Aspose.Cells Cloud SDK for Go를 사용하려면 먼저 개발 환경을 설정하고 필요한 의존성을 설치해야 합니다. 클라이언트 ID와 클라이언트 시크릿을 받기 위해 Aspose 웹사이트의 [해당 문서](https://docs.aspose.cloud/cells/quickstart/)를 참조하세요.

## Aspose.Cells Cloud용 Node 패키지 설치 방법

npm을 사용해 Aspose.Cells Cloud SDK for Node를 설치할 수 있습니다. 아래는 npm 설치 절차입니다:

```Powershell

npm install asposecellscloud

```

## Aspose.Cells Cloud용 패키지 설정 시 의존성 추가 방법

node 설정 파일: package.json

```Node

{
    "requires": true,
    "lockfileVersion": 1,
    "dependencies": {
        "@types/jest": "^26.0.24",
        "@types/request": "^2.48.7",
        "asposecellscloud": "24.4",
        "axios": "^1.5.1",
        "JSON": "^1.0.0",
        "mocha": "^10.2.0",
        "request": "^2.88.2",
        "request-debug": "^0.2.0"
    }
}

```

## Node 패키지를 사용해 Xlsx를 다른 형식으로 변환하는 방법

- Aspose.Cells Cloud 라이브러리 불러오기  
  프로젝트에 Aspose.Cells Cloud NodeJS SDK에서 필요한 패키지를 먼저 불러옵니다.
- 자격 증명으로 API 클라이언트 구성  
  고유한 클라이언트 ID와 클라이언트 시크릿을 사용해 API 클라이언트를 인증합니다.
- 변환 매개변수 준비  
  변환 작업의 매개변수를 정의합니다. 여기에는 원본 파일 이름, 원하는 출력 형식, 저장소 폴더 경로가 포함됩니다.
- 워크북 변환 실행  
  PostConvertWorkbook 메서드를 호출해 변환 작업을 실행하고 응답을 처리합니다.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}