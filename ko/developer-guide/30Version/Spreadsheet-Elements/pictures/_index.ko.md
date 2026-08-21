---
title: "Excel 그림 작업"
second_title: "문서"
linktype: "그림"
type: docs
url: /pictures/
aliases: [/working-with-pictures/]
keywords: "Excel, 그림, Aspose.Cells Cloud, REST API, 이미지 처리, Excel 그림"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 그림을 검색, 추가, 업데이트 및 삭제하는 방법을 알아보세요. C#, Java, Python 등 다양한 언어의 코드 예제가 포함되어 있습니다."
weight: 100
ArticleTitle: "Excel 그림 작업 – Aspose.Cells Cloud 문서"
---

## Excel 파일의 그림 작업하기

이 가이드에서는 Aspose.Cells Cloud REST API를 통해 Excel 워크시트에서 **그림**(이미지라고도 함)을 다루는 방법을 설명합니다. 주요 그림 관련 작업인 Excel 그림의 검색, 추가, 업데이트 및 삭제 작업을 다루며, 각 작업에 대한 자세한 예제로 연결합니다.

**사전 요구 사항**: Aspose.Cells Cloud 계정, 유효한 API 키, 선택한 언어에 적합한 SDK 설치.

- [Excel 워크시트에서 특정 형식의 그림을 가져오는 방법](/cells/pictures/get/) – 워크시트에서 요청한 형식(PNG, JPEG 등)의 단일 그림을 검색합니다.  
- [Excel 워크시트에서 모든 그림 정보를 가져오는 방법](/cells/pictures/get-all/) – 워크시트에 포함된 모든 그림에 대한 메타데이터를 나열합니다.  
- [Excel 워크시트에 그림을 추가하는 방법](/cells/pictures/add/) – 워크시트에 새 그림을 삽입하고 위치 및 크기를 지정합니다.  
- [Excel 워크시트에서 특정 그림을 업데이트하는 방법](/cells/pictures/update/) – 기존 그림의 속성(예: 치수, 배치)을 수정합니다.  
- [Excel 워크시트에서 모든 그림을 삭제하는 방법](/cells/pictures/clear/) – 단일 요청으로 워크시트에서 모든 그림 개체를 제거합니다.  
- [Excel 워크시트에서 그림을 삭제하는 방법](/cells/pictures/delete/) – 인덱스로 식별된 단일 그림을 삭제합니다.  

**API 참조**

**특정 형식의 그림 가져오기**  

| HTTP 메서드 | 엔드포인트 | 필수 매개변수 | 샘플 요청 | 샘플 응답 | 상태 코드 |
|-------------|----------|---------------------|----------------|----------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName`(경로), `sheetName`(경로), `pictureIndex`(경로), `format`(쿼리) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/0?format=png` | 바이너리 이미지 데이터(PNG, JPEG 등) | 200 OK, 400 잘못된 요청, 401 인증되지 않음, 404 찾을 수 없음, 500 서버 오류 |

**모든 그림 정보 가져오기**  

| HTTP 메서드 | 엔드포인트 | 필수 매개변수 | 샘플 요청 | 샘플 응답 | 상태 코드 |
|-------------|----------|---------------------|----------------|----------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName`(경로), `sheetName`(경로) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | 그림 메타데이터(JSON 배열, 인덱스, 이름, 위치, 크기 포함) | 200 OK, 400, 401, 404, 500 |

**그림 추가**  

| HTTP 메서드 | 엔드포인트 | 필수 매개변수 | 샘플 요청 본문 | 샘플 응답 | 상태 코드 |
|-------------|----------|---------------------|---------------------|----------------|--------------|
| POST | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName`(경로), `sheetName`(경로) | `{ "image": "<base64-인코딩된-이미지>", "upperLeftRow": 5, "upperLeftColumn": 2, "width": 200, "height": 150 }` | `{ "code": 200, "status": "OK", "pictureIndex": 3 }` | 201 생성됨, 400, 401, 404, 500 |

**그림 업데이트**  

| HTTP 메서드 | 엔드포인트 | 필수 매개변수 | 샘플 요청 본문 | 샘플 응답 | 상태 코드 |
|-------------|----------|---------------------|---------------------|----------------|--------------|
| PUT | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName`(경로), `sheetName`(경로), `pictureIndex`(경로) | `{ "upperLeftRow": 10, "upperLeftColumn": 4, "width": 300, "height": 250 }` | `{ "code": 200, "status": "OK" }` | 200 OK, 400, 401, 404, 500 |

**모든 그림 삭제**  

| HTTP 메서드 | 엔드포인트 | 필수 매개변수 | 샘플 요청 | 샘플 응답 | 상태 코드 |
|-------------|----------|---------------------|----------------|----------------|--------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName`(경로), `sheetName`(경로) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | `{ "code": 200, "status": "All pictures deleted." }` | 200 OK, 400, 401, 404, 500 |

**특정 그림 삭제**  

| HTTP 메서드 | 엔드포인트 | 필수 매개변수 | 샘플 요청 | 샘플 응답 | 상태 코드 |
|-------------|----------|---------------------|----------------|----------------|--------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName`(경로), `sheetName`(경로), `pictureIndex`(경로) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/2` | `{ "code": 200, "status": "Picture deleted." }` | 200 OK, 400, 401, 404, 500 |

**관련 주제**

Aspose.Cells Cloud에서 이미지 관련 작업을 더 탐색해 보세요:  
- [도형 작업](/cells/shapes/) – 도형 그리기 추가, 편집 및 삭제  
- [차트 작업](/cells/charts/) – 차트 객체 생성 및 조작  
- [워크시트의 이미지 작업](/cells/images/) – 원시 이미지 파일 임베딩 및 관리  

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Excel 그림 작업 – Aspose.Cells Cloud 문서",
  "description": "Aspose.Cells Cloud REST API를 통해 Excel 그림을 검색, 추가, 업데이트 및 삭제하는 가이드.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://cms.admin.containerize.com/templates/asposecloud/images/logo.png"
    }
  },
  "datePublished": "2026-07-30",
  "keywords": "Excel 그림, Aspose.Cells Cloud, REST API, 이미지 처리",
  "url": "https://docs.aspose.cloud/cells/pictures/"
}
</script>