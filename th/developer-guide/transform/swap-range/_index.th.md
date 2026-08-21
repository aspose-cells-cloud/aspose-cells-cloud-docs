---
title: "Aspose.Cells Cloud – สลับคอลัมน์ แถว และช่วงข้อมูล (v4.0)"
second_title: "เอกสาร"
ArticleTitle: "สลับ/แลกเปลี่ยนข้อมูลระหว่างคอลัมน์ แถว และเซลล์ใน Excel"
linktitle: "สลับช่วงข้อมูล"
type: docs
url: /swap-range/
keywords: "Aspose Cells, Excel API, สลับช่วงข้อมูล, สเปรดชีตบนคลาวด์"
description: "สลับคอลัมน์ แถว หรือช่วงข้อมูลในไฟล์ Excel โดยใช้ Aspose.Cells Cloud API รักษาการจัดรูปแบบ สูตร และการอ้างอิงเซลล์ไว้ในการเรียกใช้งานเพียงครั้งเดียว"
weight: 100
---

สลับข้อมูลระหว่างคอลัมน์ แถว ช่วงข้อมูล หรือเซลล์ใดๆ ในไฟล์ Excel โดยใช้ Aspose.Cells Cloud API ฟังก์ชัน Swap Range API ช่วยให้การสลับข้อมูลแม่นยำโดยรักษาการจัดรูปแบบ สูตร และการอ้างอิงเซลล์ทั้งหมดไว้ รองรับการจัดระเบียบข้อมูลที่ซับซ้อน การประมวลผลแบบแบตช์ และการผสานรวมบนคลาวด์อย่างราบรื่นสำหรับกระบวนการทำงานในองค์กร

## **Swap Range API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/swap/range
```

### **การรักษาความปลอดภัยและการตรวจสอบสิทธิ์**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วย JWT token</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์   | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                                                                     |
| ----------------- | ---------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**   | ไฟล์       | FormData | **จำเป็น** ไฟล์สมุดงาน Excel ต้นทาง (`.xlsx`, `.xls`)                                                                                       |
| **worksheet1**    | สตริง       | Query    | **จำเป็น** ชื่อแผ่นงานที่มีพื้นที่ข้อมูลแรก                                                                                    |
| **range1**        | สตริง       | Query    | **จำเป็น** ช่วงเซลล์ (เช่น `A1:D10`) ใน `worksheet1` ที่จะถูกสลับ                                                                   |
| **worksheet2**    | สตริง       | Query    | **จำเป็น** ชื่อแผ่นงานที่มีพื้นที่ข้อมูลที่สอง (อาจเป็นแผ่นงานเดียวกับ `worksheet1`)                                          |
| **range2**        | สตริง       | Query    | **จำเป็น** ช่วงเซลล์ (เช่น `F1:I10`) ใน `worksheet2` ที่จะถูกสลับ **สำคัญ:** `range1` และ `range2` ต้องมีขนาดเท่ากันทุกประการ |
| **outPath**       | สตริง       | Query    | **ไม่บังคับ** โฟลเดอร์ในพื้นที่จัดเก็บบนคลาวด์ที่จะบันทึกสมุดงานที่แก้ไขแล้ว                                                             |
| **outStorageName**| สตริง       | Query    | **จำเป็น** ชื่อของบริการพื้นที่จัดเก็บบนคลาวด์ที่กำหนดค่าไว้ (เช่น `MyCompanyStorage`)                                                    |
| **region**        | สตริง       | Query    | **ไม่บังคับ** การตั้งค่าภาษา和地区 (เช่น `en-US`, `ja-JP`) ซึ่งอาจมีผลต่อการจัดรูปแบบ                                                  |
| **password**      | สตริง       | Query    | **ไม่บังคับ** รหัสผ่านเพื่อถอดรหัสสมุดงานที่ได้รับการป้องกัน ไม่ต้องระบุหากไม่ได้เข้ารหัส                                                      |

**ตัวอย่างคำขอ (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/swap/range?worksheet1=Sheet1&range1=A1:D10&worksheet2=Sheet2&range2=F1:I10&outStorageName=MyCompanyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### **การตอบกลับ**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**หมายเหตุ:**  
- API จะส่งสมุดงานที่แก้ไขแล้วกลับมาในรูปแบบสตรีมไฟล์ หากกำหนดค่า `outPath` ไฟล์จะถูกบันทึกไว้ที่ตำแหน่งพื้นที่จัดเก็บบนคลาวด์ที่กำหนดด้วย  
- หากขนาดของช่วงข้อมูลไม่ตรงกัน จะเกิดข้อผิดพลาด **400 Bad Request**

### รหัสข้อผิดพลาด

| รหัส                 | คำอธิบาย                                                                    |
| -------------------- | --------------------------------------------------------------------------- |
| **400 Bad Request**  | URI ของคำขอไม่ถูกต้อง หรือขนาดของช่วงข้อมูลไม่ตรงกัน                            |
| **401 Unauthorized** | Token การเข้าถึงไม่ถูกต้องหรือหมดอาย หรือ client-id/secret ไม่ถูกต้อง              |
| **404 Not Found**    | ไม่สามารถเข้าถึงไฟล์สมุดงานที่ระบุได้                                        |
| **500 Server Error** | เกิดข้อผิดพลาดภายในระหว่างประมวลผลสมุดงาน                                  |

## ควรใช้ Swap Range API ในกรณีใด?

- **การปรับโครงสร้างแบบจำลองทางการเงิน** – จัดระเบียบบล็อกข้อมูลใหม่ (เช่น ย้ายการพยากรณ์ไตรมาส 3 ไปยังไตรมาส 4) โดยรักษาสูตรและการจัดรูปแบบแบบเงื่อนไขไว้
- **กระบวนการ ETL และ Data Pipeline** – สลับช่วงข้อมูลดิบกับช่วงข้อมูลที่ผ่านการปรับปรุงแล้วในแผ่นงานชั่วคราวก่อนสร้างผลลัพธ์สุดท้าย
- **การแก้ไขข้อผิดพลาดและการกู้คืนข้อมูล** – แก้ไขข้อมูลที่วางผิดตำแหน่งอย่างรวดเร็วโดยไม่ต้องคัดลอกและวางด้วยตนเอง

## ทำไมควรใช้ Swap Range API?

- **เป็นมิตรกับนักพัฒนา** – มี SDK สำหรับภาษาโปรแกรมหลายภาษา ลดความพยายามในการพัฒนาเมื่อเทียบกับการสร้างโซลูชันแบบกำหนดเอง
- **ลดต้นทุนแรงงาน** – ทำให้การจัดเรียงข้อมูลอัตโนมัติ ลดความจำเป็นในการรวมข้อมูลด้วยตนเอง
- **จ่ายตามการใช้งานจริง** – จ่ายเฉพาะค่า API calls ที่เรียกใช้งานจริงเท่านั้น
- **ไม่ต้องดูแลรักษา** – ไม่มีเซิร์ฟเวอร์ให้จัดการ ไม่มีการอัปเดตซอฟต์แวร์ และไม่มีปัญหาเรื่องความเข้ากันได้

## วิธีใช้ Swap Range API ด้วย SDK

### ข้อมูลจำเพาะ Swap Range API

[ข้อมูลจำเพาะ Swap Range API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/SwapRange) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการ REST interactions โดยตรงจากเว็บเบราว์เซอร์

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจาก SDK ซ่อนรายละเอียดระดับต่ำไว้ ช่วยให้คุณสลับช่วงข้อมูลได้ด้วยโค้ดที่กระชับ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{</tab>}}
{{< /tabs >}}
---