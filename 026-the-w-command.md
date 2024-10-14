# Lệnh `w`

Lệnh `w` hiển thị thông tin về những người dùng hiện đang hoạt động trên máy và các [quá trình](https://www.computerhope.com/jargon/p/process.htm) của họ.

### Ví dụ:

1. Chạy lệnh `w` mà không có [đối số](https://www.computerhope.com/jargon/a/argument.htm) sẽ hiển thị danh sách người dùng đã đăng nhập và các quá trình của họ.

```
w
```

2. Hiển thị thông tin cho người dùng có tên là *hope*.

```
w hope
```

### Cú pháp:

```
finger [-l] [-m] [-p] [-s] [username]
```

### Các Tham Số Bổ Sung và Chức Năng của Chúng:

|**Cờ Rút Gọn**   |**Cờ Đầy Đủ**   |**Mô Tả**   |
|:---|:---|:---|
|`-h`|`--no-header`|Không in tiêu đề.|
|`-u`|`--no-current`|Bỏ qua tên người dùng khi xác định quá trình hiện tại và thời gian CPU. *(Để xem ví dụ về điều này, chuyển sang người dùng root với `su` và sau đó chạy cả `w` và `w -u`.)*|
|`-s`|`--short`|Hiển thị đầu ra rút gọn *(không in thời gian đăng nhập, thời gian JCPU hoặc PCPU).*|
|`-f`|`--from`|Chuyển đổi việc in trường from *(tên máy từ xa)*. Mặc định khi phát hành là trường from không được in, mặc dù quản trị viên hệ thống hoặc người bảo trì phân phối của bạn có thể đã biên dịch một phiên bản mà trường from được hiển thị theo mặc định.|
|`--help`|<center>-</center>|Hiển thị thông báo trợ giúp và thoát.|
|`-V`|`--version`|Hiển thị thông tin phiên bản và thoát.|
|`-o`|`--old-style`|Đầu ra kiểu cũ *(in khoảng trống cho thời gian nhàn rỗi dưới một phút)*.|
|*`user`*|<center>-</center>|Hiển thị thông tin chỉ về người dùng được chỉ định.|

### Thông Tin Bổ Sung

[Tiêu đề](https://www.computerhope.com/jargon/h/header.htm) của đầu ra hiển thị (theo thứ tự này): thời gian hiện tại, thời gian hệ thống đã chạy, số lượng người dùng hiện đang đăng nhập và [tải](https://www.computerhope.com/jargon/l/load.htm) trung bình của hệ thống trong 1, 5 và 15 phút qua.

Các mục sau được hiển thị cho mỗi người dùng: 
- tên đăng nhập 
- [tty](https://www.computerhope.com/jargon/t/tty.htm) 
- tên máy [từ xa](https://www.computerhope.com/jargon/r/remote.htm) 
- [host](https://www.computerhope.com/jargon/h/hostcomp.htm) mà họ đang đăng nhập từ 
- thời gian họ đã đăng nhập 
- thời gian [nhàn rỗi](https://www.computerhope.com/jargon/i/idle.htm) 
- JCPU 
- PCPU 
- [dòng lệnh](https://www.computerhope.com/jargon/c/commandi.htm) của quá trình hiện tại của họ

Thời gian JCPU là thời gian được sử dụng bởi tất cả các quá trình gắn với tty. Nó không bao gồm các công việc nền trước đây, nhưng bao gồm các công việc nền hiện đang chạy.

Thời gian PCPU là thời gian được sử dụng bởi quá trình hiện tại, được đặt tên trong trường "what".
