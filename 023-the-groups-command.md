# Lệnh `groups`

Trong Linux, có thể có nhiều người dùng (những người sử dụng/vận hành hệ thống) và các nhóm (một tập hợp người dùng). 
Nhóm giúp dễ dàng quản lý người dùng với cùng quyền truy cập và bảo mật. Một người dùng có thể là thành viên của nhiều nhóm khác nhau.

Điểm quan trọng:

Lệnh `groups` in ra tên của nhóm chính và bất kỳ nhóm bổ sung nào cho mỗi tên người dùng được cung cấp, hoặc quá trình hiện tại nếu không có tên nào được đưa ra.
Nếu có nhiều hơn một tên được đưa ra, tên của mỗi người dùng được in trước danh sách các nhóm của người dùng đó và tên người dùng được tách biệt khỏi danh sách nhóm bằng dấu hai chấm.

### Cú pháp:

```
groups [username]
```

#### Ví dụ 1

Cung cấp với một tên người dùng

```
groups demon
```

Trong ví dụ này, tên người dùng demon được truyền với lệnh groups và đầu ra hiển thị các nhóm mà người dùng demon có mặt, được tách biệt bằng dấu hai chấm.

#### Ví dụ 2

Khi không có tên người dùng nào được truyền thì điều này sẽ hiển thị thành viên nhóm cho người dùng hiện tại:

```
groups
```

Ở đây người dùng hiện tại là demon. Vì vậy khi chúng ta chạy lệnh `groups` mà không có đối số, chúng ta sẽ nhận được các nhóm mà demon là thành viên.

#### Ví dụ 3

Truyền root với lệnh groups:

```
$demon# groups
```

> Lưu ý: Các nhóm chính và bổ sung cho một quá trình thường được kế thừa từ cha mẹ của nó và thường không thay đổi kể từ khi đăng nhập. Điều này có nghĩa là nếu bạn thay đổi cơ sở dữ liệu nhóm sau khi đăng nhập, groups sẽ không phản ánh các thay đổi của bạn trong phiên đăng nhập hiện tại. Các tùy chọn duy nhất là –help và –version.
