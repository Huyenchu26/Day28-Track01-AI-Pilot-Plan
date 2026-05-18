---
artifact: 7 — AI Pilot Plan core
bai-tap: Pilot Plan — cam kết hai chiều: xin – hứa – đo – dừng
phase: Double Diamond vòng 2 · ◇ giãn → ◆ siết (liệt kê hết rồi chốt gọn)
time: ~10 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 02-solution/2-FINAL-solution.md · 00-context.md · prompts/06-pilot-plan-challenge.md
nop-cuoi: Không — file trung gian (bản nộp ở 2-FINAL-pitch.md)
---

# 1 — AI Pilot Plan core

Mục tiêu: viết phần kế hoạch xin pilot — scope, người, data, budget, timeline, metric, exit criteria, adoption, lời hứa, lời xin. Bước này giãn ra (liệt kê hết những thứ cần) rồi siết lại (chốt bản gọn đủ để stakeholder quyết).

Lý do làm bước này: đây là thứ stakeholder dùng để **quyết approve hay dừng**. AI Pilot Plan **không phải proposal xin tiền** — là *cam kết hai chiều*: nhóm xin nguồn lực, đổi lại hứa giao evidence + chấp nhận dừng nếu metric fail. Demo đẹp mà không nói được "xin gì, hứa gì, đo gì, dừng khi nào" → trượt Gate 5.

Quy tắc: **budget tách từng hạng mục, không gộp 1 cục; không có mục "miscellaneous".** Exit criteria phải có người có quyền thực thi, không chỉ trên giấy.

## Quy trình 10 phút

```text
6 phút  — Điền 10 mục core (kéo nguyên liệu từ 00 + 01-frame + 02-solution)
3 phút  — Phần exit criteria + adoption (chỗ nhóm hay bỏ quên)
1 phút  — Tự phản biện
```

---

## 10 mục core

Câu hỏi phụ (tự trả lời):

- Nếu tóm vấn đề không gọn trong 1 câu → nhóm chưa hiểu vấn đề.
- Exit criteria của nhóm có ai DÁM thực thi khi sếp vẫn thích pilot không?
- Adoption: ai dùng đầu tiên — không phải "cả khóa ~500 người"?

### Trả lời

1. **Tóm vấn đề** (1 câu, từ Problem Framing): Học viên nộp bài lab/worksheet thường thiếu các mục rubric cơ bản (ngân sách, metric, exit criteria…), khiến coach mất nhiều giờ trả bài vòng 1 cho lỗi lặp lại thay vì chấm nội dung.

2. **Cách làm + lý do** (từ 02-solution, 1 câu): **Boost** — hybrid **rule (heading/cấu trúc) + LLM** map bài markdown nộp vào **checklist rubric Day 28**, trả JSON + trích dẫn hoặc `MISSING`; **formative**, cảnh báo mặc định **mềm** (không thay điểm chính thức). Không Build platform (không phải differentiator, vượt budget nhóm); không Buy Gradescope làm trụ cột pilot (license/onboarding + flow tối ưu *sau* nộp, không khớp nộp worksheet GitHub trong buổi).

3. **Scope pilot**: **Ai:** học viên **track Product** (bài có rubric Day 28 — worksheet / pilot plan) + **lab coach** hỗ trợ + **instructor** quyết policy. **Quy mô:** **Ngày D28** — dry-run **5 bài** + demo (không tính vào golden). **Phase 1 (tuần 1):** **golden 15** (coach gắn nhãn trước hoặc song song ngày 1–2) + **20 nhóm tình nguyện** chạy tiền kiểm trước nộp. **Phase 2 (tuần 2–3):** chỉ mở nếu qua cổng Phase 1 — **tối đa 100 lượt kiểm tra nhóm** tích lũy trong 2 tuần (≈50 nhóm/tuần × 2 tuần **hoặc** ít hơn nếu adoption thấp), **hard cap** để khống chế chi phí API và tải coach. **Thời gian tổng:** **3 tuần** kể từ ngày bắt đầu Phase 1 (D28 có thể trùng ngày 0 hoặc ngay trước tuần 1 — nhóm thống nhất 1 mốc ngày trên lịch khóa).

4. **Người**: **Nhóm làm:** Chu Thị Ngọc Huyền, Nguyễn Thị Tuyết, Hoàng Hiệp — script + prompt + form/link “Kiểm tra rubric”. **Review output rủi ro cao:** **Lab coach** — 100% bài bị cờ ❌/⚠️ nghiêm trọng lần đầu; **spot-check 20%** bài AI báo ✅. **Quyết approve / đổi policy (mềm vs cứng) / dừng pilot:** **Instructor** (chương trình) và **Lead lab coach** (vận hành hằng ngày) — thỏa thuận trước pilot: instructor có quyền **tắt chặn cứng** hoặc **dừng toàn bộ** nếu vi phạm red flag hoặc metric nghiêm trọng. **Chính sách mặc định (gắn open question Problem Framing):** pilot chạy **cảnh báo mềm** (luôn cho nộp / luôn cho submit GitHub); **chặn cứng** (nếu có) chỉ bật khi **instructor** đồng ý bằng văn bản — tránh adoption chết vì AI “hallucinate thiếu mục”.

5. **Data**: **Rubric Day 28** từ `templates/` + checklist 7 mục A3 (public). **Bài nộp:** 10–20 bài mẫu 🧮 (ẩn danh) để dry-run; pilot thật: **markdown** do học viên **tự paste/upload** (khuyến nghị **opt-in**, không scrape Discord DM). **Baseline tỷ lệ trả vòng 1 vì thiếu rubric (R1-RUBRIC):** 🧮 **30%** (Problem Framing) — **tuần 1 pilot** coach đếm thực tế trên log nhãn **R1-RUBRIC** để thay 🧮 bằng số đo được. **Privacy / citation:** không train thêm model; không lưu submission lâu dài — chỉ **log cờ + hash/ngắn** nếu cần audit; mỗi mục checklist AI phải **trích đoạn** từ bài hoặc `MISSING (no cited span)` — không bịa trích dẫn; thiếu nguồn khóa học thì **“không biết”** theo `00-context`.

6. **Budget** (tách hạng mục):
   - **API LLM** (Claude/GPT, prompt ngắn + JSON): 🧮 **~$5–25** toàn pilot (ước theo **≤100 lượt** kiểm tra × **≤2** lượt gọi/lượt × model rẻ; đã gồm biến động nhỏ); theo dõi thực tế trên dashboard vendor.
   - **Công cụ zero:** Google Form / link nộp static page — **$0**.
   - **Thời gian người (chi phí cơ hội, phải khai):** **Coach** ~**3–4 giờ** tuần 1 (golden 15 + calibrate + đọc cờ); **~1–2 giờ/tuần** tuần 2–3 (spot-check + họp 30′ cổng); **Nhóm 3** ~**6–8 giờ** tổng (build script nhỏ, prompt, tài liệu hướng dẫn 1 trang).
   - **Hạng mục ẩn:** **1 buổi** đồng bộ instructor + coach (policy mềm/cứng, disclaimer học viên); **buffer** ~**$10** nếu spike token; **không** hạng mục “misc”.

7. **Timeline + cổng giữa phase**:
   - **Ngày D28 (≤0.5 ngày):** Dry-run trên **5 bài** + demo flow — **cổng:** instructor + coach **đồng ý** checklist **khớp** các lỗi họ thường trả ở vòng 1 (không thiếu mục quan trọng, không thừa mục gây nhiễu).
   - **Phase 1 — Tuần 1:** Hoàn **golden 15** + chạy **20 nhóm** tình nguyện — **cổng:** trên golden, **FP% < 15%** theo định nghĩa mục 8 (nếu **0 cờ thiếu** từ AI trên golden → dùng **spot-check 100%** golden + 10 bài NV như mục 8); nếu không đạt → chỉnh prompt/rule, **không** mở Phase 2.
   - **Phase 2 — Tuần 2–3:** Mở trong giới hạn **100 lượt kiểm tra nhóm** — **cổng:** **≥20%** giảm tỷ lệ **trả bài vòng 1 vì thiếu rubric** so **baseline** (định nghĩa dưới); baseline dùng **số đo tuần 1** nếu có, nếu không dùng 🧮 **30%** đã thống nhất trong Problem Framing. **Đồng thời** **≥60%** nhóm trong cohort có **≥1 lượt** “Kiểm tra rubric” trước nộp (log) **và** trong các nhóm trả lời khảo sát ngắn sau tuần 1, tỷ lệ chọn **“Không hữu ích”** ≤ **50%** (không cho phép đa số “không”).

8. **Metrics** (SMART + baseline + ngưỡng + ai đo):

| Metric | Đo bằng gì · ai đo | Baseline | Ngưỡng đạt |
|---|---|---|---|
| False positive (AI báo “thiếu” oan) | Trên **golden 15**: **FP% = (# mục AI báo “thiếu” mà coach chấm là oan) / (# mục AI báo “thiếu” tổng cộng)**; **Lead coach** đo, có bảng tally. **Edge:** nếu mẫu có **0** cờ “thiếu” từ AI → ghi **N/A tuần đó**, bắt buộc **spot-check 100%** golden + 10 bài NV để vẫn có bằng chứng chất lượng. | Chưa có → đo cuối tuần 1 | **< 15%** trên golden (khi mẫu cờ > 0) 🧮 |
| Giảm trả bài vòng 1 (thiếu rubric) | **Định nghĩa:** “Trả vòng 1 vì thiếu rubric” = coach gắn nhãn **R1-RUBRIC** trong log (không tính trả vì đạo văn/sai nội dung). **Rate** = (# bài R1-RUBRIC) / (# bài nộp trong cohort cùng kỳ). **Lead coach** đo. | 🧮 **30%** (Problem Framing) **hoặc** baseline **tuần 1** đo trước Phase 2 | **Giảm ≥ 20 điểm phần trăm tuyệt đối** so baseline (vd 30% → ≤10%) **hoặc** giảm **≥20% tương đối** nếu baseline thấp (vd 12% → ≤9.6%) — **chốt 1 công thức** trước Phase 2 trong 1 dòng email instructor |
| Adoption (trong cohort pilot) | **% nhóm** có **≥1** lượt “Kiểm tra rubric” trước nộp (log form/script); khảo sát **1 câu** sau tuần 1 (thang hữu ích / trung lập / không) | 0% (trước pilot) | **≥60%** nhóm cohort có log kiểm tra **và** tỷ lệ **“Không hữu ích”** trong nhóm trả lời khảo sát ≤ **50%** |

**Leading indicator** (1–2 tuần đầu biết hướng): sau **10 bài NV đầu** Phase 1 — nếu **≥3** bài có **≥2 mục oan** (theo coach) → **họp khẩn** 30′ chỉnh prompt/rule **trong 48h**, không chờ hết tuần.

9. **Exit criteria** (định trước, ≥2 mức):

| Mức | Điều kiện | Hành động | Ai có quyền dừng / quyết |
|---|---|---|---|
| **Cảnh báo** | **(a)** FP golden **10% ≤ FP < 15%** (khi mẫu cờ > 0) **sau tuần 1** **hoặc** **(b)** adoption log **40–59%** nhóm cohort **hoặc** **(c)** coach ghi nhận **≥3** ticket “nhiễu cờ” có ví dụ bài trong **5 ngày** | Tinh chỉnh prompt/rule trong **48h**; **bắt buộc** disclaimer UI (“không phải điểm chính thức”); **giảm** hard cap lượt kiểm tra Phase 2 (vd 100 → 50) | **Lead lab coach** đề xuất — **instructor phê duyệt** thay đổi policy / cap |
| **Nghiêm trọng** | **(i)** FP **≥15%** sau **2 vòng** chỉnh có tài liệu (prompt diff + test golden) **hoặc** **(ii)** bằng chứng **AI sinh nội dung làm hộ bài** (đoạn dài không trích từ bài nộp + coach xác nhận) **hoặc** học viên **hiểu nhầm checklist = điểm chính thức** (≥2 báo cáo độc lập + coach xác minh) **hoặc** **(iii)** **privacy** (lưu submission trái cam kết / lộ PII) | **Dừng pilot**; tắt link công khai; **rollback** quy trình nộp cũ; **báo cáo 1 trang** nguyên nhân + học hỏi | **Instructor** quyết **dừng chương trình**; **lead lab coach** quyết **dừng vận hành** ngay khi (iii) hoặc khi instructor ủy quyền khẩn |

*Liên hệ 2 Red Flag ở `00-context.md`:* (1) **Exit nghiêm trọng (ii)** — nếu checklist khuyến khích copy-paste hoặc sinh “đáp án mẫu” → dừng; formative + trích dẫn/`MISSING` + không chấm điểm là thiết kế chống. (2) **Hint vs đáp án** — pilot này **không** làm hint bot; nếu mở rộng sau này phải là **track riêng** + rubric ngôn ngữ gợi ý; exit nếu lẫn sang hint mà không có khung.

10. **Adoption** (tool không ai dùng = $0): **Người dùng đầu tiên:** **20 nhóm tình nguyện** Product Day 28 (công bố trong Discord #lab + link pinned). **Workflow đổi:** trước “Submit” → thêm bước **“Kiểm tra rubric”** (30–60 giây); coach vẫn chấm chính thức. **Train/support:** **1 trang** hướng dẫn + **30 giây** demo trong buổi live; coach trả lời FAQ tuần 1. **Nếu không ai dùng:** coi là **fail adoption** — kích hoạt mức **Cảnh báo**, họp 15′ tìm ma sát (link khó thấy? thời gian?); sau 1 tuần vẫn **<30%** dùng → **không mở** Phase 2, báo cáo “dừng mở rộng” dù chất lượng AI tốt.

### Cam kết giao (hứa) — để khớp Gate 5 (“hứa gì?”)

- **Hứa giao bằng chứng:** cuối tuần 1 — sheet golden (FP%, tally), log adoption tuần 1, 1 trang “thay đổi prompt/rule”; cuối tuần 3 — báo cáo **R1-RUBRIC rate** trước/sau + khảo sát ngắn + quyết định **mở rộng / dừng / đổi vendor API**.
- **Hứa trung thực:** nếu metric nói **nên dừng**, nhóm **không** spin kết quả; slide 5 pitch nêu rõ điều này.
- **Hứa an toàn học tập:** không dùng output AI làm **điểm**; mọi cờ chỉ là **formative**; vi phạm → kích hoạt exit nghiêm trọng.

---

## Tự phản biện

- **Budget thiếu hạng mục ẩn nào không?** Đã tính **đồng bộ stakeholder**, **buffer API**, **thời gian coach**. Chưa tính **legal review** — **giả định** không cần ngoài policy khóa; nếu trường yêu cầu DPA → escalate instructor (rủi ro thấp vì không lưu PII thêm ngoài LMS hiện có).

- **Exit criteria đủ mạnh để THẬT SỰ dừng?** Có **hai vai** (instructor + lead coach) được ghi danh; **điều kiện số** (15% FP, red flag) tránh “dừng trên giấy”. Rủi ro còn lại: áp lực chính trị “đẹp trên slide” — giảm bằng **cam kết báo cáo trung thực** trong pitch.

- **Điểm nghẽn vận hành (để reviewer hỏi):** pilot phụ thuộc **thời gian coach** cho golden 15 — nếu coach overload, kích hoạt **plan B** trong Q&A file pitch (thu 10 bài / kéo Phase 1).

- **Giả định quan trọng nhất sai → plan gì?** Nếu **baseline 30%** sai nhiều → **đo lại tuần 1** và **đặt lại ngưỡng giảm** theo **đúng 1 công thức đã email** (tuyệt đối vs tương đối); không kết luận “thành công” nếu không có trước/sau cùng định nghĩa.

- **Vòng tự review (3 lượt) trước khi reviewer độc lập:** **(V1)** sửa mâu thuẫn scope/tuần + định nghĩa FP + typo cổng D28; **(V2)** đồng bộ **cap 100 lượt** ↔ budget API + làm rõ adoption/khảo sát; **(V3)** thêm **điểm nghẽn coach / plan B** + **đăng ký giả định 🧮** (mục dưới).

### Giả định đăng ký (🧮) — để reviewer không phải đoán

| Giả định | Dùng ở đâu | Cách thay bằng số đo |
|---|---|---|
| **~30%** bài R1-RUBRIC / **~4h** coach/đợt | Problem Framing + slide 1 | Tuần 1: log nhãn **R1-RUBRIC** trên cohort nhỏ |
| **FP% <15%** trên golden là “đủ tốt” để mở rộng | Cổng Phase 1 | Golden do coach gắn nhãn; nếu **0 cờ thiếu** → spot-check protocol mục 8 |
| **Chi phí API ~$5–25** | Budget | Theo dashboard vendor theo **lượt gọi thực tế** (cap 100 lượt) |
| **Giảm ≥20% điểm R1-RUBRIC** so baseline | Cổng Phase 2 | So sánh **cùng định nghĩa** sau khi chốt 1 công thức trong email instructor |

---

## Tổng kiểm tra trước khi sang `2-FINAL-pitch.md`

| Hạng mục | Xong? |
|---|---|
| Tóm vấn đề trong 1 câu | ✓ |
| Budget tách hạng mục, không "miscellaneous" | ✓ |
| Metric có baseline + ngưỡng + ai đo | ✓ |
| Exit criteria có người có quyền thực thi (≥2 mức) | ✓ |
| Adoption: chỉ rõ ai dùng đầu tiên (không "cả khóa") | ✓ |

⚑ Coach kiểm tra ở Mốc 4: *"Xin gì? Hứa gì? Đo gì? Dừng khi nào?"*

Sau bước này, mở `2-FINAL-pitch.md` — dồn tất cả thành 5-slide pitch + AI Support Log.

*Liên quan: handbook §A7+§A8 · `templates/ai-pilot-plan-core.md` · `prompts/06-pilot-plan-challenge.md`*
