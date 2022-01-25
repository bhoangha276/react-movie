# React Movie
Member: Bùi Hoàng Hà, Nguyễn Ngọc Đạt, Nguyễn Huy Hoàng

## Stack
<table>
  <tr>
    <td align="center" width="160">
      <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" width="75" height="30" />
      <br />
       Reactjs
    </td>
    <td align="center" width="160">
      <img src="https://img.shields.io/badge/-Scss-CC6699?style=flat-square&logo=sass&logoColor=white" width="75" height="30" />
      <br />
       Scss
    </td>
    <td align="center" width="160">
      <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" width="75" height="30" />
      <br />
       Nodejs
    </td>
    <td align="center" width="160">
      <img src="https://img.shields.io/badge/firebase-%23039BE5.svg?style=for-the-badge&logo=firebase" width="75" height="30" />
      <br />
       Firebase
    </td>
    <td align="center" width="160">
      <img src="https://img.shields.io/badge/MongoDB-2ECC71?style=for-the-badge&logo=mongodb&logoColor=4EA94B" width="75" height="30" />
      <br />
       MongoDB
    </td>
    <td align="center" width="160">
      <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" width="75" height="30" />
      <br />
       ExpressJS
    </td>
   </tr>
 </table>
  
- Reactjs để làm giao diện
- Scss để hỗ trợ làm thiết kế giao diện 
- Nodejs dùng để thiết kế, xây dựng một ứng dụng mạng mở rộng
- Firebase để quản lý file ảnh, phim
- MongoDB để làm cơ sở dữ liệu
- ExpressJS để tạo web app

## User Story
- Là người dùng
  - Đăng nhập, đăng kí
  - Tìm kiếm tên phim
  - Xem danh sách phim
  - Xem các thể loại phim
  - Xem theo loại phim (movies hoặc series) 
  - Xem phim
  - Lưu phim vào danh sách phim cá nhân
  - Đánh giá phim bằng thích hoặc không thích
-Là khách
  - Đăng nhập với tài khoản admin
  - Hiển thị các chức năng ở thanh bên trái
  - Xem, thêm, sửa, xóa tất cả các phim
  - Xem, thêm, sửa, xóa tất cả các thể loại phim

## Thiết kế cơ sở dữ liệu

- UserSchema
```ruby
const UserSchema = new mongoose.Schema(
  {
    username: { type: String, required: true},
    email: { type: String, required: true, unique: true },
    password: { type: String, required: true },
    avatar: { type: String, defaut: "" },
    wishlist: { type: Array },
    likeMovie: { type: Array },
    isAdmin: { type: Boolean, default: false },
  },
  { timestamps: true }
);
```
-MovieSchema
```ruby
const MovieSchema = new mongoose.Schema(
  {
    name: { type: String, required: true },
    desc: { type: String },
    img: { type: String },
    imgSm: { type: String },
    trailer: { type: String },
    video: { type: String },
    year: { type: String },
    limit: { type: Number },
    category: { type: String },
    isSeries: { type: Boolean, default: false },
    likeCount: { type: Number, default: 0 },
  },
  { timestamps: true }
);
```

-CategorySchema
```ruby

```
