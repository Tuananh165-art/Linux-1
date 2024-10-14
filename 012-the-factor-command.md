# Lệnh `factor`
Lệnh `factor` in ra các thừa số nguyên tố của mỗi số nguyên `NUMBER` được chỉ định. Nếu không có số nào được chỉ định trên dòng lệnh, nó sẽ đọc từ đầu vào chuẩn.

## Cú pháp
```bash
$ factor [NUMBER]...
```
HOẶC:
```bash
$ factor OPTION
```

## Tùy chọn
|**Tùy chọn**|**Mô tả**|
|:--|:--|
|`--help`|Hiển thị thông điệp trợ giúp này và thoát.|
|`--version`|Xuất thông tin phiên bản và thoát.|

## Ví dụ

1. In ra các thừa số nguyên tố của một số nguyên tố.
```bash
$ factor 50
```

2. In ra các thừa số nguyên tố của một số không phải là số nguyên tố.
```bash
$ factor 75
```