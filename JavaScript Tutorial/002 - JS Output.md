# การแสดงข้อมูลใน JavaScript

---

## รูปแบบในการเขียนข้อมูลเพื่อแสดงผล

- เขียนข้อมูลลงไปใน HTML element โดยใช้ `innerHTML`
- เขียนข้อมูลลงไปใน HTML output โดยใช้ `document.write()`
- เขียนข้อมูลลงไปใน alert box โดยใช้ `window.alert()`
- เขียนข้อมูลลงไปใน browser console โดยใช้ `console.log()`

---

## การใช้งาน innerHTML

​	ในการเข้าถึง element ของ HTML เราสามารถใช้เมธอด `document.getElementById(id)` ภายใน JavaScript ได้ 

`id` Attribute เป็นตัวกำหนด HTML element และ `innerHTML` เป็น property ที่จะกำหนด HTML content ตัวอย่างการใช้งานเช่น

```html
<!DOCTYPE html>
<html>

<body>
    <!-- ตัวเลข 5(2 + 3) จะถูกแทนที่ใน content ของแท็ก <p> -->
    <p id="demo"></p>

    <script>
        document.getElementById("demo").innerHTML = 2 + 3;
    </script>

</body>

</html>
```

> การเปลี่ยน `innerHTML` property ของ HTML element เป็นวิธีทั่วไปที่ใช้ในการแสดงผลข้อมูลใน HTML

---

## การใช้งาน document.write()

​	`document.write()` ใช้สำหรับการทดสอบการแสดงผลข้อมูลชั่วคราว ในการใช้ `document.write()` จะเป็นการลบข้อมูล html ของเราทั้งหมด และแทนที่ด้วยข้อมูลที่เพิ่งเขียนลงไปโดยใช้ `document.write()` ตัวอย่างการใช้งาน

```html
<html>

<body>
    
    <p>Hello, World</p>
    <button type="button" onclick="document.write(2 + 3)">Try it</button>
    
</body>

</html>
```

จากโค้ตด้านบน เมื่อคลิ๊กปุ่มจะทำการลบข้อมูล HTML ทั้งหมดและจะแสดง "5" ไปยังหน้าเพจ HTML ซึ่งในการใช้ `document.write()` จึงควรใช้สำหรับการทดสอบการแสดงข้อมูลเท่านั้น

---

## การใช้ window.alert()

​	เราสามารถใช้ alert box เพื่อแสดงผลข้อมูลได้ ตัวอย่างเช่น

```html
<!DOCTYPE html>
<html>

<body>
    
    <script>
        window.alert(5 + 6);
    </script>

</body>

</html>
```

​	ในการใช้ `window.alert()` เราสามารถไม่ใช้คีย์เวิร์ด `window` ได้ ในภาษา JavaScript `window` เป็น global object ซึ่งหมายถึงตัวแปร หรือฟังก์ชั่นสามารถเข้าใช้งานได้ เป็นเหตุผลที่ว่าทำไมเราถึงสามารถไม่ใส่คีย์เวิร์ด `window` ได้ ตามตัวอย่างด้านล่าง 

```html
<!DOCTYPE html>
<html>

<body>
   
    <script>
        alert(2 + 3);
    </script>

</body>

</html>
```

---

## การใช้ console.log()

​	ในการใช้ `console.log()` จะใช้ในการแก้จุดบกพร่อง หรือ debugging เราสามารถเรียกใช้คำสั่งนี้ใน browser เพื่อแสดงผลข้อมูล

```html
<!DOCTYPE html>
<html>

<body>

    <script>
        console.log(2 + 3);
    </script>

</body>

</html>
```

---

## การใช้ window.print()

​	ใน JavaScript ไม่มีเมธอดในการสั่งปริ้น เนื่องจากเราไม่สามารถเข้าถึงอุปกรณ์นำเข้าได้เช่นเครื่องปริ้นท์ มีอยู่วิธีเดียวคือการเรียกใช้ `window.print()` เมธอดนี้จะทำการปริ้นท์ข้อมูลในหน้าเพจนั้น ๆ

```html
<!DOCTYPE html>
<html>

<body>

    <button onclick="window.print()">Print this page</button>

</body>

</html>
```

