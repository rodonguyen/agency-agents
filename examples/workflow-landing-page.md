# Workflow Multi-Agent: Sprint Landing Page

> Ship một landing page tối ưu chuyển đổi trong một ngày bằng 4 agent.

## Bối cảnh

Bạn cần một landing page cho đợt ra mắt sản phẩm mới. Trang phải đẹp, có khả năng chuyển đổi visitor và được deploy trước cuối ngày.

## Đội agent

| Agent | Vai trò trong workflow |
|-------|------------------------|
| Content Creator | Viết copy |
| UI Designer | Thiết kế layout và component spec |
| Frontend Developer | Xây trang |
| Growth Hacker | Tối ưu conversion |

## Workflow

### Buổi sáng: Copy + Design song song

**Bước 1a — Kích hoạt Content Creator**

```text
Activate Content Creator.

Write landing page copy for "FlowSync" — an API integration platform
that connects any two SaaS tools in under 5 minutes.

Target audience: developers and technical PMs at mid-size companies.
Tone: confident, concise, slightly playful.

Sections needed:
1. Hero (headline + subheadline + CTA)
2. Problem statement (3 pain points)
3. How it works (3 steps)
4. Social proof (placeholder testimonial format)
5. Pricing (3 tiers: Free, Pro, Enterprise)
6. Final CTA

Keep it scannable. No fluff.
```

**Bước 1b — Kích hoạt UI Designer song song**

```text
Activate UI Designer.

Design specs for a SaaS landing page. Product: FlowSync (API integration platform).
Style: clean, modern, dark mode option. Think Linear or Vercel aesthetic.

Deliver:
1. Layout wireframe (section order + spacing)
2. Color palette (primary, secondary, accent, background)
3. Typography (font pairing, heading sizes, body size)
4. Component specs: hero section, feature cards, pricing table, CTA buttons
5. Responsive breakpoints (mobile, tablet, desktop)
```

### Giữa ngày: Build

**Bước 2 — Kích hoạt Frontend Developer**

```text
Activate Frontend Developer.

Build a landing page from these specs:

Copy: [paste Content Creator output]
Design: [paste UI Designer output]

Stack: HTML, Tailwind CSS, minimal vanilla JS (no framework needed).
Requirements:
- Responsive (mobile-first)
- Fast (no heavy assets, system fonts OK)
- Accessible (proper headings, alt text, focus states)
- Include a working email signup form (action URL: /api/subscribe)

Deliver a single index.html file ready to deploy.
```

### Buổi chiều: Tối ưu conversion

**Bước 3 — Kích hoạt Growth Hacker**

```text
Activate Growth Hacker.

Review this landing page for conversion:
[paste built HTML or screenshot]

Find:
1. Weak points in the messaging
2. Missing trust signals
3. CTA improvements
4. One A/B test idea for the hero
5. Analytics events we should track
```

**Bước 4 — Quay lại Frontend Developer**

```text
Activate Frontend Developer.

Apply these conversion improvements:
[paste Growth Hacker feedback]

Keep the page fast, accessible, and visually consistent.
```

## Bài học chính

- Chạy copy và design song song giúp tiết kiệm thời gian.
- Frontend Developer chỉ nên bắt đầu khi copy và design đã đủ rõ.
- Growth Hacker nên review sau khi có trang cụ thể, không chỉ review ý tưởng.
- Workflow nhỏ vẫn cần handoff rõ ràng: copy → design → build → optimize.