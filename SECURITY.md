# Chính sách bảo mật

## Báo cáo lỗ hổng

Nếu bạn phát hiện lỗ hổng bảo mật trong dự án, vui lòng báo cáo có trách nhiệm. **Không mở public GitHub issue** cho lỗ hổng bảo mật. Hãy dùng GitHub Security tab để tạo private security advisory.

## Thời gian phản hồi

- Xác nhận đã nhận báo cáo: trong 48 giờ.
- Đánh giá ban đầu: trong 7 ngày.
- Bản vá hoặc giảm thiểu rủi ro: tùy mức độ nghiêm trọng.

## Phạm vi

Repo này chủ yếu chứa định nghĩa agent dạng Markdown và shell script phục vụ cài đặt/chuyển đổi.

### File agent `.md`

- Là prompt/persona không thực thi trực tiếp.
- Không được lưu API key, secret, token hoặc credential trong file agent.
- Báo cáo các agent có dấu hiệu prompt injection, lừa lấy secret hoặc hướng dẫn hành vi nguy hiểm.

### Script trong `scripts/`

- `install.sh`, `convert.sh`, `lint-agents.sh` và các script liên quan có thể thực thi.
- Contributor nên review script trước khi chạy.
- PR thay đổi script cần mô tả rõ hành vi mới và lý do cần thay đổi.

## Thực hành tốt cho contributor

- Không commit API key, token, credential hoặc file cấu hình cá nhân.
- Không thêm executable code vào file Markdown agent.
- Không thêm command tải/chạy mã từ nguồn không tin cậy.
- Review shell script trước khi merge.
- Báo cáo định nghĩa agent đáng ngờ hoặc có ý định vượt rào bảo mật.