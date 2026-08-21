---
title: "Aspose.Cells Cloud 빠른 시작: 5분 만에 스프레드시트 애플리케이션 만들기"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud 빠른 시작"
linktitle: "빠른 시작"
type: docs
url: /ko/quickstart/
description: "Aspose.Cells Cloud는 Excel 파일 생성, 변환, 병합, 분할, 보호 및 내부 객체 작업 수행 등 다양한 기능을 제공합니다."
weight: 20
keywords: "Aspose.Cells Cloud, Excel, 스프레드시트, API, 클라우드 SDK, REST API, PDF, CSV, JSON, 빠른 시작"
---

이 안내서는 Aspose.Cells Cloud API를 초기화하고 필요한 스프레드시트 처리 라이브러리를 설치하는 과정을 안내합니다.

이 도구를 사용하면 최신 운영체제(OS)에서 실행되는 애플리케이션에 손쉽게 스프레드시트 변환, 생성 및 편집 기능을 통합할 수 있습니다. 이를 통해 스프레드시트를 읽고 편집하며, 병합·분할하고 다양한 파일 형식으로 변환할 수 있습니다. 이러한 프로그래밍 라이브러리는 데이터, 스타일, 수식, 테이블, 차트, 피벗 테이블, 머리글, 꼬리글, 주석, 도형 객체, 하이퍼링크, 워터마크 등 스프레드시트 구성 요소의 전체 기능을 활용할 수 있도록 지원합니다.

## 무료 계정 만들기

Aspose Cloud는 명확하고 편리한 가격 정책을 통해 제품 구매 전에 충분히 평가 및 테스트할 수 있도록 지원합니다.

먼저 클라우드 인프라에 접근하려면 무료 계정을 생성해야 합니다:

- [Aspose 대시보드](https://dashboard.aspose.cloud/#/) 로그인 페이지로 이동하세요.
- 더 빠른 로그인을 위해 **GitHub로 로그인** 또는 **Google로 로그인** 버튼을 클릭하세요.
- 필요한 정보를 입력하세요.

{{% alert style="info" %}}

축하합니다! Aspose Cloud에 성공적으로 가입하셨습니다.

{{% /alert %}}

## 계정 정보 확인 및 업데이트

다음으로 계정에 대한 개별 설정을 조정해야 합니다:

- 페이지 상단 오른쪽 모서리 아이콘을 클릭하여 [Aspose 계정 설정](https://id.containerize.com/admin/)에 접속하세요.

![dashboard.png](dashboard.png)

- 메뉴 바에서 **계정 설정** 항목을 선택하세요. 설정을 확인한 후 **변경 사항 저장** 버튼을 클릭하여 확인합니다.

![settings.png](settings.png)

## 보안 자격 증명(클라이언트 ID 및 시크릿) 얻기

Aspose는 보안 문제를 매우 중요하게 생각합니다. 우리는 JWT 토큰을 인증에 사용하고, 클라이언트-서버 간 모든 상호작용을 위해 종단 간 HTTPS 암호화를 적용합니다.

애플리케이션은 고유한 API 자격 증명인 **클라이언트 ID**(Client Id)와 **클라이언트 시크릿**(Client Secret)의 집합입니다. 이 자격 증명을 사용하여 클라우드 API를 호출할 때 인증할 수 있습니다. 대부분의 경우 단일 애플리케이션만 필요합니다. 일부 고급 시나리오에서는 별도의 **클라이언트 ID 및 시크릿** 자격 증명을 가진 여러 애플리케이션을 등록하여 사용할 수 있습니다.

애플리케이션 정보에 접근하려면 다음 단계를 수행하세요:

1. [Aspose 대시보드](https://dashboard.aspose.cloud/#/)에 로그인하세요.
2. 페이지 왼쪽에서 [애플리케이션](https://dashboard.aspose.cloud/applications) 탭을 클릭하세요.

![applications.png](applications.png)

3. 페이지 하단으로 스크롤하면 **새 애플리케이션 만들기** 버튼이 있습니다. 클릭하여 새 애플리케이션을 생성하세요.

![createnewapplication.png](createnewapplication.png)

4. 생성 페이지에서 원하는 이름, 설명 및 저장소 주소를 입력한 후 **저장** 버튼을 클릭하세요. 생성이 완료되면 이전 페이지로 돌아갑니다.

![applicationinfo.png](applicationinfo.png)

5. 페이지 하단으로 스크롤하면 방금 생성한 애플리케이션 정보 상자가 표시됩니다. 클릭하여 보안 자격 증명을 확인하거나 업데이트하세요.

![firstapp.png](firstapp.png)

{{% alert style="info" %}}

축하합니다! Aspose.Cells API 호출을 위한 인증 자격 증명을 성공적으로 획득하셨습니다.

{{% /alert %}}

## SDK 선택 및 설치

사용 가능한 다양한 Aspose.Cells Cloud 제품을 살펴보며 가능성을 더 잘 이해해 보세요. 이 소프트웨어 제품들은 24시간 365일 운영되는 고성능 [클라우드 API](https://apireference.aspose.com/)를 기반으로 구축되었습니다.

클라우드 API를 효과적으로 활용하기 위해, 거의 모든 주요 운영체제(Windows, macOS, Linux, Android) 및 주요 프로그래밍 언어([Android](https://products.aspose.cloud/cells/android), [C#](https://products.aspose.cloud/cells/net), [Python](https://products.aspose.cloud/cells/python), [Golang](https://products.aspose.cloud/cells/go), [Java](https://products.aspose.cloud/cells/java), [Node.js](https://products.aspose.cloud/cells/nodejs), [Perl](https://products.aspose.cloud/cells/perl), [PHP](https://products.aspose.cloud/cells/php), [Ruby](https://products.aspose.cloud/cells/ruby), [Swift](https://products.aspose.cloud/cells/swift) 등)에 대해 강력한 [클라우드 SDK](https://products.aspose.cloud/cells/family) 패밀리를 제공합니다.

위 SDK 모두는 [GitHub](https://github.com/aspose-cells-cloud/)에 호스팅되며, 각 저장소에는 사용 방법을 설명하는 다양한 코드 예제가 포함되어 있습니다.

## 개발자 문서 및 코드 예제 확인

이제 계정 설정이 완료되고 개발자 환경이 설치되었습니다. 선택한 SDK를 사용하여 코드 작성을 시작할 수 있습니다. 클라우드 API를 쉽게 활용하려면 [개발자 가이드](https://docs.aspose.cloud/cells/developer-guide/)를 참고하세요.

예: 워크북을 다른 형식으로 변환하기.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_Quickstart.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_Quickstart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_Quickstart.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 필요 시 도움 요청하기

문제를 설명하거나 질문은 [클라우드 포럼](https://forum.aspose.cloud/c/cells/7)에 자유롭게 게시하세요. Aspose 기술 지원 팀이 도움을 드리겠습니다. 참고로 Aspose는 전화를 통한 기술 지원을 제공하지 않으며, 전화 지원은 구매 및 판매 문의에만 한해 제공됩니다.