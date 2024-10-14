# Lệnh `mv`

Lệnh `mv` cho phép bạn **di chuyển một hoặc nhiều tệp hoặc thư mục** từ nơi này sang nơi khác trong một hệ thống tệp như UNIX.
Nó có thể được sử dụng cho hai chức năng khác nhau:

-   Để đổi tên một tệp hoặc thư mục.
-   Để di chuyển một nhóm tệp đến một thư mục khác.

_**Lưu ý:** Không có không gian bổ sung nào được tiêu thụ trên đĩa trong quá trình đổi tên, và lệnh mv không cung cấp một lời nhắc để xác nhận_

### Cú pháp:

```[linux]
mv [tùy chọn] nguồn (tệp hoặc thư mục) đích
```

### Ví dụ:

1. Để đổi tên một tệp có tên old_name.txt:

```[linux]
mv old_name.txt new_name.txt
```

2. Để di chuyển một tệp có tên _essay.txt_ từ thư mục hiện tại đến một thư mục có tên _assignments_ và đổi tên nó thành _essay1.txt_:

```[linux]
mv essay.txt assignments/essay1.txt
```

3. Để di chuyển một tệp có tên _essay.txt_ từ thư mục hiện tại đến một thư mục có tên _assignments_ mà không đổi tên nó

```[linux]
mv essay.txt assignments
```

### Các Tham Số Bổ Sung và Chức Năng của Chúng:

| **Cờ Rút Gọn** | **Cờ Đầy Đủ**   | **Mô Tả**                                                                                           |
| :------------- | :-------------- | :-------------------------------------------------------------------------------------------------------- |
| `-f`           | `--force`       | Buộc di chuyển bằng cách ghi đè tệp đích mà không cần nhắc nhở                                                 |
| `-i`           | `--interactive` | Nhắc nhở tương tác trước khi ghi đè                                                                       |
| `-u`           | `--update`      | Chỉ di chuyển khi tệp nguồn mới hơn tệp đích hoặc khi tệp đích không tồn tại |
| `-n`           | `--no-clobber`  | Không ghi đè một tệp hiện có                                                                         |
| `-v`           | `--verbose`     | In ra tệp nguồn và tệp đích                                                                        |
| `-b`           | `--backup`      | Tạo một bản sao lưu của tệp đích hiện có                                                              |

````

````

````