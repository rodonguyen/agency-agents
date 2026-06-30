# Workflow Multi-Agent: Startup MVP

> Ví dụ từng bước về cách phối hợp nhiều agent để đi từ ý tưởng đến MVP có thể ship.

## Bối cảnh

Bạn đang xây một SaaS MVP: công cụ retrospective cho team remote. Bạn có 4 tuần để ship sản phẩm chạy được với signup, một core feature và landing page.

## Đội agent

| Agent | Vai trò trong workflow |
|-------|------------------------|
| Sprint Prioritizer | Chia dự án thành sprint theo tuần |
| UX Researcher | Validate ý tưởng bằng phỏng vấn nhanh |
| Backend Architect | Thiết kế API và data model |
| Frontend Developer | Xây React app |
| Rapid Prototyper | Dựng phiên bản đầu thật nhanh |
| Growth Hacker | Lên kế hoạch launch song song khi build |
| Reality Checker | Gate từng milestone trước khi đi tiếp |

## Workflow

### Tuần 1: Discovery + Architecture

**Bước 1 — Kích hoạt Sprint Prioritizer**

```text
Activate Sprint Prioritizer.

Project: RetroBoard — a real-time team retrospective tool for remote teams.
Timeline: 4 weeks to MVP launch.
Core features: user auth, create retro boards, add cards, vote, action items.
Constraints: solo developer, React + Node.js stack, deploy to Vercel + Railway.

Break this into 4 weekly sprints with clear deliverables and acceptance criteria.
```

**Bước 2 — Kích hoạt UX Researcher song song**

```text
Activate UX Researcher.

I'm building a team retrospective tool for remote teams (5-20 people).
Competitors: EasyRetro, Retrium, Parabol.

Run a quick competitive analysis and identify:
1. What features are table stakes
2. Where competitors fall short
3. One differentiator we could own

Output a 1-page research brief.
```

**Bước 3 — Handoff cho Backend Architect**

```text
Activate Backend Architect.

Here's our sprint plan: [paste Sprint Prioritizer output]
Here's our research brief: [paste UX Researcher output]

Design the API and database schema for RetroBoard.
Stack: Node.js, Express, PostgreSQL, Socket.io for real-time.

Deliver:
1. Database schema (SQL)
2. REST API endpoints list
3. WebSocket events for real-time board updates
4. Auth strategy recommendation
```

### Tuần 2: Build core feature

**Bước 4 — Frontend Developer + Rapid Prototyper**

```text
Activate Frontend Developer.

Here's the API spec: [paste Backend Architect output]
Build the core RetroBoard UI in React.
Focus only on: create board, add cards, vote, action items.
Skip polish unless it affects usability.
```

```text
Activate Rapid Prototyper.

Help me get the first end-to-end version running quickly.
Identify the shortest path to a working demo and list what to fake, defer, or hard-code.
```

### Tuần 3: Launch preparation

**Bước 5 — Kích hoạt Growth Hacker**

```text
Activate Growth Hacker.

We are 1 week from beta launch for RetroBoard.
Target users: remote engineering managers and startup founders.
Budget: $0.

Create a launch plan with:
1. 3 acquisition channels
2. Landing page messaging angle
3. Beta user recruitment plan
4. Metrics to track in week one
```

### Tuần 4: Reality check + ship

**Bước 6 — Kích hoạt Reality Checker**

```text
Activate Reality Checker.

Review this MVP plan and current status:
[paste sprint output, demo notes, launch plan]

Tell me:
1. What is actually ready
2. What must be cut
3. What risk could block launch
4. The smallest credible launch scope
```

## Bài học chính

- Sprint Prioritizer giúp tránh scope creep ngay từ đầu.
- UX Researcher và Backend Architect nên chạy trước khi build quá sâu.
- Growth Hacker chuẩn bị launch trong khi sản phẩm đang được xây.
- Reality Checker bảo vệ MVP khỏi việc “gần xong nhưng không ship được”.