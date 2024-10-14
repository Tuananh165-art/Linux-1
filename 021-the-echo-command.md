# Lệnh `echo`

Lệnh `echo` cho phép bạn hiển thị dòng văn bản/chuỗi được truyền vào như một đối số.

### Ví dụ:

1. Để hiển thị dòng văn bản hoặc chuỗi được truyền vào như một đối số:

```
echo Hello There
```
2. Để hiển thị tất cả các tệp/thư mục tương tự như lệnh `ls`:
```
echo *
```
3. Để lưu văn bản vào một tệp có tên foo.bar:
```
echo "Hello There" > foo.bar
```
4. Để thêm văn bản vào một tệp có tên foo.bar:
```
echo "Hello There" >> foo.bar
```
### Cú pháp:

```
echo [option] [string]
```

#### Nó thường được sử dụng trong các tập lệnh shell và tệp batch để xuất văn bản trạng thái ra màn hình hoặc tệp. `-e` được sử dụng với nó để cho phép diễn giải các ký tự thoát backslash.

### Các tùy chọn bổ sung và chức năng của chúng:


|**Tùy chọn**   |**Mô tả**   |
|:---|:---|
|`\b`|xóa tất cả các khoảng trắng giữa văn bản|
|`\c`|ngăn chặn dòng mới cuối cùng với bộ diễn giải backspace ‘-e‘ để tiếp tục mà không phát ra dòng mới.|
|`\n`|tạo dòng mới từ nơi nó được sử dụng|
|`\t`|tạo khoảng cách tab ngang|
|`\r`|trả về xe với bộ diễn giải backspace ‘-e‘ để có trả về xe được chỉ định trong đầu ra|
|`\v`|tạo khoảng cách tab dọc|
|`\a`|cảnh báo trả về với bộ diễn giải backspace ‘-e‘ để có cảnh báo âm thanh|
|`-n`|bỏ qua dòng mới cuối cùng của echo.|
