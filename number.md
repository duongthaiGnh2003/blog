# Kiểu dữ liệu number trong Javascript

- Số (number) trong Javascript là một trong những kiểu giá trị quan trọng và phổ biến trong tất cả ngôn ngữ lập trình. Vậy chúng ta hãy cùng bắt đầu tìm hiểu về cách Number hoạt động và giúp bạn phát triển các ứng dụng JavaScript như thế nào nhé.

### 1. Khái niệm và phân loại

- Số (number) là kiểu dữ liệu đại diện cho tất cả các giá trị số gồm cả số nguyên và số thực (số dấu phẩy động).
- Không phân biệt giữa số nguyên (integer) và số thực (float), tất cả đều thuộc kiểu Number.

```bash
let x = 10;
let y = 10.5;
let z = 1e6;
```

- Gồm có 2 kiểu chính:
  **Các số thường:** Đây là kiểu dữ liệu số thông dụng nhất trong JavaScript, dùng để đại diện cho tất cả các giá trị số gồm:

  - Số nguyên (e.g., 10, -5)
  - Số thực (số thập phân, e.g., 3.14, -0.001)
  - Các giá trị đặc biệt: - Infinity (Vô cực). - Infinity: Âm vô cực.
    NaN (Not-a-Number): Xuất hiện khi một phép toán số học không hợp lệ.

- trong Javascript được lưu dưới dạng 64bit IEEE 754 (số phẩy động)

```bash
let a = 42;       // Số nguyên
let b = 3.14;     // Số thực
let c = Infinity; // Vô cực
let d = NaN;      // Không phải số
```

**BigInt (Kiểu số lớn):** Là loại số sử dụng để biểu thị số nguyên rất lớn (hoặc rất nhỏ) hoặc có độ dài tùy ý.

- BigInt là kiểu dữ liệu mới được giới thiệu từ ECMAScript 2020.
  Ký hiệu bằng cách thêm chữ n ở cuối số.

```bash
let largeNumber = 123456789012345678901234567890n; // Số nguyên rất lớn
let smallNumber = 10n; // Số nguyên nhỏ
```

### 2. Làm việc với số

**Các phép toán cơ bản:** cộng, trừ, nhân, chia, chia lấy dư, lũy thừa.

```bash
let x = 10;
let y = 3;

console.log(x + y); // 13
console.log(x - y); // 7
console.log(x * y); // 30
console.log(x / y); // 3.3333333333333335
console.log(x % y); // 1 (chia lấy dư)
console.log(2 ** 3); // 8 (2 mũ 3)
```

**Tăng giảm một đơn vị**

- Tăng (++)

```bash
let x = 5;
x++;  // Tăng 1 -> x = 6
```

- Giảm (--)

```bash
let x = 5;
x--;  // Giảm 1 -> x = 4
```

- Lưu ý:
  Tiền tố (++x hoặc --x): Thực hiện phép toán trước khi trả giá trị.
  Hậu tố (x++ hoặc x--): Trả giá trị trước khi thực hiện phép toán.

##### Sử dụng các phương thức của đối tượng `Math`

- Math.PI: Lấy ra số pi.
- Math.round(): Làm tròn đến số nguyên gần nhất.
- Math.abs(): Lấy giá trị tuyệt đối.
- Math.ceil() : làm tròn lên.
- Math.floor(): làm tròn dưới.
- Math.max(): trả về số lớn nhất trong dãy số.
- Math.min(): trả về số nhỏ nhất trong dãy số.
- Math.pow(): tính số mũ.
- Math..sqrt(): tính căn bậc hai.
- Math.random(): in ra dãy số thập phân ngẫu nhiên nhỏ hơn 1.

```bash
console.log(Math.PI); // 3.141592653589793
console.log(Math.round(3.7)); // 4
console.log(Math.abs(-10));   // 10
console.log(Math.ceil(3.1));  // 4
console.log(Math.floor(3.9)); // 3
console.log(Math.max(1, 2, 3)); // 3
console.log(Math.min(1, 2, 3)); // 1
console.log(Math.pow(2, 3)); // 8 (2 mũ 3)
console.log(Math.sqrt(25));  // 5
console.log(Math.random());
```

##### Sử dụng đối tượng Number

- Number.isFinite(value): Kiểm tra giá trị có phải số hữu hạn hay không.
- Number.isInteger(value): Kiểm tra giá trị có phải số nguyên hay không.
- parseInt(value): chuyển chuỗi thành số phẩy động.
- parseFloat(value): chuyển chuỗi thành số nguyên.
- toString(): chuyển số thành chuỗi.
- toFixed(): làm tròn số.

```bash
console.log(Number.isFinite(2/0)) // false
console.log(Number.isFinite(20/4)) // true
console.log(Number.isInteger(99)) // true
console.log(Number.isInteger(0.5)) // false
console.log(parseInt("42"));    // 42
console.log(parseInt("46.5"));    // 46
console.log(Number.parseFloat("3.14"));  // 3.14
```

### 3. Tổng kết

Trong bài viết này, mình đã giới thiệu với các bạn về kiểu dữ liệu số (number) và cách làm việc với chuỗi trong JavaScript, từ việc khởi tạo đến các phương thức phổ biến khi làm việc với số trong JavaScript.
Hy vọng bài viết này sẽ có thể giúp đỡ các bạn trong quá trình học và tìm hiểu về JavaScript.
