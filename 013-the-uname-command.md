# Lệnh `uname`
Lệnh `uname` cho phép bạn in ra thông tin hệ thống và mặc định là xuất tên kernel.

## Cú pháp:
```bash
$ uname [OPTION]
```

## Ví dụ
1. In ra tất cả thông tin hệ thống.
```bash
$ uname -a
```

2. In ra phiên bản kernel.
```bash
$ uname -v
```

## Tùy chọn
|**Cờ rút gọn**|**Cờ đầy đủ**|**Mô tả**|
|:-|:-|:-|
|`-a`|`--all`|In tất cả thông tin, ngoại trừ bỏ qua bộ xử lý và nền tảng phần cứng nếu không biết.|
|`-s`|`--kernel-name`|In tên kernel.|
|`-n`|`--nodename`|In tên máy chủ mạng.|
|`-r`|`--kernel-release`|In bản phát hành kernel.|
|`-v`|`--kernel-version`|In phiên bản kernel.|
|`-m`|`--machine`|In tên phần cứng máy.|
|`-p`|`--processor`|In loại bộ xử lý (không di động).|
|`-i`|`--hardware-platform`|In nền tảng phần cứng (không di động).|
|`-o`|`--operating-system`|In hệ điều hành.|