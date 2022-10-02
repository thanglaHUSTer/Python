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

### Số

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

### Phép logic

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

### Chuỗi

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
s = "hello"
print(s.capitalize())            # Viết hoa chữ cái đầu; prints "Hello"
print(s.upper())                 # Viết hoa tất cả chữ cái; prints "HELLO"
print(s.replace('l', '(ell)'))   # Thay thế chuỗi; prints "he(ell)(ell)o"
print(' world '.strip())         # Bỏ đi khoảng trắng ở đầu và cuỗi chuỗi;
                                 # prints "world"
print('Nguyen Thi  Hien'.split()) # Split chuỗi ra list, phần tích bằng 1 hoặc nhiều
                                  # khoảng trắng ; prints ['Nguyen', 'Thi', 'Hien']
print(' '.join(['Nguyen', 'Thi', 'Hien']) # Join các phần tử trong list lại với nhau,
                                          # các phần tử cách nhau bằng 1 khoảng trắng;
                                          # prints "Nguyen Thi Hien"
```     

## Containers

Các kiểu dữ liệu cơ bản chỉ chứa một giá trị mỗi biến (số, chuỗi), tuy nhiên nhiều lúc mình cần chứa nhiều giá trị, ví dụ chứa tên học sinh trong một lớp có 100 bạn. Mình không thể tạo 100 biến để lưu tên 100 bạn. Vậy nên cần các kiểu dữ liệu có thể chứa nhiều giá trị khác nhau. Đó là container (collection). Python có một số container như: list, tuple, set, dictionary. Dưới tôi sẽ trình bày hai kiểu dữ liệu collection mà mọi người hay gặp nhất trong python là list và dictionary.

### List

List trong Python giống như mảng (array) nhưng không cố định kích thước và có thể chứa nhiều
kiểu dữ liệu khác nhau trong 1 list.

```python
xs = [3, 1, 2]     # Tạo 1 list
print(xs, xs[2])   # Prints "[3, 1, 2] 2"
print(xs[-1])      # Chỉ số âm là đếm phần tử từ cuối list lên; prints "2"
xs[2] = 'foo'      # List có thể chứa nhiều kiểu phần tử khác nhau
print(xs)          # Prints "[3, 1, 'foo']"
xs.append('bar')   # Thêm phần tử vào cuối list
print(xs)          # Prints "[3, 1, 'foo', 'bar']"
x = xs.pop()       # Bỏ đi phần tử cuối cùng khỏi list và trả về phần tử đấy
print(x, xs)       # Prints "bar [3, 1, 'foo']"
```

**Slicing** Thay vì lấy từng phần tử một trong list thì python hỗ trợ truy xuất nhiều phần tử 1 lúc gọi là slicing.

```python
nums = list(range(5)) # range sinh ta 1 list các phần tử
print(nums)           # Prints "[0, 1, 2, 3, 4]"
print(nums[2:4])      # Lấy phần tử thứ 2->4, python chỉ số mảng từ 0;
print(nums[2:])       # Lấy phần tử thứ 2 đến hết; prints "[2, 3, 4]"
print(nums[:2])       # Lấy từ đầu đến phần tử thứ 2; prints "[0, 1]"
print(nums[:])        # Lấy tất cả phần tử trong list; prints "[0, 1, 2, 3, 4]"
print(nums[:-1])      # Lấy từ phần tử đầu đến phần tử gần cuối trong list;
                      # prints "[0, 1, 2, 3]"
nums[2:4] = [8, 9]    # Gán giá trị mới cho phần tử trong mảng từ vị trí 2->4
print(nums)           # Prints "[0, 1, 8, 9, 4]"
```

**Loops** Để duyệt và in ra các phần tử trong list

```python
animals = ['cat', 'dog', 'monkey']
# duyệt giá trị không cần chỉ số
for animal in animals:
    print('%s' % (animal))
# duyệt giá trị kèm chỉ số dùng enumerate
for idx, animal in enumerate(animals):
    print('#%d: %s' % (idx + 1, animal))
# Prints "#1: cat", "#2: dog", "#3: monkey", in mỗi thành phần trong list 1 dòng
```

### Dictionaries

Dictionaries lưu thông tin dưới dạng key, value.

```python
d = {'cat': 'cute', 'dog': 'furry'} # Tạo dictionary, các phần tử dạng key:value
print(d['cat'])           # Lấy ra value của key 'cat' trong dictionary prints "cute"
print('cat' in d)         # Kiểm tra key có trong dictionary không; prints "True"
d['fish'] = 'wet'         # Gán key, value, d[key] = value
print(d['fish'])          # Prints "wet"
# print(d['monkey'])      # Lỗi vì key 'monkey' không trong dictionary
del d['fish']             # Xóa phần tử key:value từ dictionary
```

**Loop** Duyệt qua các phần tử trong dictionary

```python
d = {'person': 2, 'cat': 4, 'spider': 8}
# Duyệt key
for animal in d:
    print('A %s has %d legs' % (animal, d[animal]))
# Prints "A person has 2 legs", "A cat has 4 legs", "A spider has 8"

# Duyệt value
for legs in d.values():
    print('%d legs' % (legs))
# Prints "2 legs", "4 legs", "8 legs"

# Duyệt cả key và value
for animal, legs in d.items():
    print('A %s has %d legs' % (animal, legs))
# Prints "A person has 2 legs", "A cat has 4 legs", "A spider has 8 legs"
```

## Function

Function (hàm) là một khối code python được thực hiện một hoặc một số chức năng nhất định. Hàm
có input và có ouptut, trước khi viết hàm mọi người nên xác định hàm này để làm gì? input là gì? output làm gì?

Ví dụ hàm kiểm tra số nguyên tố, mục đích để kiếm tra 1 số xem có phải là số nguyên tố hay không, input là 1 số nguyên dương, output dạng boolean (True/False). True tức là số input là số nguyên tố, False nghĩa là không phải số nguyên tố.

Function trong python được định nghĩa với keyword **def**.

```python
# Hàm có input là 1 số và output xem số đấy âm, dương hay số 0
# Định nghĩa hàm
def sign(x):
    if x > 0:
        return 'positive'
    elif x < 0:
        return 'negative'
    else:
        return 'zero'
for x in [-1, 0, 1]:
    # Gọi hàm
    print(sign(x))
# Prints "negative", "zero", "positive"
```

## Thư viện trong python

Thư viện (library) bao gồm các hàm (function) hay lớp (class) được viết sẵn với các chức năng khác nhau. Ví dụ thư viện math cung cấp các hàm về tính toán như exp, sqrt, floor,...

Muốn nhập thư viện vào chương trình, ta dùng cú pháp: import tên thư viện, ví dụ: import numpy.

Đối với những thư viện có tên dài, ta thường rút ngắn lại để sau này dễ sử dụng. Khi đó, ta
sử dụng cú pháp: import tên thư viện as tên rút gọn, ví dụ: import matplotlib.pyplot as plt. Sau này, khi sử dụng đến thư viện, ta chỉ cần gọi đến tên rút gọn thay vì phải gõ lại tên đầy đủ của thư viện, ví dụ thay vì viết matplotlib.pyplot.plot, ta chỉ cần viết plt.plot.

## Thư viện Numpy

Vì Python là scripting language nên không thích hợp cho machine learning, numpy giải quyết vấn
đề trên bằng cách xây dựng 1 thư viện viết bằng C nhưng có interface Python. Như vậy Numpy
cộng hưởng 2 ưu điểm của 2 ngôn ngữ: nhanh như C và đơn giản như Python. Điều này giúp ích rất
nhiều cho cộng đồng Machine Learning trên Python.

Mảng trong numpy gồm các phần tử có dùng kiểu giá trị, chỉ số không âm được bắt đầu từ
0, số chiều được gọi là rank của mảng Numpy, và shape của mảng là một tuple các số nguyên đưa
ra kích thước của mảng theo mỗi chiều.
