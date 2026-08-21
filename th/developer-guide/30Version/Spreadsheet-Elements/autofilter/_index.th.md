---
title: "การใช้งานตัวกรองอัตโนมัติของ Excel"
second_title: "เอกสาร"
linktype: "AutoFilter"
type: docs
url: /th/autofilter/
aliases: [/working-with-autofilter/]
keywords: "AutoFilter, Aspose.Cells Cloud, ตัวกรอง Excel, ตัวกรองสี, ตัวกรองวันที่, ตัวกรองแบบไดนามิก, ตัวกรองตัวเลข, ตัวกรองข้อความ, ตัวกรองช่องว่าง, ตัวกรองแบบกำหนดเอง"
description: "เรียนรู้วิธีเพิ่ม แก้ไข และลบตัวกรองอัตโนมัติของ Excel (สี วันที่ ไดนามิก ตัวเลข ข้อความ ช่องว่าง) โดยใช้ API ของ Aspose.Cells Cloud พร้อมตัวอย่างโค้ดในหลายภาษา"
weight: 100
ArticleTitle: "การใช้งานตัวกรองอัตโนมัติของ Excel – เอกสาร Aspose.Cells Cloud"
---

ตัวกรองอัตโนมัติ (AutoFilter) เป็นวิธีที่รวดเร็วที่สุดในการแสดงเฉพาะรายการที่คุณต้องการจากแผ่นงาน โดยคุณลักษณะนี้ช่วยให้ผู้ใช้สามารถกรองข้อมูลในรายการตามเกณฑ์ที่กำหนดไว้—ไม่ว่าจะเป็นข้อความ ตัวเลข หรือวันที่

**ประเภทของตัวกรองที่แตกต่างกัน**

Aspose.Cells Cloud มี API หลายตัวให้ใช้งานเพื่อใช้ตัวกรองประเภทต่างๆ เช่น ตัวกรองสีพื้นหลัง (Color Filter) ตัวกรองวันที่ (Date Filter) ตัวกรองตัวเลข (Number Filter) ตัวกรองข้อความ (Text Filter) ตัวกรองช่องว่าง (Blank Filter) และตัวกรองไม่ใช่ช่องว่าง (Non‑Blank Filter)

<table class="table table-striped">
  <tr>
    <td class="col-md-2"><strong>สีพื้นหลัง</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud มี <a href="/th/cells/autofilter/add-color-filter/">API สำหรับเพิ่มตัวกรองสีพื้นหลัง</a> เพื่อกรองข้อมูลตามคุณสมบัติสีพื้นหลังของเซลล์</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>วันที่</strong></td>
    <td class="col-md-10">
      <p>สามารถใช้ตัวกรองวันที่ได้หลายแบบ เช่น กรองแถวที่มีวันที่ในเดือนมกราคม ค.ศ. 2018 ใช้ <a href="/th/cells/autofilter/add-date-filter/">API สำหรับเพิ่มตัวกรองวันที่</a> เพื่อเพิ่มตัวกรองวันที่</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>วันที่แบบไดนามิก</strong></td>
    <td class="col-md-10">
      <p>ตัวกรองวันที่แบบไดนามิกช่วยให้คุณกรองเซลล์ที่อยู่ในเดือนที่ระบุโดยไม่สนใจปี (เช่น วันที่ทั้งหมดในเดือนมกราคม) ดูที่ <a href="/th/cells/autofilter/add-dynamic-filter/">API สำหรับตัวกรองแบบไดนามิก</a></p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>ตัวเลข</strong></td>
    <td class="col-md-10">
      <p><a href="/th/cells/autofilter/add-filter/">API ตัวกรองแบบกำหนดเอง</a> ช่วยให้คุณกรองเซลล์ที่มีค่าตัวเลขอยู่ในช่วงที่กำหนดไว้</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>ข้อความ</strong></td>
    <td class="col-md-10">
      <p>หากคอลัมน์มีข้อความ คุณสามารถเลือกเซลล์ที่มีสตริงที่ระบุโดยใช้ <a href="/th/cells/autofilter/add-filter/">API สำหรับเพิ่มตัวกรอง</a></p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>ช่องว่าง</strong></td>
    <td class="col-md-10">
      <p>หากต้องการดึงแถวที่คอลัมน์ว่างเปล่า ให้ใช้ <a href="/th/cells/autofilter/match-all-blank/">API สำหรับจับคู่เซลล์ที่ว่างทั้งหมด</a></p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>ไม่ใช่ช่องว่าง</strong></td>
    <td class="col-md-10">
      <p>หากต้องการกรองแถวที่คอลัมน์มีค่าที่ไม่ว่างเปล่า ให้ใช้ <a href="/th/cells/autofilter/match-all-non-blank/">API สำหรับจับคู่เซลล์ที่ไม่ว่างทั้งหมด</a></p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>ตัวกรองแบบกำหนดเอง</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud มี <a href="/th/cells/autofilter/add-custom-filter/">API สำหรับตัวกรองแบบกำหนดเอง</a> เพื่อใช้ในสถานการณ์ขั้นสูง เช่น กรองแถวที่มีสตริงย่อยที่ระบุ หรือที่ขึ้นต้น/ลงท้ายด้วยสตริงเฉพาะ</p>
    </td>
  </tr>
</table>

**การดำเนินการกับตัวกรองอัตโนมัติ**

- [วิธีเพิ่มตัวกรองสีในแผ่นงาน Excel](/th/cells/autofilter/add-color-filter/) – **วิธีการ:** POST, **จุดปลายทาง:** `/cells/autofilter/add-color-filter/`
- [วิธีเพิ่มตัวกรองแบบกำหนดเองในแผ่นงาน Excel](/th/cells/autofilter/add-custom-filter/) – **วิธีการ:** POST, **จุดปลายทาง:** `/cells/autofilter/add-custom-filter/`
- [วิธีเพิ่มตัวกรองวันที่ในแผ่นงาน Excel](/th/cells/autofilter/add-date-filter/) – **วิธีการ:** POST, **จุดปลายทาง:** `/cells/autofilter/add-date-filter/`
- [วิธีเพิ่มตัวกรองแบบไดนามิกในแผ่นงาน Excel](/th/cells/autofilter/add-dynamic-filter/) – **วิธีการ:** POST, **จุดปลายทาง:** `/cells/autofilter/add-dynamic-filter/`
- [วิธีเพิ่มตัวกรองในแผ่นงาน Excel](/th/cells/autofilter/add-filter/) – **วิธีการ:** POST, **จุดปลายทาง:** `/cells/autofilter/add-filter/`
- [วิธีเพิ่มตัวกรองไอคอนในแผ่นงาน Excel](/th/cells/autofilter/add-icon-filter/) – **วิธีการ:** POST, **จุดปลายทาง:** `/cells/autofilter/add-icon-filter/`
- [วิธีลบตัวกรองวันที่ในแผ่นงาน Excel](/th/cells/autofilter/delete-a-date-filter/) – **วิธีการ:** DELETE, **จุดปลายทาง:** `/cells/autofilter/delete-a-date-filter/`
- [วิธีลบตัวกรองในแผ่นงาน Excel](/th/cells/delete-filter/) – **วิธีการ:** DELETE, **จุดปลายทาง:** `/cells/delete-filter/`
- [วิธีรับคำอธิบายตัวกรองอัตโนมัติจากแผ่นงาน Excel](/th/cells/autofilter/get/) – **วิธีการ:** GET, **จุดปลายทาง:** `/cells/autofilter/get/`
- [วิธีจับคู่เซลล์ที่ว่างทั้งหมดในแผ่นงาน Excel](/th/cells/autofilter/match-all-blank/) – **วิธีการ:** POST, **จุดปลายทาง:** `/cells/autofilter/match-all-blank/`
- [วิธีจับคู่เซลล์ที่ไม่ว่างทั้งหมดในแผ่นงาน Excel](/th/cells/autofilter/match-all-non-blank/) – **วิธีการ:** POST, **จุดปลายทาง:** `/cells/autofilter/match-all-non-blank/`
- [วิธีรีเฟรชตัวกรองอัตโนมัติในแผ่นงาน Excel](/th/cells/autofilter/refresh/) – **วิธีการ:** POST, **จุดปลายทาง:** `/cells/autofilter/refresh/`