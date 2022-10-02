# Python Systax

## Thụt lề trong Python

Thụt lề đề cập đến khoảng trắng ở đầu dòng code.

Trong các ngôn ngữ lập trình khác, thụt lề trong code chỉ để dễ đọc, tuy nhiên thụt lề trong Python là rất quan trọng.

Python sử dụng thụt đầu dòng để chỉ một khối code.

Thí dụ:

```Python
if 5 > 2:
    print("Five is greater than two!")
```

Python sẽ báo lỗi nếu bạn bỏ qua thụt đầu dòng. `Syntax Error`

Số lượng khoảng trắng khi thụt đầu dòng là tùy thuộc vào bạn. Với tư cách là một lập trình viên, cách sử dụng phổ biến nhất là bốn khoảng trắng (1 Tab).

```Python
if 5 > 2:
 print("Five is greater than two!") 
if 5 > 2:
        print("Five is greater than two!") 
```

Bạn phải sử dụng cùng một số lượng khoảng trắng trong cùng một khối code, nếu không Python sẽ báo cho bạn một lỗi. `Syntax Error`

## Biến trong Python

Trong Python, các biến được tạo khi bạn gán giá trị cho nó:

Thí dụ:

```Python
x = 5
y = "Hello, World"
```

Python không có lệnh để khai báo một biến.

Bạn sẽ tìm hiểu thêm về các biến trong phần [Biến trong Python]().

## Comments

Python có khả năng thêm comments trong code.

Comments bắt đầu bằng ký tự `#`, và Python sẽ hiển thị phần còn lại của dòng dưới dạng một dòng nhận xét.

Thí dụ:

```Python
#This is a comment
print("Hello, World")
```

