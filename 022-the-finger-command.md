
# Lệnh `finger`

Lệnh `finger` hiển thị thông tin về người dùng hệ thống cục bộ bằng cách truy vấn các tệp như `/etc/passwd`, `/var/run/utmp`, và `/var/log/wtmp`. Đây là một lệnh cục bộ và không phụ thuộc vào bất kỳ dịch vụ hay daemon nào để chạy. Lệnh này giúp nhanh chóng truy xuất các chi tiết liên quan đến người dùng như thời gian đăng nhập, trạng thái nhàn rỗi, và thông tin hệ thống khác.

### Ví dụ:

1. Xem chi tiết về một người dùng cụ thể.

```
finger abc
```

*Output*
```
Login: abc                          Name: (null)
Directory: /home/abc                Shell: /bin/bash
On since Mon Nov  1 18:45 (IST) on :0 (messages off)
On since Mon Nov  1 18:46 (IST) on pts/0 from :0.0
New mail received Fri May  7 10:33 2013 (IST)
Unread since Sat Jun  7 12:59 2003 (IST)
No Plan.
```

2. Xem chi tiết đăng nhập và trạng thái nhàn rỗi của một người dùng.

```
finger -s root
```

*Output*
```
Login     Name       		Tty      Idle  Login Time   Office     Office Phone
root         root           *1    19d Wed 17:45
root         root           *2     3d Fri 16:53
root         root           *3        Mon 20:20
root         root           *ta    2  Tue 15:43
root         root           *tb    2  Tue 15:44
```

### Cú pháp:

```
finger [-l] [-m] [-p] [-s] [username]
```

### Các Tham Số Bổ Sung và Chức Năng Của Chúng:

| **Cờ** | **Mô tả** |
|:---|:---|
| `-l` | Buộc định dạng đầu ra dài. |
| `-m` | Chỉ khớp đối số trên tên người dùng (không phải tên đầu hoặc tên cuối). |
| `-p` | Ngăn chặn in tệp .plan trong bản in định dạng dài. |
| `-s` | Buộc định dạng đầu ra ngắn. |

### Thông Tin Bổ Sung:

**Định Dạng Mặc Định**:  
Định dạng mặc định bao gồm các mục như tên đăng nhập, tên đầy đủ của người dùng, tên terminal, và trạng thái ghi. Lệnh cung cấp các chi tiết như thời gian nhàn rỗi, thời gian đăng nhập, và thông tin cụ thể của trang web.

**Định Dạng Dài Hơn**:  
Trong định dạng dài, lệnh thêm các chi tiết như thư mục chính của người dùng, shell đăng nhập, và nội dung của các tệp `.plan` và `.project`.

---

## Cân Nhắc Về Quyền Riêng Tư

Mặc dù lệnh `finger` hữu ích để truy xuất thông tin về người dùng hệ thống, nó cũng có thể tiết lộ các chi tiết nhạy cảm trong môi trường chia sẻ hoặc nhiều người dùng:

1. **Tên Người Dùng và Thời Gian Đăng Nhập**: Hiển thị thời gian đăng nhập, có thể được sử dụng để theo dõi hoạt động của người dùng.
2. **Thư Mục Chính**: Tiết lộ đường dẫn đến thư mục chính của người dùng.
3. **Trạng Thái Nhàn Rỗi**: Cho thấy người dùng đã không hoạt động bao lâu, có thể báo hiệu liệu họ có đang sử dụng hệ thống của mình hay không.
4. **Trạng Thái Thư**: Hiển thị thông tin thư, có thể vô tình tiết lộ sự tham gia của người dùng.

### Rủi Ro Tiềm Ẩn:
Trong các môi trường có người dùng không tin cậy, thông tin được tiết lộ bởi `finger` có thể bị khai thác cho:

- **Tấn Công Kỹ Thuật Xã Hội**: Các tác nhân độc hại có thể sử dụng thông tin này để tạo ra các cuộc tấn công lừa đảo cá nhân hóa.
- **Tấn Công Thời Gian**: Biết khi nào người dùng nhàn rỗi hoặc hoạt động có thể giúp kẻ tấn công có lợi thế trong việc định thời gian cho các nỗ lực của họ.
- **Tấn Công Có Mục Tiêu**: Biết thư mục chính của người dùng có thể tập trung các cuộc tấn công vào những vị trí đó.

### Giảm Thiểu Rủi Ro Quyền Riêng Tư:
Để giảm thiểu những rủi ro này, hãy cân nhắc hạn chế quyền truy cập vào lệnh `finger` trong các môi trường mà quyền riêng tư của người dùng là quan trọng.

---

## Dịch Vụ `in.fingerd`

Điều quan trọng là phân biệt giữa lệnh `finger` và **dịch vụ `in.fingerd`**. Lệnh `finger` là cục bộ, trong khi `in.fingerd` là một daemon mạng cho phép truy vấn thông tin người dùng từ xa. Dịch vụ này thường bị vô hiệu hóa theo mặc định trong các hệ thống hiện đại do các rủi ro bảo mật tiềm ẩn.

Nếu được kích hoạt, dịch vụ `in.fingerd` có thể tiết lộ thông tin người dùng qua mạng, có thể bị khai thác bởi kẻ tấn công. Để giảm thiểu rủi ro này, quản trị viên hệ thống nên đảm bảo dịch vụ bị vô hiệu hóa nếu không cần thiết.

### Vô Hiệu Hóa Dịch Vụ `in.fingerd`:

Nếu bạn lo ngại về các truy vấn từ xa, bạn có thể vô hiệu hóa dịch vụ `in.fingerd`:

```bash
sudo systemctl disable in.fingerd
sudo systemctl stop in.fingerd
```

Bằng cách vô hiệu hóa dịch vụ `in.fingerd`, bạn ngăn chặn truy vấn thông tin người dùng từ xa, tăng cường bảo mật hệ thống.