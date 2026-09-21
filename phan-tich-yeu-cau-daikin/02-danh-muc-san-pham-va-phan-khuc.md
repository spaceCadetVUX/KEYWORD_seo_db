---
title: "Danh mục sản phẩm thực tế & phân khúc khách hàng"
last_updated: 2026-09-21
source: "https://knxstore.vn/search?keyword=daikin (30 SKU, truy xuất 2026-09-21)"
---

# Danh mục sản phẩm thực tế & phân khúc khách hàng

← [Về chỉ mục](./README.md)

30 SKU liên quan Daikin trên knxstore.vn chia thành **6 nhóm giao thức/hình thức tích hợp**, tương ứng với các phân khúc khách hàng và mức giá rất khác nhau. Đây là căn cứ chính để xây content — mỗi nhóm cần thông điệp và từ khóa riêng.

## Nhóm A — Matter Smarthome (B2C phổ thông)

| SKU | Sản phẩm | Giá |
|---|---|---|
| 81MTAC01-DAI | Bảng điều khiển Daikin Matter Wi-Fi S21/P1P2 (Micro Air) | 3.995.000đ |
| MXT-300 | Bộ điều khiển máy lạnh Matter IR (Remotec) | 1.890.000đ |

- **Đối tượng**: chủ hộ/chủ văn phòng đã có điều hòa Daikin, muốn thêm điều khiển app + giọng nói (Siri/Google Assistant/Alexa) mà **không đục tường, không đi dây lại**.
- **Đặc điểm bán hàng**: 81MTAC01-DAI thay thế trực tiếp bảng điều khiển dây cũ (giao tiếp 2 chiều, nhận trạng thái thực); MXT-300 là bộ mở rộng hồng ngoại (universal, không giới hạn thương hiệu, học mã từ remote gốc) — rẻ hơn, dễ lắp hơn nhưng chỉ điều khiển 1 chiều qua hồng ngoại.
- **Đây chính là mảng khớp với brand voice B2C** (`knx-brand-voice-b2c`, `matter-product-description`) và khớp nhất với hành vi tìm kiếm phổ thông sẵn có trong `daikin_data.csv` (người đã/đang dùng máy lạnh Daikin).

## Nhóm B — Đa giao thức smarthome qua Airzone Aidoo (B2C nâng cao / SI nhỏ)

| SKU | Sản phẩm | Giao thức | Giá |
|---|---|---|---|
| AZAI6KNX2DA0/1/2 | Aidoo KNX (S21 / P1P2 Sky Air-VRV / P1P2 Altherma) | KNX | 8.890.000đ |
| AZAI6WSPDA0/1/2/4 | Aidoo Pro Wi-Fi (S21 / P1P2 Sky Air-VRV Mini / Altherma / Altherma CB) | Wi-Fi | 9.980.000đ |
| AZAI6ZBEDA0/1 | Aidoo Zigbee (S21 / P1P2 Sky Air-VRV) | Zigbee | 9.980.000đ |
| AZAI6ZWEDA0/1 | Aidoo Z-Wave Plus (S21 / P1P2 Sky Air-VRV) | Z-Wave | 9.980.000đ |

- **Đối tượng**: nhà thông minh nâng cao đã có hệ sinh thái KNX/Zigbee/Z-Wave riêng, hoặc integrator nhỏ cần chuẩn hóa 1 dòng sản phẩm cho nhiều giao thức.
- **1 dòng sản phẩm (Aidoo), nhiều biến thể theo giao thức + theo dòng máy Daikin (S21 dân dụng / P1P2 Sky Air-VRV thương mại / Altherma máy bơm nhiệt)** → cơ hội content dạng so sánh giao thức ("nên chọn Aidoo KNX hay Zigbee cho điều hòa Daikin").

## Nhóm C — KNX chuyên nghiệp / gateway đa vùng (B2B — SI/ME Contractor)

| SKU | Sản phẩm | Giá |
|---|---|---|
| INKNXDAI001I000 | Intesis KNX cục bộ — Daikin S21 | 8.634.000đ |
| INKNXDAI001R000 | Intesis KNX cục bộ — Daikin P1P2 VRV/Sky | 10.623.000đ |
| CR-CG-DK-KNX-01 | Core P1P2 KNX | 6.640.000đ |
| IN770AIRXXSO000 | Intesis Gateway F1F2 KNX **4 IDU** | 34.997.000đ |
| IN770AIR00SO000-DAI | Intesis Gateway F1F2 KNX **16 IDU** | 84.348.000đ |
| IN770AIR00MO000-DAI | Intesis Gateway F1F2 KNX **64 IDU** | 139.242.000đ |

- **Đối tượng**: rõ ràng B2B — dự án tòa nhà, khách sạn, văn phòng có nhiều dàn lạnh (IDU = Indoor Unit) cần điều khiển tập trung qua hệ BMS/KNX.
- **Thang giá theo quy mô dự án** (4 → 16 → 64 IDU, giá tăng gấp ~4 lần mỗi bậc) — đây là tín hiệu rõ nhất cho thấy nhóm này nhắm **dự án VRV/VRF thương mại quy mô lớn**, không phải hộ gia đình.
- Đây mới đúng là mảng "tích hợp BMS/KNX" mà giả định ban đầu (file 00 cũ) hướng tới — nhưng chỉ là **1 trong 4 nhóm B2B**, không phải toàn bộ yêu cầu.

## Nhóm D — Modbus / RS485 (B2B — tích hợp hệ công nghiệp)

| SKU | Sản phẩm | Giá |
|---|---|---|
| DTA116A51 | Module điều khiển Modbus RTU/DIII-Net Daikin | 9.000.000đ |
| DVC-P-00-01 | Adapter Daikin Modbus RTU cho dàn lạnh VRV | Liên hệ |
| KAC101 | Bộ điều khiển gắn tường Daikin RS485 (Kanonbus) | 1.680.000đ |

- **Đối tượng**: tích hợp Daikin vào hệ BMS dùng chuẩn Modbus/RS485 (phổ biến trong hệ SCADA/PLC công nghiệp, khác với KNX ở nhóm C) — kỹ sư BMS/tự động hóa công nghiệp.

## Nhóm E — Gateway không dây qua cloud (B2B/B2C lai)

| SKU | Sản phẩm | Giá |
|---|---|---|
| — | Gateway CoolPlug — Cool Automation (dòng thường) | 12.100.000đ |
| — | Gateway CoolPlug — Cool Automation (Siesta Series) | 12.100.000đ |

- **Đối tượng**: điều khiển qua app/cloud riêng của Cool Automation, không qua Matter/KNX — phù hợp dự án cần điều khiển tập trung nhiều máy qua Internet mà không cần hạ tầng KNX sẵn có (VD: chuỗi cửa hàng, resort nhiều căn hộ).

## Nhóm F — Phụ kiện gốc Daikin (OEM — nền tảng/thay thế)

| SKU | Sản phẩm | Giá |
|---|---|---|
| BRP072C42 | Điều khiển không dây kết nối Wi-Fi Daikin | 3.900.000đ |
| BRP980B42 | Bộ mở rộng điều khiển Daikin S21 | 3.900.000đ |
| BRP067A42 | Bo mạch giao tiếp S21 Daikin (2.0–4.6kW) | 2.600.000đ |
| KRP928BB2S | Bộ giao tiếp kết nối máy lạnh Daikin | 3.800.000đ |
| BRC1E63 | Bảng điều khiển điều hòa Daikin có dây | 1.500.000đ |
| AC8800 | Bộ điều khiển thermostat có dây fan coil Daikin | 6.500.000đ |

- **Đối tượng**: kỹ thuật viên/thợ điện lạnh cần linh kiện thay thế/nâng cấp gốc Daikin, **hoặc là điều kiện tiên quyết** để lắp các sản phẩm nhóm A–E ở trên (VD: BRP067A42 là bo giao tiếp S21 — nhiều sản phẩm Matter/KNX ở trên yêu cầu cổng S21/P1P2 đã có sẵn hoặc cần bo này để tạo cổng).
- **Đây chính là nhóm trùng khớp trực tiếp với phát hiện ARC480A1/ARC480A21** ở [file 01](./01-phan-tich-du-lieu-hien-co.md) — tìm kiếm theo mã sản phẩm cụ thể, volume vừa phải, cạnh tranh thấp.

## Bảng tổng hợp phân khúc

| Nhóm | Đối tượng | Khoảng giá | Loại nội dung phù hợp |
|---|---|---|---|
| A — Matter | Chủ nhà/văn phòng | 1,9–4tr | Hướng dẫn dễ hiểu, so sánh, "biến máy lạnh Daikin thành điều hòa thông minh" |
| B — Aidoo đa giao thức | Nhà thông minh nâng cao / SI nhỏ | 8,9–10tr | So sánh giao thức, hướng dẫn chọn theo hệ sinh thái sẵn có |
| C — KNX chuyên nghiệp | SI/ME Contractor, dự án tòa nhà | 6,6–139tr | Kỹ thuật sâu, case study, tài liệu tích hợp BMS |
| D — Modbus/RS485 | Kỹ sư BMS công nghiệp | 1,7–9tr | Kỹ thuật sâu, thông số giao tiếp |
| E — Cloud gateway | Dự án đa điểm/chuỗi | 12,1tr | So sánh với KNX/Matter, giải pháp cho chuỗi cơ sở |
| F — OEM gốc | Kỹ thuật viên/thợ lắp đặt | 1,5–6,5tr | Nội dung theo mã sản phẩm, hướng dẫn lắp đặt/thay thế |

Xem đối chiếu với dataset từ khóa hiện có ở [03-khoang-trong-va-co-hoi-tu-khoa.md](./03-khoang-trong-va-co-hoi-tu-khoa.md).
