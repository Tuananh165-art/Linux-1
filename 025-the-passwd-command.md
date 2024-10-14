# Lệnh `passwd`

Trong Linux, lệnh `passwd` thay đổi mật khẩu của tài khoản người dùng. Một người dùng bình thường chỉ có thể thay đổi mật khẩu cho tài khoản của chính họ, nhưng một siêu người dùng có thể thay đổi mật khẩu cho bất kỳ tài khoản nào.
`passwd` cũng thay đổi thời gian hiệu lực của tài khoản hoặc mật khẩu liên quan.

## Ví dụ

```bash
$ passwd

```

## Cú pháp của lệnh `passwd` là:

```bash
$ passwd [tùy chọn] [ĐĂNG NHẬP]

```
## tùy chọn

```bash
-a, --all
        Tùy chọn này chỉ có thể được sử dụng với -S và hiển thị trạng thái cho tất cả người dùng.

-d, --delete
        Xóa mật khẩu của một người dùng.

-e, --expire
        Ngay lập tức hết hạn mật khẩu của tài khoản.

-h, --help
        Hiển thị thông báo trợ giúp và thoát.

-i, --inactive
        Tùy chọn này được sử dụng để vô hiệu hóa một tài khoản sau khi mật khẩu đã hết hạn trong một số ngày.

-k, --keep-tokens
        Chỉ ra rằng thay đổi mật khẩu chỉ nên được thực hiện cho các mã xác thực đã hết hạn (mật khẩu).

-l, --lock
        Khóa mật khẩu của tài khoản được chỉ định.

-q, --quiet
        Chế độ yên lặng.

-r, --repository
        Thay đổi mật khẩu trong kho lưu trữ.

-S, --status
        Hiển thị thông tin trạng thái tài khoản.

```