---
title: "จัดกลุ่มคอลัมน์ – เอกสารประกอบ API ของ Aspise.Cells Cloud"
description: "จัดกลุ่มคอลัมน์ในแผ่นงาน Excel โดยใช้ REST API ของ Aspose.Cells Cloud (เวอร์ชัน 3.0) รวมถึงไวยากรณ์คำขอ พารามิเตอร์ ตัวอย่าง cURL และ SDK รวมถึงรายละเอียดการตอบกลับ"
keywords: "Aspose.Cells, จัดกลุ่มคอลัมน์, Excel API, REST, cloud SDK"
weight: 60
type: docs
aliases:
  - /group-columns-in-an-excel-worksheet/
  - /group-columns-in-excel-worksheet/
---

# จัดกลุ่มคอลัมน์ในแผ่นงาน Excel

**เวอร์ชัน API:** v3.0  
**การดำเนินการ:** `PostGroupWorksheetColumns` – จัดกลุ่มคอลัมน์ในแผ่นงาน

---

## ภาพรวม

API แบบ REST นี้ช่วยให้คุณจัดกลุ่มช่วงของคอลัมน์ในแผ่นงานได้ คอลัมน์ที่จัดกลุ่มสามารถแสดงหรือซ่อนได้ ทำให้คุณสร้างส่วนที่ย่อ-ขยายได้ คล้ายกับที่พบใน Microsoft Excel

---

## ข้อกำหนดเบื้องต้น

- โทเคน JWT ที่ถูกต้อง ซึ่งได้รับจากบริการยืนยันตัวตนของ Aspose Cloud  
- สมุดงานต้องถูกจัดเก็บไว้ในตำแหน่งที่ Aspose.Cells Cloud เข้าถึงได้ (คือ พื้นที่จัดเก็บเริ่มต้น หรือชื่อพื้นที่จัดเก็บแบบกำหนดเอง)  
- เวอร์ชัน SDK ที่จำเป็น (หากใช้ SDK): เวอร์ชันล่าสุดที่รองรับ API เวอร์ชัน **v3.0**

---

## การยืนยันตัวตน

คำขอทั้งหมดต้องใช้การยืนยันตัวตนด้วย **Bearer token**

```http
Authorization: Bearer <access_token>
```

สำหรับรายละเอียดเกี่ยวกับการรับโทเคน โปรดดูที่ [คู่มือการยืนยันตัวตน JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

---

## คำขอ HTTP

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/group
```

| พารามิเตอร์ | ตำแหน่ง | จำเป็น | คำอธิบาย |
|-----------|----------|----------|-------------|
| `name` | Path | จำเป็น | ชื่อไฟล์สมุดงาน (เช่น `test.xlsx`) |
| `sheetName` | Path | จำเป็น | ชื่อแผ่นงานที่มีคอลัมน์ที่ต้องการจัดกลุ่ม |
| `firstIndex` | Query | จำเป็น | ดัชนีเริ่มต้นของคอลัมน์แรกที่จะรวมในกลุ่ม (เริ่มจาก 0) |
| `lastIndex` | Query | จำเป็น | ดัชนีเริ่มต้นของคอลัมน์สุดท้ายที่จะรวมในกลุ่ม (เริ่มจาก 0) |
| `hide` | Query | ไม่จำเป็น | หากเป็น `true` จะซ่อนคอลัมน์ที่จัดกลุ่มไว้ มิฉะนั้นจะยังคงแสดงคอลัมน์อยู่ |
| `folder` | Query | ไม่จำเป็น | เส้นทางไปยังโฟลเดอร์ที่เก็บสมุดงานไว้ |
| `storageName` | Query | ไม่จำเป็น | ชื่อของบริการพื้นที่จัดเก็บที่ไฟล์นั้นตั้งอยู่ |

---

## ตัวอย่างคำขอ (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/group?firstIndex=1&lastIndex=2&hide=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

> **หมายเหตุ:** คำขอนี้ใช้ **HTTPS** เพื่อให้มั่นใจว่าการสื่อสารนั้นเข้ารหัสอย่างปลอดภัย

---

## การตอบกลับ

### สำเร็จ (200)

| ฟิลด์ | ประเภท | คำอธิบาย |
|--------|---------|-------------|
| `Code` | integer | รหัสสถานะ HTTP (`200`) |
| `Status` | string | สถานะเชิงข้อความของการดำเนินการ (`OK`) |

**ตัวอย่าง**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### ข้อผิดพลาด (เช่น 400 Bad Request)

| ฟิลด์ | ประเภท | คำอธิบาย |
|--------------|---------|-------------|
| `Code` | integer | รหัสสถานะ HTTP (`400`, `401`, `404`, `500`, …) |
| `Status` | string | สถานะเชิงข้อความ (`Error`) |
| `ErrorMessage` | string | คำอธิบายข้อผิดพลาดในรูปแบบที่ผู้อ่านเข้าใจได้ |
| `ErrorCode` | string | ตัวระบุข้อผิดพลาดในเชิงโปรแกรม |

**ตัวอย่าง – Bad Request**

```json
{
  "Code": 400,
  "Status": "Error",
  "ErrorMessage": "ดัชนีคอลัมน์ไม่ถูกต้อง",
  "ErrorCode": "InvalidParameter"
}
```

---

## ตัวอย่าง SDK

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้การดำเนินการ **Group Worksheet Columns** โดยใช้ SDK ที่รองรับ

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

## หมายเหตุเพิ่มเติม

- **พฤติกรรมการจัดกลุ่ม:** API จะสร้างกลุ่มคอลัมน์ที่สามารถขยายหรือย่อได้ใน Excel การตั้งค่า `hide=true` จะย่อกลุ่มทันที  
- **การนับดัชนีเริ่มที่ 0:** ทั้ง `firstIndex` และ `lastIndex` เริ่มนับจาก **0** คอลัมน์แรกในแผ่นงานจึงมีดัชนีเป็น 0  
- **ข้อควรพิจารณาเกี่ยวกับพื้นที่จัดเก็บ:** หากสมุดงานอยู่ในพื้นที่จัดเก็บที่ไม่ใช่ค่าเริ่มต้น คุณต้องระบุพารามิเตอร์คำขอ `folder` และ `storageName` ทั้งสองตัว  

---

## ดูเพิ่มเติม

- [การยืนยันตัวตน – ใช้โทเคน JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [ข้อมูลจำเพาะ OpenAPI สำหรับการจัดกลุ่มคอลัมน์ในแผ่นงาน](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetColumns)  
- [SDK ของ Aspose.Cells Cloud (GitHub)](https://github.com/aspose-cells-cloud)  
- [จัดกลุ่มแถวในแผ่นงาน Excel](/rows/group/)  

---

> *รูปภาพประกอบ:* ![ภาพหน้าจอแสดงคอลัมน์ที่จัดกลุ่มในแผ่นงาน Excel](./images/group-columns.png){: .img-fluid alt="ภาพหน้าจอแสดงคอลัมน์ที่จัดกลุ่มในแผ่นงาน Excel" }

*รูปภาพตัวอย่างข้างต้นควรถูกแทนที่ด้วยภาพหน้าจอจริงที่แสดงผลลัพธ์เชิงภาพของการจัดกลุ่มคอลัมน์*