---
title: "คู่มือนักพัฒนา Aspose.Cells Cloud 3.0"
ArticleTitle: "คู่มือนักพัฒนา Aspose.Cells Cloud 3.0 REST API – การสร้างสมุดงาน Excel การแปลงรูปแบบ และการจัดรูปแบบ"
second_title: "เอกสาร"
type: docs
url: /th/developer-guide-3.0/
aliases: [  /th/developer-guide/v3.0/ , /th/developer-guide-v3.0/ ]
keywords: "Aspose.Cells Cloud, REST API สำหรับ Excel, การแปลงสมุดงาน, API สำหรับกราฟ, การนำเข้าข้อมูล, การส่งออก, PDF, CSV, JSON, คู่มือนักพัฒนา"
description: "เรียนรู้วิธีใช้ REST API ของ Aspose.Cells Cloud 3.0 สำหรับการสร้าง แปลง จัดรูปแบบ กราฟ ตาราง และอื่นๆ สำหรับสมุดงาน Excel พร้อมตัวอย่างโค้ดและเคล็ดลับแนวทางปฏิบัติที่ดีที่สุด"
weight: 150
---

## การใช้งาน REST API ของ Aspose.Cells Cloud

**คู่มือนักพัฒนา Aspose.Cells Cloud 3.0** นำเสนอสรุปแบบกระชับและค้นหาได้ง่ายเกี่ยวกับการดำเนินการ REST API ที่ใช้บ่อยที่สุดสำหรับสมุดงานและแผ่นงาน Excel โดยมีวัตถุประสงค์เพื่อสนับสนุนนักพัฒนาที่ต้องการสร้าง แก้ไข แปลง และจัดการไฟล์ Excel ผ่านการเขียนโปรแกรม ใช้หัวข้อต่อไปนี้เพื่อค้นหาการดำเนินการที่คุณต้องการ โดยแต่ละลิงก์จะนำไปสู่หน้ารายละเอียดที่มีไวยากรณ์คำขอ พารามิเตอร์ และตัวอย่างประกอบ หน้า Hub นี้รวมศูนย์ข้อมูลอ้างอิง **Aspose.Cells Cloud REST API** ไว้ที่เดียว เพื่อให้คุณค้นหา endpoint ที่เกี่ยวข้องกับสมุดงาน การจัดการกราฟ การนำเข้าและส่งออกข้อมูล รวมถึงฟังก์ชันอื่นๆ ได้ง่ายขึ้น

**ข้อกำหนดเบื้องต้น:** ก่อนใช้งาน REST API โปรดตรวจสอบให้แน่ใจว่าคุณมีบัญชี Aspose Cloud ที่ใช้งานได้ คีย์ API และความลับ (secret) ที่ถูกต้อง และ SDK ที่เหมาะสมสำหรับสภาพแวดล้อมการพัฒนาของคุณติดตั้งเรียบร้อยแล้ว

### สารบัญ
- [การดำเนินการเกี่ยวกับไฟล์](#file-operations)
- [หน้าแรก (การจัดรูปแบบเซลล์และการจัดการแถว/คอลัมน์)](#home-cell-formatting--rowcolumn-management)
- [แทรก (กราฟ ตาราง และวัตถุ OLE)](#insert-charts-tables--ole-objects)
- [การจัดหน้า (ตัวแบ่งหน้าและการตั้งค่าหน้า)](#page-layout-page-breaks--setup)
- [สูตร (การคำนวณและชื่อ)](#formulas-calculate--names)
- [ข้อมูล (การจัดกลุ่ม การกรอง และการนำเข้า)](#data-outline-filter--import)
- [การตรวจสอบ (หมายเหตุและโปรtekค์ชัน)](#review-comments--protection)
- [การดู (การควบคุมหน้าต่างและการซูม)](#view-window--zoom-controls)

### สรุป API อย่างรวดเร็ว

| กลุ่ม API | ตัวอย่าง Endpoint | การดำเนินการหลัก |
|-----------|----------------|----------------|
| **สร้างสมุดงาน** | `POST /cells/workbook` | สร้างสมุดงาน Excel ว่างเปล่า |
| **แปลงสมุดงาน** | `PUT /cells/workbook/convert` | แปลงไฟล์ Excel เป็น PDF, CSV, JSON เป็นต้น |
| **เพิ่มกราฟ** | `POST /cells/worksheets/{sheetName}/charts` | แทรกกราฟใหม่ลงในแผ่นงาน |
| **จัดการตาราง** | `PUT /cells/worksheets/{sheetName}/tables/{tableName}` | อัปเดตหรือลบวัตถุรายการ (table) |
| **นำเข้าข้อมูล** | `POST /cells/worksheets/{sheetName}/import` | นำเข้า CSV, JSON, รูปภาพ หรืออาเรย์ลงในแผ่นงาน |
| **คำนวณสูตร** | `POST /cells/workbook/calculate` | คำนวณสูตรทั้งหมดในสมุดงานใหม่ |
| **ใช้ตัวกรอง** | `POST /cells/worksheets/{sheetName}/filters` | เพิ่มหรือลบเกณฑ์ตัวกรองอัตโนมัติ |
| **โปรtekค์ชันสมุดงาน** | `POST /cells/workbook/protect` | ใช้การป้องกันด้วยรหัสผ่านกับสมุดงาน |

การดำเนินการที่ใช้บ่อยเหล่านี้ครอบคลุมฟังก์ชันหลักของ **Aspose.Cells Cloud Excel REST API** และเชื่อมโยงโดยตรงไปยังหน้าเอกสารอ้างอิงโดยละเอียด

คุณสามารถดาวน์โหลดเวอร์ชัน PDF ของตารางสรุป API อย่างรวดเร็วนี้ไว้ใช้งานแบบออฟไลน์ได้

{{< tabs tabTotal="8" tabID="1" tabName1="ไฟล์" tabName2="หน้าแรก" tabName3="แทรก" tabName4="การจัดหน้า" tabName5="สูตร" tabName6="ข้อมูล" tabName7="การตรวจสอบ" tabName8="การดู" >}}
{{< tab tabNum="1" >}}
<div class="row">
    <div class="col-md-6">
        <p>สมุดงาน: สร้างใหม่ แปลง บันทึกเป็น</p>
        <ul>
            <li><a href="/cells/create-an-empty-excel-workbook/" title="สร้างสมุดงาน Excel ว่างเปล่าผ่าน API" rel="noopener">สร้างสมุดงาน Excel ว่างเปล่า</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-template-file/" title="สร้างสมุดงานจากไฟล์เทมเพลต" rel="noopener">สร้างสมุดงาน Excel จากไฟล์เทมเพลต</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-smartmarker-template/" title="สร้างสมุดงานจากเทมเพลต SmartMarker" rel="noopener">สร้างสมุดงาน Excel จากเทมเพลต SmartMarker</a></li>
            <li><a href="/cells/convert/" title="แปลงสมุดงาน Excel เป็นรูปแบบอื่น" rel="noopener">แปลงสมุดงาน Excel เป็นรูปแบบไฟล์ต่างๆ</a></li>
            <li><a href="/cells/saveas-other-formats/" title="บันทึกสมุดงาน Excel เป็นรูปแบบอื่น" rel="noopener">บันทึกสมุดงาน Excel เป็นรูปแบบไฟล์ต่างๆ</a></li>
        </ul>
        <p>ค้นหา แทนที่</p>
        <ul>
            <li><a href="/cells/search/" title="ค้นหาข้อความในไฟล์ Excel" rel="noopener">ค้นหาข้อความจากไฟล์ Excel</a></li>
            <li><a href="/cells/replace/" title="แทนที่ค่าในไฟล์ Excel" rel="noopener">แทนที่ค่าเก่าด้วยค่าใหม่ในไฟล์ Excel</a></li>
        </ul>
        <p>บีบอัด</p>
        <ul>
            <li><a href="/cells/compress/" title="บีบอัดไฟล์ Excel" rel="noopener">บีบอัดไฟล์ Excel</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>สมุดงาน: รวม แยก</p>
        <ul>
            <li><a href="/cells/merge/" title="รวมสมุดงาน Excel หลายไฟล์" rel="noopener">รวมสมุดงาน Excel</a></li>
            <li><a href="/cells/split/" title="แยกสมุดงาน Excel เป็นไฟล์แยกต่างหาก" rel="noopener">แยกสมุดงาน Excel</a></li>
        </ul>
        <p>ลายน้ำ</p>
        <ul>
            <li><a href="/cells/add-background-in-workbook/" title="เพิ่มรูปภาพพื้นหลังให้สมุดงาน" rel="noopener">เพิ่มพื้นหลังให้สมุดงาน</a></li>
            <li><a href="/cells/delete-background-in-workbook/" title="ลบภาพพื้นหลังของสมุดงาน" rel="noopener">ลบพื้นหลังออกจากสมุดงาน</a></li>
            <li><a href="/cells/set-background-or-watermark-for-excel-worksheet/" title="ตั้งค่าพื้นหลังหรือลายน้ำให้แผ่นงาน" rel="noopener">ตั้งค่าพื้นหลังหรือลายน้ำให้แผ่นงาน Excel</a></li>
            <li><a href="/cells/delete-background-or-watermark-of-excel-worksheet/" title="ลบพื้นหลังหรือลายน้ำของแผ่นงาน" rel="noopener">ลบพื้นหลังหรือลายน้ำออกจากแผ่นงาน Excel</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="2" >}}
<div class="row">
    <div class="col-md-6">
        <p>ฟอนต์ รูปแบบ และการจัดรูปแบบตามเงื่อนไขของเซลล์ รวมถึงค่าต่างๆ</p>
        <ul>
            <li><a href="/cells/get-cell-style-from-a-worksheet/" title="ดึงข้อมูลรูปแบบเซลล์จากแผ่นงาน" rel="noopener">รับรูปแบบเซลล์จากแผ่นงาน Excel</a></li>
            <li><a href="/cells/update-multiple-cells-style/" title="อัปเดตรูปแบบของหลายเซลล์" rel="noopener">อัปเดตรูปแบบของหลายเซลล์ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/change-cell-style-in-excel-worksheet/" title="เปลี่ยนรูปแบบของเซลล์เดียว" rel="noopener">อัปเดตรูปแบบเซลล์ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/apply-rich-text-formatting-to-a-cell/" title="ใช้การจัดรูปแบบข้อความแบบมีรูปแบบ (Rich Text) ให้เซลล์" rel="noopener">ตั้งค่ารูปแบบข้อความแบบมีรูปแบบให้กับเซลล์ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/" title="ล้างเนื้อหาและรูปแบบของเซลล์" rel="noopener">ล้างเนื้อหาและรูปแบบของเซลล์ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/working-with-conditional-formatting/" title="จัดการกฎการจัดรูปแบบตามเงื่อนไข" rel="noopener">เพิ่ม ลบ และอัปเดตการจัดรูปแบบตามเงื่อนไขในแผ่นงาน Excel</a></li>
            <li><a href="/cells/set-value-of-a-cell-in-a-worksheet/" title="ตั้งค่าของเซลล์" rel="noopener">ตั้งค่าของเซลล์ในแผ่นงาน Excel</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>แถว/คอลัมน์: เพิ่ม ลบ คัดลอก ซ่อน และปรับขนาดอัตโนมัติ</p>
        <ul>
            <li><a href="/cells/add-an-empty-row-in-a-worksheet/" title="เพิ่มแถวว่างลงในแผ่นงาน" rel="noopener">เพิ่มแถวว่างในแผ่นงาน Excel</a></li>
            <li><a href="/cells/delete-row-from-a-worksheet/" title="ลบแถวจากแผ่นงาน" rel="noopener">ลบแถวจากแผ่นงาน Excel</a></li>
            <li><a href="/cells/copy-rows-in-excel-worksheet/" title="คัดลอกแถวภายในแผ่นงาน" rel="noopener">คัดลอกแถวในแผ่นงาน Excel</a></li>
            <li><a href="/cells/hide-rows-in-excel-worksheet/" title="ซ่อนแถวในแผ่นงาน" rel="noopener">ซ่อนแถวในแผ่นงาน Excel</a></li>
            <li><a href="/cells/auto-fit-rows-in-excel-workbooks/" title="ปรับขนาดแถวอัตโนมัติในสมุดงาน" rel="noopener">ปรับขนาดแถวอัตโนมัติในสมุดงาน Excel</a></li>
            <li><a href="/cells/columns/add/" title="เพิ่มคอลัมน์ว่างลงในแผ่นงาน" rel="noopener">เพิ่มคอลัมน์ว่างในแผ่นงาน Excel</a></li>
            <li><a href="/cells/columns/delete/" title="ลบคอลัมน์จากแผ่นงาน" rel="noopener">ลบคอลัมน์จากแผ่นงาน Excel</a></li>
            <li><a href="/cells/columns/copy/" title="คัดลอกคอลัมน์ภายในแผ่นงาน" rel="noopener">คัดลอกคอลัมน์ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/columns/hide/" title="ซ่อนคอลัมน์ในแผ่นงาน" rel="noopener">ซ่อนคอลัมน์ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/columns/autofit/" title="ปรับขนาดคอลัมน์อัตโนมัติในสมุดงาน" rel="noopener">ปรับขนาดคอลัมน์อัตโนมัติในสมุดงาน Excel</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="3" >}}
<div class="row">
    <div class="col-md-6">
        <p>กราฟ</p>
        <ul>
            <li><a href="/cells/add-a-chart-in-a-worksheet/" title="เพิ่มกราฟลงในแผ่นงาน" rel="noopener">เพิ่มกราฟในแผ่นงาน Excel</a></li>
            <li><a href="/cells/delete-a-chart-from-a-worksheet/" title="ลบกราฟจากแผ่นงาน" rel="noopener">ลบกราฟในแผ่นงาน Excel</a></li>
            <li><a href="/cells/delete-all-charts-from-a-worksheet/" title="ลบกราฟทั้งหมดจากแผ่นงาน" rel="noopener">ลบกราฟทั้งหมดในแผ่นงาน Excel</a></li>
            <li><a href="/cells/convert-chart-to-image/" title="แปลงกราฟเป็นไฟล์ภาพ" rel="noopener">แปลงกราฟเป็นภาพ</a></li>
            <li><a href="/cells/hide-chart-legend-in-a-worksheet/" title="ซ่อนคำอธิบายกราฟ" rel="noopener">ซ่อนคำอธิบายกราฟในแผ่นงาน Excel</a></li>
            <li><a href="/cells/update-chart-title-in-excel-worksheet/" title="อัปเดตชื่อกราฟ" rel="noopener">อัปเดตชื่อกราฟในแผ่นงาน Excel</a></li>
            <li><a href="/cells/delete-chart-title-in-a-worksheet/" title="ลบชื่อกราฟ" rel="noopener">ลบชื่อกราฟในแผ่นงาน</a></li>
        </ul>
        <p>ตาราง</p>
        <ul>
            <li><a href="/cells/add-a-list-object-or-table-inside-the-worksheet/" title="เพิ่มตาราง (วัตถุรายการ) ลงในแผ่นงาน" rel="noopener">เพิ่มวัตถุรายการในแผ่นงาน Excel</a></li>
            <li><a href="/cells/update-a-list-object-or-table-inside-the-worksheet/" title="อัปเดตตารางในแผ่นงาน" rel="noopener">อัปเดตวัตถุรายการในแผ่นงาน Excel</a></li>
            <li><a href="/cells/convert-list-object-or-table-to-range/" title="แปลงตารางเป็นช่วง" rel="noopener">แปลงวัตถุรายการเป็นช่วง</a></li>
            <li><a href="/cells/sort-table-data/" title="เรียงลำดับข้อมูลในตาราง" rel="noopener">เรียงลำดับข้อมูลในตาราง</a></li>
        </ul>
        <p>วัตถุ OLE</p>
        <ul>
            <li><a href="/cells/add-oleobject-to-excel-worksheet/" title="เพิ่มวัตถุ OLE ลงในแผ่นงาน" rel="noopener">เพิ่มวัตถุ OLE ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/update-a-specific-oleobject-from-excel-worksheet/" title="อัปเดตวัตถุ OLE ที่ระบุ" rel="noopener">อัปเดตวัตถุ OLE ที่ระบุในแผ่นงาน Excel</a></li>
            <li><a href="/cells/convert-oleobject-to-image/" title="แปลงวัตถุ OLE เป็นภาพ" rel="noopener">แปลงวัตถุ OLE เป็นภาพ</a></li>
            <li><a href="/cells/delete-all-oleobjects-from-excel-worksheet/" title="ลบวัตถุ OLE ทั้งหมดจากแผ่นงาน" rel="noopener">ลบวัตถุ OLE ทั้งหมดในแผ่นงาน Excel</a></li>
            <li><a href="/cells/delete-a-specific-oleobject-from-excel-worksheet/" title="ลบวัตถุ OLE ที่ระบุ" rel="noopener">ลบวัตถุ OLE ที่ระบุในแผ่นงาน Excel</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>รูปร่าง</p>
        <ul>
            <li><a href="/cells/add-a-shape-inside-the-worksheet/" title="เพิ่มรูปร่างลงในแผ่นงาน" rel="noopener">เพิ่มรูปร่างในแผ่นงาน Excel</a></li>
            <li><a href="/cells/delete-all-shapes-inside-the-worksheet/" title="ลบรูปร่างทั้งหมดจากแผ่นงาน" rel="noopener">ลบรูปร่างทั้งหมดในแผ่นงาน Excel</a></li>
            <li><a href="/cells/delete-a-shape-by-index-inside-the-worksheet/" title="ลบรูปร่างตามดัชนี" rel="noopener">ลบรูปร่างตามดัชนีในแผ่นงาน Excel</a></li>
        </ul>
        <p>ตาราง.pivot</p>
        <ul>
            <li><a href="/cells/add-a-pivot-table-in-a-worksheet/" title="เพิ่มตาราง.pivot ลงในแผ่นงาน" rel="noopener">เพิ่มตาราง.pivot ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/delete-worksheet-pivot-tables/" title="ลบตาราง.pivot ทั้งหมดจากแผ่นงาน" rel="noopener">ลบตาราง.pivot ทั้งหมดในแผ่นงาน Excel</a></li>
            <li><a href="/cells/delete-worksheet-pivot-table-by-index/" title="ลบตาราง.pivot ตามดัชนี" rel="noopener">ลบตาราง.pivot ตามดัชนีในแผ่นงาน Excel</a></li>
            <li><a href="/cells/update-cell-style-for-pivot-table/" title="อัปเดตรูปแบบเซลล์ในตาราง.pivot" rel="noopener">อัปเดตรูปแบบเซลล์ของตาราง.pivot ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/update-style-for-pivot-table/" title="อัปเดตรูปแบบโดยรวมของตาราง.pivot" rel="noopener">อัปเดตรูปแบบของตาราง.pivot ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/working-with-pivot-filters/" title="ทำงานกับตัวกรองตาราง.pivot" rel="noopener">ทำงานกับตัวกรองตาราง.pivot ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/hide-pivot-field-item/" title="ซ่อนรายการฟิลด์ในตาราง.pivot" rel="noopener">ซ่อนรายการฟิลด์ในตาราง.pivot ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/move-pivot-table/" title="ย้ายตาราง.pivot ภายในแผ่นงาน" rel="noopener">ย้ายตาราง.pivot ในแผ่นงาน Excel</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="4" >}}
<div class="row">
    <div class="col-md-6">
        <p>ตัวแบ่งหน้า</p>
        <ul>
            <li><a href="/cells/insert-horizontal-page-break-inside-worksheet/" title="แทรกตัวแบ่งหน้าแนวนอน" rel="noopener">แทรกตัวแบ่งหน้าแนวนอนในแผ่นงาน Excel</a></li>
            <li><a href="/cells/insert-vertical-page-break-inside-worksheet/" title="แทรกตัวแบ่งหน้าแนวตั้ง" rel="noopener">แทรกตัวแบ่งหน้าแนวตั้งในแผ่นงาน Excel</a></li>
            <li><a href="/cells/delete-horizontal-page-break-inside-worksheet/" title="ลบตัวแบ่งหน้าแนวนอน" rel="noopener">ลบตัวแบ่งหน้าแนวนอนในแผ่นงาน Excel</a></li>
            <li><a href="/cells/delete-vertical-page-break-inside-worksheet/" title="ลบตัวแบ่งหน้าแนวตั้ง" rel="noopener">ลบตัวแบ่งหน้าแนวตั้งในแผ่นงาน Excel</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>การตั้งค่าหน้า</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="5" >}}
<div class="row">
    <div class="col-md-6">
        <p>การคำนวณ</p>
        <ul>
            <li><a href="/cells/calculate-all-formulas-in-a-workbook/" title="คำนวณสูตรทั้งหมดในสมุดงาน" rel="noopener">คำนวณสูตรทั้งหมดในสมุดงาน Excel</a></li>
            <li><a href="/cells/calculate-cells-formula/" title="คำนวณสูตรของเซลล์เฉพาะ" rel="noopener">คำนวณสูตรของเซลล์ในสมุดงาน Excel</a></li>
            <li><a href="/cells/calculate-formula-in-a-worksheet/" title="คำนวณสูตรในแผ่นงาน" rel="noopener">คำนวณสูตรในแผ่นงาน Excel</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>ชื่อ</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="6" >}}
<div class="row">
    <div class="col-md-6">
        <p>การจัดกลุ่ม</p>
        <ul>
            <li><a href="/cells/group-rows-in-excel-worksheet/" title="จัดกลุ่มแถวในแผ่นงาน" rel="noopener">จัดกลุ่มแถวในแผ่นงาน Excel</a></li>
            <li><a href="/cells/ungroup-rows-in-excel-worksheet/" title="ยกเลิกการจัดกลุ่มแถวในแผ่นงาน" rel="noopener">ยกเลิกการจัดกลุ่มแถวในแผ่นงาน Excel</a></li>
        </ul>
        <p>การกรอง</p>
        <ul>
            <li><a href="/cells/add-a-filter-for-a-filter-column/" title="เพิ่มตัวกรองให้คอลัมน์" rel="noopener">เพิ่มตัวกรองสำหรับคอลัมน์ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/delete-a-filter-for-a-filter-column/" title="ลบตัวกรองของคอลัมน์" rel="noopener">ลบตัวกรองสำหรับคอลัมน์ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/remove-a-date-filter/" title="ลบตัวกรองวันที่" rel="noopener">ลบตัวกรองวันที่ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/add-an-icon-filter/" title="เพิ่มตัวกรองไอคอน" rel="noopener">เพิ่มตัวกรองไอคอนในแผ่นงาน Excel</a></li>
            <li><a href="/cells/add-date-filter-in-a-worksheet/" title="เพิ่มตัวกรองวันที่" rel="noopener">เพิ่มตัวกรองวันที่ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/filter-data-by-using-an-autofilter/" title="กรองข้อมูลโดยใช้ AutoFilter" rel="noopener">กรองข้อมูลโดยใช้ AutoFilter ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/filter-the-top-10-items-in-the-list/" title="กรอง 10 รายการแรก" rel="noopener">กรอง 10 รายการแรกในรายการในแผ่นงาน Excel</a></li>
            <li><a href="/cells/match-all-blank-cells-in-the-list/" title="ค้นหาเซลล์ว่างทั้งหมด" rel="noopener">ค้นหาเซลล์ว่างทั้งหมดในรายการในแผ่นงาน Excel</a></li>
        </ul>
        <p>การเรียงลำดับ</p>
        <ul>
            <li><a href="/cells/sort-worksheet-data/" title="เรียงลำดับข้อมูลในแผ่นงาน" rel="noopener">เรียงลำดับข้อมูลในแผ่นงาน Excel</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>การนำเข้าข้อมูล</p>
        <ul>
            <li><a href="/cells/import/" title="นำเข้าข้อมูลลงในไฟล์ Excel" rel="noopener">นำเข้าข้อมูลลงในไฟล์ Excel</a></li>
            <li><a href="/cells/import-CSV-data-into-worksheet/" title="นำเข้าข้อมูล CSV ลงในแผ่นงาน" rel="noopener">นำเข้าข้อมูล CSV ลงในแผ่นงาน Excel</a></li>
            <li><a href="/cells/import/picture/" title="นำเข้าภาพลงในแผ่นงาน" rel="noopener">นำเข้าภาพลงในแผ่นงาน Excel</a></li>
            <li><a href="/cells/import/double-array/" title="นำเข้าอาเรย์แบบ double ลงในแผ่นงาน" rel="noopener">นำเข้าอาเรย์แบบ double ลงในแผ่นงาน Excel</a></li>
            <li><a href="/cells/import/integer-array/" title="นำเข้าอาเรย์แบบ integer ลงในแผ่นงาน" rel="noopener">นำเข้าอาเรย์แบบ integer ลงในแผ่นงาน Excel</a></li>
            <li><a href="/cells/import/string-array/" title="นำเข้าอาเรย์แบบ string ลงในแผ่นงาน" rel="noopener">นำเข้าอาเรย์แบบ string ลงในแผ่นงาน Excel</a></li>
            <li><a href="/cells/import/with-using-storage/" title="นำเข้าข้อมูลโดยใช้พื้นที่จัดเก็บ" rel="noopener">นำเข้าข้อมูลลงในแผ่นงาน Excel โดยใช้พื้นที่จัดเก็บ</a></li>
            <li><a href="/cells/import/without-using-storage/" title="นำเข้าข้อมูลโดยไม่ใช้พื้นที่จัดเก็บ" rel="noopener">นำเข้าข้อมูลลงในแผ่นงาน Excel โดยไม่ใช้พื้นที่จัดเก็บ</a></li>
        </ul>
        <p>การประกอบ</p>
        <ul>
            <li><a href="/cells/assembly/" title="ประกอบข้อมูลในไฟล์ Excel" rel="noopener">ประกอบข้อมูลในไฟล์ Excel</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="7" >}}
<div class="row">
    <div class="col-md-6">
        <p>หมายเหตุ</p>
        <ul>
            <li><a href="/cells/add-a-comment-to-a-cell-in-a-worksheet/" title="เพิ่มหมายเหตุให้เซลล์" rel="noopener">เพิ่มหมายเหตุให้เซลล์ในแผ่นงาน Excel</a></li>
            <li><a href="/cells/update-a-comment-in-excel-workbook/" title="อัปเดตหมายเหตุของเซลล์" rel="noopener">อัปเดตหมายเหตุในแผ่นงาน Excel</a></li>
            <li><a href="/cells/delete-all-comments-in-a-worksheet/" title="ลบหมายเหตุทั้งหมดในแผ่นงาน" rel="noopener">ลบหมายเหตุทั้งหมดในแผ่นงาน Excel</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>การเปลี่ยนแปลง</p>
        <ul>
            <li><a href="/cells/protect-excel-workbooks/" title="โปรtekค์ชันสมุดงาน Excel" rel="noopener">โปรtekค์ชันสมุดงาน Excel</a></li>
            <li><a href="/cells/unprotect-excel-workbooks/" title="ยกเลิกการโปรtekค์ชันสมุดงาน Excel" rel="noopener">ยกเลิกการโปรtekค์ชันสมุดงาน Excel</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="8" >}}
<div class="row">
    <div class="col-md-6">
        <p>หน้าต่าง</p>
        <ul>
            <li><a href="/cells/freeze-panes-in-excel-worksheet/" title="แช่แข็งบานหน้าต่างในแผ่นงาน" rel="noopener">แช่แข็งบานหน้าต่างในแผ่นงาน Excel</a></li>
            <li><a href="/cells/unfreeze-panes-in-excel-worksheet/" title="ยกเลิกการแช่แข็งบานหน้าต่างในแผ่นงาน" rel="noopener">ยกเลิกการแช่แข็งบานหน้าต่างในแผ่นงาน Excel</a></li>
            <li><a href="/cells/hide-excel-worksheets/" title="ซ่อนแผ่นงาน" rel="noopener">ซ่อนแผ่นงาน Excel</a></li>
            <li><a href="/cells/unhide-excel-worksheets/" title="ยกเลิกการซ่อนแผ่นงาน" rel="noopener">ยกเลิกการซ่อนแผ่นงาน Excel</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>การซูม</p>
        <ul>
            <li><a href="/cells/set-zoom-in-excel-worksheet/" title="ตั้งค่าระดับการซูมของแผ่นงาน" rel="noopener">ตั้งค่าการซูมในแผ่นงาน Excel</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}

{{< /tabs >}}
---