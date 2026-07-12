# Báo cáo mẫu — Đề 13: Bệnh án điện tử

> Mục đích: lưu cấu trúc, hướng viết và các ý chính để áp dụng cho các bài báo cáo môn Quản lý An toàn thông tin.

## Tên đề tài gợi ý

**Quản lý an toàn thông tin trong hệ thống bệnh án điện tử: Phân tích thất bại thực thi và giải pháp thay đổi hành vi người dùng**

## Lời nói đầu — ý chính

- Chuyển đổi số y tế làm tăng vai trò của bệnh án điện tử.
- Dữ liệu bệnh án là dữ liệu nhạy cảm, cần bảo vệ nghiêm túc.
- Trong bệnh viện, bảo mật phải cân bằng với tốc độ khám chữa bệnh.
- Trường hợp bác sĩ dán thẻ/PIN cho thấy kiểm soát kỹ thuật đúng nhưng thiết kế vận hành sai.
- Báo cáo tiếp cận theo quản lý ATTT: chính sách, quy trình, con người, công nghệ.

## Chương 1. Cơ sở lý luận và bối cảnh

### 1.1. Lý do chọn đề tài

Bệnh án điện tử chứa thông tin định danh, chẩn đoán, xét nghiệm, đơn thuốc, bảo hiểm và ghi chú chuyên môn. Nếu truy cập trái phép hoặc sửa sai, hậu quả không chỉ là lộ dữ liệu mà còn ảnh hưởng quyết định điều trị.

### 1.2. Mục tiêu, đối tượng, phạm vi

- Phân tích nguyên nhân thất bại của quy trình bảo mật.
- Đánh giá rủi ro từ hành vi dán thẻ và dán PIN.
- Đề xuất mô hình xác thực theo bối cảnh.
- Lập kế hoạch đào tạo và truyền thông thay đổi hành vi.

### 1.3. Cơ sở lý thuyết

Nên trình bày:

- Quản lý an toàn thông tin.
- Mô hình CIA: Confidentiality, Integrity, Availability.
- Kiểm soát truy cập, xác thực, trách nhiệm giải trình.
- RBAC, ABAC, kiểm soát truy cập theo ngữ cảnh.
- Yếu tố con người và usable security.

### 1.4. Đặc thù bệnh viện

- Cấp cứu có áp lực thời gian cao.
- Bác sĩ di chuyển giữa nhiều máy trạm.
- Nhiều vai trò cùng tham gia điều trị.
- Người dùng lâm sàng ưu tiên an toàn người bệnh.
- Chính sách quá cứng dễ tạo hành vi đối phó.

## Chương 2. Phân tích nguyên nhân thất bại

### 2.1. Mô tả tình huống

Quy trình cũ:

```text
Bác sĩ cần xem hồ sơ → Quẹt thẻ từ → Nhập PIN tĩnh → Xem bệnh án → Không thao tác 3 phút → Tự động đăng xuất → Xác thực lại
```

### 2.2. Lỗi thiết kế chính sách

Các lỗi chính:

1. Không phân tích đủ nghiệp vụ lâm sàng.
2. Áp dụng một chính sách cho mọi tình huống.
3. Thiên lệch về tính bí mật, bỏ qua tính sẵn sàng.
4. Không có cơ chế ngoại lệ chính thức.
5. Thiếu tham vấn bác sĩ.
6. Thiếu quản lý thay đổi và truyền thông.

### 2.3. Hành vi đối phó

| Hành vi | Nguyên nhân gần | Rủi ro |
|---|---|---|
| Dán thẻ lên đầu đọc | Giảm thao tác lặp lại | Người khác dùng phiên bác sĩ |
| Dán PIN lên màn hình | Nhập nhanh, tránh quên | PIN mất giá trị bí mật |
| Để phiên mở | Sợ bị đăng xuất | Máy trạm bị lợi dụng |
| Dùng chung tài khoản | Áp lực thời gian | Không truy vết được |

### 2.4. Rủi ro theo CIA

| Thuộc tính | Rủi ro | Mức tác động |
|---|---|---|
| Bí mật | Hồ sơ bị xem trái phép | Cao |
| Toàn vẹn | Dữ liệu điều trị bị sửa dưới danh nghĩa bác sĩ | Cao |
| Sẵn sàng | Quy trình làm chậm truy cập hợp lệ | Trung bình đến cao |
| Trách nhiệm giải trình | Log không còn đáng tin | Cao |
| Tuân thủ | Không đáp ứng yêu cầu bảo vệ dữ liệu cá nhân/y tế | Cao |

### 2.5. Kết luận chương 2

Dự án không thất bại vì thiếu công nghệ. Dự án thất bại vì kiểm soát không phù hợp với môi trường vận hành, thiếu ngoại lệ, thiếu tham vấn người dùng và thiếu quản lý thay đổi.

## Chương 3. Đề xuất giải pháp và kế hoạch triển khai

### 3.1. Nguyên tắc điều chỉnh

- Bảo mật phải hỗ trợ khám chữa bệnh.
- Kiểm soát phải dựa trên rủi ro và bối cảnh.
- Không đánh đổi trách nhiệm giải trình.
- Đào tạo phải đi kèm cải tiến thiết kế.

### 3.2. Xác thực theo ngữ cảnh

| Bối cảnh | Cơ chế đề xuất | Kiểm soát bù trừ |
|---|---|---|
| Khu cấp cứu | Badge nhanh, giảm nhập PIN lặp lại | Log chi tiết, cảnh báo bất thường |
| Khoa nội trú | Thẻ + PIN, timeout 5–10 phút | Khóa phiên nhanh, quyền theo ca |
| Khu hành chính | Thẻ + PIN, timeout ngắn | Giới hạn quyền theo vai trò |
| Truy cập từ xa | MFA mạnh | VPN/Zero Trust, cảnh báo ngoài giờ |
| Dữ liệu rất nhạy cảm | Xác thực lại | Log bắt buộc, hậu kiểm |

### 3.3. Break-glass access

Quy trình đề xuất:

```text
Tình huống cấp cứu → Chọn truy cập khẩn cấp → Nhập lý do → Cho phép truy cập nhanh → Ghi log chi tiết → Hậu kiểm bởi trưởng khoa/ATTT
```

### 3.4. Đào tạo và truyền thông

Thông điệp chính:

- Bảo mật bệnh án là một phần của an toàn người bệnh.
- Không chia sẻ thẻ/PIN là bảo vệ danh tính nghề nghiệp của bác sĩ.
- Truy cập nhanh nhưng phải đúng người, đúng bệnh nhân, đúng mục đích.

Kế hoạch:

| Giai đoạn | Hoạt động | Kết quả |
|---|---|---|
| Khảo sát | Phỏng vấn bác sĩ, đo thời gian truy cập | Danh sách điểm bất tiện |
| Đào tạo | Tình huống rủi ro thực tế | Bác sĩ hiểu hậu quả |
| Hướng dẫn | Quy trình mới, break-glass, báo lỗi | Giảm lách quy trình |
| Truyền thông | Poster, giao ban, video ngắn | Duy trì nhận thức |
| Đánh giá | Đo KPI trước/sau | Cải tiến liên tục |

### 3.5. Chỉ số đánh giá

- Tỷ lệ còn phát hiện thẻ/PIN dán tại máy trạm.
- Thời gian trung bình để truy cập hồ sơ.
- Số lượt break-glass và tỷ lệ hợp lệ sau hậu kiểm.
- Số truy cập bất thường bị cảnh báo.
- Điểm khảo sát nhận thức trước/sau đào tạo.
- Tỷ lệ hài lòng của bác sĩ với quy trình mới.

## Kết luận mẫu

Báo cáo cho thấy vấn đề an toàn thông tin trong tổ chức không thể giải quyết chỉ bằng công nghệ. Một kiểm soát kỹ thuật chỉ có hiệu quả khi được đặt trong bối cảnh quản lý phù hợp, có quy trình vận hành rõ ràng, có sự tham gia của người dùng và có cơ chế đo lường, cải tiến liên tục. Trong môi trường bệnh viện, giải pháp bảo mật phải đồng thời bảo vệ dữ liệu bệnh nhân, bảo đảm trách nhiệm giải trình và không cản trở hoạt động cứu chữa người bệnh.
