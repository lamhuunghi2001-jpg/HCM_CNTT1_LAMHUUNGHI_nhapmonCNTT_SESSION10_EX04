# Mô hình IPO trong trang trại thông minh

## Bắt đầu từ nồi cơm điện

Bạn đổ gạo và nước vào nồi rồi bấm nút. Nồi nấu. Vài phút sau bạn có cơm chín. Gạo và nước là thứ đi vào, việc nấu là thứ nồi tự làm, cơm chín là thứ đi ra. Đó chính là IPO.

## Ba phần của IPO

| Phần | Nghĩa tiếng Việt | Trong hệ thống tưới tự động |
|---|---|---|
| Input | Đầu vào, thứ hệ thống nhận | Số đọc từ cảm biến độ ẩm đất |
| Process | Xử lý, phần "suy nghĩ" | Bo mạch Raspberry Pi so số đọc với mức đất khô |
| Output | Đầu ra, việc hệ thống làm | Máy bơm bật hoặc tắt |

## Sơ đồ luồng

```text
Cảm biến độ ẩm  -->  Raspberry Pi  -->  Máy bơm
   (Input)           (Process)         (Output)
```

## Một ví dụ cụ thể

Cảm biến báo đất đang khô. Raspberry Pi nhận tin đó và hỏi: "Đất đã khô hơn mức cho phép chưa?". Nếu rồi, nó ra lệnh cho máy bơm chạy. Đất ướt trở lại, cảm biến báo mới, và máy bơm dừng.

Cả vòng này không cần người đứng ngoài ruộng canh.

## Tự kiểm tra

- [ ] Bạn chỉ ra được đâu là Input, Process, Output trong nồi cơm điện chưa?
- [ ] Nếu cảm biến hỏng và không gửi số đọc nữa, phần nào của IPO sẽ bị ảnh hưởng đầu tiên?
