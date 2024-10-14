# Lệnh `who`

Lệnh `who` cho phép bạn in ra danh sách người dùng đã đăng nhập, mức độ chạy hiện tại của hệ thống và thời gian khởi động hệ thống lần cuối.

### Ví dụ

1. In ra tất cả chi tiết của người dùng hiện đang đăng nhập

```
who -a  
```

2. In ra danh sách tất cả các tiến trình đã chết

```
who -d -H
```

### Cú pháp:

```
who [tùy chọn] [tên tệp] 
```

### Các tham số bổ sung và chức năng của chúng

|**Cờ rút gọn**    |**Mô tả**   |
|---|---|
| `-r` |in ra tất cả các mức độ chạy hiện tại  |
| `-d` |in ra tất cả các tiến trình đã chết  |
|`-q`|in ra tất cả các tên đăng nhập và tổng số người dùng đã đăng nhập |
|`-h`|in tiêu đề của các cột được hiển thị |
|`-b`|in thời gian khởi động hệ thống lần cuối |
