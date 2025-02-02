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
[วางโค้ด HTML ที่นี่]
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Books</title>
</head>
<body>
    <nav id="nav">
        <img src="./images/logo.jpg" alt="logo" width="50" height="50">
        <a href="index.html">หน้าหลัก</a>
        <a href="pages/about.html">เกี่ยวกับเรา</a>
        <a href="pages/contact.html">ติดต่อเรา</a>
    </nav>
    <hr>
    <section>
        <h1>Gallery</h1>
        <figure>
            <a href="images/gallery/product1.png">
                <img src="images/gallery/product1.png" alt="product1" width="200"> 
            </a>
            <figcaption>
                <p>
                    <strong>TITLE:</strong>
                    DIANA & JACK
                </p>
                <p>
                    <strong>AUTHOR:</strong>
                    Teeranat Pootivirnich
                </p>
                <p>
                    <strong>PUBLISHER:</strong>
                    Panya Thai
                </p>
                <p>
                    <strong>CATEGORY:</strong>
                    Fantasy
                </p>
                <p>
                    <strong>PRICE:</strong>
                    $12.99 / 420 THB
                </p>
            </figcaption>
        </figure>
        <hr>
        <figure>
            <a href="images/gallery/product2.png">
                <img src="images/gallery/product2.png" alt="product2" width="200"> 
            </a>
            <figcaption>
                <p>
                    <strong>TITLE:</strong>
                    CHRISTMAS
                </p>
                <p>
                    <strong>AUTHOR:</strong>
                    Prachya Aksaranon
                </p>
                <p>
                    <strong>PUBLISHER:</strong>
                    Navatras Publishing
                </p>
                <p>
                    <strong>CATEGORY:</strong>
                    CLASSICS
                </p>
                <p>
                    <strong>PRICE:</strong>
                    $12.99 / 420 THB
                </p>
            </figcaption>
        </figure>
        <hr>
        <figure>
            <a href="images/gallery/product3.png">
                <img src="images/gallery/product3.png" alt="product3" width="200"> 
            </a>
            <figcaption>
                <p>
                    <strong>TITLE:</strong>
                    TERE & TONY
                </p>
                <p>
                    <strong>AUTHOR:</strong>
                    Waranya Sirisuk
                </p>
                <p>
                    <strong>PUBLISHER:</strong>
                    Withee Books
                </p>
                <p>
                    <strong>CATEGORY:</strong>
                    FANTASY
                </p>
                <p>
                    <strong>PRICE:</strong>
                    $12.99 / 420 THB
                </p>
            </figcaption>
        </figure>
        <hr>
        <figure>
            <a href="images/gallery/product4.png">
                <img src="images/gallery/product4.png" alt="product4" width="200"> 
            </a>
            <figcaption>
                <p>
                    <strong>TITLE:</strong>
                    CELTIC TALES
                </p>
                <p>
                    <strong>AUTHOR:</strong>
                    Anawin Pipattanakit
                </p>
                <p>
                    <strong>PUBLISHER:</strong>
                    Sangdao Publishing
                </p>
                <p>
                    <strong>CATEGORY:</strong>
                    SPIRITUALITY & MINDFULNESS
                </p>
                <p>
                    <strong>PRICE:</strong>
                    $12.99 / 420 THB
                </p>
            </figcaption>
        </figure>
        <hr>
        <figure>
            <a href="images/gallery/product5.png">
                <img src="images/gallery/product5.png" alt="product5" width="200"> 
            </a>
            <figcaption>
                <p>
                    <strong>TITLE:</strong>
                    THE LORD OF THE KINGS
                </p>
                <p>
                    <strong>AUTHOR:</strong>
                    Pitchada Wattanakiet
                </p>
                <p>
                    <strong>PUBLISHER:</strong>
                    Jintasill Publishing
                </p>
                <p>
                    <strong>CATEGORY:</strong>
                    FANTASY
                </p>
                <p>
                    <strong>PRICE:</strong>
                    $12.99 / 420 THB
                </p>
            </figcaption>
        </figure>
        <hr>
        <figure>
            <a href="images/gallery/product6.png">
                <img src="images/gallery/product6.png" alt="product6" width="200"> 
            </a>
            <figcaption>
                <p>
                    <strong>TITLE:</strong>
                    SIMPLE & MINIMALIST
                </p>
                <p>
                    <strong>AUTHOR:</strong>
                    Nakarin Kulpiya
                </p>
                <p>
                    <strong>PUBLISHER:</strong>
                    Dandin Books
                </p>
                <p>
                    <strong>CATEGORY:</strong>
                    SELF-HELP
                </p>
                <p>
                    <strong>PRICE:</strong>
                    $12.99 / 420 THB
                </p>
            </figcaption>
        </figure>
        <hr>
        <figure>
            <a href="images/gallery/product7.png">
                <img src="images/gallery/product7.png" alt="product7" width="200"> 
            </a>
            <figcaption>
                <p>
                    <strong>TITLE:</strong>
                    MUTED COLOR POSTER
                </p>
                <p>
                    <strong>AUTHOR:</strong>
                    Supakorn Arayatham
                </p>
                <p>
                    <strong>PUBLISHER:</strong>
                    Montra Publishing
                </p>
                <p>
                    <strong>CATEGORY:</strong>
                    NON-FICTION
                </p>
                <p>
                    <strong>PRICE:</strong>
                    $12.99 / 420 THB
                </p>
            </figcaption>
        </figure>
        <hr>
        <figure>
            <a href="images/gallery/product8.png">
                <img src="images/gallery/product8.png" alt="product8" width="200"> 
            </a>
            <figcaption>
                <p>
                    <strong>TITLE:</strong>
                    MODERN ABSTRACT
                </p>
                <p>
                    <strong>AUTHOR:</strong>
                    Charuwan Rattanasombat
                </p>
                <p>
                    <strong>PUBLISHER:</strong>
                    Aruntat Publishing
                </p>
                <p>
                    <strong>CATEGORY:</strong>
                    BUSINESS & MINDFULNESS
                </p>
                <p>
                    <strong>PRICE:</strong>
                    $12.99 / 420 THB
                </p>
            </figcaption>
        </figure>
        <hr>
    </section>
    
    <a href="#nav">กลับด้านบน</a>
</body>
</html>
```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]
![image](https://github.com/user-attachments/assets/d6f2f4f9-5043-4e98-9dee-091187bff72d)
![image](https://github.com/user-attachments/assets/54a13b5b-db96-47b1-bf87-31fc1cec15a5)
![image](https://github.com/user-attachments/assets/ab7accff-6dff-44e4-9629-7dd62a032c79)
![image](https://github.com/user-attachments/assets/216d67ec-cf29-47d9-a0d4-545f79ba2176)
![image](https://github.com/user-attachments/assets/62ae5831-c837-4fe0-982e-17f8be0cf32a)






