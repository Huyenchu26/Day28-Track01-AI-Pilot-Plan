---
artifact: 5 — Solution Approach + 6 — Demo/Mockup/Flow (bản nộp phase Solution)
bai-tap: Solution — chốt cách làm + cho stakeholder nhìn thấy
phase: Double Diamond vòng 2 · ◆ siết (chốt 1 cách làm + 1 artifact trực quan)
time: ~12 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 1-find-existing-solutions.md · 00-context.md · templates/demo-examples.md · prompts/05-demo-challenge.md
nop-cuoi: Có — bản nộp của phase Solution (Part B + C · A3 mục Solution Approach + Demo/Mockup/Flow)
---

# 2 — FINAL: Solution Approach + Demo/Mockup/Flow

Mục tiêu: chốt cách làm cho Quick Win (Build / Buy / Boost / Partner), nói rõ data & ai review cần có, và tạo 1 bản vẽ trực quan để stakeholder *nhìn* được. Đây là nửa "siết lại" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 2 và là bản nộp của phase Solution.

Lý do làm bước này: hai cái bẫy. Một, "tự build" cho oai — trong khi 80–90% nhu cầu nội bộ chỉ cần Boost/Buy; tự build là quyết định khó rút lại nhất. Hai, chỉ nói bằng chữ — stakeholder không duyệt một đoạn văn, họ duyệt khi *nhìn thấy* flow. Không có bản vẽ → trượt Gate 4 dù lập luận tốt.

Quy tắc: **bản vẽ trực quan là BẮT BUỘC; demo chạy được chỉ là điểm cộng.** *Demo đơn giản + lập luận chặt > demo đẹp + lập luận yếu.*

## Quy trình 12 phút

```text
4 phút  — Phần A: chốt Build/Buy/Boost/Partner (decision tree + ego check)
3 phút  — Phần B: data & ai review cần có
5 phút  — Phần C: vẽ 1 artifact trực quan + đánh dấu chỗ người review
```

---

## Phần A — Chốt cách làm

Đi decision tree, đừng chọn theo cảm giác:

```text
Bài này có phải LỢI THẾ CẠNH TRANH CỐT LÕI không?
 ├─ CÓ  → đội có AI engineer mạnh? CÓ → Build · KHÔNG → Boost
 └─ KHÔNG (chỉ là productivity layer) → có tool sẵn?
          CÓ → Buy · KHÔNG → Boost (model sẵn + data riêng)
```

**Nhánh nhóm đi:** KHÔNG lợi thế cốt lõi → có tool sẵn một phần (Gradescope/LMS) nhưng **không khớp** flow nộp worksheet GitHub + budget pilot → **Boost** (LLM API + rubric Day 28 + rule heading nhẹ).

Câu hỏi phụ:

- Nhóm chọn cách này vì *cần* hay vì *thích tự build*? Một câu thành thật.
- Hướng nào ở file `1` (đã tìm được người làm rồi) khớp với cách nào — "đi từ 5 lên"?

### Trả lời

- **Cách làm chốt**: **Boost** (hybrid nhẹ: rule checklist cấu trúc + LLM map rubric → JSON feedback)
- **Lý do CẦN (không phải thích), 2–3 câu**:
  - Rubric Day 28 đã có sẵn trong repo — chỉ cần ghép prompt + API, không xây engine chấm.
  - Tiền lệ formative pre-submit (pre-grader, FeedbackWriter) cho thấy giá trị ở **feedback trước nộp**, không cần auto-điểm.
  - Pilot 1 buổi–6 tuần: một form/webhook Discord hoặc Google Form + script gọi API là đủ; đổi vendor API dễ hơn rút khỏi Build.
- **Vì sao KHÔNG "Build từ số 0"**: Không phải differentiator của khóa; tốn thời gian auth, UI, lưu submission — trùng LMS/Gradescope nhưng chậm hơn Buy. Nhóm lab không có bandwidth maintain platform.
- **Vì sao KHÔNG Buy (Gradescope) làm chính**: License/onboarding không kịp pilot buổi D28; tool tối ưu chấm *sau* nộp, trong khi Quick Win là *trước* submit ([Gradescope rubrics](https://guides.gradescope.com/hc/en-us/articles/22249389005709-Grading-submissions-with-rubrics) — tham chiếu workflow, không mua cho pilot này).
- **Ego check (1 câu thành thật)**: Ban đầu nhóm nghiêng "build bot Discord" vì nghe ngầu; sau research chọn Boost vì **cần chứng minh giảm 30% bài trả vòng 1**, không cần sản phẩm đẹp.
- **"Đi từ 5 lên"**: Copy workflow pre-grader + guardrail Colleague AI (không tin auto-score) — chỉ thay domain bằng rubric `03-pilot-plan` Day 28.
- **Tool / API / vendor cần + ước lượng chi phí thô**:
  - **Claude / GPT API** — ~$0.01–0.05/bài ( 150 nhóm × 2 lần check ≈ **$5–15/pilot** nếu dùng model rẻ + prompt ngắn).
  - **Google Form / link nộp** — $0 (có sẵn).
  - **Script Python/Node** gọi API + regex heading — $0 (nhóm tự viết ~50 dòng, không coi là Build platform).
  - Tùy chọn: **GitHub Action** check markdown trên PR — $0 tier public repo.

## Phần B — Data & ai review (cách làm này cần gì để chạy được)

| Cần gì | Có sẵn trong AI20k? | Trong lab dùng (mẫu/giả định) | Privacy? |
|---|---|---|---|
| **Rubric Day 28** (scope, metric, exit, budget, adoption) | Có — template trong repo mẫu GV | Copy rubric từ `templates/` + checklist 7 mục A3 | Public template — OK |
| **Bài nộp học viên** (markdown) | Có khi nộp GitHub/LMS | 10–20 bài mẫu + bài thật pilot (opt-in, không paste Discord DM) | Chỉ lưu hash/log flag, không train model; xóa sau pilot |
| **Baseline 30% trả vòng 1** | Chưa đo chính thức | Coach đếm tuần 1 pilot vs giả định từ Problem Framing | Aggregate only |
| **Golden set để calibrate** | Không | Coach gắn nhãn 15 bài: đủ/thiếu từng mục rubric | Nội bộ coach |

- **Output nào rủi ro cao** (sai gây hậu quả):
  - AI báo **"đủ rubric"** khi thực tế thiếu → học viên nộp, coach trả lại → mất tin (false negative ngược).
  - AI **chặn oan** hoặc báo thiếu mục đã có → friction, spam coach.
  - Học viên **tin checklist AI = điểm chính thức** → vi phạm formative.
- **Ai review + bao nhiêu mẫu + pass/fail theo gì**:
  - **Lab coach** review **100%** các bài bị flag "thiếu nghiêm trọng" lần đầu; **spot-check 20%** bài AI báo "đủ".
  - **Pass pilot** nếu: false positive (AI báo thiếu mà coach thấy đủ) **< 15%** trên golden set 15 bài; **≥ 20%** giảm bài trả vòng 1 (so baseline).
  - Instructor có quyền **tắt chặn cứng**, chuyển chỉ cảnh báo.
- **Có cần citation / nói "không biết" khi thiếu nguồn không**: Có — mỗi mục rubric AI phải trích **đoạn trong bài nộp** hoặc trả `MISSING` + không bịa đoạn trích; mục cần số (budget, metric) nếu không thấy số → `MISSING (no number cited)`.

## Phần C — Bản vẽ trực quan (BẮT BUỘC)

**Dạng chọn:** Luồng người dùng **before / after** (Dạng 2 — `templates/demo-examples.md`) — vì giá trị chính là cắt vòng "nộp → coach trả → sửa".

```text
TRƯỚC (hiện tại):
  [Học viên làm xong worksheet]
        →  Submit LMS/GitHub
        →  Coach đọc (~5 phút/bài lỗi)
        →  Feedback "thiếu Budget / Exit criteria"
        →  Học viên sửa → Submit lại
        →  Coach chấm lại
  ( ~45/150 nhóm × 5 phút ≈ 225 phút coach/đợt nộp)

SAU (có AI Rubric Pre-Check — Boost):
  [Học viên dán markdown + bấm "Kiểm tra"]
        →  [Rule: có heading ## Budget, ## Exit…?]
        →  [LLM: map từng mục rubric → ✅ / ⚠️ + trích dẫn]
        →  [Màn hình checklist — sửa ngay trên máy]
        →  (Tùy pilot) Submit khi ⚠️ = 0 HOẶC submit + cờ "đã xem cảnh báo"
        →  Coach chỉ chấm bài; spot-check 20% bài AI báo đủ
  Khác biệt rõ nhất: Vòng "coach trả lỗi vặt" gom về phía học viên TRƯỚC submit.

┌─ Màn 1: Nộp bài ─────────────────────────────┐
│  Paste markdown / upload file                 │
│  [ Kiểm tra rubric ]                         │
└──────────────────────┬──────────────────────┘
                       ▼
┌─ Màn 2: Kết quả AI (formative) ──────────────┐
│  ✅ Scope  ·  ⚠️ Budget (thiếu số)          │
│  ✅ Metrics ·  ❌ Exit criteria (chỉ 1 mức) │
│  Trích dẫn: "...chưa thấy ngưỡng đo..."      │
│  ⓘ Không phải điểm chính thức               │
└──────────────────────┬──────────────────────┘
                       ▼
┌─ Màn 3: Hành động ───────────────────────────┐
│  [ Sửa và kiểm tra lại ]  [ Nộp anyway ]    │
└──────────────────────────────────────────────┘

Chỗ con người review (output rủi ro cao) nằm ở:
  ★ SAU Màn 2 — Coach review 100% case ❌/⚠️ nghiêm trọng + 20% case ✅
  ★ Instructor quyết định policy: cảnh báo mềm vs chặn cứng (trước khi scale)
```

**Prompt flow (tóm tắt — bổ sung cho Gate 4):**

```text
[INPUT: bài markdown + rubric JSON Day28]
      │
      ▼
[B1: regex — heading / độ dài tối thiểu]
      │
      ▼
[B2: LLM — "chỉ trả JSON checklist; trích dẫn hoặc MISSING"]
      │
      ▼
[OUTPUT: UI checklist] ──★ Coach spot-check / audit log
```

**Câu hỏi validate với stakeholder (sau khi chiếu artifact):**
1. *"Checklist này có đúng các mục coach hay trả bài vì thiếu không — thiếu hoặc thừa mục nào?"*
2. *"Cảnh báo mềm (vẫn cho nộp) hay chặn cứng — anh/chị chọn policy nào cho tuần pilot?"*
3. *"Mức false positive bao nhiêu thì coach mất tin — ngưỡng dừng pilot?"*

**Input làm lộ điểm yếu (chuẩn bị trước):** Bài viết đủ heading nhưng **nội dung rỗng** ("Budget: TBD") — rule pass, LLM phải báo; bài tiếng Việt lẫn Anh không chuẩn heading.

---

## Tổng kiểm tra trước khi sang `../03-pilot-plan/`

| Hạng mục | Xong? |
|---|---|
| Cách làm có lý do CẦN, không phải "mặc định tự build" | ✓ |
| Nói rõ data cần + ai review output rủi ro cao | ✓ |
| Có ≥1 bản vẽ trực quan, người ngoài hiểu trong ~20 giây | ✓ |
| Có đánh dấu chỗ con người review | ✓ |

⚑ Coach kiểm tra ở Mốc 3: *"Stakeholder nhìn vào đâu để hiểu flow? Mockup/sketch/demo đâu?"* Chỉ nói bằng chữ = chưa qua.

