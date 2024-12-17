## 📘 3. Rest Parameters và Optional Parameters

### 🔹 Rest Parameters (Tham số còn lại)

Rest Parameters (`...params`) cho phép một hàm nhận số lượng tham số không xác định dưới dạng mảng. Thay vì truyền một loạt các tham số, bạn có thể sử dụng Rest Parameters để nhận tất cả tham số dưới dạng một mảng.

#### Cú pháp cơ bản

```typescript
function tênHàm(...thamSo: kiểu[]): kiểuTrảVề {
  // logic của hàm
}
```

#### Giải thích

- **...thamSo: kiểu[]**: Dấu ba chấm (...) cho phép bạn truyền nhiều tham số và chúng sẽ được gộp thành mảng.

##### 🔹 Ví dụ 1: Rest Parameters

```typescript
function tinhTong(...so: number[]): number {
  return so.reduce((tong, giaTri) => tong + giaTri, 0);
}

console.log(tinhTong(1, 2, 3)); // Kết quả: 6
console.log(tinhTong(5, 10, 15, 20)); // Kết quả: 50
```

#### Giải thích

- Hàm `tinhTong` nhận nhiều số và tính tổng của chúng bằng phương thức `reduce()`.

### 🔹 Optional Parameters (Tham số tùy chọn)

Tham số tùy chọn (Optional Parameter) được ký hiệu bằng dấu `?`. Nếu bạn không truyền giá trị cho tham số, nó sẽ có giá trị là `undefined`.

#### Cú pháp cơ bản

```typescript
function tênHàm(thamSo?: kiểu): kiểuTrảVề {
  // logic của hàm
}
```

#### Giải thích

- Dấu chấm hỏi (?) cho biết rằng tham số đó là không bắt buộc.

##### 🔹 Ví dụ 1: Tham số tùy chọn

```typescript
function chaoHoi(ten?: string): string {
  if (ten) {
    return `Xin chào, ${ten}!`;
  } else {
    return `Xin chào, bạn!`;
  }
}

console.log(chaoHoi()); // Kết quả: Xin chào, bạn!
console.log(chaoHoi("Huy")); // Kết quả: Xin chào, Huy!
```

#### Giải thích

- Hàm `chaoHoi` nhận tham số `ten`.
- Nếu không truyền `ten`, hàm sẽ chào “bạn”.

##### 🔹 Ví dụ 2: Optional Parameters trong nhiều tham số

```typescript
function hienThiThongTin(ten: string, tuoi?: number): string {
  if (tuoi !== undefined) {
    return `Xin chào, tôi là ${ten} và tôi ${tuoi} tuổi.`;
  } else {
    return `Xin chào, tôi là ${ten}.`;
  }
}

console.log(hienThiThongTin("Huy")); // Kết quả: Xin chào, tôi là Huy.
console.log(hienThiThongTin("Huy", 25)); // Kết quả: Xin chào, tôi là Huy và tôi 25 tuổi.
```

#### Giải thích

- Tham số `tuoi` là tùy chọn.
- Nếu `tuoi` không được truyền, thông báo sẽ không bao gồm tuổi.

## 🚀 Tóm tắt

| Khái niệm               | Ý nghĩa                                           |
|------------------------|---------------------------------------------------|
| Hàm có kiểu trả về     | Đặt kiểu trả về với `: kiểuTrảVề`                |
| Giá trị mặc định       | Dùng `= giáTrịMặcĐịnh` cho tham số               |
| Rest Parameters         | Dùng `...thamSo: kiểu[]` để nhận tham số động    |
| Optional Parameters      | Dùng `thamSo?: kiểu` để cho phép tham số tùy chọn |
