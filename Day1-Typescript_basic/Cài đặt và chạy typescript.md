Tôi sẽ tái cấu trúc tài liệu sử dụng markdown với các bảng và code block được định dạng đẹp hơn. Dưới đây là phiên bản cải tiến:

# 🛠️ Hướng Dẫn Cài Đặt TypeScript và Thiết Lập Môi Trường

## ✨ Yêu Cầu Trước Khi Bắt Đầu

| Công Cụ | Mục Đích |
|---------|----------|
| Node.js | Chạy JavaScript trên máy tính |
| npm | Quản lý các gói thư viện |
| Visual Studio Code | Trình soạn thảo mã với hỗ trợ TypeScript |

## 📥 Các Bước Cài Đặt Chi Tiết

### 1. Cài Đặt Node.js và npm

#### Bước 1: Tải và Cài Đặt
- Truy cập [nodejs.org](https://nodejs.org/)
- Tải phiên bản LTS phù hợp với hệ điều hành
- Cài đặt theo hướng dẫn

#### Bước 2: Kiểm Tra Cài Đặt

```bash
# Kiểm tra phiên bản Node.js
node -v

# Kiểm tra phiên bản npm
npm -v
```

### 2. Cài Đặt TypeScript Compiler

#### Cài Đặt Toàn Cầu

```bash
# Cài đặt TypeScript
npm install -g typescript

# Kiểm tra phiên bản
tsc -v
```

### 3. Thiết Lập Dự Án TypeScript

#### Tạo Thư Mục Dự Án

```bash
# Tạo và di chuyển vào thư mục dự án
mkdir my-typescript-project
cd my-typescript-project

# Khởi tạo tệp cấu hình TypeScript
tsc --init
```

#### Cấu Hình `tsconfig.json`

```json
{
  "compilerOptions": {
    "target": "ES6",
    "module": "commonjs",
    "outDir": "./dist",
    "strict": true
  },
  "include": ["src/**/*"]
}
```

#### Tạo Mã TypeScript Đầu Tiên

```typescript
// src/index.ts
const greeting: string = "Hello, TypeScript!";
console.log(greeting);
```

#### Biên Dịch và Chạy

```bash
# Biên dịch TypeScript sang JavaScript
tsc

# Chạy tệp JavaScript
node dist/index.js
```

## 🚀 Các Lệnh Quan Trọng

| Lệnh | Chức Năng |
|------|-----------|
| `node -v` | Kiểm tra phiên bản Node.js |
| `npm -v` | Kiểm tra phiên bản npm |
| `npm install -g typescript` | Cài đặt TypeScript toàn cầu |
| `tsc -v` | Kiểm tra phiên bản TypeScript |
| `tsc` | Biên dịch toàn bộ tệp .ts |

## 💡 Khắc Phục Lỗi Thường Gặp

| Lỗi | Nguyên Nhân | Giải Pháp |
|-----|-------------|-----------|
| `tsc: command not found` | TypeScript chưa cài toàn cầu | Chạy `npm install -g typescript` |
| `Cannot find name 'console'` | Chưa thêm "lib" trong tsconfig | Thêm `"lib": ["ES6", "DOM"]` |

## 🎉 Kết Luận

Bạn đã sẵn sàng bắt đầu với TypeScript! Nếu cần hỗ trợ thêm, hãy liên hệ. 😊
