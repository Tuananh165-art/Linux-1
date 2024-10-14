# Lệnh `help`
Lệnh `help` hiển thị thông tin về các lệnh tích hợp sẵn.
Hiển thị thông tin về các lệnh tích hợp sẵn.

Nếu một `PATTERN` được chỉ định, lệnh này sẽ cung cấp trợ giúp chi tiết về tất cả các lệnh khớp với `PATTERN`, nếu không, danh sách các chủ đề trợ giúp có sẵn sẽ được in ra.

## Cú pháp
```bash
$ help [-dms] [PATTERN ...]
```

## Tùy chọn
|**Tùy chọn**|**Mô tả**|
|:--|:--|
|`-d`|Xuất mô tả ngắn cho mỗi chủ đề.|
|`-m`|Hiển thị cách sử dụng ở định dạng giả-manpage.|
|`-s`|Chỉ xuất một bản tóm tắt ngắn gọn về cách sử dụng cho mỗi chủ đề khớp với `PATTERN` được cung cấp.|

## Ví dụ sử dụng:
1. Chúng ta nhận được thông tin đầy đủ về lệnh `cd`
```bash
$ help cd
```
2. Chúng ta nhận được mô tả ngắn về lệnh `pwd`
```bash 	
$ help -d pwd
```
3. Chúng ta nhận được cú pháp của lệnh `cd`
```bash
$ help -s cd
```