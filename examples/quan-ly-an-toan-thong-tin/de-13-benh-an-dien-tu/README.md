# Ví dụ môn Quản lý An toàn thông tin — Đề 13

## Chủ đề

**Quản lý an toàn thông tin trong hệ thống bệnh án điện tử: Phân tích thất bại thực thi và giải pháp thay đổi hành vi người dùng**

## Tình huống đề bài

Bệnh viện triển khai quy trình bảo mật mới: bác sĩ khi xem hồ sơ bệnh án điện tử phải quẹt thẻ từ, nhập mã PIN tĩnh và hệ thống tự động đăng xuất sau 3 phút không thao tác. Do môi trường cấp cứu và bận rộn, bác sĩ dán thẻ từ lên đầu đọc và dán mã PIN lên màn hình. Dự án hoàn thành về kỹ thuật nhưng thất bại về thực thi.

## Yêu cầu chính

1. Phân tích lỗi do đâu.
2. Đề xuất điều chỉnh giải pháp.
3. Lập kế hoạch đào tạo lại và truyền thông để bác sĩ hiểu rủi ro, thay đổi hành vi mà không dùng biện pháp ép buộc tiêu cực.

## Cấu trúc báo cáo tham khảo

```text
CHƯƠNG 1. Cơ sở lý luận và bối cảnh quản lý ATTT trong hệ thống bệnh án điện tử
CHƯƠNG 2. Phân tích nguyên nhân thất bại của quy trình bảo mật tại Bệnh viện Y
CHƯƠNG 3. Đề xuất điều chỉnh giải pháp và kế hoạch đào tạo, truyền thông thay đổi hành vi
```

## Điểm ăn điểm

- Không đổ lỗi đơn giản cho bác sĩ.
- Phân tích nguyên nhân gốc: chính sách quá cứng, thiếu phân tích nghiệp vụ, thiếu ngoại lệ, thiếu quản lý thay đổi.
- Cân bằng CIA, đặc biệt giữa bí mật và sẵn sàng trong môi trường cấp cứu.
- Đề xuất xác thực theo ngữ cảnh, break-glass access, hậu kiểm, audit log.
- Có kế hoạch đào tạo/truyền thông theo tình huống lâm sàng.
- Có bảng kiểm, ma trận kiểm soát và lộ trình triển khai.

## File trong thư mục

- `bao-cao-mau.md`: bản tham khảo dạng Markdown để tái sử dụng cấu trúc và ý chính.
- `ghi-chu-review.md`: checklist review riêng cho đề 13.

## Lưu ý

Ví dụ này dùng để tham khảo cách triển khai báo cáo. Khi dùng cho bài mới, cần thay đổi tên đề tài, bối cảnh, tài liệu tham khảo và liên hệ thực tế.
