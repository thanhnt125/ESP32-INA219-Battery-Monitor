# Thiết bị giám sát pin dùng ESP32 + INA219

Bài tập lớn Kĩ thuật Vi xử lí – Đề tài RUOI-1

**Thành viên:** Nguyễn Trung Thành (20233648), Bùi Thế Vinh (2023)

## Giới thiệu
Đo điện áp, dòng điện, công suất của pin 18650 qua cảm biến INA219 (giao tiếp I2C),
ước lượng % pin còn lại và cảnh báo khi pin xuống dưới ngưỡng cấu hình được.

## Linh kiện
- ESP32 DevKit
- Module INA219
- Pin 18650 + đế pin + mạch sạc TP4056
- LED, buzzer cảnh báo

## Kết nối
| Linh kiện | Chân | Nối tới ESP32 |
|---|---|---|
| INA219 | VCC / GND | 3V3 / GND |
| INA219 | SDA / SCL | GPIO21 / GPIO22 |
| LED cảnh báo | Anode | GPIO … |

## Chức năng
- Lấy mẫu bằng ngắt timer (chu kì 1 s)
- Ước lượng % pin theo 2 cách: theo điện áp và coulomb counting
- Chỉnh ngưỡng cảnh báo qua UART, lưu vào Flash
- Xuất log CSV để vẽ đồ thị

## Tiến độ
- [x] Chọn đề tài, lập kế hoạch
- [ ] Mua linh kiện
- [ ] Đọc INA219 qua I2C
- [ ] Ngắt timer + cảnh báo
- [ ] Ước lượng % pin
- [ ] Kiểm thử, viết báo cáo
