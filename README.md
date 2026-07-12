# KMA HK2 Template Báo Cáo

Bộ template và skill tái sử dụng để làm báo cáo cuối kỳ / báo cáo khoa học theo phong cách Học viện Kỹ thuật Mật mã, đặc biệt cho các môn học thuộc nhóm An toàn thông tin.

## Mục tiêu

Repository này dùng để chuẩn hóa cách làm báo cáo:

- Bố cục báo cáo khoa học 3 chương.
- Format font chữ, heading, bảng, hình, mục lục.
- Checklist rà soát trước khi nộp.
- Prompt/skill để áp dụng nhanh cho các đề tài khác.
- Cách đưa liên hệ thực tế vào bài để đạt điểm cao.
- Logo và ví dụ theo môn học để tham khảo nhanh.

## Cấu trúc repo

```text
.
├── README.md
├── STYLE_GUIDE.md
├── assets/
│   └── logo/
│       ├── README.md
│       └── kma-logo.svg
├── examples/
│   ├── README.md
│   └── quan-ly-an-toan-thong-tin/
│       └── de-13-benh-an-dien-tu/
│           ├── README.md
│           ├── bao-cao-mau.md
│           └── ghi-chu-review.md
├── templates/
│   ├── bao_cao_3_chuong.md
│   ├── de_cuong_3_chuong.md
│   ├── review_checklist.md
│   └── prompt_pack.md
└── skills/
    └── kma-report-skill/
        └── SKILL.md
```

## Quy trình dùng nhanh

1. Đọc đề bài và yêu cầu của giảng viên.
2. Tạo đề cương 3 chương theo `templates/de_cuong_3_chuong.md`.
3. Mở rộng thành báo cáo theo `templates/bao_cao_3_chuong.md`.
4. Áp dụng format theo `STYLE_GUIDE.md`.
5. Thêm hình workflow, bảng phân tích, ma trận kiểm soát và phần liên hệ thực tế.
6. Chèn logo từ `assets/logo/kma-logo.svg` nếu cần trang bìa theo phong cách KMA.
7. Tham khảo ví dụ theo môn trong `examples/`.
8. Rà soát bằng `templates/review_checklist.md`.
9. Xuất PDF và kiểm tra lần cuối trước khi nộp.

## Ví dụ hiện có

- `examples/quan-ly-an-toan-thong-tin/de-13-benh-an-dien-tu/`: ví dụ đề tài về bệnh án điện tử, thất bại thực thi quy trình bảo mật, xác thực theo ngữ cảnh, break-glass access và truyền thông thay đổi hành vi.

## Nguyên tắc quan trọng

Một báo cáo tốt không chỉ trả lời đúng đề. Bài cần cho thấy:

- Hiểu bản chất quản lý an toàn thông tin.
- Biết phân tích nguyên nhân gốc, không chỉ mô tả hiện tượng.
- Có đề xuất giải pháp khả thi.
- Có liên hệ thực tế với tổ chức, quy trình, con người và công nghệ.
- Hình thức trình bày cẩn thận như một báo cáo khoa học được lưu trữ.
