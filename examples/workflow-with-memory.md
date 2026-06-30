# Workflow Multi-Agent: Làm việc có memory

> Ví dụ cách dùng memory và handoff để nhiều agent giữ được bối cảnh qua nhiều vòng làm việc.

## Vì sao memory quan trọng?

Khi một nhiệm vụ kéo dài qua nhiều phiên, vấn đề lớn nhất không phải là “agent có thông minh không”, mà là **agent có nhớ đúng quyết định, ràng buộc và trade-off đã thống nhất không**.

Workflow này dùng memory theo cách thực dụng: ghi lại quyết định quan trọng, cập nhật sau mỗi milestone và truyền context ngắn gọn cho agent tiếp theo.

## Nguyên tắc

- Memory không phải nhật ký đầy đủ; chỉ lưu điều ảnh hưởng đến quyết định sau này.
- Mỗi handoff nên có mục tiêu, ràng buộc, quyết định đã chốt và câu hỏi còn mở.
- Agent mới không nên phải đọc lại toàn bộ lịch sử nếu một summary tốt là đủ.
- Memory phải được cập nhật khi quyết định thay đổi.

## Mẫu handoff

```text
Context:
- Product: [what we are building]
- Target user: [who this is for]
- Current milestone: [where we are]

Decisions already made:
- [decision 1]
- [decision 2]

Constraints:
- [time/budget/tech constraints]

Open questions:
- [question 1]
- [question 2]

Ask:
- [what this agent should deliver]
```

## Ví dụ workflow

### Bước 1 — Product Manager tạo decision log

```text
Activate Product Manager.

Create a lightweight decision log for this project.
Capture: target user, core problem, MVP scope, non-goals, success metric, and open risks.
Keep it short enough to paste into future agent prompts.
```

### Bước 2 — Software Architect dùng memory

```text
Activate Software Architect.

Use this project memory:
[paste decision log]

Propose a technical architecture that fits the MVP scope and constraints.
Call out any product decisions that create technical risk.
```

### Bước 3 — Project Manager cập nhật handoff

```text
Activate Project Manager.

Update the project memory with the architecture decisions.
Then create a handoff summary for Frontend Developer and Backend Architect.
```

### Bước 4 — Reality Checker kiểm tra drift

```text
Activate Reality Checker.

Compare the current plan against the original project memory.
Identify scope drift, forgotten constraints, and decisions that need to be revisited.
```

## Bài học chính

- Memory tốt giúp giảm việc lặp lại context.
- Handoff tốt làm agent tiếp theo bắt đầu nhanh hơn.
- Reality Checker giúp phát hiện drift trước khi dự án lệch hướng.
- Đừng lưu mọi thứ; chỉ lưu điều ảnh hưởng đến quyết định.