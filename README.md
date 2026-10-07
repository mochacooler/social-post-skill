# social-post-skill

Claude skill `social-post`: viết social post (Facebook/LinkedIn, tiếng Việt) có kiểm chứng dữ kiện, kèm infographic tối giản 1080×1350.

## Cấu trúc
- `social-post/SKILL.md` — quy trình: kiểm chứng (Facts/Assumptions/Unknowns) → framing → viết bài → infographic HTML/CSS + Playwright (AntV Infographic là tùy chọn) → QA → giao bản nháp.
- `social-post/evals/evals.json` — 2 test case dùng khi đánh giá skill.

## Cài đặt
Chép thư mục `social-post/` vào thư mục skills của Claude (ví dụ `~/.claude/skills/social-post/`), hoặc tải lên qua phần Skills trong Claude.

## Nguyên tắc chính
- Không bịa dữ liệu; thiếu số liệu thì để placeholder.
- Chỉ soạn bản nháp, không tự đăng.
- Phản biện luôn kèm option.
