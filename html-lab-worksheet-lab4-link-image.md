# ใบงานการทดลอง HTML

## การทดลองที่ 4: การสร้างลิงก์และการแทรกรูปภาพ

### การเตรียมโครงสร้างโฟลเดอร์และไฟล์
1. สร้างโครงสร้างโฟลเดอร์:
   ```
   html-workshop/
   ├── index.html
   ├── pages/
   │   ├── about.html
   │   └── contact.html
   ├── images/
   │   ├── logo.jpg
   │   └── products/
   │       ├── product1.jpg
   │       └── product2.jpg
   └── files/
       └── document.pdf
   ```

2. ขั้นตอนการสร้างโครงสร้าง:
   - คลิกขวาในโฟลเดอร์ html-workshop > New Folder > สร้าง "pages"
   - คลิกขวาในโฟลเดอร์ html-workshop > New Folder > สร้าง "images"
   - ในโฟลเดอร์ images > New Folder > สร้าง "products"
   - คลิกขวาในโฟลเดอร์ html-workshop > New Folder > สร้าง "files"

3. สร้างไฟล์ HTML:
   - ในโฟลเดอร์หลัก: สร้าง index.html (ใช้ไฟล์เดิมที่มีได้)
   - ในโฟลเดอร์ pages: สร้าง about.html และ contact.html

4. จัดเตรียมไฟล์:
   - นำรูปภาพที่ต้องการใช้ไปไว้ในโฟลเดอร์ images
   - นำรูปภาพสินค้าไปไว้ในโฟลเดอร์ products
   - นำไฟล์เอกสารไปไว้ในโฟลเดอร์ files

### ขั้นตอนการทดลอง

#### ส่วนที่ 1: การสร้างลิงก์
1. เปิดไฟล์ index.html และใส่โครงสร้างพื้นฐาน:
```html
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>หน้าหลัก</title>
</head>
<body>
    <!-- ส่วนของเนื้อหา -->
</body>
</html>
```

2. สร้างเมนูนำทางพื้นฐาน:
```html
<nav>
    <!-- ลิงก์ภายใน - ไปยังหน้าในเว็บไซต์เดียวกัน -->
    <a href="index.html">หน้าหลัก</a>
    <a href="pages/about.html">เกี่ยวกับเรา</a>
    <a href="pages/contact.html">ติดต่อเรา</a>
    
    <!-- ลิงก์ภายนอก - เปิดในแท็บใหม่ -->
    <a href="https://www.google.com" target="_blank">
        ไปยัง Google
    </a>
</nav>
```
คำอธิบาย:
- `href="..."` - กำหนดเส้นทางของลิงก์
- `target="_blank"` - เปิดลิงก์ในแท็บใหม่

3. สร้างลิงก์ภายในหน้าเดียวกัน:
```html
<!-- สร้างจุดเชื่อมโยง -->
<section id="top">
    <h1>เนื้อหาส่วนบน</h1>
</section>

<section id="products">
    <h2>สินค้าของเรา</h2>
</section>

<!-- ลิงก์ไปยังจุดเชื่อมโยง -->
<a href="#top">กลับด้านบน</a>
<a href="#products">ไปยังสินค้า</a>
```
คำอธิบาย:
- `id="..."` - กำหนดจุดเชื่อมโยง
- `href="#..."` - ลิงก์ไปยัง id ที่กำหนด

4. สร้างลิงก์พิเศษ:
```html
<!-- ลิงก์อีเมล -->
<a href="mailto:contact@example.com">ส่งอีเมลหาเรา</a>

<!-- ลิงก์โทรศัพท์ -->
<a href="tel:+66812345678">โทร 081-234-5678</a>

<!-- ลิงก์ดาวน์โหลด -->
<a href="files/document.pdf" download>
    ดาวน์โหลดเอกสาร
</a>
```
คำอธิบาย:
- `mailto:` - เปิดโปรแกรมอีเมล
- `tel:` - เปิดโปรแกรมโทรศัพท์
- `download` - ดาวน์โหลดไฟล์แทนการเปิด

#### ส่วนที่ 2: การแทรกรูปภาพ
1. แทรกรูปภาพพื้นฐาน:
```html
<!-- รูปภาพในโฟลเดอร์ images -->
<img src="images/logo.jpg" 
     alt="โลโก้บริษัท"
     width="200">

<!-- รูปภาพในโฟลเดอร์ย่อย products -->
<img src="images/products/product1.jpg" 
     alt="สินค้าชิ้นที่ 1"
     width="300"
     height="200">
```
คำอธิบาย:
- `src="..."` - ระบุตำแหน่งของรูปภาพ
- `alt="..."` - ข้อความทดแทนเมื่อไม่สามารถแสดงรูปได้
- `width="..."` - กำหนดความกว้าง
- `height="..."` - กำหนดความสูง

2. ใช้ figure และ figcaption:
```html
<figure>
    <img src="images/products/product2.jpg" 
         alt="สินค้าชิ้นที่ 2">
    <figcaption>
        รายละเอียดสินค้าชิ้นที่ 2
    </figcaption>
</figure>
```
คำอธิบาย:
- `<figure>` - จัดกลุ่มรูปภาพและคำอธิบาย
- `<figcaption>` - คำอธิบายประกอบรูปภาพ

3. สร้างรูปภาพที่คลิกได้:
```html
<a href="images/products/product1.jpg">
    <img src="images/products/product1.jpg" 
         alt="คลิกเพื่อดูรูปขนาดใหญ่"
         width="200">
</a>
```

### หมายเหตุ
- ตรวจสอบการสะกดชื่อไฟล์และโฟลเดอร์ให้ถูกต้อง
- path ของรูปภาพต้องถูกต้องตามโครงสร้างโฟลเดอร์
- ทดสอบการทำงานของลิงก์ทุกจุด

### แบบฝึกหัด
1. สร้างแกลเลอรีสินค้า:
   - สร้างโฟลเดอร์ images/gallery
   - ใส่รูปภาพอย่างน้อย 4 รูป
   - แต่ละรูปต้องคลิกดูขนาดใหญ่ได้
   - มีคำอธิบายใต้รูป
   - มีปุ่มกลับด้านบน

### บันทึกผลการทดลอง
- รหัสเอกสาร HTML ที่เขียน:
```html
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>แบบฝึกหัด</title>
</head>
<body>
    <nav>
        <a href="index.html">หน้าหลัก</a>
        <a href="67030181">ติดต่อเรา</a>
    
    <section id="tops">
        <h1>ชีสเค้ก</H1>
        <figure>
            <img src="https://cdn.pixabay.com/photo/2021/04/05/14/48/cheese-platter-6153716_640.jpg" alt="logo website" width="300" height="300">
            
        </figure>
    </section>
<section id="products">
    <h2>สินค้าของเรา</h2>
    <h3>ชีสเค้กที่ทำจากผลไม้นานาชนิด</h3>
    <div>
        <figure>
            <a href="images/gallery/7400.png" >
                <img src="https://media.istockphoto.com/id/612521142/th/%E0%B8%A3%E0%B8%B9%E0%B8%9B%E0%B8%96%E0%B9%88%E0%B8%B2%E0%B8%A2/%E0%B8%A1%E0%B8%B1%E0%B8%87%E0%B8%AA%E0%B8%A7%E0%B8%B4%E0%B8%A3%E0%B8%B1%E0%B8%95%E0%B8%B4%E0%B9%80%E0%B8%84%E0%B9%89%E0%B8%81%E0%B9%81%E0%B8%84%E0%B8%A3%E0%B8%AD%E0%B8%97%E0%B8%94%E0%B8%B4%E0%B8%9A-%E0%B8%AD%E0%B8%B2%E0%B8%AB%E0%B8%B2%E0%B8%A3%E0%B9%80%E0%B8%9E%E0%B8%B7%E0%B9%88%E0%B8%AD%E0%B8%AA%E0%B8%B8%E0%B8%82%E0%B8%A0%E0%B8%B2%E0%B8%9E-%E0%B8%9E%E0%B8%B7%E0%B9%89%E0%B8%99%E0%B8%AB%E0%B8%A5%E0%B8%B1%E0%B8%87%E0%B8%AA%E0%B8%B5%E0%B9%80%E0%B8%97%E0%B8%B2.jpg?s=612x612&w=0&k=20&c=b1Sk23zBh7xjFGSoOBA5-hmFcaivqb9iOG3ucR7gFlg=" alt="IC 7400" width="200">
            </a>
            <figcaption>บลูเบอร์รี่ ชีสเค้ก</figcaption>
        </figure>
    </div>
    
    <div>
        <figure>
            <a href="images/gallery/7402.png">
                <img src="https://media.istockphoto.com/id/1135588755/th/%E0%B8%A3%E0%B8%B9%E0%B8%9B%E0%B8%96%E0%B9%88%E0%B8%B2%E0%B8%A2/%E0%B8%9B%E0%B8%B4%E0%B8%94%E0%B9%80%E0%B8%84%E0%B9%89%E0%B8%81%E0%B9%81%E0%B8%84%E0%B8%A3%E0%B8%AD%E0%B8%97%E0%B8%A1%E0%B8%B1%E0%B8%87%E0%B8%AA%E0%B8%A7%E0%B8%B4%E0%B8%A3%E0%B8%B1%E0%B8%95%E0%B8%B4%E0%B8%8A%E0%B8%B4%E0%B9%89%E0%B8%99%E0%B8%AB%E0%B8%99%E0%B8%B6%E0%B9%88%E0%B8%87%E0%B8%9E%E0%B8%A3%E0%B9%89%E0%B8%AD%E0%B8%A1%E0%B8%AD%E0%B8%B1%E0%B8%A5%E0%B8%A1%E0%B8%AD%E0%B8%99%E0%B8%94%E0%B9%8C%E0%B8%9A%E0%B8%99%E0%B8%88%E0%B8%B2%E0%B8%99%E0%B8%A3%E0%B8%AD%E0%B8%87%E0%B9%81%E0%B8%A5%E0%B8%B0%E0%B8%AA%E0%B9%89%E0%B8%AD%E0%B8%A1%E0%B9%83%E0%B8%81%E0%B8%A5%E0%B9%89-%E0%B9%86.jpg?s=612x612&w=0&k=20&c=GZYUHgeswPmBwHLpI1VjwgBMYFIcZaDFfVK2pzQyEJ4=" alt="IC 7402" width="200">
            </a>
            <figcaption>อัลมอล ชีสเค้ก</figcaption>
        </figure>
    </div>

    <div>
        <figure>
            <a href="images/gallery/7404.png">
                <img src="https://cdn.pixabay.com/photo/2021/05/18/12/48/cheese-cake-6263345_640.jpg" alt="IC 7404" width="200">
            </a>
            <figcaption>สตอเบอร์รี่ ชีสเค้ก</figcaption>
        </figure>
    </div>

    <div>
        <figure>
            <a href="images/gallery/7408.png">
                <img src="https://cdn.pixabay.com/photo/2014/07/21/23/00/orange-cake-398966_640.jpg" alt="IC 7408" width="200">
            </a>
            <figcaption>ส้ม ชีสเค้ก</figcaption>
        </figure>
    </div>
    <a href="#top">
        <button>กลับ</button>
    </section>
</body>
</html>
```
- ภาพผลลัพธ์:
![image](https://github.com/user-attachments/assets/e7169897-654e-4893-9103-0c55616ba2e0)




