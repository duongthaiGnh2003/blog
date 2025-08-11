# Vòng lặp cà các loại vong lặp trong JavaScript

Vòng lặp là một phần quan trọng trong JavaScript, được sử dụng để tự động hóa các tác vụ lặp lại và xử lý dữ liệu hiệu quả. Việc nắm vững cách sử dụng vòng lặp sẽ giúp bạn tối ưu hóa mã nguồn và làm cho công việc lập trình trở nên dễ dàng hơn.

Vậy, vòng lặp hoạt động như thế nào trong JavaScript? Trong bài viết này, chúng ta sẽ cùng khám phá những khái niệm cơ bản và ứng dụng thực tiễn của vòng lặp.

## I. Tổng quan

#### 1. Khái niệm

- Vòng lặp (Loop) trong JavaScript là một cấu trúc giúp thực thi lặp đi lặp lại một đoạn mã cho đến khi một điều kiện nhất định được thỏa mãn.

#### 2. Đặc điểm

\- Tự động hóa các tác vụ lặp lại
\- Kiểm soát điều kiện lặp
\- Duyệt qua cấu trúc dữ liệu: array hoặc object
\- Lồng vòng lặp (Nested Loop): để xử lý dữ liệu phức tạp
\- Phương thức hiện đại

## II. Các loại vòng lặp

#### 1. Vòng lặp `for`

Vòng lặp for là loại vòng lặp phổ biến nhất, dùng để lặp qua một dãy số hoặc mảng với số lần lặp xác định trước. Vòng lặp này thường được sử dụng khi bạn biết trước số lần lặp.

**Cú pháp:**

```bash
 for (initialization; condition; increment) {
  // Thực thi đoạn mã
}
```

- **Initialization:** Khởi tạo giá trị ban đầu của biến lặp.
- **Condition:** Điều kiện để vòng lặp tiếp tục - chạy.
- **Increment:** Thay đổi giá trị của biến lặp sau mỗi lần lặp.

**Ví dụ:**

```bash
for (let i = 0; i < 5; i++) {
console.log(i); // In ra: 0, 1, 2, 3, 4
}

// Khai báo mảng
let arr = ["a","b","c","d"];
for (let i = 0; i < arr.length; i++) {
    console.log(arr[i]); // In ra: a b c d
}
```

#### 2. Vòng lặp for...in

Vòng lặp for...in được sử dụng để duyệt qua các thuộc tính của một đối tượng. Nó giúp bạn lặp qua tất cả các khóa (key) trong một đối tượng.

**Cú pháp:**

```bash
for (let key in object) {
  // Thực thi đoạn mã
}
```

- **key:** Tên thuộc tính (key) của đối tượng.
- **object:** Đối tượng cần duyệt qua.

**Ví dụ:**

```bash
const person = { name: "Alice", age: 25, job: "Engineer" };
for (let key in person) {
console.log(key, person[key]);  // In ra: name Alice, age 25, job Engineer
}
```

#### 3. Vòng Lặp for...of

Vòng lặp for...of được sử dụng để duyệt qua các giá trị của một iterable (như mảng, chuỗi, hoặc Map). Nó giúp bạn dễ dàng truy cập các phần tử trong một mảng hoặc chuỗi mà không cần phải sử dụng chỉ số.

**Cú pháp:**

```bash
  for (let value of iterable) {
  // Thực thi đoạn mã
}
```

- **value:** Giá trị của từng phần tử trong iterable.
- **iterable:** Dữ liệu có thể lặp (mảng, chuỗi, Map, v.v.).

**Ví dụ:**

```bash
let arr = [10, 20, 30, 40];

for (let value of arr) {
    console.log(value);
}
// 10
// 20
// 30
// 40
```

#### 4. Vòng Lặp while

Vòng lặp while lặp lại đoạn mã khi điều kiện đúng. Loại vòng lặp này được sử dụng khi bạn không biết trước số lần lặp, mà thay vào đó dựa vào một điều kiện.

**Cú pháp:**

```bash
while (condition) {
   // Thực thi đoạn mã
}
```

- **condition:** Đây là biểu thức điều kiện. Vòng lặp sẽ tiếp tục chạy cho đến khi điều kiện này trả về false.
- Mã trong thân vòng lặp sẽ được thực thi mỗi lần điều kiện là true.

**Ví dụ:**

```bash
let i = 0;
while (i < 5) {
    console.log(i);
    i++;
}
```

#### 5. Vòng Lặp do...while

Vòng lặp do...while là một loại vòng lặp đặc biệt. Điểm khác biệt lớn so với vòng lặp while là vòng lặp do...while đảm bảo thực thi ít nhất một lần.
Điều kiện chỉ được kiểm tra sau khi đoạn mã trong vòng lặp được thực thi lần đầu. Điều này khiến vòng lặp do...while trở thành lựa chọn tốt khi bạn muốn đảm bảo rằng mã trong vòng lặp sẽ được thực thi ít nhất một lần.

**Cú pháp:**

```bash
do {
 // Thực thi đoạn mã
} while (condition);
```

- **condition:** Là điều kiện được kiểm tra sau mỗi lần thực thi mã trong thân vòng lặp.

**Ví dụ:**

```bash
let i = 1;
do {
    console.log(i);
    i++;
} while (i <= 5);
```

#### 6. Phương thức forEach()

`forEach` là một phương thức trong JavaScript được sử dụng để lặp qua các phần tử của một mảng. Phương thức này sẽ thực thi một hàm callback cho mỗi phần tử trong mảng theo thứ tự, và nó không trả về giá trị nào.
**Lưu ý:** `forEach` chỉ làm việc với mảng, không thể sử dụng trên các đối tượng khác.

**Cú pháp:**

```bash
array.forEach(function(currentValue, index, array) {
    // Mã lệnh thực thi cho mỗi phần tử
});
```

- **currentValue:** Giá trị của phần tử hiện tại trong mảng.
- **index (tùy chọn):** Chỉ số của phần tử trong mảng.
- **array (tùy chọn):** Mảng gốc mà bạn đang lặp qua.

**Ví dụ:**

```bash
let arr = [1, 2, 3, 4, 5];
arr.forEach(function(value, index) {
    console.log(`Index: ${index}, Value: ${value}`);
});
// Index: 0, Value: 1
// Index: 1, Value: 2
// Index: 2, Value: 3
// Index: 3, Value: 4
// Index: 4, Value: 5
```

#### 7.Phương thức Map()

Phương thức map() một phương thức được sử dụng trên mảng để tạo ra một mảng mới, trong đó mỗi phần tử là kết quả của việc áp dụng một hàm callback cho từng phần tử trong mảng gốc.
Khác với forEach(), phương thức map() sẽ trả về một mảng mới và không thay đổi mảng ban đầu.

**Cú pháp:**

```bash
let newArray = array.map(function(currentValue, index, array) {
   // Trả về giá trị mới cho mảng mới
});
```

- **currentValue:** Giá trị của phần tử hiện tại trong mảng.
- **index (tùy chọn):** Chỉ số của phần tử trong mảng.
- **array (tùy chọn):** Mảng gốc mà bạn đang lặp qua.

**Ví dụ:**

```bash
let arr = [1, 2, 3, 4, 5];
let newArr = arr.map(function(value) {
    return value * 2;
});
console.log(newArr); // Output: [2, 4, 6, 8, 10]
```
