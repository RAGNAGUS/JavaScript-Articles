# JavaScript Statements

---

```js
var x, y, z;    // Statement 1
x = 5;          // Statement 2
y = 6;          // Statement 3
z = x + y;      // Statement 4
```

โปรแกรมคอมพิวเตอร์ทำงานเป็นรายการคำสั่งเพื่อที่จะถูกดำเนินการโดยคอมพิวเตอร์

ในภาษาโปรแกรมคำสั่งต่าง ๆ จะถูกเรียกว่า Statements

โปรแกรม JavaScript จะดำเนินการ Statements ไปทีละลำดับตามตัวอย่างด้านบน

ใน HTML และ JavaScript จะถูกดำเนินการโดย web browser

----

## JavaScript Statements

​	statements ใน JavaScript จะประกอบไปด้วย Values, Operators, Expressions, Keywords, and Comments

ใน statement ด้านล่างจะเป็นการเขียนคำว่า "Hello Dolly" ภายใน HTML element ที่มี id ="demo"

```js
document.getElementById("demo").innerHTML = "Hello Dolly.";
```

โปรแกรม JavaScript ส่วนใหญ่จะมี statements หลายคำสั่ง โดย statement เหล่านั้นจะถูกดำเนินการไปทีละคำสั่งตามลำดับที่ถูกเขียนไว้

> JavaScript Program และ JavaScript Statements โดยส่วนมากจะถูกเรียกว่า JavaScript code

---

## การใช้ Semicolons ;

​	Semicolons จะเป็นตัวแบ่งแยกการทำงานของแต่ละ statements ใน JavaScript โดย Semicolon จะถูกเพิ่มเข้าไปในส่วนท้ายของแต่ละคำสั่ง

```js
var a, b, c;     // Declare 3 variables
a = 5;           // Assign the value 5 to a
b = 6;           // Assign the value 6 to b
c = a + b;       // Assign the sum of a and b to c
```

​	หากเราคั่นด้วย Semicolons JavaScript จะอนุญาตให้ใช้หลายคำสั่งในหนึ่งบรรทัดได้

 ```js
a = 5; b = 6; c = a + b;
 ```

> เราจะเห็นได้ว่าบางเว็บไซต์จะไม่มี Semicolons เพราะในการเขียนโปรแกรมภาษา JavaScript ไม่จำเป็นต้องมี Semicolons ต่อท้ายเสมอ แต่เพื่อการแบ่งแยกคำสั่งอย่างชัดเจน และป้องกันการเกิดปัญหาที่ตามมา ผมจึงแนะนำให้ใส่ Semicolons ต่อท้ายในแต่คำสั่ง

---

## การเว้นวรรค (White Space)

​	JavaScript จะไม่สนใจว่าเราเว้นวรรคแค่ไหน เราสามารถเว้นวรรคเพื่อที่จะทำให้โค้ตเราอ่านได้ง่ายยิ่งขึ้นได้ ตามตัวอย่างด้านล่าง ในแต่ละคำสั่ง เราจะได้ผลลัพธ์เหมือนกัน

```js
var person = "Hege";
var person="Hege";
```

​	ในการเขียน JavaScript เราควรเว้นวรรคในแต่ละตัวดำเนินการ ( = + - * / ) ตัวอย่างเช่น

```js
var x = y + z;
```

---

## ความยาวของโค้ตและการเว้นบรรทัด

​	เพื่อที่จะให้โค้ตของเราอ่านง่ายขึ้น โปรแกรมเมอร์ส่วนใหญ่จะพยายามหลีกเลี่ยงไม่ให้โค้ตยาวเกิน 80 ตัวอักษร หากคำสั่งของเราไม่พอดีในหนึ่งบรรทัด เราสามารถเว้นบรรทัดลงมาหลังจากตัวดำเนินการได้ตามในตัวอย่าง

```js
document.getElementById("demo").innerHTML =
"Hello Dolly!";
```

---

## บล็อคของโค้ต (Code Blocks)

​	คำสั่งของ JavaScript สามารถทำเป็นกลุ่มให้อยู่ด้วยกันโดยให้คำสั่งทั้งหมดอยู่ในปีกกา {...} จุดประสงค์ของ Code blocks คือการกำหนดคำสั่งที่จะดำเนินการร่วมกัน เช่นกันกับการใช้ฟังก์ชั่น `function` โดยฟังก์ชั่นนั้นจะทำงานโดยมีหลายคำสั่งอยู่ด้านใน ตัวอย่างเช่น

```js
function myFunction() {
  document.getElementById("demo1").innerHTML = "Hello Dolly!";
  document.getElementById("demo2").innerHTML = "How are you?";
}
```

---

## คีย์เวิร์ดใน JavaScript

​	คำสั่งหรือ statements มักจะขึ้นต้นด้วย keyword เพื่อระบุตัวดำเนินการของ JavaScript ที่จะดำเนินการ

| Keyword       | Description                                                  |
| ------------- | :----------------------------------------------------------- |
| break         | ยุติ switch หรือลูปรูปแบบต่าง ๆ                                    |
| continue      | หยุดคำสั่งต่อจากนี้แล้วเริ่มคำสั่งใหม่จากด้านบน                           |
| debugger      | Stops the execution of JavaScript, and calls (if available) the debugging function |
| do ... while  | ดำเนินการคำสั่งซ้ำเรื่อย ๆ จนกว่าเงื่อนไขจะเป็นเท็จ                     |
| for           | ดำเนินการคำสั่งตราบเท่าที่เงื่อนไขเป็นจริง                             |
| function      | ประกาศฟังก์ชั่น                                                  |
| if ... else   | การทำงานของคำสั่งจะถูกดำเนินการตามเงื่อนไข                         |
| return        | ออกจากฟังก์ชั่น                                                  |
| switch        | การทำงานของแต่ละคำสั่งจะถูกดำเนินตามกรณีต่าง ๆ                      |
| try ... catch | ดำเนินการจัดการข้อผิดพลาดของบล็อกคำสั่ง                             |
| var           | ประกาศตัวแปร                                                  |