# Refactoring
- Refactoring là viết lại source code một cách khoa học hơn mà vẫn giữ được tính đúng đắn và giá trị về chức năng của source code đó.
- Mục đích chính của refactoring là để chống lại technical debt, biến đống code lộn xộn thành code sạch.
### Clean code
- Clean code là thứ mà mọi lập trình viên phải biết
- Clean code không lặp lại code
- Clean code nên chưa ít class và các phương thức
- Clean code vượt qua tất cả các test
- Clean code dễ dàng mở rộng và phát triển.
### Technical detb
- Khi tui có một khoản nợ ở ngân hàng, tui có tiền mua những thứ tui thích nhanh hơn. Đồng nghĩa với việc mình phải thanh toán thêm tiền lãi nữa. Khoản nợ còn nhỏ thì không sao. Khi nó đã lớn đến mức tiền lãi lớn hơn thu nhập hằng tháng của tui thì việc chi trả khoản nợ đó dường như là không thể. 
- Điều tương tự cũng sảy ra với đống code. Lúc đầu phát triển ứng dụng rất nhanh mà không cần quan tâm đến vấn đề clean code, các nguyên tắc, viết test cho tính năng mới,.. Rồi theo thời gian quá trình phát triển ứng dụng chầm dần và dần về con số 0.
#### Causes of technical debt
1. Business pressure (một số tình huốn trong businees buộc bạn phải triển khai các tính năng trước khi nó hoàn thiện. Sẽ có các bug và các tính năng chưa hoàn thành buộc bạn phải ẩn hoặc vá lỗi chúng)
2. Thiếu kiến thức về hậu quả của technical debt
3. Không hạn chế các liên kết chặt chẽ giữa các thành phần trong ứng dụng
4. Thiếu test
5. Thiếu tài liệu mô tả 
6. Thiếu giao tiếp giữa thành viên trong team
7. Phát triển đồng thời và dài hạn chỉ một nhánh
8. Trì hoãn việc refactorinng
9. Thiếu sự tuân thủ các nguyên tắc chung:( Kiểu ai thích gì code đó mà không tuân thủ các nguyên tắc mà ban đầu được liệt kê và đặt ra)
10. Incompetence (Kiểu không biết viết code sao cho tử tế)
### Why
  Refactoring không hề làm hệ thống chạy nhanh hơn, bảo mật hơn tuy nhiên nó sẽ giúp source dễ tiếp cận, dễ đọc, dễ hiểu từ đó giúp cho quá trình bảo trì mở rộng hệ thống trở nên dễ dàng hơn
### When 
  Bất cứ khi nào bạn muốn code của mình trở nên tốt hơn thì đều có thể thực hiện refactoring. Tuy nhiên một số thời điểm sau là thích hợp hơn để refactoring
1. Khi thêm chức năng mới vào source code cũ
2. Khi tiến hành review code
3. Khi code quá khó để đọc
4. Khi có quá nhiều bug
5. Lặp lại code
6. Khi cần bàn giao code lại 
#### When not
- Như đã đề cập trước đó, refactoring không làm thay đổi hay cải thiện hiệu suất bảo mật và nó chỉ được coi là một hình thức dọn dẹp. Tuy nhiên có những lúc một ứng dụng cần được cải tiến hoàn toàn ngay từ đầu. Trong những trường hợp này việc cấu trúc lại là không cần thiết vì nó chỉ hiệu quả hơn khi áp dụng ngay từ đầu.
- Một trường hợp khác khi bạn đang làm một dự án và còn ít thời gian để hoàn thành. Việc refactoring nó có thể trở nên khá tốn thời gian và dẫn đến nhiều chi phí phát sinh.
### Group of Smell
  -(**Smell**: Dịch ra tiếng việt chuối quá. Nên convert lại theo cách tui hiểu là tên của các vấn đề thường gặp trong code. Ví dụ như: phương thức quá phức tạp, lặp lại code, thông tin dư thừa...)
#### 1. Bloaters
- Bloaters là code, phương thức và class đã tăng lên mức khổng lồ đến mức mà chúng ta rất khó thể hiểu được nó. Thông thường những smell này không xuất hiện ngay lập tức, mà nó tích tụ qua thời gian trong quá trình phát triển ứng dụng.
- Một số product của smell này:
  - Long Method, Large Class, Long Parameter List, Primitive Obsession, Data Clumps.
#### 2. Object-Orientation Abusers
- Tất cả những smells này những sản phẩm được sinh ra do áp dụng không đầy đủ, không chỉnh xác của nguyên tắc hướng đối tượng.
#### 3. Change Preventers
- Những smells này có nghĩa rằng nếu bạn cần thay đổi một chỗ nào đó trong ứng dụng của mình bạn phải làm điều đó với nhiều nơi trong ứng dụng. Khi phát triển ứng dụng làm cho nó trở nên phức tạp và rất tốn kém về thời gian và tiền bạc.
#### 4. Dispensables
- Dispensable thường là một điều không cần thiết, ít ý nghĩa. Sự vắng mặt của nó có thể làm cho mã sạch hơn và ý nghĩa hơn
#### 5. Couplers
- Tất cả các smells trong nhóm Coupers này tạo nên sự kết hợp quá mức giữa 2 class.(tight coupling)

### Reference
[refactoring.guru](https://refactoring.guru/refactoring)
[viblo.asia](https://viblo.asia/p/code-refactoring-PaLkDYldvlX)
[altexsoft.com](https://www.altexsoft.com/blog/engineering/code-refactoring-best-practices-when-and-when-not-to-do-it/#:~:text=The%20best%20time%20to%20consider,build%20on%20the%20original%20code.)