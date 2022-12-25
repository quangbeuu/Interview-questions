# Câu hỏi phỏng vấn Javascript

<img src="https://www.classcentral.com/report/wp-content/uploads/2022/06/JavaScript-BCG-Banner-icons.png"/>


## Mục lục
<ul>
  <li>
    <a href="#cau1">1. Các kiểu dữ liệu trong Javascript?</a>  
  </li>
  <li>
    <a href="#cau2">2. Sự khác biệt giữa toán tử "==" và "===" là như thế nào?</a>  
  </li>
  <li>
    <a href="#cau3">3. Phân biệt var, let và const?</a>  
  </li>
  
   <li>
    <a href="#cau4">4. Lập trình hướng đối tượng (OOP) trong Javascript?</a>  
  </li>
</ul>


## Câu hỏi
<b id="cau1">1. Các kiểu dữ liệu trong Javascript?</b>
<p>
  - Có 2 kiểu dữ liệu: <b> Kiểu nguyên thủy </b> và <b>object</b>
</p>

**a. Kiểu nguyên thuỷ**   


***String*** - biểu diễn một mảng ký tự hay một chuỗi. Kiểu chuỗi trong javascript có thể sử dụng một cặp dấu ngoặc kép hoặc dấu ngoặc kép đơn.

```js
 var str = "Vivek Singh Bisht"; //sử dụng dấu ngoặc kép
 var str2 = 'John Doe'; // sử dụng dấu ngoặc đơn
```

***Number*** - biểu diễn cả số nguyên và số thực.

```js
var x = 3; // số nguyên
var y = 3.6; // số thực
```

***BigInt*** - kiểu dữ liệu này được sử dụng để lưu trữ các số vượt quá giới hạn của kiểu dữ liệu Number. Nó có thể lưu trữ các số nguyên lớn và được biểu diễn bằng cách thêm “n” vào một chữ số nguyên.

```js
var bigInteger =  234567890123456789012345678901234567890;
```

***Boolean*** - kiểu luận lý, có hai giá trị là *true* và *false*. Thường được dùng với điều kiện.

```js
var a = 2;
var b =  3;
var c =  2;
(a == b) // trả về false
(a == c) // trả về true
```

***undefined*** - khi giá trị của một biến là không xác định.

```js
var x; // giá trị của x là undefined
var y = undefined; // ta cũng có thể gán một biến là undefined
```

***null*** - biểu diễn giá trị null. Vì JavaScript là case-sensitive, null sẽ không giống với` Null`, `NULL`, hoặc bất kỳ biến thể khác.

```js
var z = null;
```

***Symbol*** - mới được giới thiệu trong ES6. Nó lưu trữ các giá trị duy nhất và ẩn danh.

```js
var symbol1 = Symbol('symbol');
```
**b. Kiểu object** - nếu dữ liệu không phải là kiểu nguyên thuỷ thì tất cả đều là object  

```js
// Tập hợp dữ liệu dạng key-value 

var obj1 = {
   x:  43,
   y:  "Hello world!",
   z: function(){
      return this.x;
   }
}
      
// Tập hợp dữ liệu dạng danh sách
      
var array1 = [5, "Hello", true, 4.1];  
```

<b id="cau2">2. Sự khác biệt giữa toán tử "==" và "===" là như thế nào?</b>

<p>
   * == (abstract equality): dùng để kiểm tra xem 2 phần tử được kiểm tra đó có bằng nhau không, nhưng nó chỉ xét về giá trị mà không quan tâm đến kiểu dữ liệu của 2 phần tử đó 
  <br/>
   * === (strict equality): ngoài so sánh giá trị n còn quan tâm đến cả kiểu dữ liệu của các phần tử được so sánh 
   <br/>
 Ví dụ:

```js
var x = 2;
var y = "2";
(x == y)  // Trả về true vì cả hai cùng giá trị

(x === y) // Trả về false vì typeof x là "number" còn typeof y là "string
```
  <br/>
</p>


<b id="cau3">3. Phân biệt var, let và const?</b>
<p>
  <b>* Scope:</b> 
  <br/>
    - Xác định phạm vi bạn có thể truy cập các biến và hàm trong ứng dụng của bạn
  <br/>
    - Có 3 loại Scope: 
    <ul>
      <li>
        <b><i>Global scope</i></b>: phạm vi toàn cầu
      </li>
      <li>
        <b><i>Function scope</i></b>: phạm vi hàm
      </li>
      <li>
        <b><i>Block scope</i></b>: phạm vi khối (là một đoạn mã được giới hạn bởi {})
      </li>
    </ul>   
</p>

<img src="https://miro.medium.com/max/1400/1*KxHwVbB0zhnSVrhrWtT-gg.webp"/>
<b>* Hoisting là gì?:</b> 

<p>
 - <b>Hoisting</b> là một cơ chế JavaScript trong đó các khai báo biến và hàm được di chuyển lên đầu phạm vi của chúng trước khi thực thi mã
</p>
<img src="https://www.tutorialsteacher.com/Content/images/js/hoisting.png"/>

***A. var***
<br/>
<b>* Có phạm vi  <b><i>global scope</i></b> và  <b><i>function scope</i></b>:</b> 
<br/>
<p>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+ Global scope: Khi var dc khai báo bên ngoài 1 hàm
    <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+ Function scope: Khi var dc khai báo bên trong 1 hàm (có nghĩa là biến chỉ truy cập đc trong funciton)
</p>

```js
var greeter = "hey hi";

function newFunction() {
   var hello = "hello";
}
```
<b>* Ví dụ:</b> 
<p>
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; + greeter có phạm vi <b><i>global scope</i></b> vì nó tồn tại bên ngoài một <b>function</b>
  <br/>
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; + hello có phạm vi <b><i>function scope</i></b> => Do đó, ta ko thể truy cập biến hello ở bên ngoài hàm
</p>

```js
var greeter = "hey hi";

function newFunction() {
   var hello = "hello";
}
console.log(hello); // error: hello is not defined
```
<b>* Có thể khai báo lại và update:</b> 


```js

var greeter = "hey hi";
var greeter = "say Hello instead";

// Hoặc 

var greeter = "hey hi";
greeter = "say Hello instead";

```

<b>* Hoisting of var:</b> 

<p>
  - <b>var</b> các biến được nâng lên đầu phạm vi của nó và được khởi tạo với giá trị <b>undefined</b>.
</p>

```js

var greeter;
console.log(greeter); //greeter is undefined
greeter = "say hello"

```

***B. let***

<b>* Có phạm vi <b><i>block scope</i></b>:</b> 

```js

let greeting = "say Hi";
let times = 4;

if (times > 3) {
   let hello = "say Hello instead";
   console.log(hello);//"say Hello instead"
}
console.log(hello) // hello is not defined

```
<b>* Có thể update nhưng không thể khai báo lại:</b> 


```js

let greeting = "say Hi";
let greeting = "say Hello instead";//error: Identifier 'greeting' has already been declared

```
<p>Tuy nhiên, nếu cùng một biến được xác định trong các phạm vi khác nhau, sẽ không có lỗi.</p>


```js

let greeting = "say Hi";
if (true) {
   let greeting = "say Hello instead";
      console.log(greeting);//"say Hello instead"
    }
console.log(greeting);//"say Hi"

```

<b>* Hoisting of let:</b> 

<p>
- Giống như <b>var</b>, các khai báo <b>let</b> được đưa lên trên cùng
<br/>
  - Không giống như từ khóa <b>var</b> khởi tạo là <b>undefined</b>, từ khóa <b>let</b> không được khởi tạo. 
<br/>
- Nếu bạn cố gắng sử dụng <b>let</b> trước khi khai báo, bạn sẽ nhận được lỗi <b>Reference Error</b>.
</p>


***C. const***

<b>* Có phạm vi <b><i>block scope</i></b>:</b> 

<b>* Không thể update cũng như khai báo lại</b> 


```js

const greeting = "say Hi";
greeting = "say Hello instead";//error : Assignment to constant variable. 

// Cũng không phải cái này: 

const greeting = "say Hi";
const greeting = "say Hello instead";//error : Identifier 'greeting' has already been declared

```

<b>* Hoisting of const:</b> 

<p>
  - Cũng giống như <b>let</b>, khai báo <b>const</b> được nâng lên đầu nhưng không được khởi tạo.
</p>

<b id="cau4">4. Lập trình hướng đối tượng (OOP) trong Javascript?</b>

<img src="https://i.ytimg.com/vi/e--K9kCz-v0/maxresdefault.jpg"/>


<p>
  - <b>Javascript</b> vừa là ngôn ngữ <b>OOP (hướng đối tượng)</b> vừa là ngôn ngữ <b>hướng chức năng (Functional language)</b>
</p>
<b>* 4 tính chất của OOP:</b>
<ul>
  <li>
    Tính đóng gói <b>(encapsulation)</b>
  </li>
  <li>
    Tính trừu tượng <b>(abstraction)</b>
  </li>
  <li>
    Tính đa hình <b>(polymorphism)</b>
  </li>
  <li>
    Tính thừa kế <b>(inheritance)</b>
  </li>
</ul>

<b>* Hiểu hơn về tính chất của OOP thông qua ví dụ sau:</b>


```js
class Animal {
 constructor(name) {
  this.name = name;
 }

 eat() {
  console.log('Animal eats some food');
 }
 
 run() {
  console.log('Animal runs');
 } 
}

class Dog extends Animal {
 constructor(name, color) {
  super(name);
  this.color = color;
 }

 run() {
  console.log('Dog runs');
 }
}

class Cat extends Animal {
 constructor(name, color) {
  super(name);
  this.color = color;
 }

 run() {
  console.log('Cat runs');
 }
}

const dog = new Dog('Kiki','black');
const cat = new Cat('Meo', 'white');

dog.eat();
cat.eat();
```

**a. Tính đóng gói** 

<p>
  - <b>Tính đóng gói</b> cho thấy rằng các <b>thuộc tính (property)</b>: <b>name</b> của <b>Animal</b>, <b>color</b> của <b>Dog, Cat</b> đều được che giấu. Chúng ta không thể sửa trực tiếp đc.
  <br/>
  - Nó được gọi là các <b>thuộc tính nội tại</b> của đối tượng, nó chỉ đc cập nhật khi ta cung cấp <b>method (phương thức)</b> để thao tác trên nó
</p>

**b. Tính trừu tượng** 

<p>
  - <b>Tính trừu tượng</b> được thể hiện khi chúng ta tạo mới một <b>instance (thể hiện)</b> của đối tượng (vd: const dog = new Dog('Kiki','black')), 
  chúng ta ko cần quan tâm sâu bên trong nó làm cái gì
  <br/>
  - <b>VD</b>: đối tượng <b>Animal</b> ta chỉ cần quan tâm nó có thuộc tính <b>name</b> và phương thức <b>eat</b>
  <br/>
  => Khi tạo một Animal ta truyền dữ liệu, và gọi eat là xong, không cần quan tâm eat được cài đặt như thế nào.
</p>

**c. Tính đa hình** 

<p>
  - <b>Tính đa hình</b> được thể hiện khi gọi một phương thức nhưng cách hoạt động là khác nhau.
  <br/>
  
  - <b>Ví dụ</b>: Bạn thấy cùng một phương thức <b>run</b> nhưng <b>Dog, Cat</b> thực hiện khác nhau. 
  <br/>
  - <b>Dog</b> in ra console.log(‘Dog runs’) và <b>Cat</b> in ra console.log(‘Cat runs’);
</p>
