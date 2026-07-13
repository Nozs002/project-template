# 🚀 Docs-First AI Boilerplate

Welcome to the **Docs-First AI Boilerplate**! Đây là khung dự án (Template Repository) được thiết kế đặc biệt theo triết lý **"Tài liệu trước, Code sau" (Docs-First)**, tối ưu hóa cho quy trình làm việc kết hợp với Trí tuệ nhân tạo (AI Agents) và Kiến trúc theo miền (Domain-Driven Design).

## 🌟 Điểm Nổi Bật (Features)
- **Tech-Agnostic:** Hoàn toàn phi công nghệ. Dùng làm gốc cho dự án Web (React/Node), Mobile, AI, hay Desktop app đều được.
- **AI-Ready:** Tích hợp sẵn thư mục `.agents/` và `.ai/` chứa các luật (Rules) và quy trình chuẩn (Workflows) để AI hiểu ngữ cảnh và lập trình theo đúng khuôn khổ của bạn.
- **Bilingual Documentation:** Các file tài liệu đều có mẫu (Placeholder) song ngữ Anh-Việt.
- **Strict Quality Control:** Tự động ép chuẩn format văn bản và code với `Husky`, `Prettier`, và `Markdownlint` trước mỗi lần commit.

---

## 📂 Cấu Trúc Thư Mục Hệ Thống
```text
├── .agents/       # Các quy tắc (Skills) dành riêng cho AI Agents
├── .ai/           # Các luồng làm việc (Workflows) và prompts hướng dẫn AI
├── docs/          # Nơi chứa tài liệu tổng quan cấp độ toàn hệ thống (BRD, PRD, Architecture)
├── modules/       # Nơi chứa phân tích thiết kế chi tiết cho từng Tính năng/Nghiệp vụ riêng biệt
├── graph/         # Trực quan hóa cấu trúc dự án (Mạng lưới quan hệ tài liệu)
├── src/           # Nơi chứa Mã nguồn (Sẽ được tạo khi bạn bắt đầu code)
└── package.json   # Quản lý thư viện công cụ kiểm duyệt (Prettier, Husky, Lint)
```

---

## 🔄 Luồng Làm Việc Chuẩn (Standard Workflow)

Để hệ thống (và AI) phối hợp hiệu quả nhất, bạn **BẮT BUỘC** tuân thủ quy tắc: **Không viết code khi chưa có tài liệu rõ ràng.** 

Dưới đây là luồng hoạt động từng bước cho mọi dự án:

### Bước 1: Khởi tạo dự án
1. **Clone Repo:** Khởi tạo dự án mới từ template này.
2. **Cài đặt công cụ:** Chạy lệnh `npm install` để kích hoạt hệ thống kiểm duyệt lỗi tự động.
3. **Tạo nhánh (Branch):** Từ nhánh `main` (chứa tài liệu), rẽ nhánh ra công nghệ bạn muốn dùng (ví dụ: `git checkout -b base-react` hoặc `base-nestjs`).

### Bước 2: Đặc tả Yêu cầu Tổng quan (Cấp độ Project)
Trước khi làm chi tiết, hãy vào thư mục `docs/` để định nghĩa bài toán:
- Cập nhật mục tiêu kinh doanh tại: `docs/requirements/brd.md`
- Cập nhật yêu cầu sản phẩm tổng quan tại: `docs/requirements/prd.md`
- Đảm bảo các quy ước về đặt tên (metadata, ID quy tắc) tuân thủ đúng định nghĩa trong file `docs/project/metadata-schema.md`.

### Bước 3: Phân tích & Thiết kế Module (Cấp độ Tính năng)
Khi chuẩn bị lập trình một tính năng cụ thể (ví dụ: Thanh toán, Đăng nhập), bạn sẽ làm việc tại thư mục `modules/`:
1. Copy thư mục `modules/sample-module` và đổi tên thành tên tính năng của bạn (VD: `modules/payment`).
2. Điền đầy đủ thông tin vào các file trong đó:
   - `overview.md`: Mục đích và phạm vi của module này là gì?
   - `requirements.md`: Các yêu cầu chức năng (Functions) cụ thể phải có.
   - `flow.md`: Vẽ biểu đồ luồng hoạt động (bằng Mermaid JS).
   - `api.md`: Thiết kế luồng dữ liệu (API Request/Response).
3. **Lưu ý:** Mọi file tài liệu bạn viết phải tuân thủ chuẩn Markdown. Nếu sai định dạng (ví dụ: khoảng trắng sai thẻ Heading), hệ thống `Markdownlint` sẽ báo lỗi ngay khi bạn định lưu file. Ngoài ra, cách thức viết tài liệu cần tuân theo các luật nội bộ nằm ở thư mục `.agents/`.

### Bước 4: Triển khai Lập trình (Coding Phase)
Chỉ sau khi bước 3 hoàn tất (Tài liệu module đã chốt và commit xong):
- Bạn (hoặc AI Agent) mới được phép bắt tay vào viết Mã nguồn (Source Code).
- Code có thể đặt tập trung vào thư mục `src/`, hoặc đặt trực tiếp vào trong folder của module đó (VD: `modules/payment/controller.ts` nếu bạn làm theo chuẩn Modular Architecture).

### Bước 5: Commit & Push
Gõ lệnh `git commit`. Hệ thống Husky + Lint-staged sẽ chặn lại một nhịp để tự động format code bằng Prettier, kiểm tra lỗi chính tả markdown, rồi mới đẩy lên Repository thành công.
