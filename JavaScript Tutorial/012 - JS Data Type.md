# ชนิดของข้อมูลใน JavaScript

---

​	ตัวแปรใน JavaScript สามารถเก็บข้อมูลได้หลายชนิดเช่น ตัวเลข numbers, strings, object

```js
var length = 16;                               // Number
var lastName = "Johnson";                      // String
var x = {firstName:"John", lastName:"Doe"};    // Object
```

---

## แนวคิดของชนิดข้อมูล

​	ชนิดของข้อมูลเป็นสิ่งที่สำคัญในการเขียนโปรแกรม สำหรับนักเขียนโปรแกรม เพื่อที่จะสามารถเขียนโปรแกรมได้ การมีความรู้เรื่องของชนิดของข้อมูลนั้นเป็นสิ่งที่สำคัญมาก ถ้าไม่มีประของข้อมูล คอมพิวเตอร์จะไม่สามารถแก้ไขปัญหาบางอย่างได้

```js
var x = 16 + "Volvo";
```

​	ในตัวอย่างด้านบนมันดูไม่ค่อยสมเหตุสมผลเท่าไหร่ที่เราจะเอาจะเอา "Volvo" ไปบวกกับเลขสิบหก แต่สงสัยไหมว่าถ้าเราเขียนโค้ตแบบนี้ มันจะ error หรือมันจะทำงานได้ปกติ ? คำตอบก็คือ โปรแกรมสามารถทำงานได้ปกติครับ แต่มันจะทำงานเหมือนตัวอย่างด้านล่าง

```js
var x = "16" = "Volvo";
```

​	ในการบวกตัวเลขเข้ากับข้อความนั้น ใน JavaScript จะถือว่าตัวเลขนั้นเป็นข้อความ ตัวอย่างเช่น

```js
var x = 16 + "Volvo";
```

```js
var x = "Volvo" + 16;
```

​	แต่ใน JavaScript การคำนวณจากซ้ายไปขวาเป็นลำดับที่แตกต่างกัน สามารถให้ผลลัพธ์ที่แตกต่างกันได้เช่น ตัวเลขที่บวกหลังจากข้อความจะถือว่าตัวเลขเหล่านั้นเป็นข้อความ

```js
var x = 16 + 4 + "Volvo";
// x จะมีค่าเป็น 20Volvo
```

​	ในตัวอย่างด้านบน JavaScript จะถือว่า 16 และ 4 เป็นตัวเลข จนถึง "Volvo"

```js
var x = "Volvo" + 16 + 4;
// x จะมีค่าเป็น Volvo164
```

​	ในตัวอย่างด้านบน ตัวถูกดำเนินการตัวแรกเป็นข้อความ เพราะฉะนั้น ตัวถูกดำเนินการที่เหลือทั้งหมดจะถูกนับว่าเป็นข้อความ

---

## ชนิดข้อมูลใน JavaScript เป็นแบบ Dynamic

​	JavaScript มีชนิดข้อมูลแบบ dynamic หมายความว่า ตัวแปรบางตัวสามารถใช้เพื่อเก็บข้อมูลที่มีชนิดของข้อมูลที่ต่างกันได้ ตัวอย่างเช่น

```js
var x;           // Now x is undefined
x = 5;           // Now x is a Number
x = "John";      // Now x is a String
```

---

## ข้อความ (Strings) ใน JavaScript

​	String หรือ text string เป็นเหมือนชุดของตัวอักษรยกตัวอย่างเช่น "John Doe" โดย string จะถูกเขียนอยู่ใน quotes ซึ่งเราสามารถใช้แบบ single หรือ double quotes ได้ ตามตัวอย่างด้านล่าง

```js
var carName1 = "Volvo XC60";   // Using double quotes
var carName2 = 'Volvo XC60';   // Using single quotes
```

​	เราสามารถใช้เครื่องหมายคำพูดภายในสตริงได้ตราบเท่าที่ไม่ตรงกับเครื่องหมายที่เราใช้ครอบ string ตามตัวอย่างด้านล่าง

```js
var answer1 = "It's alright";             // Single quote inside double quotes
var answer2 = "He is called 'Johnny'";    // Single quotes inside double quotes
var answer3 = 'He is called "Johnny"';    // Double quotes inside single quotes
```

---

## ตัวเลข (Numbers) ใน JavaScript

​	ภายใน JavaScript จะมีชนิดของตัวเลขแค่ชนิดเดียว สามารถเขียนโดยมีทศนิยมหรือไม่มีทศนิยมก็ได้

```js
var x1 = 34.00;     // Written with decimals
var x2 = 34;        // Written without decimals
```

​	ตัวเลขที่มีจำนวนมากหรือทศนิยมที่น้อยมาก ๆ สามารถเขียนได้ด้วยสัญกรณ์วิทยาศาสตร์ (เลขชี้กำลัง)

```js
var y = 123e5;      // 12300000
var z = 123e-5;     // 0.00123
```

---

## Booleans ใน JavaScript

​	Boolean สามารถมีค่าได้แค่ 2 อย่างคือ `true` กับ `false` เท่านั้น ตามตัวอย่างด้านล่าง

```js
var x = 5;
var y = 5;
var z = 6;
(x == y)       // Returns true
(x == z)       // Returns false
```

> Boolean นั้นมักจะใช้ในการทอสอบเงื่อนไง

---

## Array ใน JavaScript

​	Array ใน JavaScript จะต้องเขียนอยู่ในวงเล็บสี่เหลี่ยมหรือ square brackets (`[]`) 

item ที่อยู่ใน Array จะถูกแบ่งด้วยคอมม่า ในตัวอย่างด้านล่างจะเป็นการสร้าง Array ที่มีชื่อว่า `cars` และเก็บข้อมูลชื่อรถสามชนิด

```js
var cars = ["Saab", "Volvo", "BMW"];
```

​	Array index จะเริ่มต้นด้วย 0 นั้นหมายความว่า item แรกก็คือ `cars[0]` และ item ที่สองคือ `cars[1]`

> ในส่วนของ Array สามารถดูเพิ่มเติมได้ที่หัวข้อ JS Array

---

## วัตถุ (Object) ใน JavaScript

​	ในการสร้างวัตถุจะต้องถูกเขียนให้อยู่ภายใน `{}` และจะถูกแบ่งด้วยคอมม่า

```js
var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```

​	ตัวอย่างด้านบนเป็นการสร้างวัตถุที่ชื่อว่า person โดยจะมี 4 properties คือ fiestName, lastName, age, eyeColor

> ในส่วนของ Array สามารถดูเพิ่มเติมได้ที่หัวข้อ JS Object

---

## ตัวดำเนินการที่ชื่อว่า typeof

​	ใน JavaScript เราสามารถใช้ `typeof` เพื่อดูว่าข้อมูลนั้น ๆ เป็นข้อมูลชนิดไหน ตามตัวอย่างด้านล่าง

```js
typeof ""             // Returns "string"
typeof "John"         // Returns "string"
typeof "John Doe"     // Returns "string"
typeof 0              // Returns "number"
typeof 314            // Returns "number"
typeof 3.14           // Returns "number"
typeof (3)            // Returns "number"
typeof (3 + 4)        // Returns "number"
```

---

## Undefined

​	ใน JavaScript ถ้าเราประกาศตัวแปรโดยที่ไม่ได้กำหนดค่าให้กับตัวแปรนั้น ตัวแปรนั้นจะมีค่าเป็น `undefined` ชนิดของข้อมูลก็คือ `undefined` ตามตัวอย่างด้านล่าง

```js
var car;    // Value is undefined, type is undefined
```

​	ตัวแปรทุกตัวเราสามารถกำหนดค่าให้มันเป็นค่าว่างได้ โดยกำหนดค่านั้นให้เป็น `undefined` และ  ชนิดของข้อมูลก็จะเป็น `undefined` ตัวอย่างเช่น

```js
car = undefined;    // Value is undefined, type is undefined
```

---

## ค่าว่าง (Empty Values)

​	ค่าว่างนั้นไม่เหมือนกับ `defined` ค่าว่างนั้นไม่มีข้อมูลแต่มีชนิดของข้อมูลอยู่ ตัวอย่างเช่น

```js
var car = "";    // The value is "", the typeof is "string"
```

---

## Null

​	`null` หมายถึง ไม่มีข้อมูลอะไรเลย แต่ใน JavaScript ชนิดข้อมูลของ `null` คือ Object ถ้าเราต้องการให้ Object ไหนไม่มีค่า เราสามารถกำหนดค่า `null` ให้กับมันได้ ตัวอย่างเช่น

```js
var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
person = null;    // ตรงนี้ person มีค่าเป็น null, แต่ยังคงเป็น object อยู่
```

​	นอกจากนั้นเรายังสามารถใช้ `undefined` ในการทำให้ Object นั้นไม่มีค่า แต่จะแตกต่างกันตรงที่เมื่อกำหนดให้เป็น `undefined` ทั้งค่าข้อมูลและชนิดของตัวแปร จะกลายเป็น `undefined`

```js
var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
person = undefined;   // ตรงนี้ทั้ค่าข้อมูลและชนิดของข้อมูลจะเป็น undefined
```

---

## ข้อแตกต่างระหว่าง Undefined และ Null

​	`undefined` และ `null` มีค่าเดียวกันแต่มีชนิดข้อมูลที่แตกต่างกัน

```js
typeof undefined           // undefined
typeof null                // object

null === undefined         // false
null == undefined          // true
```

---

## Primitive Data

​	Primitive Data เป็นค่าข้อมูลดั้งเดิมที่ไม่มีการเพิ่ม properties หรือ methods

ตัวดำเนินการ `typeof` สามารถแสดงค่ากับข้อมูลแบบ Primitive ได้

```js
typeof "John"              // Returns "string"
typeof 3.14                // Returns "number"
typeof true                // Returns "boolean"
typeof false               // Returns "boolean"
typeof x                   // Returns "undefined" (ถ้า x ไม่มีค่า)
```

---

## Complex Data

​	ตัวดำเนินการ `typeof` สามารถแสดงค่าหนึ่งในสอง ของ Complex Data ได้

```js
typeof {name:'John', age:34} // Returns "object"
typeof [1,2,3,4]             // Returns "object" (ไม่ใช่ "array", อ่านเพิ่มเติมด้านล่าง)
typeof null                  // Returns "object"
typeof function myFunc(){}   // Returns "function"
```

​	ตัวดำเนินการ `typeof` สามารถแสดงค่าเป็น `object` สำหรับ Array เพราะ ใน JavaScript Array เป็น Object







