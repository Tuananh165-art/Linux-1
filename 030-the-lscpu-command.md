# Lệnh `lscpu`

`lscpu` trong Linux/Unix được sử dụng để hiển thị thông tin Kiến trúc CPU. `lscpu` thu thập thông tin kiến trúc CPU từ các tệp `sysfs` và `/proc/cpuinfo`.

Ví dụ:
```
manish@godsmack:~$ lscpu
  Kiến trúc:        x86_64
  Chế độ hoạt động CPU:      32-bit, 64-bit
  Thứ tự Byte:          Little Endian
  CPU(s):              4
  Danh sách CPU trực tuyến: 0-3
  Số luồng trên mỗi lõi:  2
  Số lõi trên mỗi socket:  2
  Số socket:           1
  Số nút NUMA:        1
  ID nhà cung cấp:           GenuineIntel
  Gia đình CPU:          6
  Mô hình:               142
  Tên mô hình:          Intel(R) Core(TM) i5-7200U CPU @ 2.50GHz
  Bước:            9
  Tần số CPU MHz:             700.024
  Tần số tối đa CPU MHz:         3100.0000
  Tần số tối thiểu CPU MHz:         400.0000
  BogoMIPS:            5399.81
  Ảo hóa:      VT-x   
  Bộ nhớ đệm L1d:           32K
  Bộ nhớ đệm L1i:           32K
  Bộ nhớ đệm L2:            256K
  Bộ nhớ đệm L3:            3072K
  CPU(s) nút NUMA0:   0-3
```
  
## Tùy chọn

`-a, --all`
    Bao gồm các dòng cho CPU trực tuyến và ngoại tuyến trong đầu ra (mặc định cho -e). Tùy chọn này chỉ có thể được chỉ định cùng với tùy chọn -e hoặc -p. 
    Ví dụ: `lsof -a`

`-b, --online`
    Giới hạn đầu ra cho các CPU trực tuyến (mặc định cho -p). Tùy chọn này chỉ có thể được chỉ định cùng với tùy chọn -e hoặc -p. 
    Ví dụ: `lscpu -b`

`-c, --offline`
    Giới hạn đầu ra cho các CPU ngoại tuyến. Tùy chọn này chỉ có thể được chỉ định cùng với tùy chọn -e hoặc -p. 

`-e, --extended [=list]`
    Hiển thị thông tin CPU ở định dạng dễ đọc.
    Ví dụ: `lsof -e`
    
Để biết thêm thông tin: sử dụng `man lscpu` hoặc `lscpu --help`

````

````
