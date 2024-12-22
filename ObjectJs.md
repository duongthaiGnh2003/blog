# Tìm hiểu Object trong JavaScript

## 1. Khái niệm Object trong JavaScript?

Object là một kiểu dữ liệu cho phép bạn lưu trữ và quản lý dữ liệu dưới dạng các cặp key-value. Nó được sử dụng để biểu diễn các thực thể trong thế giới thực hoặc các cấu trúc dữ liệu phức tạp.

## 2. Đặc điểm cơ bản của Object:

- Cấu trúc dạng key-value: Mỗi thuộc tính (property) của Object là một cặp key (tên thuộc tính) và value (giá trị).
- Động: Bạn có thể thêm, sửa đổi hoặc xóa các thuộc tính bất kỳ lúc nào.
- Linh hoạt: Các giá trị trong Object có thể là bất kỳ kiểu dữ liệu nào, bao gồm cả số, chuỗi, hàm, mảng hoặc thậm chí là một Object khác.

## 3. Khởi tạo Object

**có 3 cách khởi tạo một object:**

- Dùng dấu ngoặc nhọn `{}` : đây là cách phổ biến

```bash
 const person = {
    name: "Alice",
    age: 25,
    greet: function() {
        console.log("Hello, " + this.name);
    }
  };
  console.log(person.name); // Alice
  person.greet(); // Hello, Alice
```

- Sử dụng từ khóa `new Object()`: Đây là cách tạo Object thông qua constructor Object.

```bash
const person = new Object();
person.name = "Alice";
person.age = 25;
console.log(person); // {name:"Alice",age = 25}
```

- Sử dụng phương thức `Object.create()`

```bash
const proto = { greet: () => console.log("Hello!") };
const person = Object.create(proto);
person.name = "Bob";
console.log(person.name); // Bob
person.greet(); // Hello!

```

## 4. object Constructor

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

## 5. Các thao tác với Object

- **Truy xuất giá trị thuộc tính:** Sử dụng dấu chấm `.` hoặc dấu ngoặc vuông `[]` để truy xuất giá trị thuộc tính.

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

- **Thêm, sửa, xóa thuộc tính:** Chúng ta cũng có thể cập nhật thuộc tính trong Object.

```bash
const person = {
  name: "Alice",
  age: 25,
};

// Thêm thuộc tính mới
person.address = "123 Main St";
console.log(person); // { name: "Alice", age: 25, address = "123 Main St" };

// Sửa giá trị thuộc tính
person.age = 26;
console.log(person.age); // 26

// Xóa thuộc tính
delete person.age;
console.log(person.age); // undefined
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
