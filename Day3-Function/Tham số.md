## 📘 2. Tham số có kiểu dữ liệu và giá trị mặc định

TypeScript cho phép bạn cung cấp giá trị mặc định cho tham số của hàm. Nếu tham số không được truyền khi gọi hàm, TypeScript sẽ sử dụng giá trị mặc định.

### 🔹 Cú pháp cơ bản

```typescript
function tênHàm(thamSố: kiểu = giáTrịMặcĐịnh): kiểuTrảVề {
  // logic của hàm
}
```

#### Giải thích

- **thamSố: kiểu = giáTrịMặcĐịnh**: Tham số có kiểu dữ liệu và giá trị mặc định.
- Nếu bạn không truyền tham số nào khi gọi hàm, tham số sẽ nhận giá trị mặc định.

##### 🔹 Ví dụ 1: Tham số mặc định

```typescript
function chaoHoi(ten: string = "bạn"): string {
  return `Xin chào, ${ten}!`;
}

console.log(chaoHoi()); // Kết quả: Xin chào, bạn!
console.log(chaoHoi("Huy")); // Kết quả: Xin chào, Huy!
```

#### Giải thích

- Tham số `ten` có giá trị mặc định là "bạn".
- Khi không truyền tham số, giá trị mặc định "bạn" sẽ được sử dụng.

##### 🔹 Ví dụ 2: Nhiều tham số có giá trị mặc định

```typescript
function tinhTienLuong(luongCoBan: number, thuong: number = 500): number {
  return luongCoBan + thuong;
}

console.log(tinhTienLuong(2000)); // Kết quả: 2500 (500 là giá trị mặc định của 'thuong')
console.log(tinhTienLuong(2000, 1000)); // Kết quả: 3000
```

#### Giải thích

- Nếu không truyền `thuong`, giá trị mặc định 500 sẽ được sử dụng.
