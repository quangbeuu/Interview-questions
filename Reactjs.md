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


