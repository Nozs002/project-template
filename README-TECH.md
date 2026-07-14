# Base Branch: `base-nodejs-nextjs-mongodb`

Nhánh này chứa Boilerplate (khuôn mẫu) đã được thiết lập sẵn các công nghệ:

## 💻 Tech Stack

- **Backend & Logic**: Node.js (thông qua Next.js Server Actions & API Routes).
- **Frontend**: Next.js (App Router).
- **Database**: MongoDB Atlas.
- **ORM**: Prisma.
- **Authentication**: NextAuth.js.
- **Styling**: Vanilla CSS & CSS Modules (Không dùng Tailwind).
- **3D Effects**: React Three Fiber & Drei.

## 🏗 Kiến trúc (Architecture)

- **Mono-repo**: Toàn bộ Front & Back nằm chung trong `/src/app`.
- **CSS Strategy**: Sử dụng CSS Variables trong `globals.css` làm Design System
  cốt lõi. Các component sử dụng `*.module.css` để cô lập scope.

## 🚀 Cách chạy dự án

1. `pnpm install`
2. Cấu hình biến môi trường `.env` cho MongoDB.
3. `pnpm dev`
