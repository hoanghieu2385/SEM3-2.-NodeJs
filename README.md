# SEM3-2.-NodeJs

Buổi 1: làm quen với node js 

https://nodejs.org/en/download/prebuilt-installer

setup chạy code trong terminal: setting -> search: run in terminal -> tick bật 

cài express node js: nhập: npm i express

tạo template nodejs express ()

-> npx express-generator + tên (hoặc tạo thư mục sẵn xong dán lệnh vào: npx express-generator )
-> npm install

chạy: npm start -> sẽ chạy ở http://localhost:3000/


Buổi 2:
chạy lệnh: npm i mongoose
connect db -> post / get bằng postman

Buổi 3: Mô hình mvc
b1: model: chuyển code user -> server js -> userModel
b2: định nghĩa method
b3: route

Buổi 4: tìm hiểu về ejs (Embedded JavaScript templating)

-> npx express-generator + tên (hoặc tạo thư mục sẵn xong dán lệnh vào: npx express-generator )
-> npm install

Lệnh: npm install ejs

tạo project
cài đặt view engine (ejs)
cấu hình chọn ejs trong app.js sửa app.set('view engine', 'jade'); ---> app.set('view engine', 'ejs');

dùng bootstrap: + cách 1 dùng link
                + cách 2 sài lệnh cài thẳng vào bằng lệnh: npm install bootstrap@5.3.3

nếu sài bằng cách 2 thì trong app.js cần thêm lệnh mới có thể sài được:
app.use('/node_modules', express.static(path.join(__dirname, 'node_modules')));

****** NÊN SÀI BOOTSTRAP BẰNG LINK !!!!!!!!!!

Buổi 5:
Kết hợp bài học buổi 3 + 4 (làm trong file b5_ket_hop_express_ejs)

cách lệnh cần thiết:
-> npm i mongoose
-> npx express-generator
-> npm install
-> npm install ejs

các bước:
+ app.js đổi    app.set('view engine', 'jade');   --->   app.set('view engine', 'ejs');
+ tạo trong folder view 1 folder tên là user để nhét index.ejs của user tránh bị nhầm sang index chính: 
    - error.ejs (để hiển thị lỗi)
    - index.ejs

CRUD: 
cần ==>  npm install method-override

PUT (để edit và update) và DELETE: để ghi đè vì form html chỉ có 2 phương thức là POST và GET

sau khi cài lệnh xong thì cần thêm lệnh trong app.js: 

+ var methodOverride = require('method-override');

+ app.use(methodOverride('_method'));

ví dụ: 
<form action="/users/<%= user._id %>?_method=PUT" method="POST">

Buổi 6:
node js basic: var, let, const