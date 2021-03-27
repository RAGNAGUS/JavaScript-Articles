# JavaScript Comments

---

​	Comments ใน JavaScript ใช้เพื่ออธิบายโค้ตที่อยู่ในสคริปต์ และทำให้โค้ตอ่านง่ายขึ้น และนอกจากนั้น Comments ยังสามารถใช้เป็นตัวป้องกันการทำงานคำสั่งต่าง ๆ เพื่อใช้ในการทดสอบโค้ต

---

## Single Line Comments

​	การคอมเม้นท์แบบบรรทัดเดียวสามารถทำได้โดยการเขียน `//` ไว้หน้าคำสั่ง ทุกข้อความที่อยู่หลังจาก `//` จนไปถึงข้อความสุดท้ายจะไม่ถูกดำเนินการ

ตัวอย่างด้านล่างนี้จะเป็นตัวอย่างการใช้ single-line comment

```js
// Change heading:
document.getElementById("myH").innerHTML = "My First Page";

// Change paragraph:
document.getElementById("myP").innerHTML = "My first paragraph.";
```

นี่เป็นตัวอย่างการใช้ single-line comment ในบรรทัดเดียวกัน

```js
var x = 5;      // Declare x, give it the value of 5
var y = x + 2;  // Declare y, give it the value of x + 2
```

---

## Multi-line Comments

​	การคอมเม้นท์หลายบรรทัดสามารถทำได้โดยการเขียน `/*` และปิดด้วย `*/` ทุกข้อความที่อยู่ระหว่าง `/*` และ `*/` จะไม่ถูกดำเนินการโดย JavaScript

ตัวอย่างด้านล่างนี้จะเป็นการใช้ multi-line comment หรือเรียกอีกอย่างว่า comment block เพื่ออธิบายการทำงานของโค้ต

```js
/*
The code below will change
the heading with id = "myH"
and the paragraph with id = "myP"
in my web page:
*/
document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
```

> ในการเขียนโปรแกรมส่วนใหญ่จะใช้ single line comments ในการคอมเม้นท์ ในส่วนของ Block comments จะถูกใช้ในเอกสารที่เป็นทางการ

---

## การใช้ Comments เพื่อป้องกันการดำเนินการ

​	เราสามารถใช้คอมเม้นท์เพื่อป้องกันการทำงานของคำสั่ง ซึ่งเหมาะมากสำหรับการทำสอบโค้ต โดยจะสามาถใช้ได้ทั้ง `//` และ `/**/` ในการคอมเม้นท์

ตัวอย่างด้านล่างจะเป็นการคอมเม้นท์แบบ single-line เพื่อป้องกันการดำเนินการ

```js
//document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
```

 ตัวอย่างด้านล่างจะเป็นการคอมเม้นท์แบบ comment block เพื่อป้องกันการดำเนินการ

```js
/*
document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
*/
```