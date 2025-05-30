# 🔌 LumentreeHA

Kết nối biến tần năng lượng mặt trời **Lumentree** với **Home Assistant** – cho phép giám sát, điều khiển và mở rộng khả năng tích hợp hệ thống điện mặt trời vào hệ sinh thái smarthome.

<img src="https://github.com/vboyhn/LumentreeHA/blob/main/sensor.png" width="850" alt="Lumentree Sensor Screenshot" />


---

## 🛠️ Các thay đổi trong bản chỉnh sửa này (so với repo gốc `vboyhn/LumentreeHA`)

> Đây là bản fork từ [vboyhn/LumentreeHA](https://github.com/vboyhn/LumentreeHA), được chỉnh sửa và mở rộng:

- ✅ **Fix lỗi thread-unsafe**: thay thế `async_dispatcher_send` bằng `dispatcher_send` để tương thích Home Assistant mới.
- ✅ **Sửa lỗi reconnect gây crash**: xử lý `hass.async_create_task()` đúng thread context.
- ✅ **Cải tiến log**: thêm debug rõ ràng hơn khi kết nối thất bại hoặc mất phiên.
- ✅ **Tối ưu tương thích** với Home Assistant 2024.x.
- 🔄 Có thể sẽ cập nhật thêm hỗ trợ kết nối trực tiếp với ESP32 trong tương lai.

---

## 🚀 Cách sử dụng

### ENGLISH:
- Copy the `lumentree` folder into your `custom_components` directory.
- Reboot Home Assistant.
- Add new integration: **Lumentree**.
- Enter your Device ID (serial number) to log in and start syncing data.

### TIẾNG VIỆT:
- Sao chép thư mục `lumentree` vào `custom_components` trong Home Assistant.
- Khởi động lại Home Assistant.
- Vào phần `Cấu hình > Tích hợp (Integrations)` để thêm thiết bị **Lumentree**.
- Nhập **số serial (Device ID)** để kết nối và theo dõi dữ liệu từ biến tần.

---

## 📅 Dự định phát triển trong tương lai

### Future
- Allow advanced setting changes directly from HA.
- Use **ESP32** to locally interface with inverter (no Lumentree cloud, no Internet).
- Add multiple inverter support.

### Tương lai
- Cho phép thay đổi các cài đặt nâng cao của biến tần qua Home Assistant.
- Dùng ESP32 để giao tiếp cục bộ với biến tần (bỏ qua cloud).
- Hỗ trợ nhiều biến tần cùng lúc.

---

## 🤝 Tham gia cùng phát triển
Bạn nào quan tâm có thể fork, sửa, hoặc mở pull request – hoặc cùng mình nghiên cứu phần giao tiếp nội bộ với ESP32.

---

## 📄 License
Giữ nguyên theo [Giấy phép gốc từ vboyhn](https://github.com/vboyhn/LumentreeHA). Các bản chỉnh sửa tuân thủ MIT License.
