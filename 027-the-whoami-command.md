# Lệnh `whoami`
---
Lệnh `whoami` hiển thị tên người dùng của người dùng hiệu quả hiện tại. Nói cách khác, nó chỉ in tên người dùng của người dùng hiện đang đăng nhập khi được thực thi.

Để hiển thị ID người dùng hiệu quả của bạn, chỉ cần gõ `whoami` trong terminal của bạn:

```
manish@godsmack:~$ whoami 
# Output:
manish
```

Cú pháp:

```
whoami [-OPTION]
```

Chỉ có hai tùy chọn có thể được truyền cho nó:

`--help`: Được sử dụng để hiển thị trợ giúp và thoát

Ví dụ:

```
whoami --help
```

Output:

```
Usage: whoami [OPTION]...
In tên người dùng liên kết với ID người dùng hiệu quả hiện tại.
Giống như id -un.

      --help     hiển thị trợ giúp này và thoát
      --version  xuất thông tin phiên bản và thoát
```

`--version`: Xuất thông tin phiên bản và thoát

Ví dụ:

```
whoami --version
```

Output:

```
whoami (GNU coreutils) 8.32
Bản quyền (C) 2020 Free Software Foundation, Inc.
Giấy phép GPLv3+: GNU GPL phiên bản 3 hoặc mới hơn <https://gnu.org/licenses/gpl.html>.
Đây là phần mềm miễn phí: bạn có thể thay đổi và phân phối lại nó.
Không có BẢO HÀNH, trong phạm vi pháp luật cho phép.

Được viết bởi Richard Mlynarik.
```
