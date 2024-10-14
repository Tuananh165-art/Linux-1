# Lệnh `gzip`

Lệnh `gzip` trong Linux/Unix được sử dụng để nén/giải nén dữ liệu.

# Sử dụng

## Nén một tệp

**Hành động:**
--- Nén một tệp

**Chi tiết:**
--- Giảm kích thước của tệp bằng cách áp dụng nén

**Lệnh:**
```
gzip file_name
```

## Giải nén một tệp

**Hành động:**
--- Giải nén một tệp

**Chi tiết:**
--- Khôi phục tệp về dạng gốc của nó về dữ liệu và kích thước

**Lệnh:**
```
gzip -d archive_01.gz
```

## Nén nhiều tệp:

**Hành động:**
--- Nén nhiều tệp

**Chi tiết:**
--- Nén nhiều tệp thành nhiều tệp lưu trữ

**Lệnh:**
```
gzip file_name_01 file_name_02 file_name_03
```

## Giải nén nhiều tệp:

**Hành động:**
--- Giải nén nhiều tệp

**Chi tiết:**
--- Giải nén nhiều tệp từ nhiều tệp lưu trữ

**Lệnh:**
```
gzip -d archive_01.gz archive_02.gz archive_03.gz
```

## Nén một thư mục:

**Hành động:**
--- Nén tất cả các tệp trong một thư mục

**Chi tiết:**
--- Nén nhiều tệp dưới một thư mục thành một tệp lưu trữ duy nhất

**Lệnh:**
```
gzip -r directory_name
```

## Giải nén một thư mục:

**Hành động:**
--- Giải nén tất cả các tệp trong một thư mục

**Chi tiết:**
--- Giải nén nhiều tệp dưới một thư mục từ một tệp lưu trữ duy nhất

**Lệnh:**
```
gzip -dr directory_name
```

## Đầu ra chi tiết (verbose) khi nén:

**Hành động:**
--- Nén một tệp một cách chi tiết hơn

**Chi tiết:**
--- Xuất thêm thông tin về hành động của lệnh

**Lệnh:**
```
gzip -v file_name
```