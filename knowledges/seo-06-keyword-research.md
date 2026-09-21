---
title: "Keyword Research & Search Intent"
last_updated: 2026-09-21
source: Ahrefs
---

# Keyword Research & Search Intent

← [Về chỉ mục](./seo-00-index.md)

## 1. Quy trình nghiên cứu từ khóa (theo Ahrefs)

### Bước 1 — Tìm seed keyword
Xuất phát từ nhu cầu thực tế của khách hàng, không phải đoán mò. Nguồn brainstorm:
- Ahrefs Free Keyword Generator, Google Keyword Planner, Google Trends, Answer the Public
- Từ khóa hiện có trong **Google Search Console** (site đã có traffic cho từ khóa nào)
- Phân tích đối thủ qua Site Explorer
- Diễn đàn ngành, cộng đồng kỹ thuật (Reddit, forum SI/ME Contractor)

### Bước 2 — Phân loại từ khóa

| Loại | Định nghĩa | Ví dụ (ngành KNX/Matter) |
|---|---|---|
| Matching terms | Chứa từ khóa gốc | "KNX gateway" |
| Related terms | Liên quan nhưng không chứa từ gốc | "hệ thống điều khiển chiếu sáng tòa nhà" |
| Informational | Tìm hiểu thông tin | "KNX là gì" |
| Commercial/Transactional | Có ý định mua | "mua bộ điều khiển KNX chính hãng" |
| Navigational | Tìm 1 địa điểm/site cụ thể | "knxstore.vn bảng giá" |
| Branded / Unbranded | Có/không có tên thương hiệu | "ABB KNX actuator" vs "actuator KNX 8 kênh" |

### Bước 3 — Nhóm cụm từ khóa (clustering)
Nhóm các từ khóa cùng search intent thành **1 trang duy nhất** xử lý nhiều biến thể, thay vì tạo nhiều trang mỏng cạnh tranh lẫn nhau (keyword cannibalization). Ahrefs Keywords Explorer dùng khái niệm **"Parent Topic"** để tự động gợi ý cụm.

### Bước 4 — Đánh giá theo metric

| Metric | Ý nghĩa | Lưu ý |
|---|---|---|
| **Search Volume** | Số lượt tìm/tháng | Không phải = traffic sẽ nhận được |
| **Traffic Potential** | Tổng traffic mà trang #1 nhận từ *toàn bộ* biến thể từ khóa liên quan | Chỉ số thực tế hơn Search Volume đơn lẻ |
| **Keyword Difficulty (KD)** | Ước tính độ khó dựa trên số backlink cần có để vào top 10 | Chỉ đo tín hiệu link, không đo content quality cần thiết |
| **CPC** | Giá mỗi click quảng cáo | Proxy cho intent thương mại — CPC cao thường = giá trị chuyển đổi cao |
| **Growth** | Xu hướng tăng/giảm theo thời gian | Quan trọng với ngành công nghệ thay đổi nhanh (Matter, Casambi) |

### Bước 5 — Ưu tiên hoá
Theo Ahrefs: *"Keyword research không phải là tìm từ khóa dễ rank, mà là tìm từ khóa mang lại giá trị nhiều nhất cho doanh nghiệp."*

Cân bằng 3 trục:
- **Traffic tiềm năng cao + độ khó thấp** → kết quả nhanh (phù hợp site mới)
- **Business potential cao** → dẫn đến lead/sales chất lượng, dù volume thấp (đặc biệt đúng với B2B kỹ thuật — từ khóa dài, chuyên sâu, ít volume nhưng đúng đối tượng)
- **Mục tiêu dài hạn** → từ khóa KD cao cần đầu tư nội dung + backlink ngay từ sớm

## 2. Áp dụng cho KNXStore

- **B2B (SI, ME Contractor)**: ưu tiên long-tail, intent kỹ thuật cụ thể — "cấu hình KNX gateway với BACnet", "so sánh DALI-2 và 0-10V dimming". Volume thấp nhưng business potential rất cao, ít cạnh tranh.
- **B2C (Matter Smarthome)**: có thể nhắm cả từ khóa volume trung bình hơn — "công tắc thông minh Matter là gì", "kết nối Matter với Apple Home" — cạnh tranh cao hơn nhưng traffic potential lớn hơn.
- Tránh **cannibalization**: không tạo nhiều bài cùng nhắm 1 intent (VD: 2 bài cùng trả lời "KNX là gì") — gộp thành 1 pillar page mạnh.

## 3. Search intent — nguyên tắc bắt buộc

Trước khi viết, luôn kiểm tra **top 10 kết quả hiện tại của Google cho từ khóa đó** để xác định định dạng nội dung Google đang ưu tiên (bài blog, trang sản phẩm, danh sách so sánh, video...) — viết sai định dạng so với intent thực tế là nguyên nhân phổ biến khiến bài không lên top dù nội dung tốt.

## Nguồn

- [Keyword Research: The Beginner's Guide – Ahrefs](https://ahrefs.com/seo/keyword-research)
