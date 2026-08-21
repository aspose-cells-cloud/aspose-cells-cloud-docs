---
title: "엑셀 OLE 객체 작업하기"
second_title: "문서"
linktitle: "OleObjects"
type: docs
url: /ko/oleobjects/
aliases: [  /ko/working-with-oleobjects/ ]
keywords: "OLE, 엑셀, Aspose.Cells, API, 클라우드"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트의 OLE 객체를 조회, 추가, 업데이트, 삭제 및 변환합니다. Java, .NET, Python, PHP, Ruby, Go, Node.js, Perl, Swift, Android용 SDK가 제공됩니다."
weight: 100
ArticleTitle: "엑셀 OLE 객체 작업하기 – OLE 객체 조회, 추가, 업데이트, 삭제 및 변환 가이드"
---

**엑셀 워크시트에서 OLE 객체를 작업하는 방법**

Aspose.Cells Cloud REST API는 프로그래밍 방식으로 OLE 객체를 관리할 수 있는 완전한 작업 세트를 제공합니다. 아래는 각 작업에 대한 간결한 참고 자료로, HTTP 메서드, 엔드포인트 패턴, 필수 매개변수 및 간단한 예제 응답이 포함되어 있습니다.

- [엑셀 워크시트에서 OLE 객체를 조회하는 방법](/ko/cells/oleobjects/get/)
  - **메서드:** `GET`  
  - **엔드포인트:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **매개변수:** `fileName`(문자열), `sheetName`(문자열), `oleObjectIndex`(정수)  
  - **예제 응답:**  
    ```json
    {
      "OleObject": {
        "Name": "Chart1",
        "ContentType": "image/png",
        "Width": 400,
        "Height": 300
      }
    }
    ```

- [엑셀 워크시트에 OLE 객체를 추가하는 방법](/ko/cells/oleobjects/add/)
  - **메서드:** `POST`  
  - **엔드포인트:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **매개변수:** `fileName`, `sheetName`, `oleObject`(바이너리 또는 base‑64 인코딩), `imageFormat`(선택사항)  
  - **예제 요청 본문:** 파일 스트림을 포함한 multipart/form‑data  
  - **예제 응답:** `201 Created` 상태 코드와 생성된 OLE 객체의 위치 헤더

- [엑셀 워크시트에서 특정 OLE 객체를 업데이트하는 방법](/ko/cells/oleobjects/update/)
  - **메서드:** `PUT`  
  - **엔드포인트:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **매개변수:** `fileName`, `sheetName`, `oleObjectIndex`, `oleObject`(업데이트된 콘텐츠)  
  - **예제 응답:** `200 OK` 상태 코드와 업데이트된 객체 메타데이터

- [엑셀 워크시트의 OLE 객체를 이미지로 변환하는 방법](/ko/cells/oleobjects/convert/)
  - **메서드:** `GET`  
  - **엔드포인트:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}/convert`  
  - **매개변수:** `fileName`, `sheetName`, `oleObjectIndex`, `format`(예: `png`, `jpeg`)  
  - **예제 응답:** 변환된 OLE 객체의 바이너리 이미지 스트림

- [엑셀 워크시트의 모든 OLE 객체를 삭제하는 방법](/ko/cells/oleobjects/clear/)
  - **메서드:** `DELETE`  
  - **엔드포인트:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **매개변수:** `fileName`, `sheetName`  
  - **예제 응답:** `204 No Content` 상태 코드로 모든 OLE 객체가 삭제되었음을 나타냄

- [엑셀 워크시트에서 특정 OLE 객체를 삭제하는 방법](/ko/cells/oleobjects/delete/)
  - **메서드:** `DELETE`  
  - **엔드포인트:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **매개변수:** `fileName`, `sheetName`, `oleObjectIndex`  
  - **예제 응답:** `204 No Content` 상태 코드로 객체가 삭제되었음을 확인
---