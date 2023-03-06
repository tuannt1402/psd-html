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
* **let** : phạm vi khối mã(block), có thể được cập nhật nhưng không thể khai báo lại
* **const** : phạm vi khối mã(block), không thể cập nhật và không thể khai báo lại
* **var** : phạm vi toàn cục(global) hay hàm(function), có thể được cập nhật và khai báo lại trong phạm vi tổn tại
