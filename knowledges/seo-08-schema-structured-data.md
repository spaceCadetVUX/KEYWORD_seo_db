---
title: "Schema Markup & Structured Data"
last_updated: 2026-09-21
source: Google Search Central, ngành SEO 2026
---

# Schema Markup & Structured Data

← [Về chỉ mục](./seo-00-index.md)

## 1. Khái niệm

- **Structured data** = thông tin được định dạng chuẩn hóa.
- **Schema.org** = bộ từ vựng (vocabulary) dùng để mô tả structured data.
- **JSON-LD** = định dạng code — **định dạng duy nhất Google khuyến nghị**, nhúng trong `<script type="application/ld+json">` ở `<head>` hoặc `<body>`.
- **Schema markup** = structured data cụ thể dùng từ vựng Schema.org.

> Tránh dùng **Microdata** và **RDFa** — dễ lỗi, khó bảo trì hơn JSON-LD.

## 2. Tác động thực tế

- **Không phải ranking factor trực tiếp** — Google xác nhận rõ điều này.
- Nhưng tạo **rich results** (sao đánh giá, giá, breadcrumb, FAQ...) → tăng CTR đáng kể (**~20–30%** theo dữ liệu ngành 2026).
- Ngày càng quan trọng cho **GEO**: AI Overviews và LLM dùng schema để xác thực và củng cố câu trả lời, giảm rủi ro hallucination khi trích dẫn.

## 3. Điều kiện để hiển thị rich result

Có markup đúng cú pháp **chưa đủ** — Google còn xét thêm:
- Chất lượng nội dung tổng thể của trang.
- Tín hiệu E-E-A-T (xem [file 04](./seo-04-eeat-content-quality.md)).
- Loại schema có được Google hỗ trợ hiển thị rich result hay không tại thời điểm hiện tại (danh sách loại được hỗ trợ **thay đổi theo thời gian**).

**Cập nhật quan trọng 2026:** Google đã **loại bỏ FAQ rich results** khỏi Google Search từ tháng 5/2026 — không nên phụ thuộc vào FAQPage schema chỉ để lấy rich snippet (vẫn có giá trị cho GEO/AI citation dù không còn rich result truyền thống).

## 4. Các loại schema có tác động rõ nhất (2026)

| Schema type | Dùng cho | Ưu tiên tại KNXStore |
|---|---|---|
| **Organization** | Thông tin công ty, logo, social profile | Trang chủ, trang giới thiệu |
| **Article / BlogPosting** | Bài blog kỹ thuật | Tất cả bài blog KNX/DALI/Matter |
| **Product** | Trang sản phẩm (giá, tình trạng còn hàng, đánh giá) | Trang sản phẩm B2C Matter, B2B thiết bị |
| **FAQPage** | Câu hỏi thường gặp | Vẫn nên dùng cho mục đích GEO dù không còn rich snippet Google Search |
| **LocalBusiness** | Thông tin địa chỉ, giờ hoạt động | Trang liên hệ/showroom |
| **BreadcrumbList** | Điều hướng phân cấp | Toàn site (category → subcategory → sản phẩm) |

## 5. Nguyên tắc triển khai

1. Markup phải **khớp chính xác với nội dung hiển thị thực tế trên trang** — không markup thông tin không có thật (vi phạm spam policy, có thể bị phạt).
2. Test bằng Rich Results Test / Schema Markup Validator trước khi publish.
3. Ưu tiên độ chính xác và nhất quán hơn cố nhồi nhiều loại schema không liên quan.

## Nguồn

- Google Search Central – hướng dẫn structured data (JSON-LD khuyến nghị chính thức)
- Tổng hợp xu hướng schema 2026 từ các phân tích ngành SEO (FAQ rich result bị loại bỏ 5/2026)
