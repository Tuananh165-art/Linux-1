# Lệnh `history`

Nếu bạn gõ `history`, bạn sẽ nhận được danh sách 500 lệnh cuối cùng đã sử dụng. Điều này cho phép bạn sao chép và dán các lệnh mà bạn đã thực hiện trong quá khứ.

Điều này rất mạnh mẽ khi kết hợp với grep. Vì vậy, bạn có thể tìm kiếm một lệnh trong lịch sử lệnh của mình.

### Ví dụ:

1. Nếu bạn muốn tìm kiếm trong lịch sử của mình các lệnh artisan mà bạn đã chạy trong quá khứ.

```
history | grep artisan
```

2. Nếu bạn chỉ muốn hiển thị 10 lệnh cuối cùng, bạn có thể.

```
history 10
```
