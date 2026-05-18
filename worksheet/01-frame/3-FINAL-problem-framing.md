---
artifact: 4 — Problem Framing (bản nộp phase Frame)
bai-tap: Frame — đóng khung vấn đề thật
phase: Double Diamond vòng 1 · ◆ output (chốt — owner xác nhận)
time: ~13 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 2-quick-win.md · prompts/03-problem-framing-challenge.md
nop-cuoi: Có — đây là bản nộp của phase Frame (Part A · A3 Working Canvas mục Problem Framing)
---

# 3 — FINAL: Problem Framing

Mục tiêu: đóng khung Quick Win đã chọn cho thật cụ thể. Đây **không phải** bản đề xuất giải pháp — là tài liệu trả lời đúng 1 câu: *"nhóm đã hiểu đúng vấn đề chưa?"*. Đây là output chốt của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 1, và là một mục trong A3 Working Canvas nộp cuối buổi.

Lý do làm bước này: một AI Pilot Plan cho vấn đề SAI — dù viết hay — vẫn sai. Đa số nhóm trượt Gate 3 vì khung chung chung ("học viên cần học tốt hơn", "coach quá tải") — câu đó không đo được, không ai chịu trách nhiệm, không biết khi nào thành công.

Quy tắc: **pain phải có số.** "Nhiều người phàn nàn" không phải evidence. "200 câu hỏi/tuần × 20 phút = 67 giờ/tuần" mới là evidence. Trong lab dùng số giả định cũng được, nhưng phải nói rõ số đến từ đâu.

## Quy trình 13 phút

```text
9 phút  — Điền 9 mục Problem Framing
3 phút  — Tự phản biện
1 phút  — Chốt: owner (giả định) có xác nhận đúng vấn đề không
```

---

## 9 mục Problem Framing

Câu hỏi phụ (tự trả lời trước khi điền):

- Một người ngoài đọc khung này có biết CHÍNH XÁC ai đau, đau cái gì không?
- Nếu KHÔNG có baseline thì nhóm đo "tốt hơn" bằng cách nào?
- Mục Open Questions trống = nguy hiểm (chưa nghĩ đủ). Nhóm còn chưa biết gì?

### Trả lời

1. **Original Ask** (stakeholder nói gì, nguyên văn): "AI hỗ trợ học viên làm lab/code/bài tập: gợi ý bước tiếp theo, debug, review trước khi nộp — nhưng không làm hộ bài."
2. **Reframed problem** (vấn đề thật sau khi tách): Học viên nộp bài lab D28 thường thiếu các tiêu chí cơ bản trong rubric (chỉ số, ngân sách, tiêu chí dừng), khiến coach mất thời gian trả lại bài và chấm lại. Cần một công cụ AI tiền kiểm tra tự động rubric trước khi submit để giảm tải cho coach.
3. **Current workflow** (hiện tại đang xử lý thế nào, kể cả "không ai làm gì"): Học viên làm xong -> Nộp bài -> Coach đọc, phát hiện thiếu mục -> Trả bài (hoặc trừ điểm) -> Học viên sửa nộp lại -> Coach chấm lại từ đầu.
4. **Pain evidence — bằng SỐ** (ai đau · đau ở khoảnh khắc nào trong việc · tần suất · quy mô; số giả định ghi rõ nguồn giả định):

```text
- Tần suất/Quy mô: 150 nhóm học viên nộp bài mỗi ngày lab. Khoảng 30% bài nộp (45 nhóm) bị thiếu thông tin cơ bản ngay từ vòng 1.
- Thời gian lãng phí: Mỗi bài lỗi vặt coach tốn ~5 phút đọc và viết feedback trả lại. Tổng cộng mất 225 phút (gần 4 tiếng) chỉ để nói học viên "bạn thiếu mục ngân sách".
- Baseline: 30% bài bị trả lại ở vòng 1 do lỗi format/thiếu rubric.
```

5. **Affected people** (ai dùng · ai quyết · ai là người review/expert): Người dùng: Học viên (lúc nộp). Người quyết: Instructor. Người review kết quả: Lab Coach.
6. **Constraints** (từ `00-context.md`: privacy / human review / citation / budget / formative / adoption): Chấm formative (mang tính góp ý, chưa phải điểm cuối). Cần human review (coach vẫn là người chốt điểm). Budget nhỏ (dùng LLM prompt cơ bản check theo ý).
7. **Quick Win đã chọn** (1 dòng, lấy từ file `2`): AI tiền kiểm bài nộp theo rubric trước khi submit.
8. **Open questions** (còn chưa biết gì — không được để trống): AI nên trả lại thông báo chặn không cho nộp, hay chỉ cảnh báo nhưng vẫn cho nộp? Hạn chế việc AI ảo giác báo thiếu mục dù học viên đã viết rồi thì thế nào?
9. **Validation** (đóng vai owner: *"đúng, đây là vấn đề đáng giải"* — Có / Chưa, vì sao):

```text
Có. Vấn đề này rất thực tế, rất "đau" với người vận hành (coach). Nó có số liệu đo lường rõ ràng (tiết kiệm 4 tiếng/lần nộp bài) và không can thiệp vào quá trình học lõi của học viên, đáp ứng đủ ràng buộc "không làm thay".
```

---

## Tự phản biện

- Khung này còn câu chung chung kiểu "cần học tốt hơn" không?
- 3 câu sẽ bị hỏi: *số/giả định lấy ở đâu · giả định chính sai thì sao · tình huống nào khiến dừng.* Trả lời thử 1 câu.

---

## Tổng kiểm tra trước khi sang `02-solution/`

| Hạng mục | Xong? |
|---|---|
| Chỉ rõ 1 nhóm người + 1 khoảnh khắc cụ thể (không "user nói chung") | / |
| Pain có số (hoặc kế hoạch lấy số), nói rõ số từ đâu | / |
| Có baseline (hoặc cách đo baseline) + ≥1 chỉ số có ngưỡng | / |
| Mục 9: owner (giả định) xác nhận đúng vấn đề = qua cổng phase Frame | / |

⚑ Coach kiểm tra ở Mốc 2: *"Ai đau? Baseline là gì? Không có baseline thì đo thế nào?"*

Owner chưa xác nhận → quay lại file `1`/`2`, đừng sang Solution. Owner xác nhận → mở `../02-solution/1-find-existing-solutions.md`.

*Liên quan: handbook §A4 · `prompts/03-problem-framing-challenge.md`*
