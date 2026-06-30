# Theo dõi upstream

File này ghi lại repo gốc dùng làm nền cho bản tiếng Việt, để việc đồng bộ thay đổi sau này rõ ràng hơn.

## Baseline hiện tại

- **Repo upstream**: https://github.com/msitarzewski/agency-agents
- **Commit tham chiếu**: `2448583`
- **Fork tiếng Việt**: https://github.com/rodonguyen/agency-agents
- **Phạm vi hiện tại**: Việt hóa README, tài liệu khởi đầu và frontmatter của các agent được dùng nhiều.

## Cách tiếp cận dịch

Bản tiếng Việt học theo cấu trúc của các repo dịch cộng đồng khác: README chính dùng ngôn ngữ bản địa, có link về upstream, nêu rõ phạm vi dịch và mời đóng góp theo thị trường địa phương.

Nguyên tắc:

- Path, command, URL, code block: giữ nguyên.
- Thuật ngữ kỹ thuật phổ biến: giữ tiếng Anh khi tự nhiên hơn.
- Nội dung giải thích: dịch sang tiếng Việt dễ hiểu.
- Agent chuyên ngành: dịch sau, ưu tiên nhóm được dùng nhiều trước.

## Lộ trình dịch

| Nhóm | Trạng thái | Ghi chú |
|---|---|---|
| README | Đã dịch | Tập trung quick start và chọn agent |
| CONTRIBUTING | Đã dịch | Hướng dẫn đóng góp và nguyên tắc dịch thuật |
| SECURITY | Đã dịch | Báo cáo lỗ hổng và best practices |
| examples/README | Đã dịch | Giải thích cách đọc ví dụ multi-agent |
| Agent phổ biến | Đang dịch | Đã Việt hóa frontmatter cho 13 agent dùng nhiều |
| Agent chuyên ngành | Chưa dịch | Dịch theo nhu cầu thực tế |
| Agent riêng Việt Nam | PR welcome | Zalo, MoMo, VNPAY, Shopee VN, Tiki, pháp lý VN |

## Cập nhật bản dịch

- Đã dịch `CONTRIBUTING.md`, `SECURITY.md`, `examples/README.md`.
- Đã Việt hóa frontmatter `name`, `description`, `vibe` cho 13 agent thường dùng trong engineering, design, marketing, product, testing và project management.
- Ước tính phạm vi hiện tại: khoảng 20% nội dung onboarding/high-use; chưa phải bản dịch toàn bộ repo.

## Chính sách đồng bộ

- Theo dõi branch `main` của upstream.
- Khi upstream đổi cách cài đặt, cập nhật README tiếng Việt trước.
- Khi thêm bản dịch agent, cập nhật bảng trạng thái trong file này.