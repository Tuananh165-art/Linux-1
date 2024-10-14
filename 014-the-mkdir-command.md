# Lệnh `mkdir`
Lệnh `mkdir` trong Linux/Unix được sử dụng để tạo một thư mục.

## Cú pháp
```bash
$ mkdir [-m=mode] [-p] [-v] [-Z=context] directory [directory ...]
```

## Ví dụ
1. Tạo một thư mục có tên là **myfiles**.
```bash
$ mkdir myfiles
```

2. Tạo một thư mục có tên là **myfiles** tại thư mục home:
```bash
$ mkdir ~/myfiles
```

3. Tạo thư mục **mydir**, và đặt chế độ file của nó (`-m`) để tất cả người dùng (`a`) có thể đọc (`r`), ghi (`w`), và thực thi (`x`) nó.
```bash
$ mkdir -m a=rwx mydir
```

Bạn cũng có thể tạo các thư mục con của một thư mục. Nó sẽ tạo thư mục cha trước, nếu nó chưa tồn tại. 
Nếu nó đã tồn tại, thì nó sẽ tiếp tục tạo các thư mục con mà không có thông báo lỗi nào.

Đối với các thư mục, điều này có nghĩa là bất kỳ người dùng nào trên hệ thống đều có thể xem ("đọc"), và tạo/sửa/xóa ("ghi") các tệp trong thư mục. Bất kỳ người dùng nào cũng có thể thay đổi ("thực thi") thư mục, ví dụ với lệnh `cd`.

4. Tạo thư mục **/home/test/src/python**. Nếu bất kỳ thư mục cha nào **/home**, **/home/test**, hoặc **/home/test/src** chưa tồn tại, chúng sẽ được tự động tạo.
```bash
$ mkdir -p /home/test/src/python
```

## Tùy chọn
|**Cờ rút gọn**|**Cờ đầy đủ**|**Mô tả**|
|:-|:-|:-|
|`-m`|`--mode=MODE`|Đặt chế độ file (như trong chmod), không phải `a=rwx - umask`.|
|`-p`|`--parents`|Không có lỗi nếu đã tồn tại, tạo các thư mục cha khi cần thiết.|
|`-v`|`--verbose`|In một thông báo cho mỗi thư mục được tạo.|
|`-Z`|`--context=CTX`|Đặt ngữ cảnh bảo mật SELinux của mỗi thư mục được tạo thành CTX.|
|<center>-</center>|`--help`|Hiển thị một thông điệp trợ giúp và thoát.|
|<center>-</center>|`--version`|Xuất thông tin phiên bản và thoát.|