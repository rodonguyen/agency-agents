# Đóng góp cho agency-agents Tiếng Việt

Cảm ơn bạn muốn đóng góp cho bản tiếng Việt của **agency-agents**. Mục tiêu của fork này là giúp người dùng Việt Nam bắt đầu nhanh với thư viện agent, đồng thời vẫn bám sát upstream gốc.

## Mục lục

- [Quy tắc ứng xử](#quy-tắc-ứng-xử)
- [Bạn có thể đóng góp gì?](#bạn-có-thể-đóng-góp-gì)
- [Nguyên tắc dịch thuật](#nguyên-tắc-dịch-thuật)
- [Nguyên tắc thiết kế agent](#nguyên-tắc-thiết-kế-agent)
- [Quy trình Pull Request](#quy-trình-pull-request)
- [Kiểm tra trước khi gửi](#kiểm-tra-trước-khi-gửi)

---

## Quy tắc ứng xử

Dự án này chào đón mọi người đóng góp một cách tôn trọng và chuyên nghiệp.

- **Tôn trọng:** tranh luận về ý tưởng, không công kích cá nhân.
- **Bao hàm:** chào đón người dùng ở mọi trình độ, nền tảng và vai trò.
- **Hợp tác:** ưu tiên cải thiện agent và tài liệu hơn là thắng tranh luận.
- **Thực tế:** tập trung vào nội dung có ích cho người dùng thật.

---

## Bạn có thể đóng góp gì?

### 1. Dịch tài liệu và agent

Ưu tiên dịch theo mức độ người dùng chạm vào nhiều nhất:

1. `README.md`, `CONTRIBUTING.md`, `SECURITY.md`, `examples/README.md`.
2. Tên, mô tả ngắn và phần mở đầu của agent phổ biến.
3. Nhóm `engineering/`, `design/`, `marketing/`, `product/`, `testing/`.
4. Ví dụ workflow trong `examples/`.
5. Agent chuyên ngành khi có nhu cầu thực tế.

### 2. Cải thiện bản dịch hiện có

Bạn có thể làm câu tiếng Việt tự nhiên hơn, sửa thuật ngữ chưa nhất quán, giữ đúng ý kỹ thuật của upstream, cập nhật khi upstream thay đổi, hoặc thêm ghi chú thị trường Việt Nam nếu thật sự hữu ích.

### 3. Tạo agent mới

Nếu muốn thêm agent mới, hãy chọn đúng thư mục chuyên môn:

- `academic/` — nghiên cứu, học thuật, chuyên gia lĩnh vực.
- `design/` — UX/UI, research, visual design.
- `engineering/` — phát triển phần mềm, kiến trúc, DevOps, AI engineering.
- `finance/` — tài chính, kế toán, đầu tư, thuế.
- `game-development/` — thiết kế và phát triển game.
- `gis/` — bản đồ, geospatial, phân tích không gian.
- `marketing/` — nội dung, growth, SEO, social.
- `paid-media/` — quảng cáo trả phí và media buying.
- `product/` — product management, roadmap, feedback.
- `project-management/` — điều phối, planning, delivery.
- `sales/` — bán hàng, proposal, discovery, deal strategy.
- `security/` — AppSec, pentest, threat intel, incident response.
- `spatial-computing/` — AR/VR/XR và spatial interface.
- `specialized/` — chuyên gia đặc thù không thuộc nhóm khác.
- `support/` — operations, customer support, reporting.
- `testing/` — QA, API testing, accessibility, performance.

`divisions.json` là nguồn sự thật cho danh sách division. Nếu đề xuất division mới, cần cập nhật directory, `divisions.json`, `scripts/convert.sh` và `scripts/lint-agents.sh` cho nhất quán.

---

## Nguyên tắc dịch thuật

Bản tiếng Việt ưu tiên **dễ dùng và đúng ngữ cảnh**, không dịch máy từng chữ.

### Nên giữ nguyên

- Tên file, thư mục, command, URL.
- Code block và cấu trúc YAML/frontmatter quan trọng.
- Thuật ngữ kỹ thuật phổ biến: API, backend, frontend, deploy, CI/CD, prompt, agent, workflow, roadmap, stakeholder, benchmark.
- Tên sản phẩm, framework, thư viện, tiêu chuẩn kỹ thuật.

### Nên dịch

- Heading, mô tả vai trò, workflow, checklist, tiêu chí thành công.
- Giải thích dành cho người mới.
- Hướng dẫn đóng góp và onboarding.
- Ví dụ dùng ngôn ngữ tự nhiên.

### Tránh

- Dịch làm sai nghĩa kỹ thuật.
- Thêm nội dung quảng cáo hoặc claim không có trong upstream.
- Đổi tên file hoặc path chỉ vì dịch.
- Dịch toàn bộ repo bằng máy mà không review.

---

## Nguyên tắc thiết kế agent

Một agent tốt cần cụ thể, có trách nhiệm rõ ràng và tạo được đầu ra thực tế.

Agent nên có identity rõ ràng, mission cụ thể, workflow có thể lặp lại, deliverable kiểm chứng được, tiêu chí thành công và giới hạn phạm vi. Agent không nên quá chung chung như “AI expert”, hứa kết quả không kiểm chứng được, khuyến khích hành vi nguy hiểm hoặc trộn quá nhiều vai trò không liên quan.

---

## Quy trình Pull Request

1. Fork repo và tạo branch mới.
2. Thực hiện thay đổi nhỏ, có phạm vi rõ ràng.
3. Chạy kiểm tra phù hợp.
4. Mô tả PR gồm: mục tiêu, file đã đổi, cách đã kiểm tra.
5. Nếu là bản dịch, ghi rõ phần nào được dịch và phần nào chưa dịch.

Ví dụ branch:

```bash
git checkout -b translate-engineering-frontmatter
```

Ví dụ commit:

```bash
git commit -m "Translate engineering agent summaries to Vietnamese"
```

---

## Kiểm tra trước khi gửi

Tối thiểu nên chạy:

```bash
bash scripts/check-divisions.sh
bash scripts/check-tools.sh
```

Nếu thay đổi agent, cân nhắc chạy thêm:

```bash
bash scripts/lint-agents.sh
```

Trước khi mở PR, tự kiểm tra link Markdown, command, path, phạm vi thay đổi và nội dung tiếng Việt. Đừng commit secret, token hoặc file local.

---

## Agent riêng cho Việt Nam

PR agent riêng cho thị trường Việt Nam rất được chào đón nếu có bối cảnh rõ ràng, ví dụ Zalo OA, Zalo Mini App, MoMo, ZaloPay, VNPAY, Shopee Việt Nam, Lazada Việt Nam, Tiki, TikTok Shop, SEO tiếng Việt, social commerce, pháp lý dữ liệu cá nhân hoặc thương mại điện tử Việt Nam.

Hãy tránh tạo agent “Việt Nam” quá rộng. Agent tốt nên có nhiệm vụ hẹp, ví dụ `Zalo OA Growth Strategist` tốt hơn `Vietnam Marketing Expert`.