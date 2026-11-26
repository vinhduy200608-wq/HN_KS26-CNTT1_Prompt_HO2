# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 08
- **Họ tên:** NGUYỄN CÔNG VINH
- **Lớp:** CNTT3
- **Link repository Pha2:** https://github.com/vinhduy200608-wq/HN_KS26-CNTT1_Prompt_HO2.git
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt lịch khám ra JSON

**KET QUA AI**

```text
[
  {
    "ma_dich_vu": "TRAMRANG",
    "ngay_hen": "2026-12-17",
    "nguoi_lon": 2,
    "tre_em": 1,
    "khung_gio": "chieu",
    "ghi_chu": "bé 9 tuổi"
  },
  {
    "ma_dich_vu": "CAOVOI",
    "ngay_hen": "2027-01-06",
    "nguoi_lon": null,
    "tre_em": null,
    "khung_gio": null,
    "ghi_chu": "tổng 3 người, chưa rõ số người lớn và trẻ em; 1 người bị tiểu đường"
  },
  {
    "ma_dich_vu": "TAYTRANG",
    "ngay_hen": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "khung_gio": "sang",
    "ghi_chu": "1 người dị ứng thuốc tê; hỏi lịch cuối năm, chưa rõ ngày"
  }
]
```

**Link trò chuyện:** https://claude.ai/share/d2e2f3d8-d039-43da-9038-f964a2b85222

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
<suy_luan>

Tiền người lớn: 6 × 350.000 = 2.100.000 đồng
Tiền trẻ em:
Trẻ 7 và 11 tuổi: 2 × (350.000 × 80%) = 560.000 đồng
Bé 4 tuổi: 1 × 0 = 0 đồng (giả định bé chỉ khám, không cạo vôi)
Tiền dịch vụ: 2.100.000 + 560.000 + 0 = 2.660.000 đồng
Giảm giá nhóm (6 người lớn, đạt mức từ 5 người):
Số tiền giảm: 2.660.000 × 10% = 266.000 đồng
Còn lại: 2.660.000 − 266.000 = 2.394.000 đồng
Phí X-quang: 3 × 150.000 = 450.000 đồng
Tổng tiền: 2.394.000 + 450.000 = 2.844.000 đồng
</suy_luan>

[RESULT: 2.844.000 đồng]
```

**Link trò chuyện:** https://claude.ai/share/cbee143a-8845-4099-a555-62ccc685e7f9

### b) Kiểm tra kết quả AI

ai đúng kết quả

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{"loai_su_co": "tre_hen", "so_khach": 3, "so_lan_bi_tre": 2, "tom_tat": "Gia đình 3 khách chờ hơn 1 tiếng cả 2 lần hẹn, đề nghị giải quyết."}
```

**Link trò chuyện:** https://claude.ai/share/0cb12543-b346-40c1-b5c9-ff749ea6c7b5

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
|---|---|---|---|
| **Đúng thông tin (50%)** | **Chưa chấm** (tối đa 5) | Bài nêu "450k/răng" và "Bong sau 8 tháng thì em làm lại free". Chưa có thông tin chuẩn để đối chiếu. Câu bảo hành cũng mơ hồ: bong **trong** hay **sau** 8 tháng? | Bổ sung giá và chính sách bảo hành chuẩn để chốt điểm. Viết rõ thời hạn, điều kiện bảo hành theo chính sách đó. |
| **Đầy đủ (30%)** | **1,5/3** (chia đều 2 yêu cầu) | Có trả lời về giá và bảo hành (hiểu đây là hai câu khách hỏi, vì đề không kèm tin nhắn của khách). Chưa mời khách cung cấp ngày hẹn và khung giờ; "Cần gì cứ inbox" chưa đáp ứng yêu cầu này. | Thêm: "Anh vui lòng cho em xin ngày hẹn và khung giờ thuận tiện để em đặt lịch ạ." |
| **Giọng điệu (20%)** | **1/2** | Lịch sự ở "Dạ chào anh", "ạ". Còn suồng sã hoặc thiếu chuyên nghiệp: "450k", "thôi", "luôn", "free", "Cần gì cứ inbox". Ghi chú yêu cầu cho 10/10 không được dùng làm căn cứ chấm. | Đổi "450k" thành "450.000 đồng", "free" thành "miễn phí" (nếu đúng chính sách), "inbox" thành "nhắn tin". Bỏ "thôi", "luôn" và cam kết "đẹp như răng thật". |

**Tổng điểm: chưa chốt /10** (đã chấm được 2,5/5 điểm của hai tiêu chí sau; tổng có thể từ 2,5 đến 7,5/10, tùy kết quả đối chiếu thông tin)
```

**Link trò chuyện:** https://claude.ai/share/87d0bfbb-1923-47c8-8a75-076124e28b31
