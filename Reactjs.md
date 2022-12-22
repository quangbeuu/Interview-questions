# Câu hỏi phỏng vấn ReactJS

<img src="https://ms314006.github.io/static/b7a8f321b0bbc07ca9b9d22a7a505ed5/97b31/React.jpg"/>


## Mục lục
<ul>
  <li>
    <a href="#cau1">1. JSX là gì?</a>  
  </li>
  <li>
    <a href="#cau2">2. Virtual Dom (Dom ảo) là gì?</a>
  </li>
  <li>
    <a href="#cau3">3. Sự khác biệt giữa class component và function component?</a>
  </li>
  
   <li>
    <a href="#cau4">4. Sự khác biệt giữa useState và useRef ?</a>
  </li>
  
   <li>
    <a href="#cau5">5. Dùng useRef và querySelector khác gì nhau?</a>
  </li>
 </ul>


## Câu hỏi
<b id="cau1">1. JSX là gì?</b>
<p>
  - Viết tắt của Javascript XML
   <br/>
  - ReactJS sử dụng JSX làm pattern (khuôn mẫu) thay vì JS thông thường
   <br/>
  - Dễ hiểu hơn, JSX đc sử dụng vơi React để mô tả giao diện người dùng trông như thế nào
  <br/>
  - Với JSX, ta có thể viết các mã HTML trong cùng một tệp chứa code Javascript
</p>
<p>
  * Để trình duyệt web có thể đọc được tệp JSX, tệp cần được chuyển đổi thành một đối tượng JavaScript thông thường. Để làm điều này, chúng tôi sử dụng Babel.
</p>
<div align="center">
  <img src="https://firebasestorage.googleapis.com/v0/b/mindcard-99b06.appspot.com/o/interview%2FScreenshot%202022-12-22%20at%2010.22.09.png?alt=media&token=7c18c74c-9f02-48b9-beaa-23baf029ee4c" width="820">
</div>


<b id="cau2">2. Virtual Dom (Dom ảo) là gì?</b>
<p>
  <b>* DOM là gì?</b>
  <br/>
      - DOM là viết tắt của <b>Document Object Model</b>. 
      <br/>
      - DOM đại diện cho một tài liệu HTML có cấu trúc cây logic. 
      <br/>
      - DOM có cấu trúc được định nghĩa thành các <b>đối tượng, phương thức, thuộc tính</b> để có thể truy xuất dễ dàng. Chúng được coi như các node và được biểu diễn dưới dạng <b>DOM Tree</b>.
      <br/>
</p>
  
<div align="center">
  <img src="https://images.viblo.asia/74e0e748-dff2-4790-a202-f80b29519951.gif" />
</div>
<p>
  <b>* Vấn đề với DOM thật?</b> 
  <br/>
  - Mỗi thay đổi đến DOM sẽ có khả năng khiến browser phải thay đổi layout, tính toán style, re-render.
  <br/>
  - Chúng ta có thể hình dung rằng một hành động của người dùng làm UI thay đổi ở 20 điểm khác nhau trên màn hình, chúng ta gọi DOM API 20 lần dẫn đến phải browser phải chạy tính toán lại 20 lần (!!!)
</p>

<p>
  <b>* Virtual DOM là gì?</b>
</p>

<img src="https://github.com/Ren0503/fullstack-interviews/raw/main/frontend/react/assets/virtual_DOM.png"/>

<p>
  - Đối với mỗi đối tượng DOM thật, có một đối tượng DOM ảo tương ứng (bản sao). Sự khác biệt chính giữa đối tượng DOM thực và đối tượng DOM ảo là bất kỳ thay đổi nào trong đối tượng DOM ảo sẽ không phản ánh trực tiếp trên màn hình.
  <br/>
  - React sử dụng hai virtual DOM để hiển thị giao diện người dùng. Một cái được sử dụng để lưu trữ trạng thái hiện tại của các đối tượng và cái còn lại để lưu trữ trạng thái trước đó của các đối tượng. React sẽ so sánh phiên bản DOM ảo hiện tại với phiên bản trước đó. Quá trình này được gọi là <b>"diffing"</b>.
  <br/>
  - Khi React biết các đối tượng DOM ảo nào đã thay đổi, sẽ tiến hành cập nhật duy nhất đối tượng đó vào DOM thật
</p>

<b id="cau3">3. Sự khác biệt giữa class component và function component?</b>

<b id="cau4">4. Sự khác biệt giữa useState và useRef?</b>
<p>
  - <b>useState</b>: là 1 hook dùng để update state trong functional component
  <br/>
  - <b>useRef</b>  : là 1 hook cung cấp cách để truy cập vào DOM. Nó sẽ trả về một đối tượng ref để bạn có thể lấy value bằng cách .current
</p>
<p>
  * Sự khác biệt:
  <br/>
  - Khi update state với <b>useState</b> thì components sẽ bị re-render. 
  <br> 
  VD: Khi tôi thay đổi state 'A' thành 'B' khi đó components sẽ re-render và cập nhật ngay lập tức 
  <br/>
  - Còn khi update state với <b>useRef</b> components sẽ ko bị re-render và ta vẫn lấy đc giá trị state bằng cách .current
</p>

<b id="cau5">5. Dùng useRef và querySelector khác gì nhau</b>
