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
      <li>Global scope: phạm vi toàn cầu</li>
      <li>Function scope: phạm vi hàm</li>
      <li>Block scope: phạm vi khối</li>
    </ul>   
</p>

<img src="https://miro.medium.com/max/1400/1*KxHwVbB0zhnSVrhrWtT-gg.webp"/>