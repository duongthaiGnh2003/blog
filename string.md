# Chuỗi (String) strong Jacascript

## I. Khái quát

### 1. Khái niệm

chuỗi (string) là một kiểu dữ liệu được sử dụng để lưu trữ một chuỗi ký tự có thể bao gồm chữ cái, số, ký hiệu, từ hoặc câu .
Chuỗi là một tập hợp các ký tự được bao bọc bởi dấu nháy đơn (') hoặc dấu nháy kép ("), và từ ES6, bạn cũng có thể sử dụng template literals với dấu backtick (`).

### 2. Tạo chuỗi

Có 3 cách để tạo chính để tạo chuỗi:

- Sử dụng Dấu Nháy Đơn hoặc Dấu Nháy Kép:

```bash
let singleQuote = 'Hello, world!';
let doubleQuote = "Hello, world!";
```

- Sử dụng Constructor `String`:

```bash
let str = String("Hello, world!"); // Chuyển đổi sang chuỗi
let anotherStr = new String("Hello, world"); // Tạo đối tượng chuỗi
```

Lưu ý: Trong trường hợp sử dụng dấu nháy đơn `'` và dấu nháy kép `""` trong chuỗi bạn cần sử dụng thêm ký tự backslash (\) để có thể hiển thị chúng.

```bash
let escapeSingle = 'It\'s a sunny day.'; // It's a sunny day.
let escapeDouble = "He said, \"Hello!\""; // He said, "Hello!"
```

- Dấu nháy ngược ` `` ` (Template literals):

```bash
let str1 = "World";
let str2 = `Hello ${str1}`; // Template literals, hỗ trợ nội suy
console.log(str2); // Output: Hello World
```

## II. Làm việc với chuỗi

#### 1. Kiểm tra độ dài chuỗi (length)

cú pháp: `string.length`

```bash
let text = "JavaScript";
console.log(text.length); // Output: 10
```

#### 2. Tìm kiếm chuỗi

**Tìm vị trí xuất hiện đầu tiên:**
cú pháp: `string.indexOf(searchValue, start)`

- searchValue: Chuỗi con cần tìm.
- start (tùy chọn): Vị trí bắt đầu tìm kiếm trong chuỗi cha (mặc định là 0).

```bash
let text = "Hello, world!";
console.log(text.indexOf("world")); // Output: 7
console.log(text.indexOf("JavaScript")); // Output: -1
```

**Tìm vị trí xuất hiện cuối cùng:**
cú pháp: `string.lastIndexOf(searchValue, start)`

- searchValue: Chuỗi con cần tìm.
- start (tùy chọn): Vị trí bắt đầu tìm kiếm trong chuỗi cha (mặc định là 0).

```bash
let text = "Hello, world!, Hello, world!";
console.log(text.lastIndexOf("world")); // Output: 22
console.log(text.lastIndexOf("Python")); // Output: -1
console.log(text.lastIndexOf("world", 10)); // Output: 7

```

**Lưu ý:**

- Nếu chuỗi con không được tìm thấy, indexOf() sẽ trả về giá trị -1.
- indexOf() chỉ tìm được vị trí đầu tiên mà chuỗi con xuất hiện. Javascript sẽ bỏ qua những vị trí xuất hiện sau đó.
- lastIndexOf() chỉ tìm được vị trí cuối mà chuỗi con xuất hiện. Javascript sẽ bỏ qua những vị trí xuất hiện trước đó.

#### 4. Cắt chuỗi (slice)

Cú pháp: `string.slice(startIndex, endIndex)`

- startIndex: Vị trí bắt đầu (tính từ 0).
- endIndex (tùy chọn): Vị trí kết thúc, không bao gồm ký tự tại endIndex. Nếu bỏ qua, chuỗi sẽ được cắt từ startIndex đến hết.

```bash

let text = "JavaScript is awesome";
console.log(text.slice(0, 10));  // Output: "JavaScript"
console.log(text.slice(11));     // Output: "is awesome"
console.log(text.slice(-7));     // Output: "awesome"
console.log(text.slice(-7, -1)); // Output: "awesom"
```

#### 5. Thay Thế (replace)

Cú pháp: `string.replace(searchValue, newValue)`

- searchValue: Chuỗi con cần tìm.
- newValue: Chuỗi thay thế.

**Lưu ý:** Phương thức replace() có phân biệt chữ hoa và chữ thường

```bash
let text = "Hello, world!";
let newText1 = text.replace("World", "JavaScript");
let newText2 = text.replace("world", "JavaScript");
console.log(newText1); // Output: "Hello, world!" (không thay thế vì "world" khác "World")
console.log(newText2); // Output: "Hello, JavaScript!"
```

#### 6. Chuyển đổi chữ hoa và chữ thường

- `string.toUpperCase()`: Chuyển thành chữ in hoa
- `string.toLowerCase()`: Chuyển thành chữ thường

```bash
let text = "JavaScript";
console.log(text.toUpperCase()); // Output: JAVASCRIPT
console.log(text.toLowerCase()); // Output: javascript
```

#### 7. Kiểm tra chuỗi con

- `string.includes(searchString, position)`: kiểm tra có giá trị trong chuỗi không.
- `string.startsWith(searchString, position)`: kiểm tra giá trị bắt đầu.
- s`tring.endsWith(searchString, length)`: kiểm tra giá trị kết thúc.

```bash
let text = "JavaScript is fun";
console.log(text.includes("fun")); // Output: true
console.log(text.startsWith("Java")); // Output: true
console.log(text.endsWith("fun")); // Output: true
```

#### 8. Tách chuỗi

Dựa vào điểm chung để cắt chuỗi và trả về dạng array.

Cú pháp: `string.split(separator)`

- separator: Ký tự hoặc điểm chung. Nếu không chỉ định, chuỗi sẽ không bị tách.

```bash
let text = "Apple, Banana, Orange";
let fruits = text.split(", ");
console.log(fruits); // Output: ["Apple", "Banana", "Orange"]
```

#### 9. Nối chuỗi

```bash
let text1 = "Hello";
let text2 = "World";
let result = text1 + " " + text2;
let result2 = `${text1} ${text2}`; // Template literals
console.log(result); // Output: Hello World
console.log(result2); // Output: Hello World
```

#### 10. Xóa khoảng trắng

Cú pháp: `string.trim()`

```bash
let text = "   JavaScript   ";
console.log(text.trim()); // Output: JavaScript
```

#### 10. Chuyển đổi kiểu

```bash
let str = "123";
let num = 123;
console.log(Number(str)); // Output: 123
console.log(parseInt(str)); // Output: 123
console.log(String(num)); // Output: "123"
console.log(num.toString()); // Output: "123"
```

## III. Lời kết

Trong bài viết này, mình đã giới thiệu cho các bạn những điều cơ bản về cách làm việc với chuỗi trong JavaScript, từ việc tạo và hiển thị các ký tự chuỗi và các phương thức phổ biến khi làm việc với chuỗi trong JavaScript.
Hy vọng bài viết trên có thể giúp đỡ các bạn trong việc hiểu thêm về JavaScript.
