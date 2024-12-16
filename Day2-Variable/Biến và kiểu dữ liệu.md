
**🎯 Mục tiêu trong ngày**

• Hiểu được cách khai báo biến trong TypeScript.
• Nắm rõ các kiểu dữ liệu cơ bản và nâng cao của TypeScript.
• Phân biệt any, unknown, never, void và khi nào sử dụng chúng.
• Thực hành khai báo và sử dụng biến với các kiểu dữ liệu khác nhau.

**📝 1. Khai báo biến trong TypeScript**

**🔹 3 từ khóa khai báo biến**

• let: Khai báo biến có thể thay đổi giá trị.
• const: Khai báo biến không thể thay đổi giá trị.
• var: Không khuyến khích sử dụng, phạm vi (scope) của nó là **function scope** thay vì **block scope**.

**Cú pháp:**

```ts
let myVariable: string = 'Hello TypeScript'; // biến có kiểu string
const pi: number = 3.14; // biến không thể thay đổi
```

**📝 2. Các kiểu dữ liệu cơ bản trong TypeScript**

| **Kiểu**     | **Ví dụ**                                       | **Mô tả**                                 |
|--------------|------------------------------------------------|-------------------------------------------|
| **string**   | `let name: string = "John";`                   | Chuỗi ký tự (text)                        |
| **number**   | `let age: number = 25;`                        | Số nguyên hoặc số thực                   |
| **boolean**  | `let isAdmin: boolean = true;`                 | Giá trị đúng/sai (true/false)            |
| **null**     | `let x: null = null;`                          | Biến rỗng, trống                          |
| **undefined**| `let y: undefined = undefined;`                | Biến chưa gán giá trị                     |
| **any**      | `let z: any = 123; z = 'abc';`                 | Kiểu dữ liệu tự do                        |
| **unknown**  | `let v: unknown;`                              | Giống any, nhưng an toàn hơn             |
| **void**     | `function log(): void {}`                      | Hàm không trả về giá trị                  |
| **never**    | `function throwError(): never {}`              | Hàm không bao giờ kết thúc (thường là error) |
| **object**   | `let obj: object = { name: 'John' };`         | Biến đối tượng                            |
| **array**    | `let nums: number[] = [1, 2, 3];`              | Mảng các số                               |
| **tuple**    | `let person: [string, number] = ['John', 25];`| Mảng cố định kiểu dữ liệu                 |
**📝 3. Cách khai báo kiểu dữ liệu cho biến**

**🔹 Cách cơ bản**

```ts
let name: string = 'John';
let age: number = 25;
let isAdmin: boolean = true;
```

**🔹 Kiểu dữ liệu “any” (hạn chế sử dụng)**

• Dùng khi không biết trước kiểu dữ liệu.
• Không được khuyến khích vì mất kiểm soát type.

```ts
let variable: any = 42;
variable = 'Now it is a string';
```

**🔹 Kiểu dữ liệu “unknown” (an toàn hơn “any”)**

• Giống any, nhưng bắt buộc phải kiểm tra kiểu dữ liệu trước khi sử dụng.

```ts
let input: unknown;

input = 123;
if (typeof input === 'number') {
  console.log(input + 10); // OK, vì đã kiểm tra input là number
}
```

**📝 4. Kiểu dữ liệu nâng cao**

**🔹 Union Type**

• Một biến có thể có nhiều kiểu dữ liệu.

```ts
let id: number | string;
id = 101; // OK
id = 'A101'; // OK
```

**🔹 Type Alias (Bí danh kiểu)**

• Tạo kiểu tùy chỉnh để sử dụng lại.

```ts
type UserID = number | string;
let id: UserID;
id = 123; // OK
id = 'abc'; // OK
```

**🔹 Tuple (Bộ giá trị)**

• Mảng với số phần tử cố định và kiểu dữ liệu xác định.

```ts
let person: [string, number, boolean];
person = ['John', 25, true]; // OK
```

**🔹 Enum (Kiểu liệt kê)**

• Tạo các tập giá trị có tên định nghĩa trước.

```ts
enum Role {
  ADMIN = 'admin',
  USER = 'user',
  GUEST = 'guest',
}

let userRole: Role = Role.ADMIN;
console.log(userRole); // admin
```

**📝 5. Các kiểu dữ liệu đặc biệt**

**🔹 Void**

• Dùng cho các hàm không trả về giá trị.

```ts
function greet(): void {
  console.log('Hello, World!');
}
```

**🔹 Never**

• Dùng cho các hàm **không bao giờ hoàn thành** (ví dụ: lỗi ném ra throw).

```ts
function throwError(message: string): never {
  throw new Error(message);
}
```

**📝 6. Thực hành**

**🚀 Bài tập 1: Khai báo biến với kiểu dữ liệu**

Khai báo các biến sau đây với kiểu dữ liệu TypeScript:

1. Biến name có kiểu **string** và giá trị là “John”.
2. Biến age có kiểu **number** và giá trị là 25.
3. Biến isActive có kiểu **boolean** và giá trị là **true**.
4. Biến skills có kiểu là mảng string và chứa các giá trị ["HTML", "CSS", "TypeScript"].

```ts
let name: string = 'John';
let age: number = 25;
let isActive: boolean = true;
let skills: string[] = ['HTML', 'CSS', 'TypeScript'];  
```

**🚀 Bài tập 2: Union Type**

Khai báo biến userID có kiểu dữ liệu là **number hoặc string**. Gán giá trị 123, sau đó gán giá trị 'abc'.

```ts
let userID: number | string;
userID = 123; // OK
userID = 'abc'; // OK
```

**🚀 Bài tập 3: Tuple**

Khai báo biến person có kiểu dữ liệu tuple với 3 giá trị:

1. **name** là string
2. **age** là number
3. **isEmployed** là boolean

```ts
let person: [string, number, boolean];
person = ['Alice', 30, true];
```

**🚀 Bài tập 4: Function with “void” và “never”**

1. Viết một function greet không trả về giá trị gì cả, chỉ in ra **“Hello, World!”**.
2. Viết một function throwError luôn ném ra lỗi.

```ts
function greet(): void {
  console.log('Hello, World!');
}

function throwError(message: string): never {
  throw new Error(message);
}
```
