# Cấu trúc điều kiện trong Javascript

Cấu trúc điều kiện là một phần quan trọng và phổ biến trong JavaScript, Nó được sử dụng để kiểm tra điều kiện và quyết định hành động tiếp theo dựa trên kết quả đúng hoặc sai của các điều kiện đó. Việc nắm vững cách sử dụng cấu trúc điều kiện sẽ giúp bạn kiểm soát luồng hoạt động của chương trình và làm cho công việc lập trình trở nên dễ dàng hơn.

Vậy, cấu trúc điều kiện hoạt động như thế nào trong JavaScript? Trong bài viết này, chúng ta sẽ cùng khám phá những khái niệm cơ bản và ứng dụng thực tiễn của cấu trúc điều kiện.

## 1. Câu lệnh if...else

Câu lệnh if...else là một trong những cấu trúc điều kiện cơ bản nhất trong JavaScript, được sử dụng để kiểm tra một điều kiện và thực hiện các hành động khác nhau dựa trên việc điều kiện đó đúng hay sai.

#### Câu lệnh `if`

Đối với câu lệnh if...else không nhất thiết phải có else, mà ta có thể sử dụng if độc lập để kiểm tra một điều kiện và thực hiện một đoạn mã nếu điều kiện đó đúng.

```bash
if (condition) {
    // Khối mã thực thi nếu điều kiện đúng true
}
```

**Cú Pháp:**

- **condition** là biểu thức điều kiện mà bạn muốn kiểm tra.
  Nếu biểu thức này trả về `true` đoạn mã trong dấu {} sẽ được thực thi.
  Nếu điều kiện là `false` thì đoạn mã bên trong câu lệnh if sẽ bị bỏ qua.

```bash
let age = 18;
if (age >= 18) {
    console.log("Bạn đủ tuổi để lái xe.");
}
```

Trong ví dụ trên, nếu giá trị của `age` là 18 hoặc lớn hơn, thì chương trình sẽ in ra `"Bạn đủ tuổi để lái xe."`.

#### Câu lệnh `if...else`

Câu lệnh đầy đủ `if...else` cho phép bạn kiểm tra một điều kiện và thực hiện logic theo hai trường hợp đúng hoặc sai.

**Cú Pháp:**

```bash
if (condition) {
    // Khối mã thực thi nếu điều kiện đúng (true)
} else {
    // Khối mã thực thi nếu điều kiện sai (false)
}
```

**Ví dụ:**

```bash
let age = 18;
if (age >= 18) {
    console.log("Bạn đủ tuổi để lái xe.");
} else {
    console.log("Bạn chưa đủ tuổi để lái xe.");
}
```

Trong ví dụ trên, nếu giá trị của `age` là 18 hoặc lớn hơn, thì chương trình sẽ in ra `"Bạn đủ tuổi để lái xe."`. Nếu giá trị của `age` nhỏ hơn 18, thì chương trình sẽ in ra `"Bạn chưa đủ tuổi để lái xe."`

#### 2. Câu lệnh `switch...case`

Câu lệnh switch...case trong lập trình được sử dụng để kiểm tra một giá trị và thực thi các đoạn mã tương ứng với giá trị đó. Câu lệnh này giúp thay thế một chuỗi các câu lệnh if...else khi cần kiểm tra nhiều giá trị khác nhau của một biến.

**Cú Pháp:**

```bash
switch (biến) {
    case giá_trị_1:
        // Mã thực thi khi biến == giá_trị_1
        break; // Để dừng lại sau khi thực thi
    case giá_trị_2:
        // Mã thực thi khi biến == giá_trị_2
        break;
    case giá_trị_n:
        // Mã thực thi khi biến == giá_trị_n
        break;
    default:
        // Mã thực thi khi không có giá trị nào đúng
}
```

**Ví dụ:**

```bash
let day = 2;
switch (day) {
    case 1:
        console.log("Thứ 2");
        break;
    case 2:
        console.log("Thứ 3");
        break;
    case 3:
        console.log("Thứ 4");
        break;
    case 4:
        console.log("Thứ 5");
        break;
    case 5:
        console.log("Thứ 6");
        break;
    case 6:
        console.log("Thứ 7");
        break;
    case 7:
        console.log("Chủ nhật");
        break;
    default:
        console.log("Invalid day");
}
// Kết quả: "Thứ 3"
```

**Cú Pháp:**

#### 3. Toán tử 3 ngôi (toán tử điều kiện)

Toán tử 3 ngôi cho phép thực hiện một phép kiểm tra đơn giản mà không cần dùng câu lệnh if...else.

```bash
condition ? block_1 : block_2;
```

- **condition:** Điều kiện bạn muốn kiểm tra.
- **block_1:** Biểu thức sẽ được thực thi nếu điều kiện đúng.
- **block_2:** Biểu thức sẽ được thực thi nếu điều kiện sai.

```bash
let age = 18;
let message = age >= 18 ? "Bạn đã đủ tuổi." : "Bạn chưa đủ tuổi.";
console.log(message); // Bạn đã đủ tuổi.
```

#### 4. Toán tử logic `&&`

Toán tử `&&` trong JavaScript có thể được sử dụng để kiểm tra một điều kiện và thực thi mã nếu điều kiện đó đúng. Là một kỹ thuật phổ biến để viết mã ngắn gọn.

```bash
condition && codeToExecute;
```

- **condition:** Điều kiện bạn muốn kiểm tra.
- **codeToExecute:** Mã sẽ được thực thi nếu điều kiện là true.

```bash
let age = 20;
age >= 18 && console.log("You are an adult.");
```

- Nếu age >= 18, sẽ in ra "You are an adult.",nếu sai thì sẽ ko có gì.

#### 5. Các Trường hợp sử dụng

- **`if...else`** nên dùng khi:

  \- Khi bạn có các điều kiện phức tạp hoặc cần thực hiện nhiều phép kiểm tra với các hành động khác nhau cho từng điều kiện.
  \- Khi bạn cần kiểm tra điều kiện với các phép toán phức tạp, kết hợp nhiều điều kiện logic, hoặc kiểm tra điều kiện với các kiểu dữ liệu khác nhau.
  \- Khi bạn cần thêm các khối mã khác nhau cho các điều kiện khác nhau.

- `switch...case` nên dùng khi:

  \- Khi bạn cần kiểm tra một biến với nhiều giá trị khác nhau (một giá trị cụ thể) và thực thi các hành động khác nhau tùy thuộc vào giá trị của biến đó.
  \- Khi bạn có một số lượng lớn các điều kiện dựa trên một giá trị duy nhất và muốn mã ngắn gọn và dễ hiểu hơn so với chuỗi if...else if...else.

- `Toán tử ba ngôi (? :)`nên dùng khi:

  \- Khi bạn chỉ có hai lựa chọn (đúng - sai) và muốn viết mã ngắn gọn.
  \- Khi bạn muốn thay thế một câu lệnh if...else đơn giản trong một dòng, đặc biệt khi gán giá trị hoặc thực hiện hành động đơn giản.

- `Toán tử logic (&&)` nên dùng khi:

  \- Khi bạn muốn kiểm tra một điều kiện và chỉ thực thi mã nếu điều kiện đúng.
  \- Khi bạn muốn tránh lỗi do truy cập thuộc tính không tồn tại (null hoặc undefined).

### 6. Tổng kết

Trong bài viết này, mình đã giới thiệu với các bạn về các câu lệnh điều kiện và cách việc thông dụng với nó trong JavaScript,  
Hy vọng bài viết này sẽ có thể giúp đỡ các bạn trong quá trình học và tìm hiểu về JavaScript.
