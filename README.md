# 🚀 Docs-First AI Boilerplate

Welcome to the **Docs-First AI Boilerplate**! Đây là khung dự án (Template Repository) được thiết kế đặc biệt theo triết lý "Tài liệu trước, Code sau", tối ưu hóa cho quy trình làm việc với Trí tuệ nhân tạo (AI Agents) và Domain-Driven Design (DDD).

## 🌟 Điểm Nổi Bật (Features)
- **Tech-Agnostic:** Hoàn toàn phi công nghệ. Dùng làm gốc cho dự án Web (React/Node), Mobile, AI, hay Game đều được.
- **AI-Ready:** Thư mục `.agents/` và `.ai/` chứa sẵn các luật (Rules) và quy trình chuẩn (Workflows) để AI hiểu và code theo đúng ý bạn.
- **Bilingual Documentation:** Các tài liệu phân tích nghiệp vụ (`brd.md`, `prd.md`) và thiết kế hệ thống được bố trí sẵn cấu trúc điền (Placeholder) song ngữ Anh-Việt.
- **Strict Quality Control:** Tích hợp sẵn `Husky`, `Prettier`, và `Markdownlint` để đảm bảo format văn bản và code luôn hoàn hảo trước khi lưu (commit).

## 📂 Cấu Trúc Thư Mục (Folder Structure)
```text
├── .agents/       # Các quy tắc (Skills) dành riêng cho AI Agents
├── .ai/           # Các luồng làm việc (Workflows) và prompts cho AI
├── docs/          # Tài liệu tổng quan (BRD, PRD, Architecture)
├── modules/       # Các phân hệ nghiệp vụ theo Domain-Driven Design
├── graph/         # Trực quan hóa cấu trúc dự án
└── package.json   # Quản lý thư viện công cụ (Prettier, Husky, Lint)
```

## 🛠 Hướng Dẫn Sử Dụng (How to Use)
1. **Clone Repo này:** Tạo một bản sao dự án mới từ template này.
2. **Cài đặt công cụ:** Chạy lệnh `npm install` để kích hoạt hệ thống kiểm duyệt lỗi (Husky, Prettier).
3. **Phân nhánh công nghệ:**
   - Nếu bạn code React, hãy tạo nhánh `base-react`.
   - Nếu code Node.js, tạo nhánh `base-node`.
4. **Điền tài liệu:** Mở thư mục `docs/` và `modules/` để hoàn thiện tài liệu nghiệp vụ cùng AI.
5. **Bắt đầu code:** Viết mã nguồn vào thư mục `src/` (hoặc trực tiếp trong `modules/`).
