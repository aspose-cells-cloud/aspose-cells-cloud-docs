---
title: "Aspose.Cells Cloud AI – 사용자 작업 분해 API(v4.0) | SMART 작업 계획"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud AI 작업 분해 API를 사용해 사용자 목표를 순차적 행동 계획으로 변환하는 방법"
linktitle: "사용자 작업 분해"
type: docs
url: /decompose-user-task/
keywords: "Aspose.Cells AI, 작업 분해 API, SMART 작업 계획, Redmine 가져오기, 프로젝트 자동화"
description: "Aspose.Cells Cloud AI를 사용해 자유 서술 형식의 목표를 SMART 기준에 부합하고 시간 추정이 적용된 작업 목록으로 변환하세요. 단일 PUT 요청으로 Redmine, Jira, Azure DevOps에 바로 사용할 수 있는 CSV/XLSX 형식의 출력물을 받아보세요."
weight: 100
---

**DecomposeUserTask** 엔드포인트는 자유 서술 형식의 작업 설명을 SMART 기준을 충족하는 자세한 순차적 행동 계획으로 변환하는 REST 엔드포인트를 제공합니다. 이 API는 자동으로 시간 기준(시간 단위)의 추정치를 할당하고, Redmine 호환 가져오기 형식으로 출력물을 포맷하며, 프로젝트 마일스톤 노드를 생성합니다. 사용자는 간단한 작업 목록과 선택적 시간 추정치만 제공하면 되며, API는 프로젝트 관리 도구에 바로 가져와 사용할 수 있는 파일(CSV, XLSX 등)을 반환하여 작업 분해를 자동화하고 수작업 부담을 줄여줍니다.

## **사용자 작업 분해 API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/task/decompose
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### **요청 매개변수:**

| 매개변수 이름     | 유형     | 위치   | 필수/선택적 | 설명                                                                                                                                                                                                                              |
| :-------------- | :----- | :------- | :---------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TaskDescription | string | Body     | 필수          | 사용자의 전체 목표에 대한 일반 텍스트 설명입니다. 서비스는 이 설명을 분석해 개별 작업을 생성합니다. 예: “제3분기(Q3) 마케팅 캠페인을 실행합니다. 콘텐츠 제작, 이메일 블라스트, 소셜 미디어 광고 포함.” |

### **응답**

성공 응답(200 OK)  
Content‑Type: `application/octet-stream` (이진 파일 스트림)

헤더:

- `Content-Disposition: attachment; filename="DecomposedTaskPlan.xlsx"`
- `Content-Length: <size in bytes>`

XLSX/ODS 형식의 경우에도 동일한 구조를 사용하며, 열은 첫 번째 워크시트에 배치됩니다.

**HTTP 상태 코드**

| 코드 | 의미                   | 설명                                                           |
| ---- | --------------------- | ------------------------------------------------------------- |
| 200  | OK (성공)             | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.        |
| 400  | 잘못된 요청(Bad Request) | 누락되었거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 형식) |
| 401  | 인증되지 않음(Unauthorized) | 잘못되거나 누락된 JWT 토큰                                     |
| 413  | 요청 페이로드가 너무 큼(Payload Too Large) | 업로드된 파일이 크기 제한을 초과함                             |
| 500  | 내부 서버 오류(Internal Server Error) | 예기치 않은 서버 오류 발생                                      |

**오류 응답 예시(400 Bad Request)**

```json
{
  "code": "InvalidParameter",
  "message": "'TaskDescription' 필드는 필수이며 비워둘 수 없습니다."
}
```

**요청 본문 예시(JSON)**

```json
{
  "TaskDescription": "기존 시스템에 작업 분할 기능을 위한 웹 API를 개발합니다."
}
```

**응답 예시**  
API는 생성된 파일을 포함한 이진 스트림을 반환합니다. CSV 응답의 처음 몇 줄을 미리 보려면 스트림을 디코딩한 뒤 헤더 행을 확인하면 됩니다. 예:

```
ID,Subject,Trucker,Estimated Duration,Description
1	작업 분할 API 요구사항 수집	Business Analyst	8	새로운 작업 분할 엔드포인트에 대한 기능 및 비기능 요구사항, 사용자 스토리, 수용 기준을 수집합니다.
2	API 사양(OpenAPI)	Business Analyst	6	POST /tasks/split에 대한 OpenAPI 계약을 정의합니다. 요청 스키마, 응답 형식, 오류 코드, 보안 요구사항 포함.
3	분할 알고리즘 및 데이터 모델 설계	Solution Architect	5	부모 작업을 하위 작업으로 분할하는 핵심 알고리즘을 설계하고, 계층 구조 및 메타데이터를 저장하기 위해 데이터 모델(DB 테이블/엔티티)을 확장합니다.
4	아키텍처 통합 검토	Solution Architect	4	기존 서비스, 이벤트 흐름, 데이터베이스 마이그레이션에 미치는 영향을 분석하고 통합 계획을 작성합니다.
...
```

## 사용자 작업 분해 API는 어디에 사용해야 하나요?

- **프로젝트 시작**: 고수준 프로젝트 개요를 시간 추정이 포함된 Redmine 호환 작업 목록으로 변환해 즉각적인 스프린트 계획을 가능하게 합니다.
- **마케팅 자동화**: 캠페인 목표를 실행 가능한 단계로 분해해 CSV로 내보내고, 작업 관리 도구로 가져와 팀 간 협업을 촉진합니다.
- **자원 배분**: 각 하위 작업에 대한 시간 기준 추정치를 생성해 프로젝트 시작 전 팀원 간 업무 부하를 균형 있게 조정할 수 있습니다.
- **마일스톤 추적**: Gantt 차트 도구와 동기화 가능한 마일스톤 노드를 자동 생성해 각 단계가 명확한 산출물을 갖도록 보장합니다.

## 왜 사용자 작업 분해 API를 사용해야 하나요?

- **SMART 준수 결과물**: 생성된 각 작업이 구체적(Specific), 측정 가능(Measurable), 달성 가능(Achievable), 관련성 있음(Relevant), 기한 명확(Time-bound) 조건을 충족합니다.
- **내장된 시간 기준 추정 기능**: 수동 계산이 필요 없어 예측 정확도가 향상됩니다.
- **즉시 사용 가능한 가져오기 파일 형식**(CSV, XLSX 등): Redmine, Jira, Azure DevOps 및 기타 프로젝트 관리 플랫폼과의 통합이 용이합니다.
- **단일 요청 자동화**: 단일 요청으로 작업 분해를 수행해 프로젝트 시작을 가속화하고 수작업을 최소화합니다.

## SDK를 활용해 사용자 작업 분해 API 사용하기

### 사용자 작업 분해 API 사양

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/DecomposeUserTask" target="_blank" rel="noopener noreferrer">사용자 작업 분해 API 사양</a>은 웹 브라우저에서 직접 REST 상호 작용을 실행할 수 있는 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공합니다.

## Excel API SDK

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 저수준 세부 사항을 추상화해 간결한 코드로 DecomposeUserTask 엔드포인트를 호출할 수 있어 개발 속도가 가장 빠릅니다.  
Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.  
다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스와 상호 작용하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_DecomposeUserTask.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_DecomposeUserTask.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_DecomposeUserTask.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_DecomposeUserTask.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_DecomposeUserTask.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_DecomposeUserTask.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_DecomposeUserTask.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_DecomposeUserTask.go" >}}
{{</tab>}}
{{< /tabs >}}

---