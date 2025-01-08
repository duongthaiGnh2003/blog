## Tìm hiểu về mảng (Array) trong Javascript

Mảng (Array) trong Javascript là một loại dữ liệu đặc biệt dùng để lưu trữ nhiều giá trị trong một biến duy nhất được sử dụng phổ biến trong các ngôn ngữ lập trình. Vậy chúng ta hãy cùng tìm hiểu về cách mảng hoạt động và giúp bạn phát triển các ứng dụng JavaScript như thế nào nhé.

### I. Khái niệm

- Mảng là một cấu trúc dữ liệu được sử dụng để lưu trữ một danh sách các giá trị (phần tử). Là một đối tượng đặc biệt được xây dựng sẵn trong JavaScript và cung cấp cách để quản lý và thao tác các tập hợp dữ liệu một cách hiệu quả.

### II. Khởi tạo

Có 2 cách chính để khởi tạo mảng:

- Dùng dấu ngoặc vuông `[]`: Cách phổ biến và đơn giản nhất.

```bash
let arr = [1, 2, 3, 4, 5]; // Mảng chứa các số
let emptyArr = [];         // Mảng rỗng
let mixedArr = [1, "two", true]; // Mảng chứa các kiểu dữ liệu khác nhau
```

- Sử dụng Array() constructor:

```bashlet arr1 = new Array(5);          // Tạo mảng với độ dài 5, các phần tử ban đầu là undefined
let arr2 = new Array(1, 2, 3);    // Tạo mảng chứa các giá trị [1, 2, 3]
```

Lưu ý: Nếu truyền một số duy nhất, nó sẽ được hiểu là độ dài của mảng, không phải phần tử.

### III. Đặc điểm

- Mảng có thể chứa nhiều giá trị, mỗi giá trị được gọi là một phần tử.
- Các phần tử trong mảng được phân biệt thông qua chỉ số (index), bắt đầu từ 0.
- Hỗ trợ các kiểu dữ liệu khác nhau như: number, string, boolean, object hoặc array.
- Là một đối tượng đặc biệt: được coi là một đối tượng (object), nhưng có các tính năng và phương thức đặc biệt để xử lý danh sách dữ liệu.
- Kích thước động: có thể thêm hoặc xóa phần tử mà không cần khai báo lại.

### IV. Truy cập mảng
