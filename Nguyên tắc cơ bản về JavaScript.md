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
## 2.3. Chế độ nghiêm ngặt "user" strict
### chỉ thị phải viết ở đầu tập lệnh hoặc đầu thân hàm
~~~
'user strict';
~~~
## 2.4. Biến
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
## 2.6. Sự Tương Tác
### Chức năng cơ bản:
* **prompt(question, [default])**