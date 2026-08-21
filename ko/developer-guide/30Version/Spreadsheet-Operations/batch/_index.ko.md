---
title: "Excel 파일 일괄 처리: 변환, 잠금, 보호, 분할, 잠금 해제"
second_title: "문서"
linktype: "Excel 파일 일괄 처리"
type: docs
url: /ko/batch/
keywords: "일괄 처리, Excel, 변환, 잠금, 보호, 분할, 잠금 해제, Aspose.Cells Cloud API, API 참조, 일괄 작업"
description: "Aspose.Cells Cloud API를 사용하면 여러 Excel 파일을 일괄적으로 변환, 잠금, 보호, 분할, 잠금 해제할 수 있습니다. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, Swift를 위한 자세한 API 사양 및 SDK 지원을 제공합니다."
weight: 35
ArticleTitle: "Excel 파일 일괄 처리 – Aspose.Cells Cloud API를 사용하여 변환, 잠금, 보호, 분할, 잠금 해제"
---

Aspose.Cells Cloud API는 여러 Excel 파일에 대해 단일 요청으로 일반적인 작업을 수행할 수 있는 일괄 처리 엔드포인트를 제공합니다. 아래는 사용 가능한 일괄 처리 작업의 간략한 개요와 각 작업에 대한 간결한 API 사양입니다.

- **["Excel 파일 일괄 변환"](https://docs.aspose.cloud/cells/batch/convert "Excel 파일 일괄 변환")**  
  *단일 요청으로 여러 Excel 파일을 선택한 출력 형식으로 변환합니다.*  

  **API 세부 정보**  
  ```http
  POST /cells/batch/convert
  Content-Type: multipart/form-data
  Authorization: Bearer {access_token}
  ```  

  **파라미터**  

  | 이름           | 유형      | 설명                                    |
  |---------------|----------|-------------------------------------------|
  | files         | file[]   | 변환할 하나 이상의 Excel 파일.            |
  | outputFormat  | string   | 원하는 출력 형식 (예: pdf, csv, html).    |
  | storage       | string   | (선택 사항) 클라우드 스토리지 이름.        |

  **응답 코드**  

  | 코드 | 설명                                      |
  |------|---------------------------------------------|
  | 200  | 변환 성공; 파일 반환.                      |
  | 400  | 잘못된 파라미터가 제공되었습니다.           |
  | 401  | 인증되지 않음 – 토큰 누락 또는 잘못됨.      |
  | 500  | 내부 서버 오류.                             |

- **["Excel 파일 일괄 잠금"](https://docs.aspose.cloud/cells/batch/lock "Excel 파일 일괄 잠금")**  
  *여러 Excel 파일에 동시에 비밀번호로 잠금을 적용합니다.*  

  **API 세부 정보**  
  ```http
  POST /cells/batch/lock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **파라미터**  

  | 이름     | 유형   | 설명                              |
  |----------|--------|-------------------------------------|
  | files    | array  | 파일 식별자 또는 URL의 목록.        |
  | password | string | 워크북에 적용할 비밀번호.           |
  | storage  | string | (선택 사항) 클라우드 스토리지 이름.  |

  **응답 코드**  

  | 코드 | 설명                                      |
  |------|---------------------------------------------|
  | 200  | 파일 잠금 성공.                             |
  | 400  | 누락되거나 잘못된 파라미터.                 |
  | 401  | 인증되지 않은 접근.                         |
  | 500  | 서버 오류.                                  |

- **["Excel 파일 일괄 보호"](https://docs.aspose.cloud/cells/batch/protect "Excel 파일 일괄 보호")**  
  *여러 워크북에 보호 설정(예: 읽기 전용, 구조)을 추가합니다.*  

  **API 세부 정보**  
  ```http
  POST /cells/batch/protect
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **파라미터**  

  | 이름          | 유형   | 설명                                          |
  |---------------|--------|-----------------------------------------------|
  | files         | array  | 파일 식별자 또는 URL의 목록.                  |
  | protection    | object | 보호 옵션 (예: readOnly, structure).         |
  | storage       | string | (선택 사항) 클라우드 스토리지 이름.            |

  **응답 코드**  

  | 코드 | 설명                                      |
  |------|---------------------------------------------|
  | 200  | 보호 적용 성공.                             |
  | 400  | 잘못된 요청 데이터.                         |
  | 401  | 인증 실패.                                  |
  | 500  | 예기치 않은 서버 오류.                       |

- **["일괄 분할"](https://docs.aspose.cloud/cells/batch/split "일괄 분할")**  
  *워크시트 또는 행 범위를 기준으로 큰 Excel 워크북을 작은 파일들로 분할합니다.*  

  **API 세부 정보**  
  ```http
  POST /cells/batch/split
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **파라미터**  

  | 이름        | 유형   | 설명                                      |
  |-------------|--------|-------------------------------------------|
  | files       | array  | 분할할 파일.                              |
  | splitBy     | string | 기준: "worksheet" 또는 "rowRange".        |
  | criteria    | object | 선택된 분할 방식에 대한 세부 정보.         |
  | storage     | string | (선택 사항) 클라우드 스토리지 이름.        |

  **응답 코드**  

  | 코드 | 설명                                      |
  |------|---------------------------------------------|
  | 200  | 분할 작업 완료; 분할된 파트 반환.           |
  | 400  | 잘못된 분할 파라미터.                      |
  | 401  | 인증되지 않은 요청.                         |
  | 500  | 처리 오류.                                  |

- **["일괄 잠금 해제"](https://docs.aspose.cloud/cells/batch/unlock "일괄 잠금 해제")**  
  *단일 호출로 여러 Excel 파일의 비밀번호 보호를 제거합니다.*  

  **API 세부 정보**  
  ```http
  POST /cells/batch/unlock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **파라미터**  

  | 이름     | 유형   | 설명                              |
  |----------|--------|-------------------------------------|
  | files    | array  | 잠긴 파일 식별자 또는 URL의 목록.   |
  | password | string | 파일의 현재 비밀번호.               |
  | storage  | string | (선택 사항) 클라우드 스토리지 이름.  |

  **응답 코드**  

  | 코드 | 설명                                      |
  |------|---------------------------------------------|
  | 200  | 파일 잠금 해제 성공.                        |
  | 400  | 잘못된 비밀번호 또는 누락된 파일.           |
  | 401  | 인증되지 않은 접근.                         |
  | 500  | 서버 측 실패.                               |
---