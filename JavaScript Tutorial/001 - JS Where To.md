# วิธีการเรียกใช้ JavaScript

---

## The < script > Tag

​	ในภาษา HTML โค้ตของ JavaScript จะอยู่ระหว่างแท็ก `<script>` และ `</script>`

ตัวอย่างเช่น

```html
<script>
document.getElementById("demo").innerHTML = "My First JavaScript";
</script>
```

> ใน JavaScript สมัยเก่าเราจะต้องใช้ type attribute  อย่างเช่น: `<script type="text/javascript">` แต่ในปัจจุบัน JavaScript เป็นภาษาสคริปต์เริ่มต้นของ HTML อยู่แล้ว เราจึงไม่จำเป็นต้องกำหนด type attribute

---

## JavaScript ฟังก์ชั่น และ อีเว้นท์

​	`function` ใน JavaScript เป็นเหมือนกล่องใส่โค้ตของ JavaScript ที่เราสามารถเรียกใช้ได้ทุกเมื่อ ตัวอย่างเช่น เมื่อเมื่อเราทำการสร้างอีเว้นท์โดยการคลิ๊กเม้าส์ อีเว้นท์คลิ๊กเม้าส์จะทำการเรียก `function` ตามที่เรากำหนดไว้

> นี่เป็นเพียงตัวอย่างคร่าว ๆ เท่านั้น ผมจะพูดถึงเรื่องนี้เพิ่มเติมในส่วนของ JS Functions และ JS Events

---

## JavsScript ในแท็ก < head > และ < body >

​	เราสามารถวางสคริปต์ไว้ในส่วนของ `<body>` และ `<head>` ของหน้าต่าง HTML ได้ ตามตัวอย่างด้านล่าง

```html
<!DOCTYPE html>
<html>

<head>
    <script>
        function male() {
            document.getElementById("demo").innerHTML = "My gender is male";
        }
    </script>
</head>

<body>
    <script>
        function female() {
            document.getElementById("demo").innerHTML = "My gender is female"
        }
    </script>

    <h1>What is your gender?</h1>
    <p id="demo">My gender is </p>
    <button type="button" onclick="male()">Male</button>
    <button type="button" onclick="female()">Female</button>
</body>

</html>
```

---

## การสร้างไฟล์ JavaScript และการนำไปใช้

​	JavaScript สามารถสร้างไฟล์สคริปต์ได้ เพื่อนำไปใช้กับ HTML ในภายหลัง โดยไฟล์ของ JavaScript จะต้องมีนามสกุลเป็น **.js** ตัวอย่างภายในไฟล์ JavaScript ที่มีชื่อไฟล์ว่า myScript.js

```js
function myFunction() {
  document.getElementById("demo").innerHTML = "Hello, World";
}
```

จากนั้นเราสามาถนำไฟล์ JavaScript ใส่เข้าไปใน HTML โดยการใส่ชื่อไฟล์ JavaScript เข้าไปใน Attribute ที่ชื่อว่า `src` (source) ในแท็ก < script > 

```html
<script src="myScript.js"></script>
```

 เราสามารถวางไฟล์ JavaScript ไว้ในส่วนของ `<head>` และ `<body>` ได้ตามที่เราต้องการ

> ภายในไฟล์ JavaScript ไม่สามาถมีแท็ก `<script>` ได้

---

## ข้อดีของการสร้างไฟล์ JavaScript

​	ในการสร้างไฟล์ JavaScript เพื่อนำไปใช้ใน HTML ในภายหลัง มีข้อดีเช่น

- สามารถแบ่งแยกระหว่าง JavaScript และ HTML ได้อย่างชัดเจน
- ง่ายต่อการอ่านโค้ต การที่เรานำโค้ต HTML และ JavaScript มาปนกันทำให้อ่านยากขึ้น และยากต่อการแก้ไขหากเกิดปัญหา
- ทำให้หน้าเพจโหลดได้ไวขึ้น

หากต้องการนำเข้าไฟล์ JavaScript หลาย ๆ ไฟล์สามารถทำได้ดังนี้

```html
<script src="myScript1.js"></script>
<script src="myScript2.js"></script>
```

---

## การใช้สคริปต์ผ่านลิ้งค์ URL

​	เราสามารถอ้างอิงสคริปต์ผ่านการใช้ URL ได้ โดยการกำหนด Path ไปยังเว็บไซต์ที่ต้องการ ตัวอย่างเช่น

```html
<script src="https://www.w3schools.com/js/myScript1.js"></script>
```

---

## ตำแหน่งของไฟล์สคริปต์ในโฟลเดอร์มีผลต่อการนำไฟล์สคริปต์มาใช้

​	หากเราเก็บไฟล์สคริปต์ไว้ในโฟลเดอร์ที่แตกต่างกันเช่น /scripts/myScript.js แต่ HTML ของเราไม่ได้อยู่ในโฟลเดอร์ scripts เราจะไม่สามารถเรียกใช้ตามวิธีก่อนหน้านี้ได้ เช่น

```html
<!-- ไม่สามารถเรียกใช้งานได้ -->
<script src="myScript.js"></script> 
```

หากต้องการใช้งานเราจะต้องกำหนด Path ของไฟล์นั้น ๆ ด้วย เช่น

```html
<!-- เรียกใช้งานได้ -->
<script src="/scripts/myScript.js"></script>
```