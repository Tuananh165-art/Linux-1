# Lệnh `ps`

Lệnh `ps` được sử dụng để xác định các chương trình và quá trình đang chạy trên hệ thống và các tài nguyên mà chúng đang sử dụng.
Nó thường được [kết hợp](<https://en.wikipedia.org/wiki/Pipeline_(Unix)>) với các lệnh khác như `grep` để tìm kiếm một chương trình/quá trình hoặc `less` để người dùng có thể phân tích đầu ra từng trang một.

Giả sử bạn có một chương trình như openshot nổi tiếng với việc chiếm dụng tài nguyên hệ thống khi xuất video, và bạn muốn đóng nó, nhưng giao diện đồ họa đã trở nên không phản hồi.

### Ví dụ

1. Bạn muốn tìm PID của openshot và kết thúc nó.

```
ps aux | grep openshot
kill - <openshot PID>
```

2. Để hiển thị tất cả các quá trình đang chạy:

```
ps -A
```

### Cú pháp

`ps [tùy chọn]`

Khi chạy mà không có tùy chọn nào, nó vô dụng và sẽ in: `CMD` - các quá trình/chương trình thực thi đang chạy, `PID` - ID quá trình, `TTY` - loại terminal và `Time` - Thời gian quá trình đã sử dụng CPU hoặc luồng.

### Tùy chọn Thông Thường

Nếu bạn chỉ nhớ một điều từ trang này, hãy nhớ ba chữ cái `aux`:
`a` - hiển thị tất cả các quá trình đang chạy, bao gồm cả những quá trình đang được chạy bởi người dùng khác.
`u` - hiển thị người dùng hiệu quả của một quá trình, tức là người có quyền truy cập tệp được sử dụng bởi quá trình.
`x` - hiển thị các quá trình không có `TTY` liên kết với chúng.

### Tùy chọn Bổ Sung:

|**Tùy chọn**   |**Mô tả**   |
|:---|:---|
|`a`|Hiển thị danh sách tất cả các quá trình với một terminal (tty)|
|`-A`|Liệt kê tất cả các quá trình. Giống với `-e`|
|`-a`|Hiển thị tất cả các quá trình ngoại trừ cả hai lãnh đạo phiên và các quá trình không liên kết với một terminal|
|`-d`|Chọn tất cả các quá trình ngoại trừ lãnh đạo phiên|
|`--deselect`|Hiển thị tất cả các quá trình ngoại trừ những quá trình đáp ứng các điều kiện đã chỉ định. Giống với `-N`|
|`-e`|Liệt kê tất cả các quá trình. Giống với `-A`|
|`-N`|Hiển thị tất cả các quá trình ngoại trừ những quá trình đáp ứng các điều kiện đã chỉ định. Giống với `-deselect`|
|`T`|Chọn tất cả các quá trình liên kết với terminal này. Giống với tùy chọn `-t` mà không có đối số|
|`r`|Giới hạn lựa chọn chỉ cho các quá trình đang chạy|
|`--help simple`|Hiển thị tất cả các tùy chọn cơ bản|
|`--help all`|Hiển thị tất cả các tùy chọn có sẵn|

Một lệnh hữu ích khác cung cấp ảnh chụp nhanh thời gian thực của các quá trình và tài nguyên mà chúng đang sử dụng khoảng mỗi mười giây là `top`.
