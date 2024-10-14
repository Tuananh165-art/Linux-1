# Lệnh `cp`

Lệnh `cp` là một tiện ích dòng lệnh để sao chép tệp và thư mục.
`cp` là viết tắt của copy. Lệnh này được sử dụng để sao chép tệp hoặc nhóm tệp hoặc thư mục. Nó tạo ra một bản sao chính xác của một tệp trên đĩa với tên tệp khác. Lệnh cp yêu cầu ít nhất hai tên tệp trong các đối số của nó.

### Ví dụ:

1. Để sao chép nội dung của tệp nguồn vào tệp đích.

```
cp sourceFile destFile
```

Nếu tệp đích không tồn tại thì tệp được tạo và nội dung được sao chép vào đó. Nếu nó tồn tại thì tệp bị ghi đè.

2. Để sao chép một tệp vào một thư mục khác, chỉ định đường dẫn tuyệt đối hoặc tương đối đến thư mục đích.

```
cp sourceFile /folderName/destFile
```

3. Để sao chép một thư mục, bao gồm tất cả các tệp và thư mục con của nó

```
cp -R folderName1 folderName2
```

Lệnh trên tạo ra thư mục đích và sao chép đệ quy tất cả các tệp và thư mục con từ nguồn sang thư mục đích.

Nếu thư mục đích đã tồn tại, thư mục nguồn và nội dung của nó được sao chép vào bên trong thư mục đích.

4. Để sao chép chỉ các tệp và thư mục con nhưng không phải thư mục nguồn

```
cp -RT folderName1 folderName2
```

### Cú pháp:

Cú pháp chung cho lệnh cp như sau:

```
cp [OPTION] SOURCE DESTINATION
cp [OPTION] SOURCE DIRECTORY
cp [OPTION] SOURCE-1 SOURCE-2 SOURCE-3 SOURCE-n DIRECTORY
```

Cú pháp thứ nhất và thứ hai được sử dụng để sao chép tệp Nguồn vào tệp hoặc Thư mục Đích.
Cú pháp thứ ba được sử dụng để sao chép nhiều Nguồn (tệp) vào Thư mục.

#### Một số tùy chọn hữu ích

1. `-i` (tương tác)
   `i` là viết tắt của sao chép Tương tác. Với tùy chọn này, hệ thống trước tiên cảnh báo người dùng trước khi ghi đè tệp đích. cp nhắc nhở một phản hồi, nếu bạn nhấn y thì nó ghi đè tệp và với bất kỳ tùy chọn nào khác để lại nó không được sao chép.

```
$ cp -i file1.txt fileName2.txt
cp: overwrite 'file2.txt'? y
```

2. `-b`(sao lưu)
   -b(sao lưu): Với tùy chọn này, lệnh cp tạo bản sao lưu của tệp đích trong cùng thư mục với tên khác và định dạng khác.

```
$ ls
a.txt b.txt

$ cp -b a.txt b.txt

$ ls
a.txt b.txt b.txt~
```

3. `-f`(buộc)
   Nếu hệ thống không thể mở tệp đích để thực hiện thao tác ghi vì người dùng không có quyền ghi cho tệp này thì bằng cách sử dụng tùy chọn -f với lệnh cp, tệp đích bị xóa trước và sau đó sao chép nội dung từ nguồn sang tệp đích.
```
$ ls -l b.txt
-r-xr-xr-x+ 1 User User 3 Nov 24 08:45 b.txt
```
Người dùng, nhóm và những người khác không có quyền ghi.

Không có tùy chọn `-f`, lệnh không được thực thi

```
$ cp a.txt b.txt
cp: cannot create regular file 'b.txt': Permission denied
```

Với tùy chọn -f, lệnh được thực thi thành công
```
$ cp -f a.txt b.txt
```

### Các Tham Số Bổ Sung và Chức Năng của Chúng:

|**Cờ Rút Gọn**   |**Cờ Đầy Đủ**   |**Mô Tả**   |
|:---|:---|:---|
|`-i`|<center>--interactive</center>|nhắc nhở trước khi ghi đè|
|`-f`|<center>--force</center>|Nếu một tệp đích hiện có không thể được mở, hãy xóa nó và thử lại|
|`-b`|<center>-</center>|Tạo bản sao lưu của tệp đích trong cùng thư mục với tên khác và định dạng khác.|
|`-r hoặc -R`|`--recursive`|Lệnh **cp** thể hiện hành vi đệ quy của nó bằng cách sao chép toàn bộ cấu trúc thư mục đệ quy.|
|`-n`|`--no-clobber`|không ghi đè một tệp hiện có (ghi đè một tùy chọn -i trước đó)|
|`-p`|<center>-</center>|bảo toàn các thuộc tính được chỉ định (mặc định: chế độ, quyền sở hữu, dấu thời gian), nếu có thể các thuộc tính bổ sung: ngữ cảnh, liên kết, xattr, tất cả|

````
