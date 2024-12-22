# Toán tử trong Javascript

## I. Toán tử là gì?

- Toán tử là các dấu hay ký tự đặc biệt, dùng để thực hiện các thao tác trên giá trị hoặc biến nào đó để cho ra kết quả cuối cùng.

## II. Các loại toán tử

Trong JavaScript có nhiều loại toán tử mà bạn nên biết như :

- Toán tử số học - Arithmetic Operators
- Toán tử gán - Assignment Operators
- Toán tử so sánh - Comparison Operators
- Toán tử logic - Logical Operators
- Toán tử chuỗi - String Operators
- Toán tử ba ngôi - ternary operator

#### 1. Toán tử số học - Arithmetic Operators

Toán tử số học trong JavaScript là các ký hiệu dùng để thực hiện các phép tính toán học cơ bản trên số. Chúng giúp xử lý các phép toán như cộng, trừ, nhân, chia...

| <div style="width: 200px;text-align: center;">Toán tử</div> | <div style="width: 200px;text-align: center;"> Mô tả</div> |
| :---------------------------------------------------------: | :--------------------------------------------------------: |
|                              +                              |                            Cộng                            |
|                              -                              |                            Trừ                             |
|                             \*                              |                            Nhân                            |
|                            \*\*                             |                       Nhân lũy thừa                        |
|                              /                              |                            chia                            |
|                              %                              |                        Chia lấy dư                         |
|                             ++                              |                 Tăng giá trị lên 1 đơn vị                  |
|                             --                              |                Giảm giá trị xuống 1 đơn vị                 |

**Ví dụ :**

```bash
let x = 10;
let y = 3;

console.log(x + y);  // 13
console.log(x - y);  // 7
console.log(x * y);  // 30
console.log(x / y);  // 3.3333333333333335
console.log(x % y);  // 1
console.log(x ** y); // 1000
x++;
console.log(x);      // 11
x--;
console.log(x);      // 10
```

#### 2. Toán tử gán - Assignment Operators

Toán tử gán được sử dụng để gán giá trị cho một biến. Toán tử gán cơ bản là `=`, nhưng JavaScript cũng cung cấp nhiều toán tử gán kết hợp để thực hiện các phép tính và gán giá trị cùng lúc.

| <div style="width: 150px;text-align: center;">Toán tử</div> | <div style="width: 150px;text-align: center;"> Mô tả</div> | <div style="width: 150px;text-align: center;"> Tương đương</div> |
| :---------------------------------------------------------: | :--------------------------------------------------------: | :--------------------------------------------------------------: |
|                              =                              |                           x = y                            |                              x = y                               |
|                             +=                              |                           x += y                           |                            x = x + y                             |
|                             -=                              |                           x -= y                           |                            x = x - y                             |
|                             \*=                             |                          x \*= y                           |                            x = x \* y                            |
|                             /=                              |                           x /= y                           |                            x = x / y                             |
|                             %=                              |                           x %= y                           |                            x = x % y                             |
|                            \*\*=                            |                         x \*\*= y                          |                            x = x\*\*y                            |

**Ví dụ:**

```bash
let x = 10;

x += 5;  // x = 10 + 5 (x = 15)
x -= 3;  // x = 15 - 3 (x = 12)
x *= 2;  // x = 12 * 2 (x = 24)
x /= 4;  // x = 24 / 4 (x = 6)
x %= 5;  // x = 6 % 5 (x = 1)
x **= 3; // x = 1 ** 3 (x = 1)
```

#### 3. Toán tử so sánh - Comparison Operators

Dùng để so sánh hai giá trị và trả về một kết quả kiểu boolean (true hoặc false). Chúng thường được dùng trong các điều kiện hoặc các biểu thức logic.

| <div style="width: 200px;text-align: center;">Toán tử</div> | <div style="width: 200px;text-align: center;"> Mô tả</div> |
| :---------------------------------------------------------: | :--------------------------------------------------------: |
|                             ==                              |                 So sánh bằng theo giá trị                  |
|                             ===                             |              So sánh bằng cả giá trị và kiểu               |
|                             !=                              |              So sánh không bằng theo giá trị               |
|                             !==                             |         So sánh không bằng theo cả giá trị và kiểu         |
|                              >                              |                          Lớn hơn                           |
|                              <                              |                           Bé hơn                           |
|                             >=                              |                     Lớn hơn hoặc bằng                      |
|                             <=                              |                      Bé hơn hoặc bằng                      |

**Lưu ý:** khi sử dụng `==` `===` và `!=` `!==`

- == không so sánh kiểu dữ liệu, do đó nó sẽ tự động chuyển đổi (coerce) kiểu dữ liệu để so sánh.

- === yêu cầu cả giá trị và kiểu phải giống nhau.

```bash
console.log("5" == 5); // true
console.log("5" === 5); // false
```

- `!=` và `!==` tương tự

```bash
console.log("5" != 5); // false
console.log("5" !== 5); // true
```

#### 4. Toán tử logic - Logical Operators

Toán tử logic được sử dụng để thực hiện các phép toán logic, thường dùng để kết hợp nhiều điều kiện hoặc biểu thức và trả về kết quả dạng boolean (true hoặc false) Rất phổ biến trong các cấu trúc điều khiển như if-else, while, hoặc trong các điều kiện phức tạp.

| <div style="width: 200px;text-align: center;">Toán tử</div> | <div style="width: 200px;text-align: center;"> Tên </div> |                          <div style="width: 200px;text-align: center;"> Mô tả</div>                           |
| :---------------------------------------------------------: | :-------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------: |
|                             &&                              |                        Toán tử AND                        |                   Trả về `true` nếu tất cả các biểu thức đều đúng, ngược lại trả về `false`                   |
|                            \|\|                             |                        Toán tử OR                         |               Trả về `true` nếu ít nhất một trong các biểu thức đúng, ngược lại trả về `false`                |
|                              !                              |                        Toán tử NOT                        | Đảo ngược giá trị logic của một biểu thức. <br> Nếu biểu thức là `true`, kết quả sẽ là `false`, và ngược lại. |

```bash
// AND
console.log(true && true);   // true
console.log(true && false);  // false
console.log(5 > 3 && 10 > 8); // true
// OR
console.log(true || false);  // true
console.log(false || false); // false
console.log(5 > 10 || 8 > 3); // true
// NOT
console.log(!true);    // false
console.log(!false);   // true
console.log(!(5 > 3)); // false
```

#### 5. Toán tử nối chuỗi

- Toán tử nối chuỗi (+): dừng để nối các chuỗi và biến lại với nhau
  Cú pháp: chuỗi1 + chuỗi2

```bash
let firstName = "John";
let lastName = "Doe";
console.log(firstName + " " + lastName); // "John Doe"
console.log(5 + "5");// 55
```

Lưu ý: Nếu một trong các toán hạng là số và toán hạng còn lại là chuỗi, thì JavaScript sẽ chuyển số thành chuỗi trước khi nối

#### 6. Toán tử ba ngôi - ternary operator

Toán tử ba ngôi là một cách ngắn gọn để viết các câu lệnh điều kiện if-else một cách ngắn gọn. Đây là toán tử duy nhất trong JavaScript có ba toán hạng.
Điều kiện ? giá trị 1 : giá trị 2

giá trị 1: Giá trị hoặc biểu thức được thực thi nếu Điều kiện là true.
giá trị 2: Giá trị hoặc biểu thức được thực thi nếu Điều kiện là false.

```bash
let age = 20;
let access = (age >= 18) ? "Được phép truy cập" : "Bạn chưa đủ tuổi";
console.log(access); // "Được phép truy cập"
```

Ưu điểm:

- Ngắn gọn và dễ viết: Giúp mã ngắn hơn khi xử lý điều kiện đơn giản.
- Trực quan hơn: Khi viết mã ngắn gọn, dễ hiểu hơn.

Nhược điểm:

- Khó đọc: Nếu lồng nhiều toán tử ba ngôi, mã sẽ trở nên khó hiểu.
- Hạn chế với logic phức tạp: Với các điều kiện phức tạp, if-else sẽ rõ ràng hơn.

#### 7. Lời kết

Trên đây là các loại toán tử phổ biến thường gặp, ngoài ra trong Js còn một số toán tử khác mang tính chuyên dụng hơn các bạn có thể chủ động tìm hiểu thêm nhé. Để giải quyết các bài toán lập trình với Javascript việc nắm vững các toán tử Js là yêu cầu bắt buộc đối với các lập trình viên.
