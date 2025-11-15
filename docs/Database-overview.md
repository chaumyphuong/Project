Bảng Sách 
| Field name  | Data type | Width | Description                  |
| ----------- | --------- | :---: | ---------------------------- |
| Masach      | Char      |   6   | Mã sách (PK)                 |
| Tensach     | Nvarchar  |  100  | Tên sách                     |
| Maloaisach  | Char      |   6   | Mã loại sách (FK → Loaisach) |
| Manxb       | Char      |   6   | Mã nhà xuất bản (FK → NXB)   |
| Giaca       | Money     |   —   | Giá cả                       |
| Soluong     | Char      |   10  | Số lượng                     |
| Hinhthucbia | Nvarchar  |   30  | Hình thức bìa                |

Bảng Loại sách 
| Field name  | Data type | Width | Description       |
| ----------- | --------- | :---: | ----------------- |
| Maloaisach  | Char      |   6   | Mã loại sách (PK) |
| Tenloaisach | Nvarchar  |   50  | Tên loại sách     |

Bảng Tác giả 
| Field name | Data type | Width | Description     |
| ---------- | --------- | :---: | --------------- |
| Matacgia   | Char      |   6   | Mã tác giả (PK) |
| Tentacgia  | Nvarchar  |  100  | Tên tác giả     |

Bảng Nhà xuất bản 
| Field name | Data type | Width | Description          |
| ---------- | --------- | :---: | -------------------- |
| Manxb      | Char      |   6   | Mã nhà xuất bản (PK) |
| Tennxb     | Nvarchar  |  100  | Tên nhà xuất bản     |
| Namnxb     | Date      |   —   | Năm xuất bản         |

Bảng Nhân viên (Nhanvien)
| Field name | Data type | Width | Description       |
| ---------- | --------- | :---: | ----------------- |
| Manv       | Char      |   6   | Mã nhân viên (PK) |
| Ho         | Nvarchar  |   10  | Họ                |
| Ten        | Nvarchar  |   50  | Tên               |
| Sdt        | Char      |   10  | Số điện thoại     |
| Ngaysinh   | Datetime  |   —   | Ngày sinh         |
| Gioitinh   | Nvarchar  |   10  | Giới tính         |

Bảng Khách hàng (Khachhang)
| Field name | Data type | Width | Description        |
| ---------- | --------- | :---: | ------------------ |
| Makh       | Char      |   4   | Mã khách hàng (PK) |
| Ho         | Nvarchar  |   10  | Họ                 |
| Ten        | Nvarchar  |   30  | Tên                |
| Gioitinh   | Nvarchar  |   5   | Giới tính          |
| Sdt        | Char      |   10  | Số điện thoại      |
| Diachi     | Nvarchar  |  100  | Địa chỉ            |

Bảng Hóa đơn (Hoadon)
| Field name | Data type | Width | Description                    |
| ---------- | --------- | :---: | ------------------------------ |
| Mahd       | Char      |   8   | Mã hóa đơn (PK)                |
| Makh       | Char      |   4   | Mã khách hàng (FK → Khachhang) |
| Manv       | Char      |   10  | Mã nhân viên (FK → Nhanvien)   |
| Ngaymua    | Date      |   —   | Ngày mua hàng                  |
| Tongcong   | Money     |   —   | Tổng tiền                      |

Bảng Sách – Tác giả (Sach_Tacgia)
| Field name | Data type | Width | Description                  |
| ---------- | --------- | :---: | ---------------------------- |
| Masach     | Char      |   6   | Mã sách (PK, FK → Sach)      |
| Matacgia   | Char      |   6   | Mã tác giả (PK, FK → Tacgia) |

Bảng Chi tiết hóa đơn (Chitiethoadon)
| Field name | Data type | Width | Description                  |
| ---------- | --------- | :---: | ---------------------------- |
| Masach     | Char      |   6   | Mã sách (PK, FK → Sach)      |
| Mahd       | Char      |   8   | Mã hóa đơn (PK, FK → Hoadon) |
| Soluong    | Int       |   —   | Số lượng mua                 |
| Thanhtien  | Money     |   —   | Thành tiền                   |