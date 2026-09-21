---
title: "Đề xuất cấu trúc Topic Cluster theo phân khúc sản phẩm"
last_updated: 2026-09-21
---

# Đề xuất cấu trúc Topic Cluster

← [Về chỉ mục](./README.md) · Áp dụng mô hình: [seo-10-topic-cluster.md](../knowledges/seo-10-topic-cluster.md)

## 1. Vì sao không dùng 1 pillar chung cho tất cả 30 SKU

Theo nguyên tắc ở [seo-10](../knowledges/seo-10-topic-cluster.md#1-định-nghĩa): mỗi cluster page nên nhắm **1 search intent hẹp**, và pillar chỉ nên bao quát **1 chủ đề đủ hẹp để không loãng**. Ở đây, người đọc "chủ nhà tìm cách điều khiển máy lạnh bằng Siri" và "kỹ sư SI tìm gateway KNX cho 64 dàn lạnh VRV" có:
- Trình độ kỹ thuật khác nhau hoàn toàn
- Ngân sách khác nhau 50–100 lần (1,9tr vs 139tr)
- Định dạng nội dung mong đợi khác nhau (bài dễ hiểu có ảnh minh họa vs tài liệu kỹ thuật/case study)

→ Gộp chung sẽ vi phạm nguyên tắc "mỗi trang 1 intent", gây loãng cả 2 nhóm. Đề xuất **2 pillar riêng biệt** + 1 cụm phụ trợ.

## 2. Cấu trúc đề xuất

```
PILLAR B2C
"Điều khiển điều hòa Daikin thông minh: kết nối App, Siri, Google Assistant"
(brand voice B2C — knx-brand-voice-b2c)
        │
        ├── Cluster: Matter là gì? Vì sao chọn Matter để smarthome hóa điều hòa Daikin
        ├── Cluster: 81MTAC01-DAI vs MXT-300 — nên chọn loại nào cho nhà bạn
        ├── Cluster: Cổng P1/P2, S21 trên điều hòa Daikin là gì, làm sao biết máy mình có cổng nào
        ├── Cluster: Hướng dẫn lắp bảng điều khiển Matter thay bảng dây cũ (không đục tường)
        ├── Cluster: Điều khiển điều hòa Daikin bằng Apple Home / Google Home / Alexa — cấu hình từng bước
        └── Cluster: Aidoo là gì — khi nào chủ nhà nâng cao nên chọn KNX/Zigbee/Z-Wave thay vì Matter

PILLAR B2B
"Tích hợp điều hòa Daikin (VRV/Sky Air) vào hệ thống BMS/KNX tòa nhà"
(brand voice B2B — knx-brand-voice-b2b)
        │
        ├── Cluster: So sánh phương án tích hợp Daikin vào KNX — Intesis vs Core vs Airzone Aidoo
        ├── Cluster: Gateway Intesis F1F2 KNX — chọn bản 4/16/64 IDU theo quy mô dự án
        ├── Cluster: Tích hợp Daikin qua Modbus RTU/DIII-Net (DTA116A51) — thông số & sơ đồ đấu nối
        ├── Cluster: Gateway không dây CoolPlug — giải pháp điều khiển tập trung không cần hạ tầng KNX
        ├── Cluster: Case study tích hợp VRV Daikin vào BMS tòa nhà văn phòng/khách sạn
        └── Cluster: Checklist khảo sát trước khi báo giá gateway tích hợp Daikin cho SI

CỤM PHỤ TRỢ — Phụ kiện & linh kiện gốc Daikin (dùng chung, hỗ trợ SEO theo mã sản phẩm)
        │
        ├── Trang sản phẩm/hướng dẫn riêng cho từng mã: BRC1E63, BRP072C42, BRP067A42,
        │   KRP928BB2S, BRP980B42, AC8800 — theo đúng pattern đã kiểm chứng (ARC480A1/A21)
        └── Link chéo vào cả 2 pillar khi mã đó là điều kiện tiên quyết để lắp sản phẩm smarthome/KNX
```

## 3. Vai trò của "Cụm phụ trợ OEM" — không phải pillar thứ 3

- Không cần 1 pillar riêng vì mỗi mã sản phẩm là **trang sản phẩm/bài hướng dẫn độc lập, tự thân đã có search demand** (theo pattern ARC) — không cần 1 "trang tổng quan" đứng trên chúng.
- Vai trò chính: **internal link 2 chiều** — từ cluster "Hướng dẫn lắp bảng điều khiển Matter" link tới trang sản phẩm "BRP067A42" (vì đây là bo giao tiếp cần có sẵn), và ngược lại trang BRP067A42 link tới cluster hướng dẫn Matter/KNX liên quan — đúng nguyên tắc internal linking ở [seo-02](../knowledges/seo-02-onpage-content.md#7-internal-linking) và [seo-10](../knowledges/seo-10-topic-cluster.md#3-internal-linking-chuẩn).

## 4. Thứ tự triển khai đề xuất

| Thứ tự | Hạng mục | Lý do ưu tiên |
|---|---|---|
| 1 | Trang sản phẩm/mã OEM (BRC1E63, BRP072C42...) | Bằng chứng volume + competition thấp đã có sẵn (ARC pattern) — ROI nhanh nhất, ít rủi ro |
| 2 | Pillar B2C + 2–3 cluster đầu (Matter là gì, 81MTAC01 vs MXT-300, cổng P1/P2 là gì) | Khớp brand voice sẵn có, đối tượng dễ tiếp cận, dataset hiện tại đã chứng minh thị trường "máy lạnh daikin" có volume lớn để dẫn traffic vào |
| 3 | Pillar B2B + cluster theo giao thức (KNX trước, vì đã có 6 SKU thuộc nhóm C — nhiều nhất) | Business potential cao (giá trị đơn hàng lớn: 6,6–139tr) dù volume tìm kiếm thấp hơn |
| 4 | Cluster Modbus/RS485, CoolPlug | Thị trường hẹp hơn, làm sau khi 2 pillar chính đã ổn định |

## 5. Điều cần xác nhận trước khi viết bài đầu tiên

Xem [05-cau-hoi-mo-va-buoc-tiep-theo.md](./05-cau-hoi-mo-va-buoc-tiep-theo.md).
