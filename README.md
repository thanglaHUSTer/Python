# Python cơ bản

## Kiểu dữ liệu cơ bản

Giống với các ngôn ngữ lập trình khác, Python cũng có các kiểu dữ liệu cơ bản như integers (số
nguyên), floats (số thực), booleans (kiểu dữ liệu True/False) và strings (chuỗi).

Để khai báo biến trong Python không cần chỉ định kiểu dữ liệu trước như những ngôn ngữ
khác mà khi ta gán dữ liệu cho biến thì python tự gán kiểu phù hợp cho biến.

Cú pháp để khai báo biến:

```python
# variable_name = value
x = 3
```

Đặt tên biến trong python có một vài quy tắc:
- Tên biến nên có nghĩa. Tên biến do mọi người tự đặt nhưng nên đặt theo ý nghĩa, tác dụng
của biến đấy trong chương trình. Thứ nhất là khi mọi người code dài, muốn ở dưới dùng lại
thì cũng dễ nhớ. Thứ hai là khi người khác đọc code của bạn sẽ dễ hiểu hơn.
- Tên biến phải bắt đầu với chữ cái hoặc dấu gạch dưới (_).
- Tên biến không được bắt đầu với số.
- Tên biến chỉ được chứa các chữ cái, các số và dấu gạch dưới (A-Z, a-z, 0-9, _)
- Tên biến có phân biệt chữ hoa chữ thường. Ví dụ age, AGE, Age, aGE là 4 tên biến khác nhau.

## Số

Số nguyên và số thực dùng như các ngôn ngữ khác

```python
x = 3
print(type(x))             # Prints "<class 'int'>"
print(x)                   # Prints "3"
print(x + 1)               # Cộng; prints "4"
print(x - 1)               # Trừ; prints "2"
print(x * 2)               # Nhân; prints "6"
print(x ** 2)              # Lũy thừa; prints "9"
x += 1                     # Giống với x = x + 1
print(x)
x *= 2                     # Giống x = x * 2
print(x)
y = 2.5
print(type(y))             # Prints "<class 'float'>"
print(y, y + 1, y * 2, y ** 2) # Prints "2.5 3.5 5.0 6.25"
```

## Phép logic

Python có kiểu dữ liệu boolean, các biến kiểu này nhận 2 giá trị là True hoặc False. Python có các phép tính logic nhưng dùng các từ tiếng anh (and, or) thay cho kí hiệu (&&, ||):

```python
t = True
f = False
print(type(t))   # Prints "<class 'bool'>"
print(t and f)   # AND; prints "False"
print(t or f)    # OR; prints "True"
print(not t)     # NOT; prints "False"
print(t != f)    # XOR; prints "True"
```

## Chuỗi

Python có hỗ trợ dạng chuỗi, để lưu giá trị dạng chuỗi có thể để trong dấu " hoặc ’ nhưng mở bằng dấu nào phải đóng bằng dấu đấy.

```python
# greet = "hello'          # câu lệnh này lỗi
hello = 'hello'            # gán giá trị chuỗi cho biến, chuỗi đặt trong 2 dấu'
world = "world"            # chuỗi cũng có thể đặt trong 2 dấu "
print(hello)               # Prints "hello"
print(len(hello))          # Độ dài chuỗi; prints "5"
hw = hello + ' ' + world   # Nối chuỗi bằng dấu +
print(hw)                  # prints "hello world"
hw12 = '{} {} {}'.format(hello, world, 12) # Cách format chuỗi
print(hw12)                # prints "hello world 12"
```

Kiểu string có rất nhiều method để xử lý chuỗi.

```python
print(s.capitalize())            # Viết hoa chữ cái đầu; prints "Hello"
print(s.upper())                 # Viết hoa tất cả chữ cái; prints "HELLO"
print(s.replace('l', '(ell)'))   # Thay thế chuỗi; prints "he(ell)(ell)o"
print(' world '.strip())         # Bỏ đi khoảng trắng ở đầu và cuỗi chuỗi;
                                 # prints "world"
print('Nguyen Thi  Hien'.split()) # Split chuỗi ra list, phần tích bằng 1 hoặc nhiều
                                  # khoảng trắng ; prints ['Nguyen', 'Thanh', 'Tuan']
print(' '.join(['Nguyen', 'Thi', 'Hien']) # Join các phần tử trong list lại với nhau,
                                          # các phần tử cách nhau bằng 1 khoảng trắng;
                                          # prints "Nguyen Thi Hien"
```     

