
### 📘 1. Cách khai báo hàm có kiểu trả về trong TypeScript

TypeScript cho phép bạn khai báo kiểu trả về của một hàm, giúp bạn biết được hàm sẽ trả về kiểu dữ liệu gì. Nếu không chỉ định kiểu trả về, TypeScript sẽ tự động suy diễn (inference) kiểu dữ liệu.

#### 🔹 Cú pháp cơ bản

```typescript
function tênHàm(thamSố: kiểuThamSố): kiểuTrảVề {
  // logic của hàm
  return giáTrị;
}
```

#### Giải thích

- **tênHàm**: Tên của hàm.
- **thamSố: kiểuThamSố**: Tham số của hàm và kiểu của tham số.
- **kiểuTrảVề**: Loại dữ liệu mà hàm sẽ trả về.

#### 🔹 Ví dụ 1: Hàm trả về kiểu `number`

```typescript
function congHaiSo(a: number, b: number): number {
  return a + b;
}
console.log(congHaiSo(5, 7)); // Kết quả: 12
```

#### Giải thích

- Hàm `congHaiSo` nhận 2 tham số kiểu `number`.
- Trả về giá trị kiểu `number`.

#### 🔹 Ví dụ 2: Hàm trả về kiểu `string`

```typescript
function chaoHoi(ten: string): string {
  return `Xin chào, ${ten}!`;
}
console.log(chaoHoi("Huy")); // Kết quả: Xin chào, Huy!
```

#### Giải thích

- Hàm `chaoHoi` nhận một tham số kiểu `string`.
- Trả về kiểu `string` được tạo từ chuỗi nội suy.

#### 🔹 Ví dụ 3: Hàm không trả về gì (`void`)

```typescript
function hienThiThongBao(message: string): void {
  console.log(message);
}
hienThiThongBao("Chào mừng bạn đến với TypeScript!");
```

#### Giải thích

- `void` được sử dụng khi hàm không trả về gì (không có `return`).

#### 🔹 Ví dụ 4: Trả về một `object`

```typescript
function taoNguoiDung(ten: string, tuoi: number): { ten: string; tuoi: number } {
  return { ten, tuoi };
}
const nguoiDung = taoNguoiDung("Huy", 25);
console.log(nguoiDung); // Kết quả: { ten: 'Huy', tuoi: 25 }
```

#### Giải thích

- Kiểu trả về của hàm là một `object` có 2 thuộc tính: `ten` và `tuoi`.
