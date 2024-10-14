# Lệnh `man`

Lệnh `man` được sử dụng để hiển thị hướng dẫn sử dụng của bất kỳ lệnh nào mà chúng ta có thể chạy trên terminal.
Nó cung cấp thông tin như: MÔ TẢ, TÙY CHỌN, TÁC GIẢ và nhiều hơn nữa.

### Ví dụ:

1. Trang hướng dẫn cho printf:

```
man printf
```

2. Trang hướng dẫn phần 2 cho intro:

```
man 2 intro
```
3. Xem hướng dẫn sử dụng cho một tệp cục bộ (sử dụng cờ -l):

```
man -l [LOCAL-FILE]
```

### Cú pháp:

```
man [SECTION-NUM] [COMMAND NAME]
```

### Các Tham Số Bổ Sung và Chức Năng của Chúng:

|**Cờ Rút Gọn**   |**Cờ Đầy Đủ**   |**Mô Tả**   |
|:---|:---|:---|
|`-f`|<center>-</center>|Trả về các phần của một lệnh|
|`-a`|<center>-</center>|Hiển thị tất cả các trang hướng dẫn của một lệnh|
|`-k`|<center>-</center>|Tìm kiếm lệnh đã cho với RegEx trong tất cả các trang hướng dẫn|
|`-w`|<center>-</center>|Trả về vị trí của trang hướng dẫn lệnh đã cho|
|`-I`|<center>-</center>|Tìm kiếm hướng dẫn lệnh phân biệt chữ hoa chữ thường|
