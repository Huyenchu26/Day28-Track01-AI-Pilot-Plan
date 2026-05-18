---
artifact: 3 — Quick Win Selection
bai-tap: Frame — chọn lát cắt làm trước
phase: Double Diamond vòng 1 · ◆ siết (hội tụ về 1 lựa chọn)
time: ~10 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 1-intake-breakdown.md · prompts/02-quick-win-challenge.md
nop-cuoi: Không — file trung gian (bản chốt phase này ở 3-FINAL-problem-framing.md)
---

# 2 — Quick Win: chọn lát cắt làm trước

Mục tiêu: từ 5–8 use case ở file `1`, chấm điểm nhanh và chốt **1 Quick Win** để pilot đầu tiên — kèm lý do chọn và lý do *không* chọn các phần khác. Đây là nửa "siết lại" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 1.

Lý do làm bước này: đây là quyết định quan trọng nhất của phase Frame. Quick Win **không phải** phần dễ nhất hay nghe hay nhất — là phần *chứng minh được giá trị nhanh và có người ủng hộ*. Chọn sai → pilot fail → mất uy tín → khó xin pilot tiếp. Nhóm phải chọn được *và bảo vệ được bằng lý do*, không bằng cảm tính.

Quy tắc: **điểm số chỉ là gợi ý, không phải đáp án.** Đừng để con số quyết thay nhóm — nó chỉ giúp so sánh.

## Bước 0 — Lấy 4–6 use case mạnh nhất từ file `1` (1 phút)

## Quy trình 10 phút

```text
1 phút  — Bước 0: chọn 4–6 ứng viên
5 phút  — Phần A: chấm điểm 4 trục
3 phút  — Phần B: 1 lý do nên / 1 lý do không cho top 2
1 phút  — Phần C: chốt + ai ủng hộ + cái KHÔNG chọn
```

---

## Phần A — Chấm điểm 4 trục (1–5 mỗi trục)

Câu hỏi phụ (tự trả lời):

- "Risk" ở đây là *sai thì mất gì* — chọn đúng việc chính của user (task centrality) thì sai cũng đỡ đau; chọn việc lớn nhất thì sai rất đắt. Use case nào risk thấp thật?
- Use case nào có sẵn data + có người trong AI20k thật sự muốn dùng?

| Use case | Impact | Feasibility | Evidence nhanh | Risk (cao = an toàn) | Tổng |
|---|:--:|:--:|:--:|:--:|:--:|
| 1. AI giải thích đề lab | 3 | 5 | 4 | 4 | 16 |
| 2. AI hint bot gợi ý gỡ bí | 4 | 3 | 3 | 2 | 12 |
| 3. AI trợ lý debug code | 5 | 4 | 4 | 3 | 16 |
| 4. AI tiền kiểm bài nộp theo rubric | 4 | 5 | 5 | 4 | 18 |

(Thang điểm chi tiết: `templates/quick-win-scoring.md`.)

## Phần B — 1 lý do nên / 1 lý do không, cho top 2

**Ứng viên A — AI tiền kiểm bài nộp theo rubric**

```text
Nên chọn vì: Rất dễ làm ngay (dựa trên rubric), mang lại giá trị tức thời cho cả coach và học viên (giảm việc lặp lại). An toàn vì không can thiệp nội dung làm bài.
Không nên vì: Không giúp học viên trong quá trình "làm bài", chỉ giúp ở bước "nộp bài".
```

**Ứng viên B — AI trợ lý debug code**

```text
Nên chọn vì: Impact cao nhất với học viên, giải quyết đúng chỗ kẹt đau nhất của họ khi làm bài kỹ thuật.
Không nên vì: Rủi ro cao (dễ sinh code giải hộ bài), khó kiểm soát prompt để AI chỉ "gợi ý" mà không lộ đáp án.
```

## Phần C — Chốt Quick Win

- **Quick Win nhóm chọn**: AI tiền kiểm bài nộp theo rubric trước khi submit.
- **Vì sao chọn cái này trước** (2–4 câu, bám điểm + impact + evidence nhanh): Điểm tổng cao nhất (18). Có thể triển khai ngay vì dựa vào Rubric có sẵn. Rủi ro thấp (an toàn cao) vì không sinh đáp án, chỉ nhắc học viên các mục thiếu, giúp tiết kiệm hàng chục giờ review lỗi cơ bản cho coach.
- **Ai trong AI20k sẽ ủng hộ pilot này** (và vì sao họ care — "có người ủng hộ" thường quan trọng hơn "impact cao"): Lab Coach và Instructor. Họ rất mệt mỏi khi phải trả lại bài vì thiếu ngân sách, thiếu chỉ số đo lường, làm mất thời gian chấm lỗi vặt.
- **Nhóm KHÔNG chọn gì + vì sao** (≥2 use case bị loại): 1. Trợ lý debug code (vì rủi ro AI làm hộ bài cao, cần thời gian tinh chỉnh prompt lâu).  2. Hint bot gợi ý (khó đánh giá mức độ gợi ý phù hợp cho 500 học viên khác nhau).

---

## Phát hiện ban đầu

- Đôi khi Quick Win không phải là phần ngầu nhất (như bot sửa code), mà là phần giảm tải nhiều nhất cho hệ thống vận hành với rủi ro thấp nhất.

## Câu hỏi mở (mang sang Problem Framing)

- Nếu bài nộp bị AI đánh dấu là thiếu, học viên có bị bắt buộc phải sửa mới được nộp không? Hay chỉ là cảnh báo?

---

## Tổng kiểm tra trước khi sang `3-FINAL-problem-framing.md`

| Hạng mục | Xong? |
|---|---|
| Có bảng chấm 4 trục cho ≥4 use case | / |
| Chốt 1 Quick Win, lý do bám số/impact (không "nghe hay") | / |
| Nêu rõ ai ủng hộ pilot này | / |
| Ghi rõ ≥2 phần KHÔNG chọn + lý do | / |

⚑ Đây là phần coach kiểm tra ở Mốc 1: *"Vì sao không làm full tool? Vì sao chọn lát cắt này trước?"*

Sau bước này, mở `3-FINAL-problem-framing.md` — đóng khung vấn đề thật (bản nộp của phase Frame).

*Liên quan: handbook §A3 · `templates/quick-win-scoring.md` · `prompts/02-quick-win-challenge.md`*
