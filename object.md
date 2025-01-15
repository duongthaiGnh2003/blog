# Tìm hiểu Object trong JavaScript

Object là một phần quan trọng trong JavaScript, được sử dụng để lưu trữ và quản lý dữ liệu. Việc nắm vững cách hoạt động của Object sẽ giúp bạn viết code hiệu quả hơn. Vậy chúng ta hãy cùng tìm hiểu trong bsif viết này nhé!

## 1. Khái niệm

- Object trong JavaScript là một cấu trúc dữ liệu dùng để lưu trữ các giá trị dưới dạng cặp key-value
  Trong đó:
  **Key:** Là tên thuộc tính, thường là chuỗi hoặc ký hiệu.
  **Value:** Là dữ liệu được lưu trữ, có thể thuộc bất kỳ kiểu dữ liệu nào như số, chuỗi, mảng...
- Một object có thể bao gồm một hoặc nhiều thuộc tính (properties) và phương thức (methods).

## 2. Đặc điểm cơ bản của Object:

- Cấu trúc dạng key-value: Mỗi thuộc tính (property) của Object là một cặp key (tên thuộc tính) và value (giá trị).
- Động: Bạn có thể thêm, sửa đổi hoặc xóa các thuộc tính bất kỳ lúc nào.
- Linh hoạt: Các giá trị trong Object có thể là bất kỳ kiểu dữ liệu nào, bao gồm cả số, chuỗi, hàm, mảng hoặc thậm chí là một Object khác.

## 3. Khởi tạo

- Sử dụng dấu ngoặc nhọn `{}`: đây là cách khai báo phổ biến.

```bash
const person = {
  name: "John", // Thuộc tính name có giá trị "John"
  age: 30  // Thuộc tính age có giá trị 30
};
```

- Sử dụng `Object()` constructor

```bash
let car = new Object();
car.brand = "Toyota";
car.model = "Corolla";
```

- Sử dụng `Object.create()`

```bash
const animal = Object.create(null);
animal.type = "Dog";
animal.sound = "Bark";
```

- Sử dụng class (ES6)

```bash
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}
const person = new Person("Alice", 25);
```

## 4. Truy cập thuộc tính

- Dùng dấu chấm `.`
- Dùng dấu ngoặc vuông `[]`

```bash
const person = {
  name: "Alice",
  age: 25,
};
// Sử dụng dấu chấm
console.log(person.name); // "Alice"
console.log(person.age);  // 25

// Sử dụng dấu ngoặc vuông (có thể sử dụng khi tên thuộc tính chứa ký tự đặc biệt hoặc biến)
console.log(person["name"]); // "Alice"
console.log(person["age"]);  // 25
```

## 5. object Constructor

Được hiểu là việc sử dụng một hàm constructor để tạo ra các đối tượng với cấu trúc và hành vi giống nhau. Cách sử dụng này cho phép bạn tái sử dụng mã và tạo ra các đối tượng với các thuộc tính và phương thức chung

```bash
function Person(name, age) {
    this.name = name;
    this.age = age;
}

let person1 = new Person("Alice", 25);
let person2 = new Person("Bob", 30);

console.log(person1); // Person { name: 'Alice', age: 25 }
console.log(person2); // Person { name: 'Bob', age: 30 }

```

**Ưu điểm**

- Tái sử dụng mã
- Tạo đối tượng với cấu trúc xác định
- Quản lý đối tượng dễ dàng hơn
- Hỗ trợ kế thừa

**Nhược điểm**

- Cú pháp phức tạp hơn so với cách tạo đối tượng bằng dấu ngoặc nhọn `{}`
- Không linh hoạt cho các đối tượng đơn giản
- Khó khăn trong việc kế thừa (đối với các hàm constructor truyền thống)

## 6. Các thao tác với Object

- **Thêm hoặc sửa thuộc tính:** Chỉ cần gán giá trị cho một key mới hoặc key đã tồn tại:

```bash
person.city = "New York"; // Thêm mới
person.age = 35;          // Sửa giá trị
```

- **Xoá thuộc tính:** Dùng từ khoá `delete`.

```bash
delete person.age;
console.log(person); // Thuộc tính "age" đã bị xoá
```

- **Kiểm tra sự tồn tại của thuộc tính:** Sử dụng toán tử `in` hoặc phương thức `hasOwnProperty()`.

```bash
const person = {
  name: "Alice",
};

// Toán tử in
console.log("name" in person);  // true
console.log("address" in person);  // false

// hasOwnProperty()
console.log(person.hasOwnProperty("name")); // true
console.log(person.hasOwnProperty("address")); // false
```

- **Duyệt qua Object:** dùng `for...in` để duyệt qua các thuộc tính liệt kê được (enumerable properties) của một Object.

```bash
const obj = { a: 1, b: 2, c: 3 };

for (let key in obj) {
    if (obj.hasOwnProperty(key)) { // Đảm bảo chỉ lấy các thuộc tính của chính obj, không lấy từ prototype
        console.log(`${key}: ${obj[key]}`);
    }
}
```

- **Sao chép Object:**
  \- sử dụng vòng lặp:

```bash
let copy = {};
for (let key in person) {
  copy[key] = person[key];
}
```

\- Sử dụng `Object.assign()`:

```bash
let copy = Object.assign({}, person);
```

\- Sử dụng Spread Operator (...):

```bash
let copy = { ...person };
```

### 7. Tổng kết

Trong bài viết này, mình đã giới thiệu với các bạn về Object và các hàm cách việc thông dụng với Object trong JavaScript,  
Hy vọng bài viết này sẽ có thể giúp đỡ các bạn trong quá trình học và tìm hiểu về JavaScript.
