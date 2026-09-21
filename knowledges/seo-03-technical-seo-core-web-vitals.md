---
title: "Technical SEO & Core Web Vitals"
last_updated: 2026-09-21
source: Google Search Central
---

# Technical SEO & Core Web Vitals

← [Về chỉ mục](./seo-00-index.md)

## 1. Crawl & Index — kiểm soát Google thấy gì

| Công cụ | Mục đích |
|---|---|
| `robots.txt` | Chặn crawl các phần không cần index (VD: `/checkout/`, `/admin/`) |
| `<meta name="robots" content="noindex">` | Loại 1 trang khỏi index nhưng vẫn cho crawl |
| `X-Robots-Tag` (HTTP header) | Tương tự noindex nhưng áp dụng ở tầng server, dùng cho file không phải HTML (PDF...) |
| `rel="canonical"` | Chỉ định URL gốc khi có nội dung trùng/tương tự ở nhiều URL |
| `301 redirect` | Chuyển hướng vĩnh viễn từ URL cũ/không mong muốn sang URL chính |
| **URL Inspection Tool** (Search Console) | Kiểm tra Google thấy trang như thế nào, có index hay không, lỗi gì |

**Lưu ý quan trọng:** Không có "duplicate content penalty" — Google chỉ tự chọn 1 URL canonical để hiển thị, các URL còn lại không hiển thị (không bị phạt).

## 2. Sitemap & site architecture

- Sitemap chỉ là **tín hiệu phụ trợ**, không bắt buộc — nhưng nên có để hỗ trợ crawl trang mới/ít liên kết nội bộ.
- Google **không dùng HTML sitemap** để hỗ trợ SEO (chỉ XML sitemap có giá trị kỹ thuật).
- Nhóm nội dung theo thư mục logic (`/san-pham/`, `/blog/`, `/du-an/`) giúp Google học tần suất thay đổi của từng nhóm.
- Không cần cấu trúc "hoàn hảo" — Google xử lý tốt cả site có cấu trúc lộn xộn, miễn là crawl được.

## 3. HTTPS / SSL

- Google xác nhận đây là **ranking signal chính thức**, nhưng hoạt động như "tiebreaker" (yếu tố phân định khi các trang khác ngang nhau), không phải yếu tố quyết định lớn.
- Bắt buộc về mặt bảo mật & UX (đặc biệt site có form liên hệ, giỏ hàng B2C Matter Smarthome).

## 4. Mobile

- **Mobile-first indexing**: Google dùng phiên bản mobile của trang để index và xếp hạng, kể cả khi người dùng tìm trên desktop.
- Nội dung ẩn sau tab/accordion trên mobile: Google *có thể* vẫn index nhưng đánh giá thấp hơn nội dung hiển thị ngay.
- Kiểm tra: không có nội dung/link chỉ tồn tại ở bản desktop mà thiếu ở bản mobile.

## 5. Core Web Vitals (cập nhật Q2/2026)

Ba metric nằm trong "điểm hiệu suất tổng hợp" mà từ core update tháng 3/2026 được xếp **cùng cấp với tín hiệu nội dung** (trước đó chỉ là yếu tố phụ):

| Metric | Đo gì | Ngưỡng "Tốt" | Ngưỡng "Kém" |
|---|---|---|---|
| **LCP** (Largest Contentful Paint) | Tốc độ render phần tử lớn nhất trong viewport | ≤ 2.5s | > 4s |
| **INP** (Interaction to Next Paint) | Độ trễ phản hồi tương tác (đã thay thế FID) | ≤ 200ms | > 500ms |
| **CLS** (Cumulative Layout Shift) | Độ ổn định bố cục khi tải trang | < 0.1 | > 0.25 |

**Dữ liệu thực tế đáng chú ý:** sau core update 3/2026, trang ở vị trí #1 có tỷ lệ "pass" Core Web Vitals cao hơn **~10%** so với trang ở vị trí #9 — cho thấy khi nội dung 2 trang tương đương, CWV là yếu tố phân định thứ hạng.

> **Theo dõi thêm:** Google đang thử nghiệm **Visual Stability Index (VSI)** — chưa phải ranking signal chính thức nhưng dự kiến trở thành hard ranking factor trong 12–18 tháng tới (thu thập qua CrUX).

### Cách cải thiện nhanh (ưu tiên theo hiệu quả/chi phí)

1. Nén & lazy-load hình ảnh, dùng định dạng WebP/AVIF.
2. Giảm JavaScript chặn render (defer/async), loại bỏ thư viện không dùng.
3. Dùng CDN, bật caching trình duyệt & server.
4. Đặt kích thước cố định (width/height) cho ảnh & embed để tránh layout shift.
5. Ưu tiên tải font hệ thống hoặc `font-display: swap`.

## 6. Server & uptime

- Downtime kéo dài → ảnh hưởng ranking; downtime lặp lại nhiều → rủi ro bị deindex.
- Vị trí server ảnh hưởng nhẹ đến local ranking (geo-targeting).

## 7. Checklist audit kỹ thuật nhanh

- [ ] Robots.txt không chặn nhầm CSS/JS/trang quan trọng
- [ ] Sitemap.xml cập nhật, submit qua Search Console
- [ ] Không có chuỗi redirect 301 dài (mỗi lần redirect làm loãng "link equity")
- [ ] HTTPS toàn site, không mixed content
- [ ] Core Web Vitals đạt "Good" trên cả mobile & desktop (kiểm tra qua PageSpeed Insights / CrUX)
- [ ] Không có trang trùng lặp thiếu canonical
- [ ] Structured data hợp lệ (xem [file 08](./seo-08-schema-structured-data.md))
- [ ] Broken link = 0 (link gãy là tín hiệu "trang bị bỏ bê")

## Nguồn

- [SEO Starter Guide – Google Search Central](https://developers.google.com/search/docs/fundamentals/seo-starter-guide)
- [Search Essentials – Google Search Central](https://developers.google.com/search/docs/essentials)
- Core Web Vitals Q2 2026 threshold data (tổng hợp từ các báo cáo phân tích CrUX công khai, 2026)
