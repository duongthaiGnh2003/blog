# 1. Khái niệm Object trong JavaScript?

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

## 4. Những Lưu ý khi khởi tạo Object

- Sử dụng đúng cách để tạo object
- Đặt tên thuộc tính và phương thức rõ ràng
- Tránh lặp lại thuộc tính
- Sử dụng thuộc tính động khi cần thiết
