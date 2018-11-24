# OOP-PHP




## Sự khác nhau giữa Trait, Interface, Abstract
Interface | Abstract | Trait 
----------|----------|------
 chỉ  khai báo phương thức , các hằng. Không được khai báo biến  Không định nghĩa các phương thức  | Là một lớp  chứa các biến , hằng , abstract method và method ,các abstract method không được định  |  Traits là một module giúp cho chúng ta có thể sử dụng lại các phương thức, thuộc  được khai báo trong trait  vào các class khác nhau một cách đơn giản
Khai báo Interface dùng từ khóa interface để thay thế cho từ khóa class | Thêm từ khóa abstract trước từ khóa class |  Để khai báo , sử dụng cú pháp trait thay cho class
Một class có thể implement nhiều interface | class chỉ có thể kết thừa 1 asbstract | class có thể use nhiều trait 
Nếu một lớp khác implement một interface thì nó phải khai báo và định nghĩa tất cả các phương thức trong interface | Lớp abstract sẽ định nghĩa các phương thức mà từ đó các lớp con sẽ kế thừa nó và OVERWITE lại | Các phương thức trong Traits có thể bị override lại trong class sử dụng nó
Có tính kế thừa : Một interface A có thể kế thừa một interface B. Lúc này lớp nào implement interface A thì phải định nghĩa lại tất cả các phương thức mà cả hai interface A và B đã khai báo | Lớp Abstract cũng có tính kế thừa. abstract A kế thừa abstract B thì một lớp nào đó kế thừa A phải viết lại toàn bộ các phương thức của  abstract A và B | Có thể lồng nhau một cách đơn giản
Không có khái niệm phạm vi của interface, tất cả đều là public. |  visibility là một trong 2 từ khóa public, protected | Các phương thức trong trait có thể thay đổi được phạm vi
Sử  dụng : Khi muốn lớp con tuân thủ theo các phương thức được khai báo trong interface và lớp con có thể kế thừa nhiều interface |Khi bạn muốn người lập trình phải tuân thủ theo một số các phương thức và các phương thức này đã được định nghĩa sẵn những thứ cơ bản, để giúp cho lập trình viên có thể kế thừa các phương thức này và phát triển lớp con của họ. | Khi nhiều class sử dụng chung phương thức, ta có thể gom các phương thức chung vào 1 trait để sử dụng nhiều lần



## Sự khác biệt giữa public, private và protected
Private | Protected | Public
--------|-----------|--------
Ta không thể truy xuất tới thành phần private ở lớp con hoặc ở bên ngoài lớp | Chỉ cho phép truy xuất nội bộ trong lớp đó và lớp kế thừa, riêng ở bên ngoài lớp sẽ không truy xuất được, mức protected thường được sử dụng cho những phương thức và thuộc tính có khả năng bị lớp con định nghĩa lại | Có thể truy cập tới các phương thức và thuộc tính ở bất cứ đâu, dù trong nội bộ của lớp hay ở lớp con hay cả bên ngoài lớp đều được
## Từ khóa Final : 
  - Để chống kế thừa : Muốn tước quyền kế thừa cho một class, đặt từ kháo Final trước class đó 
  - Chống Override : Khi muốn một phương thức không được Override từ các phương thức của class khác. Đặt từ khóa final trước tên phương thức đó