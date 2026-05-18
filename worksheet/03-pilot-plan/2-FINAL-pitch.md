---
artifact: 8 — 5-slide Pitch + AI Support Log (bản nộp cuối lab)
bai-tap: Pilot Plan — dồn thành pitch, sẵn sàng phản biện
phase: Double Diamond vòng 2 · ◆ output (bản nộp cuối + present)
time: ~5 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 1-pilot-plan.md + toàn bộ 01-frame + 02-solution · templates/5-slide-pitch.md
nop-cuoi: Có — bản nộp cuối lab (Part E · 5-slide Pitch + AI Support Log)
---

# 2 — FINAL: 5-slide Pitch + AI Support Log

Mục tiêu: dồn cả A3 Working Canvas thành 5 slide pitch (5 phút), chuẩn bị trả lời 3 câu phản biện, và ghi AI Support Log. Đây là bản nộp cuối cùng của lab.

Lý do làm bước này: nguyên tắc *demo đơn giản + lập luận chặt > demo đẹp + lập luận yếu*. Slide đẹp mà không trả lời được "số này lấy ở đâu" thì hỏng. Pitch không phải kể chuyện — là đưa evidence để stakeholder ra được một quyết định.

Quy tắc: **slide cuối phải là một lời xin rõ ràng** (xin gì · đổi lại hứa gì). Không có lời xin = stakeholder không biết approve cái gì.

## Quy trình 5 phút

```text
3 phút  — Dồn 5 slide (mỗi slide 1 thông điệp)
1 phút  — Chuẩn bị 3 câu phản biện
1 phút  — AI Support Log
```

---

## Phần A — 5 slide (mỗi slide 1 thông điệp)

Kéo nguyên liệu từ các file đã làm, đừng viết mới. Khung đầy đủ: `templates/5-slide-pitch.md`.

| # | Slide | Lấy từ | Nội dung 1–2 gạch đầu dòng | Ai nói |
|---|---|---|---|---|
| 1 | Problem & user | `01-frame/3-FINAL` | **Ai đau:** Lab coach + học viên lúc nộp bài. **Đau gì:** 🧮 **~30%** bài **R1-RUBRIC** (thiếu rubric vòng 1) → coach 🧮 **~4h/đợt** cho feedback “thiếu Budget/Exit…”. **Vì sao giờ:** ~500 HV, coach không scale kịp “đọc lỗi vặt”. | Chu Thị Ngọc Huyền |
| 2 | Breakdown & Quick Win | `01-frame/1`, `2` | **Công cụ lớn:** AI Lab Copilot (giải đề, hint, debug, tiền kiểm, log coach…). **Quick Win:** **Tiền kiểm rubric trước Submit** — điểm cao nhất, rủi ro thấp, không sinh đáp án. **Không chọn trước:** debug/hint bot (red flag: làm hộ + khó phân tầng gợi ý). | Nguyễn Thị Tuyết |
| 3 | Solution + bản vẽ trực quan | `02-solution/2-FINAL` | **Boost:** rule heading + LLM → JSON checklist + trích dẫn/`MISSING`. **Chiếu artifact trong pitch:** mở `worksheet/02-solution/2-FINAL-solution.md` — **Phần C** (flow TRƯỚC/SAU + 3 màn hình ASCII + pipeline B1→B2). **Người:** ★ coach sau Màn 2; instructor quyết policy mềm/cứng. | Nguyễn Thị Tuyết |
| 4 | AI Pilot Plan | `03-pilot-plan/1` | **D28 + 3 tuần:** dry-run 5 bài → **Phase 1** golden **15** + **20 nhóm NV** → cổng **FP% <15%** (edge **0 cờ** xem `1-pilot-plan`) → **Phase 2** tối đa **100 lượt** kiểm tra nhóm. **Mặc định cảnh báo mềm**; chặn cứng chỉ khi **instructor** bật. **Người:** nhóm script+prompt; coach review cờ; **instructor + lead coach** approve/dừng. **Budget tách:** API 🧮 ~$5–25 (kèm buffer) + form $0 + **giờ coach** đã khai. | Hoàng Hiệp |
| 5 | Metric · exit criteria · **lời xin** | `03-pilot-plan/1` | **Đo:** FP% (mẫu sương/mục), **R1-RUBRIC rate** (định nghĩa trong `1-pilot-plan`), adoption log + khảo sát ngắn. **Dừng:** **Cảnh báo** (**10% ≤ FP < 15%**, adoption 40–59%, ticket nhiễu cờ) vs **Nghiêm trọng** (FP ≥15% sau 2 vòng chỉnh có bằng; red flag; privacy). **LỜI XIN (tách 3 ý):** **Xin** phê duyệt pilot + **~3–4h coach tuần 1** + **golden 15** + **20 nhóm NV** + **~$5–25 API** 🧮 + **cap 100 lượt** Phase 2. **Hứa** giao báo cáo tuần 1 & tuần 3 + quyết định mở rộng/dừng trung thực. **Rủi ro** thấp nếu giữ formative + người review. | Hoàng Hiệp |

## Phần A2 — Bản tự chấm 3 vòng (để reviewer / Claude đọc nhanh)

| Vòng | Trọng tâm | Kết quả đã ghi nhận |
|---|---|---|
| **1** | Gate 5 “đo được”: **FP%**, **R1-RUBRIC**, edge **0 cờ**; sửa **scope/cap**; cổng D28 | `1-pilot-plan.md` mục 3–8 |
| **2** | Vận hành: **cảnh báo vs cổng**; adoption/khảo sát rõ nghĩa; **budget ↔ cap 100 lượt**; **mặc định cảnh báo mềm** | Exit + budget + Phase 2 gate |
| **3** | Rủi ro người: **điểm nghẽn coach** + plan B; **đăng ký 🧮**; **cam kết giao** | `1-pilot-plan` Tự phản biện + bảng 🧮; pitch slide 5 |

## Phần B — Chuẩn bị 3 câu phản biện

Business owner/instructor sẽ hỏi mỗi nhóm 1–2 câu. Viết sẵn câu trả lời:

1. *"Số liệu / giả định này lấy ở đâu?"* → **30% R1-RUBRIC** và **~4 giờ coach/đợt** là **🧮** từ Problem Framing (150 nhóm × 30% × 5 phút) — **chưa phải sổ LMS**. **Tuần 1** đo **R1-RUBRIC** thực trên log (nhãn thống nhất) để thay 🧮. **FP%** = **(# mục oan) / (# mục AI báo thiếu)** trên golden — nếu **0 cờ thiếu** thì **không chia cho 0**: chuyển sang **spot-check 100%** golden + 10 bài NV (đã ghi trong `1-pilot-plan`).

2. *"Nếu giả định quan trọng nhất của bạn sai thì sao?"* → Nếu **30% R1-RUBRIC** sai → **đo tuần 1** và **baseline mới** làm chuẩn. Với **mục tiêu giảm 20%**, nhóm **chốt 1 công thức duy nhất** (tuyệt đối vs tương đối) **bằng email instructor trước Phase 2** — không đổi công thức giữa chừng. Nếu **coach không đủ thời gian** golden → **plan B:** golden **10** bài hoặc **kéo Phase 1** + giữ cổng FP.

3. *"Tình huống nào sẽ khiến bạn dừng pilot?"* → **(1)** **FP% ≥15%** sau **2 vòng** chỉnh **có diff prompt + kết quả golden**; **(2)** bằng chứng **AI làm hộ** / **≥2 báo cáo** hiểu nhầm checklist = điểm chính thức (coach xác minh); **(3)** **privacy** sai cam kết. **Instructor** dừng chương trình; **lead coach** dừng vận hành khẩn khi (3) — chi tiết bảng trong `1-pilot-plan.md`.

## Phần C — AI Support Log

| Câu hỏi | Trả lời |
|---|---|
| AI giúp được gì trong lab này? | Gợi ý **cấu trúc** 4 tầng deep research, **từ khóa** tiền lệ, **nháp** metric/exit/pitch — và **3 vòng** nhóm tự đọc–chấm–sửa phase 03 trước khi đóng bài. |
| AI đưa output nào nghe hợp lý nhưng nhóm phải sửa? | **Scope “50/tuần”** lệch **cap API**; **cảnh báo vs cổng <15%** chồng nhau; thiếu **định nghĩa mẫu số FP** khi AI không cờ — đã sửa trong `1-pilot-plan`. Các con số 🧮 giữ nguyên nhưng **gắn công thức + người đo**. |
| Phần nào nhóm tự lập luận, KHÔNG copy AI? | **Chọn Quick Win**, **Boost vs Buy**, **R1-RUBRIC + FP%**, **ai được dừng**, **mặc định cảnh báo mềm**, **cam kết giao**, **bảng A2 3 vòng** — và **phân vai pitch** theo `group-members.md`. |

---

## Phần D — Checklist reviewer nhanh (Gate 5 / Claude)

- [ ] **Xin / hứa / đo / dừng** đều có **chủ thể** (ai đo, ai dừng) — không chỉ “nhóm”.
- [ ] **Số 🧮** có **bảng đăng ký** + **đường thay bằng đo thực** (tuần 1).
- [ ] **Metric** có **mẫu số** (FP% mẫu sương) + **định nghĩa vận hành** (R1-RUBRIC) + **edge** (0 cờ).
- [ ] **Exit** có **≥2 mức** và **không mâu thuẫn** với cổng Phase (cảnh báo nằm *dưới* ngưỡng nghiêm trọng).
- [ ] **Slide 5** tách **Xin / Hứa / Rủi ro**; **slide 3** trỏ **đúng file artifact**.

---

## Tổng kiểm tra trước khi nộp

| Hạng mục | Xong? |
|---|---|
| 5 slide, mỗi slide 1 thông điệp, đã phân ai nói slide nào | ✓ |
| Slide 5 có lời xin rõ ràng (xin gì · hứa gì) | ✓ |
| Có câu trả lời sẵn cho cả 3 câu phản biện | ✓ |
| AI Support Log điền đủ 3 dòng | ✓ |
| Tất cả file worksheet/ đã commit + push, link dán vào Discord | / *(nhóm tự làm khi nộp)* |

Đây là file cuối. Pitch 5 phút + nhận phản biện theo bảng 5 Gate (`templates/rubric-gate-sheet.md`).

*Liên quan: handbook §A9 · `templates/5-slide-pitch.md` · `templates/ai-support-log.md`*
