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
  
  <li>
    <a href="#cau5">5. Callback function là gì? </a>  
  </li>
  
  <li>
    <a href="#cau6">6. Hãy cho biết Falsy value và Truthy value là gì? Có những falsy value nào trong JavaScript? </a>  
  </li>
  
  <li>
    <a href="#cau7">7. Sự khác biệt giữa undefined và null là gì? </a>  
  </li>
  
  <li>
    <a href="#cau8">8. DOM là gì? </a>  
  </li>
  
  <li>
    <a href="#cau9">9. Sự khác biệt giữa i++ và ++i là gì?</a>  
  </li>
  
  <li>
    <a href="#cau10">10. Web storage là gì??</a>  
  </li>
  
  <li>
    <a href="#cau11">11. Closure là gì ?</a>  
  </li>
  
  <li>
    <a href="#cau12">12. Coercion là gì ?</a>  
  </li>
  
  <li>
    <a href="#cau13">13. Cách để lặp qua các Object trong Javascript?</a>  
  </li>
  
  
  <li>
    <a href="#cau14">14. Cách để lặp qua các Array trong Javascript?</a>  
  </li>
  
  <li>
    <a href="#cau15">15. Thuộc tính NaN là gì?</a>  
  </li>
  
  <li>
    <a href="#cau16">16. Giải thích về bubbling event và cách để ngăn chặn nó?</a>  
  </li>
  
  <li>
    <a href="#cau17">17. Cách để copy một mảng?</a>  
  </li>
  
  <li>
    <a href="#cau18">18. Destructuring là gì?</a>  
  </li>
  
  <li>
    <a href="#cau19">19. Code splitting là gì?</a>  
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

**d. Tính thừa kế**

<p>
  - <b>Tính thừa kề</b> thể hiện khi <b>Dog, Cat</b> thừa kế từ <b>Animal</b>. Do đó chúng đều có các thuộc tính, phương thức của <b>Animal</b>.
</p>


<b id="cau5">5. Callback function là gì?</b>
<div align="center">
  <img src="https://allma.si/blog/wp-content/uploads/2020/10/callback-in-javascript.png" height="500"/>
</div>

<p>
  - <b>Callback function (hàm gọi lại)</b> là một hàm được thực thi sau khi một hàm khác đã thực thi sau.
  <br/>
  - Một <b>callback function</b> là một hàm được truyền cho một hàm khác như một đối số và được thực thi sau khi một số tác vụ đã hoàn thành. 
</p>

<b>- Ví dụ:</b>

```js

function writeBlog(topic, callback) {
  alert(`Starting my ${topic} blog.`);
// then execute the callback function that was passed
  callback();
}

writeBlog('JS', function() {
  alert('Finished my blog!');
});

```

<p>
  - Nếu bạn chạy đoạn code, bạn sẽ nhận được hai thông báo. Thông báo đầu tiên <b>“Starting my JS blog.”</b> và thông báo thứ hai: <b>“Finished my blog!”</b>
</p>

<b id="cau6">6. Hãy cho biết Falsy value và Truthy value là gì? Có những falsy value nào trong JavaScript?</b>

<p>
  - <b>Falsy values</b> là những giá trị trong Javascripts mà khi ép kiểu về Boolean, thì sẽ cho ra giá trị <b><i>False</i></b>.
  <br/>
  - <b>Truthy values</b> là những giá trị mà khi ép kiểu về Boolean, thì sẽ cho ra giá trị <b><i>True</i></b>
</p>

<b>* 7 giá trị falsy values: </b>

<ul>
  <li>number 0</li>
  <li>BigInt 0n</li>
  <li>undefined</li>
  <li>null</li>
  <li>NaN</li>
  <li>false</li>
  <li>""</li>
</ul>

<p>
  => Tất cả những kiểu dữ liệu trên sẽ thành false trong các điều kiện.
</p>


<b id="cau7">7. Sự khác biệt giữa undefined và null là gì?</b>

**Null**

<p>
  - Có nghĩa là một giá trị rỗng hoặc không tồn tại 
  <br/>
  - <b>null</b> được gán cho một biến như là một đại diện không có giá trị 
  <br/>
  - <b>typeof</b> của null là <b>object</b>
</p>

```js
var test1 = null;
console.log(typeof test1);
// object
```

**Undefined**

<p>
  - Có nghĩa là một biến đã được khai báo nhưng giá trị của biến đó chưa được xác định
  <br/>
  - <b>typeof</b> của undefined là <b>undefined</b>
</p>

```js
var test2;
console.log(test2);
// undefined
console.log(typeof test2);
// undefined
```

<b id="cau8">8. DOM là gì?</b>

<p>
  - DOM là viết tắt của Document Object Modal
  <br/> 
  - DOM đại diện cho một tài liệu HTML có cấu trúc cây logic 
  <br/> 
  - DOM có cấu trúc được định nghĩa thành các <b>đối tượng, phương thức, thuộc tính</b> để có thể truy xuất dễ dàng. Chúng được coi như các node và được biểu diễn dưới dạng <b>DOM Tree</b>.
  <br/>
  - Ví dụ về cách code HTML được chuyển đổi thành DOM:
</p>
<img src="https://github.com/Ren0503/fullstack-interviews/raw/main/frontend/javascript/assets/dom.png"/>


<b id="cau9">9. Sự khác biệt giữa i++ và ++i là gì?</b>

<p>
  - Cả <b>i++</b> và <b>++i</b> đều sẽ tăng giá trị lên 1 
  <br/>
  - Tuy nhiên: 
  <ul>
    <li><b>i++</b> được gọi là bước tăng hậu tố (postfix increment) sẽ trả về giá trị trước khi nó được tăng lên</li>
    <li><b>++i</b> được gọi là bước tăng tiền tố (prefix increment) sẽ trả về giá trị sau khi nó được tăng</li>
  </ul>
</p>

```js
let i = 0;

i++ // Will evaluate to 0
++i // Will evaluate to 1
```

<b id="cau10">10. Web storage là gì?</b>
<p>
  - Web storage là một API cung cấp cách để trình duyệt lưu trữ các kặp key-value cho trình duyệt của người dùng cục bộ (local) 
  <br/>
  - Web storage cung cấp 2 cách để lưu trữ dữ liệu: 
  
  <ul>
    <li>
      <b>Local storage</b> - lưu trữ dữ liệu cho client mà không có ngày hết hạn.
    </li>
    <li>
      <b>Session storage</b> - chỉ lưu trữ dữ liệu cho một phiên. Dữ liệu sẽ biến mất khi trình duyệt bị đóng. 
    </li>
  </ul>
</p>

<p>
  - Dưới đây là một ví dụ về cách bạn có thể lưu, truy cập và xóa một mục khỏi sessionStorage
</p>

```js
// Save data to sessionStorage
sessionStorage.setItem('favoriteColor', 'gray');

// Get the color from the sessionStorage
let data = sessionStorage.getItem('favoriteColor');
console.log(data);

// Remove saved color preset from sessionStorage
sessionStorage.removeItem('favoriteColor');

// Remove ALL the saved data from sessionStorage
sessionStorage.clear();
```
<p>
  - Và đây là cách bạn có thể làm điều tương tự bằng cách sử dụng localStorage:
</p>


```js
// Save data to localStorage
localStorage.setItem('favoriteColor', 'gray');

// Get the color from the localStorage
let data = localStorage.getItem('favoriteColor');
console.log(data);

// Remove saved color preset from localStorage
localStorage.removeItem('favoriteColor');

// Remove ALL the saved data from localStorage
localStorage.clear();
```

<b id="cau11">11. Closure là gì?</b>

<p>
  
  - <b>Closure</b> là một tập hợp các hàm được viết lồng vào trong một hàm khác, và nó cho phép bạn truy cập vào biến của hàm khác ngoài các biến của nó và các biến global (biến toàn cục).
  
  - <b>Closure</b> vẫn có khả năng lưu trữ được các biến bên trong nó, hay nói một cách khác mỗi khi bạn <b><i>return</i></b> một hàm hoặc gán một hàm cho một biến thì hàm đó sẽ mang theo giá trị tất cả các biến mà nó phụ thuộc.
</p>


```js

function sayHello(){      //parent function
  let message = "Hi";
  function sayHi(){       //inner function
    console.log(message)
  }
}

const fnc = sayHello();
fnc()                     //Hi

```

<p>
  
  - Không ai có thể truy cập được biến <b>message</b> ngoài function <b>sayHello</b> nhưng nhờ <b>closure</b> function <b>sayHi</b> vẫn có quyền truy cập vào biến <b>message</b>.
  
</p>

<b id="cau12">12. Coercion là gì?</b>

<p>
  - <b>Coercion</b> là cách thức chuyển đổi type của các giá trị trong Javascript.
  <br/>
  - <b>Coercion</b> có 2 kiểu là: 
  
  - <b><i>explicit</i></b> (tường minh - chuyển dữ liệu nhìn dc qua mã)
  
  - <b><i>implicit</i></b> (không tường minh - ngầm định)
</p>

<p>
  - Đây là một ví dụ về <i>explicit coercion</i>
</p>

```js

var a = "42";
var b = Number(a);
a; // "42"
b; // 42 -- the number!

```

<p>
  - Đây là một ví dụ về <i>implicit coercion</i>
</p>


```js

var a = "42";
var b = a \* 1; // "42" implicitly coerced to 42 here
a; // "42"
b; // 42 -- the number!

```
**Equality operator (==)**

```js

console.log(69 == "69"); // true

```

<p>
  - Điều này xả ra là do trước khi phép so sánh thực sự xảy ra, JS sẽ thực hiện <b>coercion</b>. Nói cách khác, nếu 2 value có cùng <b><i>type</i></b>, thì ta sẽ thực hiện so sánh luôn, nhưng nếu chúng khác <b><i>type</i></b>, JS sẽ cố gắng để convert chúng về cùng 1 type rồi mới so sánh. 
  
 <br/>
  - Ở đây 69 và '69' đã được convert về cùng 1 type là number. 
</p>

***Lưu ý** - <b>coercion</b> không tuân theo 1 logic nào cả mà nó tuân theo 1 số rules mà ta phải nhớ 

**a. So sánh number và string** 

<p>
  <b>string</b> sẽ được convert thành <b>number</b>, sau đó so sánh.
  <br/>
  => Từ đó dẫn tới 2 trường hợp: 
  
  - Một là <b>string</b> convert được thành number (ví dụ các string như '10', '1235',...), việc so sánh là bình thường. 
  
  - Hai là <b>string</b> không thể convert đc thành number (ví dụ string như 'abc', 's123',... ), các giá trị này sẽ convert thành <b>NaN</b> => Kết quả luôn trả về <b>false</b>
</p>

**b. So sánh boolean với các type values khác** 

<p>
- Đầu tiền boolean value (true => 1, false => 0) thành number, rồi mới so sánh. 
<br/>  
- Ví dụ "1" == true sẽ được đổi thành 1 == 1 do true được convert thành number 1 và string "1" convert thành number 1 => dẫn tới result là <b>true</b>.
</p>

**c. Strict equality operator (===)** 

<p>- Thằng này chỉ compare 2 value, ko coercion (ko convert type)</p>


**d. Operator (+,-,*,/)** 

<p>
  - Khi so sánh <b>number</b> với <b>string</b>, ngoại trừ toán tử <b>+</b> sẽ tiến hành chuyển đổi <b>number</b> thành <b>string</b> rồi tiến hành phép nối string
  - Còn các toán tử khác <b>(-,*,/)</b> đều sẽ convert <b>string</b> thành <b>number</b> và tiến hành phép toán như thông thường
  - Trong trường hợp ko convert được nó sẽ return về <b>NaN</b>
</p>

```js

4 + "3"; // "43"
4 - "3"; // 1
"4" * "3"; //12
"4" / 3; //1.33333

4 + "a";
("4a");
4 - "a"; // NaN
4 * "a"; // NaN
4 / "a"; //NaN

```

<b id="cau13">13. Cách để lặp qua các Object trong Javascript?</b>

<p>
  <b>Cách thứ nhất:</b> sử dụng <b>for...in</b> => sẽ lặp qua tất cả các key của obj. Chúng ta có thể ktra bằng lệnh <b>obj.hasOwnProperty(property)</b> trước khi sử dụng nó.
</p>

```js

const object = { a: 1, b: 2, c: 3 };

for (const property in object) {
  console.log(`${property}: ${object[property]}`);
}

// expected output:
// "a: 1"
// "b: 2"
// "c: 3"

```

<p>
  <b>Cách thứ hai:</b> sử dụng <b>Object.keys()</b> => sẽ lặp qua tất cả các key của obj. 
</p>

```js

const object1 = {
  a: 'somestring',
  b: 42,
  c: false
};

console.log(Object.keys(object1));
// expected output: Array ["a", "b", "c"]


Object.keys(obj).forEach(function (property) {
  ...
})

```

<p>
  <b>Cách thứ ba:</b> sử dụng <b>Object.getOwnPropertyNames()</b>
</p>

```js

const object1 = {
  a: 1,
  b: 2,
  c: 3
};

console.log(Object.getOwnPropertyNames(object1));
// expected output: Array ["a", "b", "c"]

```

<p>
  <b>Cách thứ tư:</b> sử dụng <b>Object.entries()</b>
</p>

```js

const object1 = {
  a: 'somestring',
  b: 42
};

for (const [key, value] of Object.entries(object1)) {
  console.log(`${key}: ${value}`);
}

// expected output:
// "a: somestring"
// "b: 42"

```


<b id="cau14">14. Cách để lặp qua các Array trong Javascript?</b>


<p>
  <b>Cách thứ nhất:</b> sử dụng <b>for</b>, <b>let</b> có phạm vi <b>block scope</b> nên ta nên khai báo biến i bằng <b>let</b>
</p>

```js
for (let i = 0; i <arr.length; i ++) {
  ...for (let i = 0; i <arr.length; i ++)
}
```

<p>
  <b>Cách thứ hai:</b> sử dụng <b>forEach</b>, (nhược điểm của thằng này là ko sử dụng được <b>break</b>)
</p>

```js

arr.forEach(function (el, index) {
  ...
}).

```

<b id="cau15">15. Thuộc tính NaN là gì?</b>

<p>
  - Thuộc tính NaN biểu diễn một giá trị <b>Not-a-Number</b> (một giá trị ko phải là số)
  <br/>
  
  - Muốn kiểm tra xem một giá trị có phải <b>NaN</b> có thể dùng hàm <b>isNaN()</b>
</p>


```js

isNaN("Hello"); // Returns true
isNaN(345); // Returns false
isNaN("1"); // Returns false, since '1' is converted to Number type which results in 0 ( a number)
isNaN(true); // Returns false, since true converted to Number type results in 1 ( a number)
isNaN(false); // Returns false
isNaN(undefined); // Returns true

```


<b id="cau16">16. Giải thích về bubbling event và cách để ngăn chặn nó?</b>

<p>
  - <b>Bubbling event</b> là khái niệm trong đó một event kích hoạt ở phần tử sâu nhất và kích hoạt trên các phần tử mẹ theo thứ tự lồng vào nhau. Do đó, khi click vào một phần tử con, sự kiện click của phần tử cha cũng sẽ được kích hoạt.
<br/>
  - Một cách để ngắn <b>sự kiện nổi bọt (Bubbling event)</b> là sử dụng <b>event.stopPropagation()</b> hoặc <b>event.cancelBubble</b>
  
</p>
<div align="center">
<img src="https://user-images.githubusercontent.com/29374426/139020948-a4570605-5286-4d66-9ef6-d20ba1e16b0c.png"/>
</div>


<b id="cau17">17. Cách để copy một mảng?</b>

<p>
  - Để có thể copy một mảng, chúng ta có thể sử dụng một trong các cách dưới đây: 
</p>

**a. Sử dụng hàm slice:**

```js

const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];

console.log(animals.slice());
// expected output: Array ["ant", "bison", "camel", "duck", "elephant"]

```


**b. Sử dụng hàm JSON.stringify() và JSON.parse (deep copy):**

```js

// array of objects
const objsArr = [{ name: "John Doe" }, { name: "Roy Daniel" }];

// first convert the array into a string
// using the JSON.stringify() method
const objsArrStr = JSON.stringify(objsArr);

// conver the string again to array of objects
// using the JSON.parse() method
const objsArrDeepCopy = JSON.parse(objsArrStr);

console.log(objsArrDeepCopy);
// copied array of objects -> [{ name: "John Doe" }, { name: "Roy Daniel" }]

```

**c.Sử dụng toán tử spread operator [...] trong ES6:**

```js
const sheeps = ['🐑', '🐑', '🐑'];

const cloneSheepsES6 = [...sheeps];
```

**d. Sử dụng Object.assign:**

```js
let newArr = Object.assign([], originArr);

```

**e. Sử dụng Array.map():**

```js

const arrOrigin = [1, 2, 3];
const newArr = arrOrigin.map(x => x);

```


<b id="cau18">18. Destructuring là gì?</b>

<p>
  <b>Destructuring</b> là một biểu thức có sẵn trong ES6 cho phép một cách ngắn gọn và thuận tiện để trích xuất các giá trị của Object hoặc Array và đặt chúng vào các biến riêng biệt.
</p>

**Array destructuring**

```js

// Variable assignment.
const foo = ["one", "two", "three"];
const [one, two, three] = foo;
console.log(one); // "one"
console.log(two); // "two"
console.log(three); // "three"
// Swapping variables
let a = 1;
let b = 3;
[a, b] = [b, a];
console.log(a); // 3
console.log(b); // 1

```


**Object destructuring**

```js

// Variable assignment.
const o = { p: 42, q: true };
const { p, q } = o;
console.log(p); // 42
console.log(q); // true

```

<b id="cau19">19. Code splitting là gì?</b>

**Code splitting**

<img src="https://wiki.tino.org/wp-content/uploads/2021/10/code-splitting.png"/>

<p>
  - Hầu hết các file trong ứng dụng React sẽ dc <b><i>bundle</i></b> (đóng gói) bằng các công cụ như <b><i>Webpack, Rollup hoặc Browserify</i></b>. Đóng gói là quá trình xử lý những files đã được import và kết hợp chúng thành một file duy nhất. 
  <br/>
  <br/>
  - Nếu một ứng dụng có kích thước lớn,file đóng gói sẽ phình to theo, đặc biệt, khi chúng ta sử dụng thêm các thư viện bên thứ 3 (third party library). Để tránh việc nhận một gói bundle lớn, chúng ta cần phải <b><i>chia nhỏ file bundle.</i></b>
</p>

<b id="cau20">20. Các phương thức của ?</b>

**a. Phương thức length**

```js
// - Trả về độ dài của chuỗi

const str = 'Hello, world!';
console.log(str.length); // 13

```

**b. Phương thức charAt(index)**


```js

// - Phương thức này trả về ký tự ở vị trí index của chuỗi. Nếu index vượt quá độ dài của chuỗi, phương thức sẽ trả về một chuỗi rỗng.

const str = 'Hello, world!';
console.log(str.charAt(0)); // H
console.log(str.charAt(6)); // ,
console.log(str.charAt(13)); // ''

```

**c. Phương thức concat(str1, str2, ..., strN)**

```js

// - Phương thức này để nối các chuỗi với nhau

const str1 = 'Hello';
const str2 = 'world!';
console.log(str1.concat(', ', str2)); // Hello, world!

```

**d. Phương thức indexOf(substr, start)**

```js

// - Phương thức này trả về vị trí đầu tiên mà chuỗi con substr xuất hiện trong chuỗi hiện tại, bắt đầu tìm kiếm từ vị trí start. Nếu không tìm thấy, phương thức trả về -1.

const str = 'Hello, world!';
console.log(str.indexOf('world')); // 7
console.log(str.indexOf('l', 3)); // 3
console.log(str.indexOf('goodbye')); // -1

```

**e. Phương thức lastIndexOf(substr, start)**

```js

// - Phương thức này hoạt động tương tự như indexOf, nhưng bắt đầu tìm kiếm từ cuối chuỗi.

const str = 'Hello, world!';
console.log(str.lastIndexOf('o')); // 8
console.log(str.lastIndexOf('l', 3)); // 3
console.log(str.lastIndexOf('goodbye')); // -1

```

**f. Phương thức replace(searchValue, replaceValue)**

```js

// - Phương thức này thay thế tất cả các chuỗi con được tìm thấy bằng searchValue bằng chuỗi replaceValue.

const str = 'Hello, world!';
console.log(str.replace('world', 'John')); // Hello, John!

```

**g. Phương thức slice(start, end)**


```js

// - Phương thức này trích xuất một phần của chuỗi bắt đầu từ vị trí start và kết thúc ở vị trí end. Nếu end không được cung cấp, phương thức sẽ trích xuất từ vị trí start đến cuối chuỗi.

const str = 'Hello, world!';
console.log(str.slice(7)); // world!
console.log(str.slice(0, 5)); // Hello

```


**h. Phương thức split(separator, limit)**

```js

// - Phương thức này để cắt chuỗi. Tham số limit xác định số lượng phần tử tối đa trong mảng kết quả.

const str = 'Hello, world!';
console.log(str.split(' ')); // [ 'Hello,', 'world!' ]
console.log(str.split('l', 2)); // [ 'He', '', 'o, wor' ]

```

**i. Phương thức toLowerCase**

```js

// - Chuyển đổi chuỗi thành chữ thường.

const str = 'HeLLo, WorlD!';
console.log(str.toLowerCase()); // hello, world!

```

**k. Phương thức toUpperCase**

```js

// - Chuyển đổi chuỗi thành chữ hoa

const str = 'HeLLo, WorlD!';
console.log(str.toUpperCase()); // HELLO, WORLD!

```

**l. Phương thức trim()**

```js

// - Phương thức này loại bỏ khoảng trắng từ đầu và cuối chuỗi.

const str = '   Hello, world!   ';
console.log(str.trim()); // Hello, world!

```
