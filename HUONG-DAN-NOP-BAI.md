# Hướng dẫn hoàn thành bài kiểm tra Green Tech Hub

## ✅ Đã hoàn thành (Bước 1 & 2)

- [x] Website: Hero "Technology for a Greener Future", 3 Solutions, Form liên hệ + validation
- [x] Git: .gitignore, init, nhánh main, feature/landing-page, feature/contact-form

---

## Bước 3: Thiết lập Jira (Bạn thực hiện)

### 3.1 Tạo Project

1. Đăng nhập [Jira](https://www.atlassian.com/software/jira) (Cloud hoặc self-hosted)
2. **Create Project** → Chọn **Scrum Software**
3. Cấu hình:
   - **Project Name:** Green Tech Hub (GTH)
   - **Key:** GTH
4. Workflow: To Do → In Progress → Code Review → Testing → Done

### 3.2 Tạo 4 Epic

| Epic Name | Mô tả |
|-----------|-------|
| Foundation & Infrastructure | Thiết lập môi trường phát triển và cấu trúc Git |
| Web Interface (Frontend) | Xây dựng giao diện Landing Page quảng bá dự án |
| Source Control Management | Quản lý phiên bản và đồng bộ mã nguồn lên Cloud |
| Quality Assurance | Kiểm thử giao diện và quản lý lỗi phát sinh |

### 3.3 Tạo 3 User Stories

**EPIC: Web Interface (Frontend)**
- **Story 1 (GTH-1):** Là một khách truy cập, tôi muốn xem các giải pháp công nghệ xanh để hiểu về giá trị của dự án.
- **Story 2 (GTH-2):** Là một đối tác tiềm năng, tôi muốn để lại thông tin liên hệ để nhận tư vấn.

**EPIC: Source Control Management**
- **Story 3 (GTH-3):** Là một developer, tôi muốn quản lý mã nguồn theo nhánh để tránh xung đột khi làm việc nhóm.

### 3.4 Phân rã Story 2 thành Task & Sub-task

- **Task 1:** Thiết kế Form liên hệ (Họ tên, Email, Lời nhắn)
- **Task 2:** Viết mã Validation cho Form (Kiểm tra định dạng Email)
- **Sub-task:** Tích hợp CSS cho trạng thái Success/Error của Form

### 3.5 Tạo Risk Issues

| Risk | Mức độ | Biện pháp |
|------|--------|-----------|
| Xung đột mã nguồn khi Merge | Cao | Yêu cầu Pull Request và Review code |
| Giao diện vỡ trên Mobile | Trung bình | Sử dụng CSS Media Queries |

### 3.6 Tạo Bug Issue

- **Mô tả:** Form liên hệ không nhận được ký tự tiếng Việt
- **Priority:** High
- **Linked:** Relates to GTH-02

### 3.7 Chuyển tất cả Task sang Done

Sau khi code xong, chuyển trạng thái các Task sang **Done** trên Scrum Board.

---

## Bước 4: Đẩy lên GitHub/GitLab (Bạn thực hiện)

### 4.1 Tạo Repository

1. Vào [GitHub](https://github.com) hoặc [GitLab](https://gitlab.com)
2. **New Repository** → Tên: **GTH-Project-2026**
3. Không khởi tạo README (đã có sẵn)

### 4.2 Kết nối và Push

```bash
cd d:\green-tech-hub
git remote add origin https://github.com/<username>/GTH-Project-2026.git
git push -u origin main
```

### 4.3 Pull Request (theo đề)

1. Tạo nhánh từ feature: `git checkout feature/landing-page`
2. Push nhánh: `git push -u origin feature/landing-page`
3. Trên GitHub: **Compare & pull request** → Merge vào `main`
4. Lặp lại với `feature/contact-form` nếu cần

---

## Bước 5: Chuẩn bị nộp bài

### Sản phẩm bàn giao

1. **Link Repository** (GitHub/GitLab) có đầy đủ lịch sử commit
2. **Ảnh chụp màn hình** bảng Jira với tất cả Task ở trạng thái "Done"
3. **File Word** `mssv_hoten.docx` gồm:
   - Ảnh chụp kết quả (Jira, website, v.v.)
   - Link GitHub dự án
   - Link demo (nếu có, ví dụ: GitHub Pages)
4. **File .zip** mã nguồn Website

### Nén mã nguồn

```powershell
# Trong thư mục chứa green-tech-hub
Compress-Archive -Path "d:\green-tech-hub\*" -DestinationPath "GTH-source.zip"
```

(Lưu ý: Có thể loại .git nếu file quá lớn)

### Link nộp bài

https://drive.google.com/drive/folders/1MYVHPajW9Yc9oxtMjINUbIjdLMhuXSP-?usp=sharing

---

## Gợi ý: Deploy demo (GitHub Pages)

1. Vào repo → **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: **main** → folder **/ (root)**
4. Save → Đợi vài phút, link dạng: `https://<username>.github.io/GTH-Project-2026/`
