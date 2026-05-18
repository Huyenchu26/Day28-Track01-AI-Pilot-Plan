---
artifact: 5 — Solution Approach (phần khám phá)
bai-tap: Solution — tìm lời giải đã có sẵn trước khi tự xây
phase: Double Diamond vòng 2 · ◇ giãn (mở hết lựa chọn, chưa chốt)
time: ~8 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 01-frame/3-FINAL-problem-framing.md · 00-context.md · prompts/04-find-solutions.md
nop-cuoi: Không — file trung gian (bản chốt ở 2-FINAL-solution.md)
---

# 1 — Find existing solutions (đừng xây lại từ số 0)

Mục tiêu: trước khi quyết Build / Buy / Boost / Partner, nhóm phải biết bài này đã có ai giải ở chỗ khác chưa, và họ giải bằng cách nào. Đây là nửa "giãn ra" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 2 — mở hết các lời giải đang tồn tại, chưa chốt cái nào.

Lý do làm bước này: đây là chỗ nhiều nhóm hỏng mà không biết. Hỏng vì nhảy thẳng vào "tự build" cho oai, trong khi 80–90% nhu cầu nội bộ chỉ cần Boost hoặc Buy. Hỏng vì không hỏi "ai làm rồi" nên đi lại từ số 0. Gần như bài nào cũng đã có người giải ở một ngành khác — không thấy thì phí cả pilot.

Quy tắc: **không có nguồn = giả định.** Mỗi cái AI/web nói ra, hỏi lại "lấy ở đâu?". Không chỉ được nguồn thì đánh dấu (giả định để giảng), đừng xài như fact.

## Bước 0 — Bài này thực ra là dạng bài gì? (2 phút)

Bỏ context AI20k sang một bên. Mô tả Quick Win của nhóm như một bài toán chung — không có chữ "học viên / coach / Discord". Vài ví dụ cho dễ hình dung:

- "câu hỏi của user → câu trả lời kèm nguồn" → đây là bài Q&A có citation
- "một đống văn bản lộn xộn → data có cấu trúc" → bài extraction
- "bài nộp → nhận xét theo rubric" → bài rubric grading

Dạng bài (the pattern) đó gần như chắc chắn đã có người làm ở ngành khác. Tìm ra dạng bài → tìm ra người đã giải nó.

- **Quick Win của nhóm, viết lại thành 1 dạng bài chung (không có chữ domain)**: **Kiểm tra tuân thủ checklist trên tài liệu tự do trước khi gửi đi** (formative compliance check) — không chấm điểm cuối, chỉ báo mục thiếu/thiếu cấu trúc so với rubric đã định nghĩa.
- **Input → output thực chất là gì**: Văn bản/markdown bài nộp + rubric dạng checklist → Báo cáo có/không từng tiêu chí + gợi ý sửa ngắn (không viết hộ nội dung).
- **Ràng buộc không bỏ được (lấy từ `00-context.md`)**: Budget nhỏ · output formative (không thay điểm chính thức) · human review mẫu · privacy (không lưu submission nhạy cảm tùy tiện) · adoption (phải dùng được ngay lúc nộp) · pilot nhỏ trong khóa hiện tại.

## Quy trình 8 phút

```text
2 phút  — Bước 0: gọi tên dạng bài
4 phút  — Phần A: deep research 4 tầng "ai giải dạng bài này rồi"
2 phút  — Phần B: rút về 2–3 hướng khả thi, đánh dấu nguồn
```

---

## Phần A — Deep research: ai giải dạng bài này rồi, giải sao?

Không phải gõ 1 câu vào AI rồi chép. Chạy 4 tầng, **tầng sau lấy kết quả tầng trước làm input**. Khung câu lệnh ở `prompts/04-find-solutions.md`.

Câu hỏi phụ (tự trả lời — viết ra cái nhóm *tìm thấy*, không phải cái nhóm *đoán*):

- Dạng bài này giống bài nào ở một ngành hoàn toàn khác?
- Hướng nào AI gợi ý mà nhóm **không kiểm được nguồn** — vậy có nên tin không?
- Một ca thất bại của người đi trước dạy nhóm tránh đúng điều gì?
- Nhóm "đi từ mức mấy" — kế thừa được gì để khỏi bắt đầu từ 0?

### Trả lời — điền theo 4 tầng

| Tầng | Hỏi AI/web câu gì | Tìm được gì | Nguồn / nếu là giả định |
|---|---|---|---|
| 1 · Map | "Dạng bài checklist compliance trên văn bản tự do thường giải bằng những hướng nào?" | **(1) Rule/schema gate** — bắt buộc field/heading có mặt (giống CI lint trên repo). **(2) LMS form validation** — Canvas/Moodle bắt điền đủ mục trước submit. **(3) Buy — nền tảng chấm có rubric** (Gradescope: rubric nhất quán, auto cho MCQ/short answer; free-text vẫn cần người). **(4) Boost — LLM + rubric prompt** — feedback formative trước/sau nộp. **(5) Peer/human pre-review** — TA checklist tay. **(6) Hybrid** — regex cấu trúc + LLM cho mục ngữ nghĩa. |  tổng hợp pattern từ map; Gradescope: [Grading with rubrics](https://guides.gradescope.com/hc/en-us/articles/22249389005709-Grading-submissions-with-rubrics) |
| 2 · Tiền lệ | "Đội nào đã làm pre-submission rubric feedback ở quy mô lớp học?" | **Gradescope** — rubric áp đồng loạt, giảm thời gian chấm *sau* nộp; auto một phần cho câu có đáp án cố định. **Giáo viên dùng LLM làm "pre-grader"** — học viên nộp draft + rubric vào ChatGPT, sửa rồi mới nộp chính thức (có guardrail: phải có bản nháp trước, không copy-paste đáp án AI). **Pilot Colleague AI (K-12)** — AI rubric + feedback nhanh; giáo viên không tin auto-score, học viên cần human oversight. **FeedbackWriter (RCT)** — AI-mediated feedback cải thiện revision (d ≈ 0.50) so với chỉ feedback người. | [Gradescope rubrics](https://guides.gradescope.com/hc/en-us/articles/22249389005709-Grading-submissions-with-rubrics) · [How to Teach with AI — pre-grader workflow](https://howtoteachwithai.substack.com/p/stop-being-the-first-person-to-grade) · [arXiv:2506.07955 — Colleague AI co-design](https://arxiv.org/abs/2506.07955) · [arXiv:2602.16820 — FeedbackWriter](https://arxiv.org/abs/2602.16820) |
| 3 · Phản chứng | "Ca nào automated rubric/essay scoring thất bại?" | **False positive/negative** — AES nhạy wording rubric, lệch điểm theo framing ([GMU JSSR](https://journals.gmu.edu/jssr/article/view/5344)). **Bias nhóm học** — hệ thống train thiếu đa dạng → chấm sai ELL/nhóm khác ([ACL BEA 2024](https://aclanthology.org/2024.bea-1.18/)). **Gaming** — học viên tối ưu cho checklist thay vì hiểu bài; hoặc tin AI báo "đủ" rồi nộp thiếu thật. **Chặn cứng gây friction** — chặn submit khi AI hallucinate "thiếu mục" → mất adoption. **Over-trust** — pilot Colleague AI: giáo viên từ chối auto-score, chỉ tin feedback có người spot-check. | [JSSR rubric language & LLM](https://journals.gmu.edu/jssr/article/view/5344) · [ACL BEA 2024 fairness AES](https://aclanthology.org/2024.bea-1.18/) · [arXiv:2506.07955](https://arxiv.org/abs/2506.07955) |
| 4 · Thu hẹp | "Với budget nhỏ, human review, pilot 1 buổi–6 tuần — hướng nào?" | **Loại Build platform** (LMS mới, engine chấm riêng). **Loại Buy Gradescope** cho pilot D28 — license/ops nặng, tập trung *sau* nộp hơn *trước* nộp. **Chọn Boost hybrid nhẹ**: rubric Day 28 (có sẵn trong repo) + prompt LLM trả JSON checklist + **cảnh báo mềm** (không chặn cứng) + coach review mẫu 10–20% để calibrate false alarm. Regex tùy chọn cho heading bắt buộc (`## Budget`, `## Exit criteria`) — giảm hallucination. | Ràng buộc từ `00-context.md`; tiền lệ trên |

---

## Phần B — Rút về 2–3 hướng khả thi

Câu hỏi phụ:

- Hướng nào *kế thừa được nhiều nhất* từ người đã làm?
- Hướng nào nghe hay nhưng nhóm **không có nguồn** để tin?

### Trả lời

| Hướng giải khả thi | Ai làm rồi (gần bài mình nhất) | Nguồn  | Hợp ràng buộc `00-context`? |
|---|---|---|---|
| **Boost — LLM + rubric khóa (prompt + JSON checklist)** | Workflow "pre-grader" trước nộp; pilot Colleague AI / FeedbackWriter (formative, có người giám sát) | [Substack pre-grader](https://howtoteachwithai.substack.com/p/stop-being-the-first-person-to-grade) · [arXiv:2506.07955](https://arxiv.org/abs/2506.07955) · [arXiv:2602.16820](https://arxiv.org/abs/2602.16820) | **Có** — budget API nhỏ, không build platform, human review mẫu, formative |
| **Buy — Gradescope / LMS rubric có sẵn** | Gradescope rubric + auto một phần | [Gradescope guides](https://guides.gradescope.com/hc/en-us/articles/22249389005709-Grading-submissions-with-rubrics) | **Không cho pilot D28** — chi phí/license, setup assignment, không gắn trực tiếp flow nộp GitHub worksheet trong buổi |
| **Boost nhẹ + rule — regex heading + LLM cho mục ngữ nghĩa** | CI/lint tài liệu (tương tự pre-commit); kết hợp LLM chỉ cho mục "có baseline chưa", "exit criteria ≥2" | analogy CI; pattern phổ biến trong eng | **Có** — giảm false positive, vẫn không cần Build full app |

**"Đi từ 5 lên" — nhóm kế thừa cụ thể cái gì** (1–2 câu):

```text
Kế thừa rubric/pilot formative đã được chứng minh (pre-grader + Colleague AI/FeedbackWriter): dùng LLM chỉ để map bài nộp → checklist rubric Day 28, không auto-điểm. Thêm lớp rule cho tiêu đề/mục bắt buộc để tránh lỗi AES classic (báo thiếu oan). Coach vẫn chấm chính thức — giống Gradescope nhưng chạy TRƯỚC submit.
```

---

## Phát hiện ban đầu

- Bài này **không phải lợi thế cạnh tranh cốt lõi** — là productivity layer; mặc định Boost/Buy, không Build LMS.
- Người đi trước **không tin auto-score**; pilot của nhóm cũng phải là **cảnh báo + coach chốt**, không "AI cho điểm".
- Thất bại hay gặp: **hallucinate thiếu mục** và **chặn submit cứng** → adoption chết.

## Câu hỏi mở (mang sang bước chốt)

- Cảnh báo mềm hay chặn cứng khi thiếu mục bắt buộc? (Problem Framing mục 8)
- Ngưỡng false positive chấp nhận được để coach không mất niềm tin? 

---

## Tổng kiểm tra trước khi sang `2-FINAL-solution.md`

| Hạng mục | Xong? |
|---|---|
| Gọi được dạng bài trong 1 câu, không còn chữ domain | ✓ |
| Đủ 4 tầng deep research, tầng nào cũng có kết quả | ✓ |
| Mỗi kết quả có nguồn, hoặc đánh dấu nếu là giả định | ✓ |
| Rút về 2–3 hướng + nói được "đi từ 5 lên" cái gì | ✓ |

Hàng nào chưa xong → quay lại Phần A, đừng sang bước chốt vội.

Sau bước này, mở `2-FINAL-solution.md` — chốt Build/Buy/Boost/Partner + data & ai review + bản vẽ trực quan (đây là bản nộp của phase này).


