---
title: "Aspose.Cells Cloud SDK for Ruby: 변환, 병합, 분할, 보호, 검색, 바꾸기 등"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud SDK for Ruby: 변환, 병합, 분할, 보호, 검색, 바꾸기 등"
linktitle: "Aspose.Cells Cloud SDK for Ruby"
type: docs
url: /ko/available-sdks/aspose-cells-cloud-ruby/
description: "Aspose.Cells Cloud SDK for Ruby는 Office 설치 없이 Excel 개체를 생성, 변환, 병합, 분할, 보호, 검색 및 바꾸기 위한 유연하고 크로스 플랫폼 API를 제공합니다."
weight: 30
keywords: "Ruby, Aspose.Cells Cloud, Excel SDK, REST API, 변환, 병합, 분할, 보호, 검색, 바꾸기, 차트, 피벗 테이블, 테이블/목록 개체, PDF, CSV, JSON, Markdown"
---

이 SDK는 오픈소스이며 MIT 라이선스로 제공됩니다. Aspose.Cells Cloud용 Ruby 라이브러리 소스 코드는 [여기](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby)에서 확인할 수 있습니다.

# **Aspose.Cells Cloud SDK for Ruby 사용 방법**

Aspose.Cells Cloud SDK for Ruby는 Ruby 프로그래밍 언어를 사용해 마이크로소프트 Excel 파일을 조작하고 처리할 수 있는 강력한 라이브러리입니다. 이 SDK를 사용하면 로컬 머신에 추가 소프트웨어나 의존성을 설치하지 않고도 클라우드에서 Excel 문서를 생성, 편집 및 변환할 수 있습니다.

이 글에서는 Aspose.Cells Cloud SDK for Ruby를 사용해 일반적인 작업을 수행하는 방법을 알아보겠습니다. 예를 들어 새 Excel 워크북 생성, 셀에 데이터 삽입, 수정된 워크북을 클라우드에 저장 등이 있습니다.

## 시작하기

Aspose.Cells Cloud SDK for Ruby를 사용하려면 먼저 개발 환경을 설정하고 필요한 종속성을 설치해야 합니다. 클라이언트 ID와 클라이언트 비밀번호를 얻으려면 Aspose 웹사이트의 [해당 문서](https://docs.aspose.cloud/cells/quickstart/)를 참조하십시오.

## Aspose.Cells Cloud용 Ruby 패키지 설치 방법

아래 명령어를 사용해 Aspose.Cells Cloud SDK for Ruby를 설치할 수 있습니다:

```bash

    gem install aspose_cells_cloud
  
 ```

## Ruby 패키지를 사용해 Xlsx를 다른 형식으로 변환하는 방법

- Aspose.Cells Cloud 라이브러리 가져오기  
  먼저 Aspose.Cells Cloud Ruby SDK에서 필요한 패키지를 프로젝트에 가져옵니다.
- 자격 증명으로 API 클라이언트 구성  
  고유한 클라이언트 ID와 클라이언트 비밀번호로 API 클라이언트를 인증합니다.
- 변환 파라미터 준비  
  변환 작업의 파라미터를 정의합니다. 여기에는 소스 파일 이름, 원하는 출력 형식, 저장소 폴더 경로가 포함됩니다.
- 워크북 변환 실행  
  PostConvertWorkbook 메서드를 호출해 변환 작업을 실행하고 응답을 처리합니다.

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_AvailableSDKs.rb" >}}