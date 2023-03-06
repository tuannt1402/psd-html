# Nguyên tắc cơ bản về javascript
## 2.1. Cấu trúc mã
### Các câu lệnh được phân cách bằng dấu chấm phẩy:
~~~
alert('Hello'); alert('World');
~~~
### Thông thường ngắt dòng cũng được coi là dấu phân cách, được gọi là" chán dấu chấm phẩy tự động", nhưng đôi khi nó không hoạt động:
~~~
alert('Hello')
alert('World')
~~~
### => Hầu hết đều đặt dấu chấm phẩy sau mỗi câu lệnh, Dấu chấm phẩy không bắt buộc sau các khối mã {...}
## 2.2. Chế độ nghiêm ngặt "user" strict
### chỉ thị phải viết ở đầu tập lệnh hoặc đầu thân hàm
~~~
'user strict';
~~~
## 2.3. Biến
### Khai báo:
* **let** : phạm vi khối mã(block), có thể được cập nhật nhưng không thể khai báo lại
* **const** : phạm vi khối mã(block), không thể cập nhật và không thể khai báo lại
* **var** : phạm vi toàn cục(global) hay hàm(function), có thể được cập nhật và khai báo lại trong phạm vi tổn tại

### Một biến có thể gồm:
* Chữ cái và chữ số, nhưng ký tự đầu tiên có thể không phải là chữ số.
* Ký tự $và _là bình thường, ngang bằng với chữ cái.
* Bảng chữ cái không phải tiếng Latinh và chữ tượng hình cũng được cho phép, nhưng thường không được sử dụng.
### Có 8 kiểu dữ liệu:
* **number** cho cả số dấu phẩy động và số nguyên,
* **bigint** cho các số nguyên có độ dài tùy ý,
* **string** cho chuỗi,
* **boolean** cho các giá trị logic: **true/false**,
* **null** – một loại có một giá trị duy nhất **null**, nghĩa là “trống rỗng” hoặc “không tồn tại”,
* **undefined** – một loại có một giá trị duy nhất **undefined**, nghĩa là “không được chỉ định”,
* **object** và **symbol** là cấu trúc dữ liệu phức tạp và số nhận dạng duy nhất.
## 2.4. Sự Tương Tác
### Chức năng cơ bản:
* **prompt(question, [default])**
> Hỏi **question** và trả lại những gì khách truy cập đã nhập hoặc **null** nếu họ nhấp vào “hủy”.

* **confirm(question)**
> Hỏi a **question** và đề nghị chọn giữa Ok và Cancel. Lựa chọn được trả về dưới dạng **true/false**.

* **alert(message)**
> Đầu ra một **message**.
#### => Các chức năng này đều là *phương thức* , chúng tạm dừng thực thi mã và ngăn khách truy cập tương tác với trang cho đến khi họ trả lời.

## 2.5. Operators
### Số học
##### Hỗ trợ các toán tử: + - * /, cũng như % số dư và ** lũy thừa của một số
##### Nhị phân cộng + nối các chuỗi. Và nếu bất kì toán hạng nào là 1 chuỗi, thì toán hạng còn lại cũng được chuyển thành chuỗi:
~~~
alert( '1' + 2 ); // '12', string
alert( 1 + '2' ); // '12', string
~~~

##### Toán tử Bitwise: hoạt động với số nguyên 32 bit ở cấp độ bit thấp nhất
##### Điều Kiện:
> Toán tử duy nhất có ba tham số: **cond ? resultA : resultB**. Nếu **cond** là sự thật, trả về **resultA**, nếu không **resultB**.
##### Toán tử logic 
> Logic AND **&&** và OR **||** thực hiện đánh giá ngắn mạch và sau đó trả về giá trị tại nơi nó dừng (không cần thiết **true/ false**). Logical NOT **!** chuyển đổi toán hạng thành kiểu boolean và trả về giá trị nghịch đảo.

##### Toán tử hợp nhất Nullish
> Toán **??** tử cung cấp một cách để chọn một giá trị xác định từ danh sách các biến. Kết quả của **a ?? b** là **a** trừ khi nó là **null/undefined**, sau đó **b**.

##### So sánh
> Kiểm tra đẳng thức **==** cho các giá trị của các loại khác nhau sẽ chuyển đổi chúng thành một số (ngoại trừ **null** và **undefined** bằng nhau và không có gì khác), vì vậy các giá trị này bằng nhau:
~~~
alert( 0 == false ); // true
alert( 0 == '' ); // true
~~~
> Toán tử đẳng thức nghiêm ngặt **===** không thực hiện chuyển đổi: các loại khác nhau luôn có nghĩa là các giá trị khác nhau.
> Các giá trị **null** và **undefined** đặc biệt: chúng bình đẳng ==với nhau và không bình đẳng với bất kỳ thứ gì khác.
## 2.6. Vòng lặp
* 3 loại vòng lặp:

~~~
// 1
while (condition) {
  ...
}

// 2
do {
  ...
} while (condition);

// 3
for(let i = 0; i < 10; i++) {
  ...
}
~~~

* Biến được khai báo trong **for(let...)** vòng lặp chỉ hiển thị bên trong vòng lặp. Nhưng chúng ta cũng có thể bỏ qua **let** và sử dụng lại một biến hiện có.
* Chỉ thị **break/continue**cho phép thoát khỏi toàn bộ vòng lặp/lặp lại hiện tại. Sử dụng nhãn để ngắt các vòng lặp lồng nhau.

## 2.7. Cấu trúc "switch"
Cấu trúc “switch” có thể thay thế nhiều **if** lần kiểm tra. Nó sử dụng ***===**(bình đẳng nghiêm ngặt) để so sánh.

~~~
let age = prompt('Your age?', 18);

switch (age) {
  case 18:
    alert("Won't work"); // the result of prompt is a string, not a number
    break;

  case "18":
    alert("This works!");
    break;

  default:
    alert("Any value not equal to one above");
}
~~~
## 2.8. Chức năng

