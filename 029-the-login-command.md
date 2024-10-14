# Lệnh `login`

Lệnh `login` khởi tạo một phiên người dùng.

## Cú pháp

```bash
$ login [-p] [-h host] [-H] [-f username|username]
```

## Các tham số và chức năng của chúng

|**Cờ Rút Gọn**    |**Mô Tả**   |
|---|---|
| `-f` |Được sử dụng để bỏ qua xác thực đăng nhập. Tùy chọn này thường được sử dụng bởi tính năng autologin của getty(8).  |
| `-h` | Được sử dụng bởi các máy chủ khác (như telnetd(8)) để truyền tên của máy chủ từ xa đến login để nó có thể được đặt trong utmp và wtmp. Chỉ có siêu người dùng mới được phép sử dụng tùy chọn này.  |
|`-p`|Được sử dụng bởi getty(8) để yêu cầu login bảo toàn môi trường. |
|`-H`|Được sử dụng bởi các máy chủ khác (ví dụ, telnetd(8)) để yêu cầu login không in tên máy chủ trong lời nhắc login:.  |
|`--help`|Hiển thị văn bản trợ giúp và thoát.|
|`-v`|Hiển thị thông tin phiên bản và thoát.|

## Ví dụ

Để đăng nhập vào hệ thống với tư cách người dùng abhishek, nhập lệnh sau tại lời nhắc đăng nhập:
```bash
$ login: abhishek
```
Nếu một mật khẩu được định nghĩa, lời nhắc mật khẩu sẽ xuất hiện. Nhập mật khẩu của bạn tại lời nhắc này.
