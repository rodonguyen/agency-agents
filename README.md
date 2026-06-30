# agency-agents Tiếng Việt (đội ngũ chuyên gia AI)

🌐 **Tiếng Việt** | [English upstream](https://github.com/msitarzewski/agency-agents) | [Bahasa Indonesia](https://github.com/jnMetaCode/agency-agents-id) | [Português BR](https://github.com/jnMetaCode/agency-agents-pt-BR) | [Русский](https://github.com/jnMetaCode/agency-agents-ru) | [한국어](https://github.com/jnMetaCode/agency-agents-ko)

> **Bộ persona AI agent sẵn sàng dùng** — bao phủ engineering, design, marketing, product, testing, security, finance và nhiều nhóm chuyên môn khác. Đây không phải prompt mẫu chung chung: mỗi agent có vai trò, cách nghĩ, workflow và deliverable rõ ràng.

Bản tiếng Việt cộng đồng của [agency-agents](https://github.com/msitarzewski/agency-agents). Giai đoạn đầu dịch có chọn lọc, ưu tiên những phần người dùng chạm vào nhiều nhất trước: README, hướng dẫn cài đặt, cách chọn agent và định hướng đóng góp. PR tiếng Việt hoặc agent phù hợp thị trường Việt Nam luôn được chào đón.

[![GitHub stars](https://img.shields.io/github/stars/rodonguyen/agency-agents?style=social)](https://github.com/rodonguyen/agency-agents)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://makeapullrequest.com)

### 📊 Quy mô dự án

| 🤖 AI agent | 🌏 Đã Việt hóa | 🇻🇳 Agent riêng cho Việt Nam | 🧰 Công cụ | 🏢 Nhóm chuyên môn |
|:---:|:---:|:---:|:---:|:---:|
| **232** | **README + docs khởi đầu** | **PR welcome** | **14** | **16** |

---

## Đây là gì?

**agency-agents** là thư viện persona AI dùng được ngay. Mỗi agent mô tả một chuyên gia cụ thể: họ chịu trách nhiệm gì, làm việc theo quy trình nào, tạo ra đầu ra gì và giao tiếp ra sao.

**Khác với prompt thông thường:** prompt thường chỉ nói “hãy đóng vai chuyên gia”. Agent trong repo này định nghĩa sâu hơn: **chuyên gia đó suy nghĩ thế nào, kiểm tra điều gì, bàn giao gì và biết từ chối phạm vi nào**.

Ví dụ:

- `engineering/engineering-frontend-developer.md` phù hợp khi cần xây hoặc refactor UI.
- `engineering/engineering-code-reviewer.md` phù hợp khi cần review code có cấu trúc.
- `design/design-ui-designer.md` phù hợp khi cần hệ thống giao diện rõ ràng.
- `marketing/marketing-seo-specialist.md` phù hợp khi cần chiến lược SEO thực dụng.
- `testing/testing-api-tester.md` phù hợp khi cần kiểm thử API có bằng chứng.

---

## Bắt đầu nhanh

### Cách 1: Cài tự động vào công cụ AI

Repo hỗ trợ nhiều công cụ AI coding phổ biến. Nếu bạn không chắc mình dùng gì, hãy để script tự phát hiện:

```bash
./scripts/install.sh
```

Hoặc chỉ định công cụ cụ thể:

```bash
./scripts/install.sh --tool claude-code
./scripts/install.sh --tool cursor
./scripts/install.sh --tool codex
./scripts/install.sh --tool copilot
./scripts/install.sh --tool gemini-cli
```

Một số công cụ cần tạo file tích hợp trước:

```bash
./scripts/convert.sh
./scripts/install.sh
```

### Cách 2: Cài ứng dụng desktop

Nếu bạn muốn giao diện dễ dùng hơn, hãy dùng **Agency Agents** app cho macOS, Linux và Windows:

- Website: https://agencyagents.app
- Release mới nhất: https://github.com/msitarzewski/agency-agents-app/releases/latest

Trên macOS:

```bash
brew install --cask msitarzewski/agency-agents/agency-agents
```

### Cách 3: Copy thủ công agent cần dùng

```bash
cp engineering/*.md ~/.claude/agents/
```

Sau đó gọi agent bằng ngôn ngữ tự nhiên, ví dụ:

```text
Activate Frontend Developer mode and help me build a React component.
```

### Cách 4: Dùng như thư viện prompt tham khảo

Mở các file `.md`, chọn agent gần với việc cần làm, rồi copy/adapt phần persona, workflow và deliverable vào công cụ AI của bạn.

---

## Nên dùng agent nào trước?

Chọn theo kết quả bạn muốn có, không chọn theo tên nghe hay.

| Mục tiêu | Agent nên thử trước |
|---|---|
| Xây tính năng web/app | `engineering/engineering-frontend-developer.md`, `engineering/engineering-backend-architect.md`, `engineering/engineering-senior-developer.md` |
| Review code hoặc kiến trúc | `engineering/engineering-code-reviewer.md`, `engineering/engineering-software-architect.md` |
| Thiết kế UI/UX | `design/design-ui-designer.md`, `design/design-ux-researcher.md`, `design/design-ux-architect.md` |
| Nội dung và tăng trưởng | `marketing/marketing-content-creator.md`, `marketing/marketing-seo-specialist.md`, `marketing/marketing-growth-hacker.md` |
| Product và ưu tiên roadmap | `product/product-manager.md`, `product/product-sprint-prioritizer.md` |
| Kiểm thử và chất lượng | `testing/testing-api-tester.md`, `testing/testing-accessibility-auditor.md` |
| Quản lý dự án | `project-management/project-manager-senior.md` |

---

## Trạng thái bản dịch tiếng Việt

Bản dịch này cố ý bắt đầu nhỏ, khoảng 5% nội dung có giá trị sử dụng cao nhất, để dễ review và tránh dịch ồ ạt kém chất lượng.

Ưu tiên dịch tiếp theo:

1. README, quick start và hướng dẫn cài đặt.
2. Tên + mô tả ngắn của agent phổ biến.
3. Nhóm `engineering/`, `design/`, `marketing/`, `product/`.
4. Ví dụ workflow trong `examples/`.
5. Agent chuyên ngành khi có người dùng Việt Nam thực sự cần.

---

## Đóng góp

Khi đóng góp bản dịch:

- Giữ nguyên tên file, path, command, URL và block code.
- Dịch tự nhiên cho người Việt, không dịch máy từng chữ.
- Giữ thuật ngữ kỹ thuật tiếng Anh nếu cộng đồng Việt Nam dùng phổ biến: API, backend, frontend, deploy, CI/CD, prompt, agent, workflow.
- Không thay đổi nội dung kỹ thuật nếu PR chỉ nhằm dịch thuật.
- Nếu thêm agent riêng cho Việt Nam, hãy nêu rõ bối cảnh: Zalo, MoMo, VNPAY, Shopee/Lazada/Tiki, pháp lý Việt Nam, thương mại điện tử Việt Nam, v.v.

Xem baseline upstream trong [`UPSTREAM.md`](UPSTREAM.md).

---

## Giấy phép

Dự án dùng giấy phép MIT giống upstream. Xem [`LICENSE`](LICENSE).
