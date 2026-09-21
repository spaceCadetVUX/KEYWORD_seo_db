---
name: knxstore-seo-writer
description: Viết bài mô tả sản phẩm hoặc bài blog chuẩn SEO/GEO cho KNXStore.vn (KNX, DALI-2, BACnet, Casambi, Modbus, Matter Smarthome) từ dữ liệu sản phẩm hoặc chủ đề + fact có sẵn, theo đúng quy trình đã hệ thống hóa trong knowledges/seo-11 và knowledges/seo-12 của repo này (heading H1/H2/H3 chuẩn, answer-first GEO, FAQ cuối bài, tuyệt đối không dùng em dash). Luôn dùng skill này khi người dùng đưa specs/datasheet sản phẩm (kể cả từ data_base/) và yêu cầu viết mô tả, hoặc đưa chủ đề/câu hỏi kỹ thuật KNX/DALI/Casambi/BACnet/Modbus/Matter và yêu cầu viết bài blog, kể cả khi họ không nói rõ từ "SEO" hay "GEO", chỉ nói "viết bài cho sản phẩm này" hay "viết bài về chủ đề này". Không dùng skill này cho việc nghiên cứu từ khóa thuần túy (đó là seo-06) hay chỉ chỉnh giọng văn cho bài đã viết sẵn (đó là knx-brand-voice-b2b/b2c).
---

# KNXStore SEO/GEO Content Writer

Skill này viết bản nháp hoàn chỉnh (mô tả sản phẩm hoặc bài blog) cho KNXStore.vn, dựa trên 2 quy trình đã được nghiên cứu và hệ thống hóa kỹ trong repo này. Việc của skill là viết đúng theo quy trình đó, không phải tự nghĩ ra cách viết mới mỗi lần. Đọc kỹ file quy trình tương ứng trước khi viết, đừng chỉ dựa vào tóm tắt dưới đây.

## Bước 0: Xác định loại nội dung và đọc đúng quy trình

- Input là 1 sản phẩm cụ thể (tên sản phẩm, SKU, datasheet, bảng thông số) → đây là **mô tả sản phẩm**. Đọc toàn bộ `knowledges/seo-11-viet-mo-ta-san-pham.md`.
- Input là 1 chủ đề, câu hỏi, hoặc yêu cầu so sánh/hướng dẫn cần giải thích → đây là **bài blog**. Đọc toàn bộ `knowledges/seo-12-viet-bai-blog-chuan-seo-geo.md`.
- Nếu không rõ, hỏi người dùng 1 câu ngắn thay vì đoán, vì 2 quy trình có cấu trúc heading và độ dài khác nhau hẳn.

## Bước 1: Kiểm tra 3 input bắt buộc trước khi viết

Cả seo-11 và seo-12 đều giả định đã có sẵn 3 thứ này (xem block "Đầu vào cần có" ở đầu mỗi file). Đừng viết khi thiếu, vì thiếu 1 trong 3 thứ này là nguyên nhân phổ biến nhất khiến bản nháp phải viết lại:

1. **Từ khóa chính đã xác thực nhu cầu tìm kiếm thật.** Nếu người dùng chưa cho từ khóa, đọc `knowledges/seo-06-keyword-research.md` để tự đề xuất, hoặc hỏi lại.
2. **Dữ liệu sản phẩm/sự kiện thật** (thông số, tương thích, giá, case study, số dự án...). Không suy diễn hay bịa số liệu để lấp chỗ trống. Nếu 1 trường dữ liệu bị thiếu, đánh dấu ngay tại vị trí đó trong bản nháp bằng `[CẦN BỔ SUNG: <mô tả cái còn thiếu>]` thay vì tự nghĩ ra thông số, và nói rõ với người dùng những chỗ đã đánh dấu khi giao bản nháp.
3. **Giọng thương hiệu**: B2B (KNX/DALI-2/BACnet/Casambi/Modbus, đối tượng SI/ME Contractor) hay B2C (Matter Smarthome, đối tượng chủ nhà). Suy ra từ loại sản phẩm/chủ đề nếu người dùng không nói rõ. Nếu có thể invoke được skill `knx-brand-voice-b2b` hoặc `knx-brand-voice-b2c` ở cấp tổ chức thì dùng để tinh chỉnh giọng văn; nếu không, ít nhất tuân theo phần phân biệt B2B/B2C đã ghi trong seo-11 mục 9 và seo-12 mục "Áp dụng cho KNXStore".

## Bước 2: Viết theo đúng cấu trúc của quy trình đã chọn

Làm theo file seo-11 hoặc seo-12 (đã đọc ở Bước 0) cho phần cấu trúc chi tiết, độ dài từng phần, và nguyên tắc viết câu. Vài điểm hay bị bỏ sót cần nhớ kỹ:

- **Heading**: chỉ 1 H1, không nhảy cấp H1→H3, heading là câu truy vấn giả lập (viết gần cách người dùng thật gõ trên Google hoặc hỏi AI), không dùng heading chỉ để đổi cỡ chữ cho phần không phải nội dung chính.
- **Answer-first**: mỗi H2/H3 dạng câu hỏi phải có câu trả lời trực tiếp 40–60 từ ngay bên dưới, trước khi mở rộng. Đây là yếu tố có tác động thật đến việc được trích dẫn trong AI Overviews/ChatGPT/Perplexity, không phải tùy chọn.
- **FAQ cuối bài** (blog) hoặc **FAQ trong trang sản phẩm**: chọn 3–5 câu hỏi từ nhu cầu thật (không bịa câu hỏi để lấp chỗ trống), mỗi cặp hỏi-đáp là 1 khối tự chứa 60–180 từ hiểu được dù bị trích tách riêng. Chi tiết cách chọn câu hỏi và cân nhắc schema: xem mục "Cách viết FAQ cuối bài" trong seo-12.
- **Đọc dễ**: câu dưới 20 từ, đoạn 1–2 câu, kim tự tháp ngược, plain language kể cả với độc giả chuyên môn (giữ đúng thuật ngữ ngành nhưng câu văn xung quanh vẫn rõ ràng).

## Quy tắc cứng: tuyệt đối không dùng em dash (—)

Đây là quy tắc dễ bị bỏ sót nhất vì mô hình AI có xu hướng dùng em dash rất tự nhiên khi viết. Toàn bộ bản nháp (H1, H2, H3, thân bài, bullet, bảng, FAQ) không được chứa ký tự "—" ở bất kỳ đâu. Lý do và bảng thay thế theo từng trường hợp đã có đầy đủ trong mục "Quy tắc định dạng bắt buộc" của seo-11/seo-12, áp dụng luôn khi viết chứ không phải sửa lại sau.

Trước khi đưa bản nháp cho người dùng, chủ động rà lại toàn bộ text vừa viết xem còn ký tự "—" nào sót không (có thể lướt qua bằng mắt hoặc tìm kiếm ký tự này trong bản nháp), coi đây là bước bắt buộc giống như đọc lại chính tả.

## Bước 3: Lưu bản nháp thành file .md trong output/

Đầu ra của skill này là 1 file thật, không phải chỉ trả text trong chat. Đóng gói bản nháp theo khung sau (frontmatter + nội dung), rồi dùng Write để lưu vào thư mục `output/` của repo:

```markdown
---
title: "[Title tag đề xuất, ~50-60 ký tự]"
meta_description: "[Meta description đề xuất, ~150-160 ký tự]"
target_keyword: "[từ khóa chính]"
content_type: san-pham | blog
schema_suggested: [Product / FAQPage / Product, FAQPage]
status: draft
created: [ngày hôm nay, định dạng YYYY-MM-DD]
---

# [H1]

[Toàn bộ thân bài theo cấu trúc đã chọn ở seo-11 hoặc seo-12, đúng heading hierarchy]

## Câu hỏi thường gặp
[3-5 cặp H3 hỏi-đáp]
```

**Đặt tên file:**
- Mô tả sản phẩm: `output/<sku-viết-thường>.md`, VD SKU `81MTAC01-DAI` → `output/81mtac01-dai.md`. Nếu không có SKU, dùng slug từ tên sản phẩm.
- Bài blog: `output/<slug-từ-H1>.md`, slug viết thường, bỏ dấu, nối bằng gạch nối, VD H1 "KNX vs DALI-2 cho chiếu sáng thương mại" → `output/knx-vs-dali-2-chieu-sang-thuong-mai.md`.

**Nếu file trùng tên đã tồn tại trong output/**: đọc file cũ trước, hỏi người dùng muốn ghi đè hay lưu bản mới với hậu tố `-v2`, `-v3`... Không tự ý ghi đè, vì file cũ có thể đang được người khác chỉnh sửa.

## Bước 4: Tự kiểm tra trước khi coi là xong

Trước khi báo hoàn thành, đối chiếu bản nháp vừa lưu với checklist gốc trong file đã dùng (mục "Checklist" ở seo-11 hoặc "Checklist nhanh trước khi publish" ở seo-12), đặc biệt các mục dễ sót:

- [ ] Không còn ký tự em dash (—) ở bất kỳ đâu
- [ ] Chỉ 1 H1, không nhảy cấp heading
- [ ] Mỗi H2/H3 dạng câu hỏi có answer-first 40–60 từ ngay dưới
- [ ] FAQ 3–5 câu, câu hỏi từ nhu cầu thật, không trùng nội dung đã có ở H2 phía trên
- [ ] Không có số liệu/case study bị bịa để lấp chỗ dữ liệu thiếu, những chỗ thiếu đã được đánh dấu rõ
- [ ] Giọng văn khớp B2B hoặc B2C đã xác định ở Bước 1
- [ ] Đã lưu đúng file trong `output/`, không ghi đè bản cũ mà chưa hỏi

Nếu có mục nào không đạt, sửa file rồi lưu lại trước khi báo xong. Sau khi mọi mục đạt, trả lời ngắn gọn trong chat: đường dẫn file vừa lưu và tóm tắt các chỗ đã đánh dấu `[CẦN BỔ SUNG]` nếu có, không cần dán lại toàn bộ nội dung bài viết vì đã có trong file.

## Tài liệu tham chiếu

| Cần gì | Đọc file |
|---|---|
| Quy trình viết mô tả sản phẩm đầy đủ | `knowledges/seo-11-viet-mo-ta-san-pham.md` |
| Quy trình viết blog 8 bước đầy đủ | `knowledges/seo-12-viet-bai-blog-chuan-seo-geo.md` |
| Cách xác định từ khóa nếu chưa có | `knowledges/seo-06-keyword-research.md` |
| Chi tiết schema Product/FAQPage | `knowledges/seo-08-schema-structured-data.md` |
| Title tag/meta description chi tiết | `knowledges/seo-02-onpage-content.md` |
| Tín hiệu E-E-A-T cho phần "Proof" | `knowledges/seo-04-eeat-content-quality.md` |
| Internal link theo mô hình Pillar-Cluster | `knowledges/seo-10-topic-cluster.md` |
| Giọng văn B2B kỹ thuật | skill `knx-brand-voice-b2b` |
| Giọng văn B2C Matter Smarthome | skill `knx-brand-voice-b2c` |
