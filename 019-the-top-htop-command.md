# Lệnh `top/htop`

`top` là tiện ích dòng lệnh mặc định được cài đặt sẵn trên các bản phân phối Linux và hệ điều hành giống Unix. Nó được sử dụng để hiển thị thông tin về hệ thống và các tiến trình tiêu thụ CPU hàng đầu cũng như sử dụng RAM.

`htop` là trình xem tiến trình tương tác và quản lý tiến trình cho hệ điều hành Linux và giống Unix dựa trên ncurses. Nếu bạn lấy top và tăng cường nó, bạn sẽ có htop.

## So sánh giữa top và htop:

|**Tính năng**   |**top**   |**htop**   |
|:---|:---|:---|
|Loại|Trình giám sát hệ thống tương tác, trình xem tiến trình và quản lý tiến trình|Trình giám sát hệ thống tương tác, trình xem tiến trình và quản lý tiến trình|
|Hệ điều hành|Các bản phân phối Linux, macOS |Các bản phân phối Linux, macOS |
|Cài đặt|Được tích hợp sẵn và luôn có mặt. Cũng có sự chấp nhận rộng rãi hơn do thực tế này.|Không được cài đặt sẵn trên hầu hết các bản phân phối Linux. Cần cài đặt thủ công|
|Giao diện người dùng|Chỉ có văn bản cơ bản|Giao diện đồ họa văn bản đầy màu sắc và đẹp hơn|
|Hỗ trợ cuộn|Không|Có, hỗ trợ cuộn ngang và dọc|
|Hỗ trợ chuột|Không|Có|
|Sử dụng tiến trình|Hiển thị các tiến trình nhưng không ở định dạng cây|Có, bao gồm các luồng người dùng và kernel|
|Sử dụng mạng|Không|Không|
|Sử dụng đĩa|Không|Không|
|Nhận xét|Có một đường cong học tập cho một số tùy chọn nâng cao như tìm kiếm, gửi tin nhắn đến các tiến trình, v.v. Tốt nhất là có một số kiến thức về top vì nó là trình xem tiến trình mặc định trên nhiều hệ thống.|Dễ sử dụng hơn và hỗ trợ tìm kiếm kiểu vi với `/`. Gửi tin nhắn đến các tiến trình (kill, renice) dễ dàng hơn và không yêu cầu nhập số tiến trình như top.|

## Ví dụ:

###  `top`

1. Để hiển thị thông tin thời gian thực động về các tiến trình đang chạy:

```
top
```

2. Sắp xếp các tiến trình theo kích thước bộ nhớ nội bộ (thứ tự mặc định - ID tiến trình):

```
top -o mem
```

3. Sắp xếp các tiến trình trước tiên theo CPU, sau đó theo thời gian chạy:

```
top -o cpu -O time
```

4. Chỉ hiển thị các tiến trình thuộc sở hữu của người dùng đã cho:

```
top -user {user_name}
```

###  `htop`

1. Hiển thị thông tin thời gian thực động về các tiến trình đang chạy. Một phiên bản nâng cao của `top`.

```
htop
```

2. Hiển thị các tiến trình thuộc sở hữu của một người dùng cụ thể:

```
htop --user {user_name}
```

3. Sắp xếp các tiến trình theo một `sort_item` được chỉ định (sử dụng `htop --sort help` để biết các tùy chọn có sẵn):

```
htop --sort {sort_item}
```

## Cú pháp:

```
top [OPTIONS] 
```

```
htop [OPTIONS] 
```


## Các tham số bổ sung và chức năng của chúng:

|**Cờ rút gọn**   |**Cờ đầy đủ**   |**Mô tả**   |
|:---|:---|:---|
|`-a`|<center>-</center>|Sắp xếp theo sử dụng bộ nhớ.|
|`-b`|<center>-</center>|Chế độ hoạt động hàng loạt. Bắt đầu top ở 'Chế độ hàng loạt', có thể hữu ích để gửi đầu ra từ top đến các chương trình khác hoặc đến một tệp. Trong chế độ này, top sẽ không chấp nhận đầu vào và chạy cho đến khi đạt giới hạn lặp bạn đã đặt với tùy chọn dòng lệnh '-n' hoặc cho đến khi bị giết.|
|`-h`|<center>-</center>|`top --user {user_name}` Chỉ hiển thị các tiến trình thuộc sở hữu của người dùng.|
|`-U`|<center>-user</center>|Trợ giúp.|
|`-u`|<center>-</center>|Đây là một bí danh tương đương với: -o cpu -O time.|
