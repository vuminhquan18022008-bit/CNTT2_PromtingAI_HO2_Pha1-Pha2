# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 06
- **Họ tên:Vũ Minh Quân**
- **Lớp:CNT22**
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):Chat-GPT**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt bàn ra JSON

**KET QUA AI**

```text
[\
&#x20; {\
&#x20;   "ma_buffet": "NUONG",\
&#x20;   "ngay_dat": "2026-12-19",\
&#x20;   "nguoi_lon": 2,\
&#x20;   "tre_em": 1,\
&#x20;   "khu_vuc": "trong_nha",\
&#x20;   "ghi_chu": null\
&#x20; },\
&#x20; {\
&#x20;   "ma_buffet": "HAISAN",\
&#x20;   "ngay_dat": "2027-01-03",\
&#x20;   "nguoi_lon": 3,\
&#x20;   "tre_em": 0,\
&#x20;   "khu_vuc": null,\
&#x20;   "ghi_chu": "1 người dị ứng sữa"\
&#x20; },\
&#x20; {\
&#x20;   "ma_buffet": "LAU",\
&#x20;   "ngay_dat": "2026-12-25",\
&#x20;   "nguoi_lon": 4,\
&#x20;   "tre_em": 0,\
&#x20;   "khu_vuc": "san_vuon",\
&#x20;   "ghi_chu": "Ông ngoại đi xe lăn"\
&#x20; }\
]
```

**Link trò chuyện:https://chatgpt.com/share/6b079e4f-cac0-83ec-b3b7-7bcd88c57f37**

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
### **Bước 1: Tiền người lớn**

- Số người lớn: 10 người.
- Giá buffet nướng (NUONG): 399.000 đồng/người.

Phép tính:

10 × 399.000 = **3.990.000 đồng**

### **Bước 2: Tiền trẻ em**

Giá trẻ em cao từ 1 m đến 1,4 m bằng 50% giá người lớn.

- Trẻ thứ nhất (1,1 m): 399.000 × 50% = 199.500 đồng.
- Trẻ thứ hai (1,2 m): 399.000 × 50% = 199.500 đồng.
- Trẻ thứ ba (1,35 m): 399.000 × 50% = 199.500 đồng.
- Bé thứ tư (0,8 m): Dưới 1 m nên được miễn phí = 0 đồng.

Tổng tiền trẻ em:

199.500 × 3 + 0 = **598.500 đồng**

### **Bước 3: Tổng tiền buffet trước giảm giá**

Tiền người lớn + tiền trẻ em:

3.990.000 + 598.500 = **4.588.500 đồng**

### **Bước 4: Giảm giá nhóm**

- Đoàn có 10 người lớn.
- Điều kiện giảm giá: Từ 10 người lớn trở lên.
- Đoàn đủ điều kiện được giảm 5% trên tiền buffet.

Số tiền được giảm:

4.588.500 × 5% = **229.425 đồng**

Tiền buffet sau giảm:

4.588.500 − 229.425 = **4.359.075 đồng**

### **Bước 5: Phụ thu phòng riêng**

- Thuê 1 phòng riêng.
- Phụ thu: 500.000 đồng/phòng.
- Phụ thu không được giảm giá.

Phép tính:

1 × 500.000 = **500.000 đồng**

### **Bước 6: Tổng tiền**

Tổng tiền = Tiền buffet sau giảm + Phụ thu phòng riêng.

4.359.075 + 500.000 = **4.859.075 đồng**

Tổng thanh toán: 4.859.075 đồng

[RESULT: 4.859.075 đồng]
```

**Link trò chuyện:https://chatgpt.com/share/6b079e4f-cac0-83ec-b3b7-7bcd88c57f37**

### b) Kiểm tra kết quả AI

(Ghi kết luận AI đúng hay sai; nếu sai, ghi bước sai đầu tiên và kết quả đúng của bước đó – xoá dòng này)

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{\
&#x20; "loai_su_co": "thieu_mon",\
&#x20; "so_khach": 5,\
&#x20; "so_mon_bi_thieu": 2,\
&#x20; "tom_tat": "Gia đình 5 người không được phục vụ tôm hùm và cua dù đã chờ bổ sung 2 lần."\
}
```

**Link trò chuyện:https://chatgpt.com/share/6b079ec0-ed08-83ec-99b6-b87274deeeb4**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí                 | Điểm       | Minh chứng                                                                                                                                                                                                                                                                            | Đề xuất sửa                                                                                                          |
| ------------------------ | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Đúng thông tin (50%)** | **0/5**    | **Lỗi 1:** “Buffet lẩu bên em 279k/người lớn thôi” – Sai giá. Giá chuẩn của công ty là **299.000 đồng/người lớn**, không phải 279.000 đồng. **Lỗi 2:** “Chị trễ 40 phút em vẫn giữ bàn cho chị nha” – Sai quy định. Khách trễ 40 phút là trên 30 phút, công ty quy định phải hủy bàn. | “Buffet lẩu bên em có giá 299.000 đồng/người lớn. Theo quy định, bàn sẽ bị hủy nếu khách đến trễ trên 30 phút.”      |
| **Đầy đủ (30%)**         | **2/3**    | **Lỗi:** “Có gì nhắn em nhé!” – Chưa chủ động mời khách cung cấp thông tin để đặt bàn. Nhân viên chưa yêu cầu khách cung cấp ngày đến, giờ đến và số lượng khách.                                                                                                                     | “Chị vui lòng cho em xin ngày đến, giờ đến và số lượng khách để em hỗ trợ kiểm tra và đặt bàn cho chị nhé!”          |
| **Giọng điệu (20%)**     | **0,5/2**  | **Lỗi:** “Dạ chào chị nha!”, “ngon bá cháy luôn”, “chị nha”, “Có gì nhắn em nhé!” – Cách diễn đạt suồng sã, thiếu tính chuyên nghiệp trong giao tiếp tư vấn khách hàng.                                                                                                               | “Dạ, em xin chào chị! Buffet lẩu bên em có giá 299.000 đồng/người lớn. Em rất sẵn lòng hỗ trợ chị đặt bàn ạ.”        |
| **Tổng cộng**            | **2,5/10** | Bài làm sai cả giá buffet và quy định giữ bàn; thiếu thông tin cần thiết để hoàn tất đặt bàn; giọng điệu chưa chuyên nghiệp.                                                                                                                                                          | Cần kiểm tra thông tin chuẩn trước khi tư vấn, tuân thủ quy định giữ bàn và sử dụng ngôn ngữ lịch sự, chuyên nghiệp. |

**Tổng điểm: 2,5/10.**
```

**Link trò chuyện:
https://chatgpt.com/share/6b079f2d-fcbc-83ec-9609-1abd71522fdb
**
