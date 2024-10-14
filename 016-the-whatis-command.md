# Lệnh `whatis`

Lệnh `whatis` được sử dụng để hiển thị mô tả một dòng của trang hướng dẫn cho các lệnh. Nó có thể được sử dụng để có một hiểu biết cơ bản về một lệnh (không rõ) được sử dụng để làm gì.

### Ví dụ sử dụng:

1. Để hiển thị `ls` được sử dụng để làm gì:

```
whatis ls
```

2. Để hiển thị cách sử dụng của tất cả các lệnh bắt đầu với `make`, thực hiện lệnh sau:

```
whatis -w make*
```

### Cú pháp:

```
whatis [-OPTION] [KEYWORD]
```

### Các tham số bổ sung và chức năng của chúng:

|**Cờ rút gọn**   |**Cờ đầy đủ**   |**Mô tả**   |
|:---|:---|:---|
|`-d`|`--debug`|Hiển thị thông điệp gỡ lỗi|
|`-r`|`--regex`|Diễn giải mỗi từ khóa như một regex|
|`-w`|`--wildcard`|Các từ khóa chứa ký tự đại diện|
