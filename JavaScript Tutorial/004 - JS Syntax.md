# JavaScript Syntax

---

​	JavaScript Syntax ก็คือกฏที่กำหนดระเบียบการจัดโครงสร้างของการเขียนโค้ต เช่น การประกาศตัวแปร การกำหนดค่าให้ตัวแปร และการประมวลผล

```js
var x, y, z;       // ประกาศตัวแปร
x = 5; y = 6;      // กำหนค่าให้กับตัวแปร
z = x + y;         // การประมวลผล
```

---

## JavaScript Values

​	Value ที่อยู่ใน JavaScript Syntax ถูกกำหนดเป็น 2 ประเภท

- Fixed values
- Variable values

Fixed values จะถูกเรียกว่า Literals

Variable values จะถูกเรียกว่า Variables

---

 ## JavaScript Literals

​	สองสิ่งที่สำคัญของ Fixed values คือ

1. Numbers จะเขียนแบบมีทศนิยมหรือไม่มีทศนิยมก็ได้ ตัวอย่างเช่น

```js
10.50
1001
```

2. Strings เป็นข้อความ จะต้องอยู่ภายใน Double หรือ Single quotes ตัวอย่างเช่น

```js
"John Doe"

'John Doe'
```

โดยข้อมูลแบบ Fixed values จะเห็นว่าเมื่อกำหนดออกมาแล้วจะไม่สามารถเปลี่ยนแปลง หรือนำกลับมาใช้ใหม่ได้

----

## JavaScript Variables

ในภาษาคอมพิวเตอร์ Variables หรือตัวแปร ใช้ในการเก็บค่าของข้อมูล

ใน JavaScript เราใช้ `var` ในการประกาศตัวแปร

เครื่องหมายเท่ากับ `=` เราใช้ในการกำหนดค่าให้กับตัวแปร

ตามตัวอย่างด้านล่าง `x` ถูกประกาศออกมาในรูปของตัวแปร หลังจากนั้นกำหนดค่า `x` ให้เท่ากับ 6

```js
var x;

x = 6;
```

---

## JavaScript Operators

​	ใน JavaScript เราใช้ตัวดำเนินการทางคณิตศาสตร์ (`+` `-` `*` `/`) เพื่อคำนวณค่า

```js
(5 + 6) * 10
```

​	ใน JavaScript จะใช้เครื่องหมาย `=` เพื่อกำหนดค่าให้กับตัวแปร

```js
var x, y;
x = 5;
y = 6;
```

---

## JavaScript Expressions

​	Expressions เป็นการผสมผสานกันระหว่าง ข้อมูล ตัวแปร ตัวดำเนินการ เพื่อคำนวณออกมาเป็นข้อมูล การดำเนินการนี้คอมพิวเตอร์จะเรียกว่า evaluation

ตัวอย่างเช่น 5 * 10 evaluates to 50

```js
5 * 10
```

​	นอกจากนั้น Expression ยังสามารถเก็บตัวแปรไว้แล้วนำไปคำนวณได้ ตัวอย่างเช่น

```js
x * 10
```

​	ข้อมูลสามารถเป็นได้หลายประเภทเช่นตัวเลข หรือข้อความ

ตัวอย่างเช่น "John" + " " + "Doe", evaluates to "John Doe"

```js
"John" + " " + "Doe"
```

---

## JavaScript Keywords

​	คีย์เวิร์ดใน JavaScript ใช้ในการระบุคำสั่งที่จะทำ เช่น `var` keyword จะเป็นการบอก browser ว่าเรากำลังจะทำการประกาศตัวแปร

```js
var x, y;
x = 5 + 6;
y = x * 10;
```

---

## JavaScript Comments

​	ไม่ใช่ทุกคำสั่งที่เราต้องการให้ JavaScript ทำงาน บางครั้งเราต้องการให้คำสั่งนั้น ๆ ไม่ทำงานแต่เราก็ไม่อยากลบคำสั่งนั้นทิ้ง สามารถทำได้โดยการคอมเม้นท์ โดยการคอมเม้นท์จะทำได้โดยการพิมพ์ double slashes `//` หรือ ให้ข้อมูลอยู่ระหว่าง `/*` และ `*/` คำสั่งที่ถูกคอมเม้นท์จะถูกเพิกเฉย และจะไม่ทำงาน

```js
var x = 5;   // คำสั่งจะทำงานปกติ

// var x = 6;	คำสั่งจะไม่ทำงาน
```

---

## JavaScript Identifiers

​	Identifiers คือการตั้งชื่อต่าง ๆ

ใน JavaScript, identifiers ถูกใช้ในการตั้งชื่อให้กับตัวแปร รวมไปถึงคีย์เวิร์ด ฟังก์ชั่น และตัวอักษร

ในการตั้งชื่อตัวแปรจะมีกฏของการตั้งชื่อที่จะคล้าย ๆ กับภาษาอื่น

ใน JavaScript ตัวอักษรตัวแรกจะต้องเป็นตัวอักษร underscore(_) หรือ dollar sign ($) 

ในการตั้งชื่อตัวแปร เราจะไม่สามารถใช้ตัวเลขเป็นตัวแรกในชื่อตัวแปรได้

---

## JavaScript is Case Sensitive

​	ภาษา JavaScript ทั้งหมดเป็น Case Sensitive การตั้งตัวแปรเช่น `lastName` และ `lastname` จะถือว่าเป็นคนละตัวแปรกัน

```js
var lastname, lastName;
lastName = "Doe";
lastname = "Peterson";
```

> JavaScript ไม่สามารถใช้คีย์เวิร์ดคำว่า VAR หรือ Var แทน `var` ได้ เพราะถือว่าเป็นคนละตัวกัน

---

## JavaScript and Camel Case

​	ในอดีตโปรแกรมเมอร์ส่วนใหญ่จะใช้วิธีในการรวมคำศัพย์หลาย ๆ คำโดยใช้ Hyphens เช่น first-name, last-name, master-card, inter-city เป็นต้น

แต่ว่า Hyphens **ไม่**อนุญาตให้ใช้ใน JavaScript เพราะถูกสงวนไว้ใช้ในการดำเนินการ ลบ ในคณิตศาสตร์ ซึ่งเราสามารถใช้วิธีอื่นแทนในการรวมคำศัพย์เช่น

- Underscore:

    first_name, last_name, master_card, inter-city

- Upper Camel Case (Pascal Case):

    FirstName, LastName, MasterCard, InterCity.

- Lower Camel Case:

    โปรแกรมเมอร์ส่วนใหญ่มักจะใช้วิธีนี้ คือการขึ้นต้นด้วยตัวอักษรเล็กเช่น

    firstName, lastName, masterCard, interCity

---

## JavaScript Character Set

​	ภายใน JavaScript ใช้ Unicode เป็นชุดตัวอักษร

Unicode โดยส่วนมากจะครอบคลุมไปถึงตัวอักษร เครื่องหมายวรรคตอน สัญลักษณ์ ที่มีอยู่ในโลกนี้

