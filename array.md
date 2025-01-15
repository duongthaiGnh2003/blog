## Tìm hiểu về mảng (Array) trong Javascript

Mảng (Array) trong Javascript là một loại dữ liệu đặc biệt dùng để lưu trữ nhiều giá trị trong một biến duy nhất được sử dụng phổ biến trong các ngôn ngữ lập trình. Vậy chúng ta hãy cùng tìm hiểu về cách mảng hoạt động và giúp bạn phát triển các ứng dụng JavaScript như thế nào nhé.

### I. Khái niệm

- Mảng (Array) là một cấu trúc dữ liệu cho phép lưu trữ nhiều giá trị trong một biến, giúp quản lý và thao tác danh sách dữ liệu dễ dàng hơn.

### II. Khởi tạo

Có 2 cách chính để khởi tạo mảng:

- Dùng dấu ngoặc vuông `[]`: Cách phổ biến và đơn giản nhất.

```bash
let arr = [1, 2, 3, 4, 5]; // Mảng chứa các số
let emptyArr = [];         // Mảng rỗng
let mixedArr = [1, "two", true]; // Mảng chứa các kiểu dữ liệu khác nhau
```

- Sử dụng Array() constructor:

```bash
let arr1 = new Array(5);          // Tạo mảng với độ dài 5, các phần tử ban đầu là undefined
let arr2 = new Array(1, 2, 3);    // Tạo mảng chứa các giá trị [1, 2, 3]
```

Lưu ý: Nếu truyền một số duy nhất, nó sẽ được hiểu là độ dài của mảng, không phải phần tử.

### III. Đặc điểm

- Mảng có thể chứa nhiều giá trị, mỗi giá trị được gọi là một phần tử.
- Các phần tử trong mảng được phân biệt thông qua chỉ số (index), bắt đầu từ 0.
- Hỗ trợ các kiểu dữ liệu khác nhau như: number, string, boolean, object hoặc array.
- Là một đối tượng đặc biệt: được coi là một đối tượng (object), nhưng có các tính năng và phương thức đặc biệt để xử lý danh sách dữ liệu.
- Kích thước động: có thể thêm hoặc xóa phần tử mà không cần khai báo lại.

### IV. Các hàm làm việc với mảng

#### 1. Truy cập mảng

Một phần tử trong một mảng JavaScript được truy cập bằng cách tham chiếu đến vị trí index của phần tử đó trong [] (index bắt đầu từ 0).

```bash
let fruits = ["Apple", "Banana", "Cherry"];
console.log(fruits[0]); // Kết quả: "Apple"
console.log(fruits[1]); // Kết quả: "Banana"
```

#### 2. Độ dài mảng

- Độ dài mảng được xác định thông qua thuộc tính `.length` thuộc tính này trả về số lượng phần tử trong mảng.

```bash
console.log(fruits.length); // Kết quả: 3
```

#### 3. Thêm và xóa phần tử

- push(element): Thêm phần tử vào cuối mảng.
- pop(): Xóa phần tử cuối cùng và trả về phần tử đó.
- unshift(element): Thêm phần tử vào đầu mảng.
- shift(): Xóa phần tử đầu tiên và trả về phần tử đó.

```bash
let arr = [1, 2, 3];
arr.push(4); // Thêm 4 vào cuối
console.log(arr); // [1, 2, 3, 4]

arr.pop(); // Xóa phần tử cuối
console.log(arr); // [1, 2, 3]

arr.unshift(0); // Thêm 0 vào đầu
console.log(arr); // [0, 1, 2, 3]

arr.shift(); // Xóa phần tử đầu
console.log(arr); // [1, 2, 3]
```

#### 4. Cắt, nối, và thay đổi

- slice(start, end): Lấy ra một phần của mảng (không làm thay đổi mảng gốc).
- splice(start, deleteCount, ...items): Xóa, thay thế hoặc chèn phần tử vào mảng.
- concat(...arrays): Nối mảng với các mảng khác.

```bash
let arr = [1, 2, 3, 4, 5];

let sliced = arr.slice(1, 4); // Cắt từ index 1 đến index 4 (không bao gồm index 4)
console.log(sliced); // [2, 3, 4]

arr.splice(1, 2, "a", "b"); // Từ index 1 Xóa 2 phần tử và chèn "a", "b" vào
console.log(arr); // [ 1, 'a', 'b', 4, 5 ]

let newArr = arr.concat([6, 7]);
console.log(newArr); // [ 1, 'a', 'b', 4, 5, 6, 7]
```

#### 5. Chuyển đổi mảng thành chuỗi

- join(separator): Kết hợp các phần tử thành chuỗi.
- toString(): Chuyển mảng thành chuỗi (dùng dấu phẩy mặc định).

```bash
let fruits = ["Apple", "Banana", "Cherry"];
console.log(fruits.join(" - ")); // "Apple - Banana - Cherry"
console.log(fruits.toString()); // "Apple,Banana,Cherry"
```

#### 6. Sắp xếp và đảo ngược

- sort(): Sắp xếp mảng (mặc định theo thứ tự chữ cái).
- reverse(): Đảo ngược mảng.

```bash
let numbers = [3, 1, 4, 2];
numbers.sort(); // Sắp xếp (mặc định theo chuỗi)
console.log(numbers); // [1, 2, 3, 4]

numbers.reverse(); // Đảo ngược
console.log(numbers); // [4, 3, 2, 1]
```

#### 7. Lặp qua mảng

- forEach(callback): Duyệt qua mảng, thực hiện một hành động trên mỗi phần tử.
- map(callback): Tạo một mảng mới từ kết quả của hàm callback.

```bash
let numbers = [1, 2, 3, 4, 5];

// forEach
numbers.forEach((item) => {
 // logic
   console.log(item * 2
)}); // 2, 4, 6, 8, 10

// map
let squares = numbers.map(num => num * num);
console.log(squares); // [1, 4, 9, 16, 25]
```

### 8. Kiểm tra điều kiện

- some(callback): Kiểm tra xem chỉ cần có ít nhất một phần tử thỏa mãn điều kiện.
- every(callback): Kiểm tra xem tất cả các phần tử có thỏa mãn điều kiện không.

```bash
let numbers = [1, 2, 3, 4];

let hasEven = numbers.some(num => num % 2 === 0); // Có số chẵn không?
console.log(hasEven); // true

let allPositive = numbers.every(num => num > 0); // Tất cả đều dương?
console.log(allPositive); // true
```

#### 9. Tìm kiếm

- indexOf(element): Tìm vị trí của phần tử
- lastIndexOf(element): Tìm vị trí cuối cùng của phần tử trong mảng

```bash
let numbers = [5, 12, 8, 130, 44];
console.log(numbers.indexOf(12)); // 1 (vị trí đầu tiên của 12)
console.log(numbers.indexOf(2)); // -1 (không tìm thấy)
console.log(numbers.lastIndexOf(130)); // 3 (vị trí cuối cùng của 130)
```

- find(callback): Tìm kiếm và trả về 1 giá trị thỏa mãn điều kiện.

```bash
let found = numbers.find(num => num > 10);
console.log(found); // 12 (phần tử đầu tiên lớn hơn 10)
```

- filter(callback): Tìm kiếm và trả về 1 giá trị thỏa mãn điều kiện.

```bash
let evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // [12, 8, 130, 44] (các số chẵn)
```

### V. Tổng kết

Trong bài viết này, mình đã giới thiệu với các bạn về mảng (Array) và các hàm làm việc thông dụng với mảng trong JavaScript, từ việc khởi tạo đến các phương thức phổ biến khi làm việc với mảng trong JavaScript.
Hy vọng bài viết này sẽ có thể giúp đỡ các bạn trong quá trình học và tìm hiểu về JavaScript.
