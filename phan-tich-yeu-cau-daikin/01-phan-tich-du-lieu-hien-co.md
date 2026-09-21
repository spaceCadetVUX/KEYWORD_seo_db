---
title: "Phân tích dữ liệu từ khóa Daikin hiện có"
last_updated: 2026-09-21
source: "../data_base/daikin_data.csv"
---

# Phân tích dữ liệu từ khóa Daikin hiện có

← [Về chỉ mục](./README.md)

## 1. Thông tin file nguồn

- Đường dẫn: `data_base/daikin_data.csv`
- Nguồn export: **"Công Cụ Phân Tích Từ Khóa Miễn Phí – Keyword Planner Free"** (ghi ở dòng tiêu đề file)
- Số dòng dữ liệu: **3.919 từ khóa**
- Cột dữ liệu: `STT, Keyword, Volume, Length, Trend, Trend Data, Difficulty, Competition, Avg.CPC, KW Type, Question`

## 2. Giới hạn của bộ dữ liệu (đọc kỹ trước khi dùng)

| Giới hạn | Bằng chứng |
|---|---|
| **Cột "Question" gần như bị khóa** | 3.912/3.919 dòng để trống; 7 dòng còn lại chỉ hiện `"Upgrade VIP to view" → YES` — đây là tính năng trả phí của công cụ, dữ liệu "People Also Ask" thực tế **chưa có** |
| Công cụ ghi rõ là bản **miễn phí** | Nhiều khả năng Volume/Difficulty/Competition là ước tính gần đúng (estimate), không phải số liệu chính xác như Ahrefs/Semrush/Google Keyword Planner trả phí |
| Không có cột Search Intent | Phải tự suy luận intent từ nội dung từ khóa, dữ liệu không gán sẵn |

→ Coi bộ dữ liệu này là **điểm khởi đầu để thấy bức tranh tổng thể**, không phải cơ sở đủ tin cậy để quyết định ngân sách/ưu tiên cuối cùng.

## 3. Top từ khóa theo volume

| Keyword | Volume/tháng | Difficulty | Competition |
|---|---|---|---|
| điều hoà đaikin | 14.800 | 84 | 96 |
| điều hòa daikin | 14.800 | — | — |
| máy lạnh daikin | 14.800 | 90 | 99 |
| may lanhdaikin (không dấu, dính chữ) | 14.800 | — | — |
| daikina / daikin | 9.900 | — | — |
| **arc480a21** (mã remote điều khiển) | 6.600 | 50 | **9** |
| **arc480a1** (mã remote điều khiển) | 4.400 | 49 | **10** |
| điều hòa trung tâm vrv | 3.600 | 28 | — |
| máy lọc không khí daikin | 3.600 | — | — |
| vrv daikin | 2.900 | 42 | — |

**Difficulty toàn bộ dataset**: min = 2, median = 41, max = 90 (thang phổ biến 0–100).

## 4. Phân bố loại match (KW Type)

| Loại | Số lượng | Tỷ lệ |
|---|---|---|
| broad | 1.514 | ~38,6% |
| phrase | 1.480 | ~37,8% |
| exact | 925 | ~23,6% |

→ Phân bố này là chuẩn của công cụ nghiên cứu từ khóa PPC (Google Ads Keyword Planner-style), không phản ánh gì về nội dung SEO — chỉ cho biết cách công cụ mở rộng từ khóa gốc.

## 5. Phân loại theo chủ đề thực tế (đọc thủ công mẫu dữ liệu)

Sau khi rà từ khóa theo nội dung, dataset chia thành các nhóm sau:

| Nhóm chủ đề | Ví dụ | Ước lượng tỷ trọng | Liên quan mục tiêu "phụ kiện tích hợp"? |
|---|---|---|---|
| Mua máy lạnh/điều hòa Daikin (dân dụng) | "máy lạnh daikin 1hp", "điều hòa daikin 2 ngựa" | Rất lớn, chiếm đa số | ❌ Không — đây là khách mua máy, không phải khách tích hợp hệ thống |
| Model/mã sản phẩm cụ thể | "arc480a21", "arc480a1" | Rất nhỏ (4 dòng) | ⚠️ **Một phần có** — đây là mã remote điều khiển Daikin, thuộc nhóm phụ kiện điều khiển |
| Hệ thống trung tâm/VRV | "vrv daikin", "điều hòa trung tâm vrv" | Rất nhỏ (3 dòng) | ⚠️ Gần đúng hướng — VRV là nền tảng hay được tích hợp BMS, nhưng bản thân từ khóa vẫn chỉ nói về "hệ thống VRV" chung, chưa nói tới tích hợp |
| Vệ sinh/bảo trì/sửa chữa/bảo hành | "bảo hành daikin", nhiều biến thể sửa chữa | Đáng kể | ❌ Không |
| **Gateway/BACnet/Modbus/KNX/BMS/tích hợp** | *(không tìm thấy)* | **0 dòng / 3.919** | — |

## 6. Phát hiện đáng chú ý: nhóm "arc480a1 / arc480a21"

Đây là 2 từ khóa **gần nhất với hướng phụ kiện** trong toàn bộ dataset:
- Volume khá tốt so với mặt bằng chung (4.400–6.600/tháng)
- Difficulty trung bình (~49–50, thấp hơn nhiều so với từ khóa "máy lạnh daikin" ở mức 90)
- **Competition rất thấp (9–10/100)** — đây là tín hiệu tích cực hiếm hoi trong dataset

ARC480A1/ARC480A21 là mã **remote điều khiển có dây** của Daikin — người tìm kiếm thường đang cần: mua remote thay thế, hoặc tìm hiểu cách dùng/reset. Đây có thể là điểm khởi đầu tốt để mở rộng sang cụm "phụ kiện điều khiển Daikin" nói chung (remote, bo mạch điều khiển, cảm biến) — **nhưng vẫn chưa phải nhóm "tích hợp hệ thống" (BACnet/Modbus/KNX/BMS)** mà yêu cầu ban đầu nhắm tới.

## Kết luận file này

Dataset hiện có phù hợp để tham khảo **thị trường Daikin nói chung** (quy mô tìm kiếm, mức độ cạnh tranh chung của brand), nhưng **không đủ** để lập kế hoạch content cho ngách "phụ kiện điều khiển/tích hợp hệ thống Daikin" — ngách này gần như chưa được nghiên cứu trong dataset. Xem danh mục sản phẩm thật ở [02-danh-muc-san-pham-va-phan-khuc.md](./02-danh-muc-san-pham-va-phan-khuc.md) và đề xuất từ khóa bổ sung ở [03-khoang-trong-va-co-hoi-tu-khoa.md](./03-khoang-trong-va-co-hoi-tu-khoa.md).
