---
title: "การทำงานกับรูปภาพใน Excel"
second_title: "เอกสาร"
linktype: "รูปภาพ"
type: docs
url: /th/pictures/
aliases: [  /th/working-with-pictures/ ]
keywords: "Excel, รูปภาพ, Aspose.Cells Cloud, REST API, การจัดการภาพ, รูปภาพใน Excel"
description: "เรียนรู้วิธีการดึงข้อมูล เพิ่ม แก้ไข และลบภาพในแผ่นงาน Excel ผ่าน REST API ของ Aspose.Cells Cloud มีตัวอย่างโค้ดสำหรับ C#, Java, Python และภาษาอื่นๆ"
weight: 100
ArticleTitle: "การทำงานกับรูปภาพใน Excel – เอกสารประกอบของ Aspose.Cells Cloud"
---

## การทำงานกับรูปภาพในไฟล์ Excel

คู่มือนี้อธิบายวิธีการใช้งาน **รูปภาพ** (หรือที่เรียกว่าภาพ) ในแผ่นงาน Excel ผ่าน REST API ของ Aspose.Cells Cloud โดยครอบคลุมการดำเนินการหลักที่เกี่ยวข้องกับรูปภาพ ได้แก่ การดึงข้อมูล การเพิ่ม การแก้ไข และการลบรูปภาพใน Excel พร้อมลิงก์ไปยังตัวอย่างรายละเอียดสำหรับแต่ละงาน

**ข้อกำหนดเบื้องต้น**: บัญชี Aspose.Cells Cloud, API key ที่ถูกต้อง และ SDK ที่เหมาะสมซึ่งติดตั้งไว้แล้วสำหรับภาษาที่คุณเลือก

- [วิธีการดึงรูปภาพในรูปแบบที่ระบุจากแผ่นงาน Excel](/cells/pictures/get/) – ดึงรูปภาพเดียวในรูปแบบที่ร้องขอ (PNG, JPEG เป็นต้น) จากแผ่นงาน  
- [วิธีการดึงข้อมูลรูปภาพทั้งหมดจากแผ่นงาน Excel](/cells/pictures/get-all/) | แสดงรายการข้อมูลเมตาของรูปภาพทุกรูปที่มีอยู่ในแผ่นงาน  
- [วิธีการเพิ่มรูปภาพลงในแผ่นงาน Excel](/cells/pictures/add/) – แทรกรูปภาพใหม่ลงในแผ่นงาน โดยระบุตำแหน่งและขนาดของรูปภาพ  
- [วิธีการแก้ไขรูปภาพที่ระบุจากแผ่นงาน Excel](/cells/pictures/update/) – แก้ไขคุณสมบัติของรูปภาพที่มีอยู่ (เช่น มิติ ตำแหน่งที่วาง)  
- [วิธีการลบรูปภาพทั้งหมดจากแผ่นงาน Excel](/cells/pictures/clear/) – ลบวัตถุรูปภาพทั้งหมดออกจากแผ่นงานด้วยคำขอเพียงครั้งเดียว  
- [วิธีการลบรูปภาพเดียวจากแผ่นงาน Excel](/cells/pictures/delete/) – ลบรูปภาพเดียวที่ระบุด้วยดัชนีของรูปภาพ  

**การอ้างอิง API**

**ดึงรูปภาพในรูปแบบที่ระบุ**

| วิธี HTTP | เอ็นพอยน์ท์ | พารามิเตอร์ที่จำเป็น | ตัวอย่างคำขอ | ตัวอย่างคำตอบ | โค้ดสถานะ |
|-----------|------------|---------------------|--------------|---------------|-----------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (path), `sheetName` (path), `pictureIndex` (path), `format` (query) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/0?format=png` | ข้อมูลภาพแบบไบนารี (PNG, JPEG เป็นต้น) | 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Server Error |

**ดึงข้อมูลรูปภาพทั้งหมด**

| วิธี HTTP | เอ็นพอยน์ท์ | พารามิเตอร์ที่จำเป็น | ตัวอย่างคำขอ | ตัวอย่างคำตอบ | โค้ดสถานะ |
|-----------|------------|---------------------|--------------|---------------|-----------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (path), `sheetName` (path) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | อาเรย์ JSON ที่มีข้อมูลเมตาของรูปภาพ (ดัชนี ชื่อ ตำแหน่ง ขนาด) | 200 OK, 400, 401, 404, 500 |

**เพิ่มรูปภาพ**

| วิธี HTTP | เอ็นพอยน์ท์ | พารามิเตอร์ที่จำเป็น | เนื้อหาคำขอตัวอย่าง | ตัวอย่างคำตอบ | โค้ดสถานะ |
|-----------|------------|---------------------|---------------------|---------------|-----------|
| POST | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (path), `sheetName` (path) | `{ "image": "<base64‑encoded‑image>", "upperLeftRow": 5, "upperLeftColumn": 2, "width": 200, "height": 150 }` | `{ "code": 200, "status": "OK", "pictureIndex": 3 }` | 201 Created, 400, 401, 404, 500 |

**แก้ไขรูปภาพ**

| วิธี HTTP | เอ็นพอยน์ท์ | พารามิเตอร์ที่จำเป็น | เนื้อหาคำขอตัวอย่าง | ตัวอย่างคำตอบ | โค้ดสถานะ |
|-----------|------------|---------------------|---------------------|---------------|-----------|
| PUT | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (path), `sheetName` (path), `pictureIndex` (path) | `{ "upperLeftRow": 10, "upperLeftColumn": 4, "width": 300, "height": 250 }` | `{ "code": 200, "status": "OK" }` | 200 OK, 400, 401, 404, 500 |

**ลบรูปภาพทั้งหมด**

| วิธี HTTP | เอ็นพอยน์ท์ | พารามิเตอร์ที่จำเป็น | ตัวอย่างคำขอ | ตัวอย่างคำตอบ | โค้ดสถานะ |
|-----------|------------|---------------------|--------------|---------------|-----------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (path), `sheetName` (path) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | `{ "code": 200, "status": "All pictures deleted." }` | 200 OK, 400, 401, 404, 500 |

**ลบรูปภาพที่ระบุ**

| วิธี HTTP | เอ็นพอยน์ท์ | พารามิเตอร์ที่จำเป็น | ตัวอย่างคำขอ | ตัวอย่างคำตอบ | โค้ดสถานะ |
|-----------|------------|---------------------|--------------|---------------|-----------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (path), `sheetName` (path), `pictureIndex` (path) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/2` | `{ "code": 200, "status": "Picture deleted." }` | 200 OK, 400, 401, 404, 500 |

**หัวข้อที่เกี่ยวข้อง**

สำรวจการดำเนินการที่เกี่ยวข้องกับภาพอื่นๆ ใน Aspose.Cells Cloud:  
- [การทำงานกับรูปร่าง](/cells/shapes/) – เพิ่ม แก้ไข และลบรูปร่างวาด  
- [การทำงานกับกราฟ](/cells/charts/) – สร้างและจัดการวัตถุกราฟ  
- [การทำงานกับภาพในแผ่นงาน](/cells/images/) – ฝังและจัดการไฟล์ภาพดิบ  

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "การทำงานกับรูปภาพใน Excel – เอกสารประกอบของ Aspose.Cells Cloud",
  "description": "คู่มือสำหรับการดึงข้อมูล เพิ่ม แก้ไข และลบรูปภาพใน Excel ผ่าน REST API ของ Aspose.Cells Cloud",
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
  "keywords": "รูปภาพ Excel, Aspose.Cells Cloud, REST API, การจัดการภาพ",
  "url": "https://docs.aspose.cloud/cells/pictures/"
}
</script>