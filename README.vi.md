# Truepod

Trình phát nhạc bit-perfect cho **TrimUI Brick Pro**.

*[English](README.md)*

Mọi trình phát khác trên máy này đều chốt chất lượng đầu ra ngay lúc biên dịch:
44.1 kHz, hoặc 48, hoặc 16-bit. Truepod phát file đúng sample rate và bit depth
của nó, và nói cho bạn biết khi không làm được.

## Tải về

Chọn bản đúng với firmware của bạn ở **[bản phát hành mới nhất](../../releases/latest)**:

| Firmware | File |
|---|---|
| spruceOS | `Truepod-<phiên-bản>-spruceOS.zip` |
| TrimUI gốc | `Truepod-<phiên-bản>-stockOS.zip` |

Cùng một trình phát. Chỉ khác thư mục mà firmware tìm app.

## Cài đặt

1. Giải nén, được một thư mục `Truepod`.
2. Copy vào thẻ SD. spruceOS: `/mnt/SDCARD/App/`. TrimUI gốc: `/mnt/SDCARD/Apps/`.
   Kết quả phải là `…/Truepod/truepod`.
3. Để nhạc vào `/mnt/SDCARD/MEDIA`. Các thư mục con chính là cách bạn duyệt nhạc.
4. Khởi động máy và mở **Truepod**.

## Hướng dẫn

| Nút | Danh sách nhạc | Đang phát |
|---|---|---|
| D-pad lên/xuống | di chuyển | — |
| A | mở thư mục, hoặc phát | play / pause |
| B | lùi ra thư mục cha | về danh sách |
| X | xoá bài (hỏi lại) | bật / tắt shuffle |
| Y | upload Wi-Fi | repeat all / one / off |
| L1 / R1 | lật trang | bài trước / bài sau |
| L2 / R2 | — | tua 10 giây |
| START | sang Đang phát | về danh sách |

Dùng được ở mọi màn hình: **SELECT** mở Options, **MENU** thoát, **bấm cần
analog phải** tắt màn hình mà nhạc vẫn chạy, và hai nút cạnh máy là âm lượng.

Muốn thêm nhạc mà không có đầu đọc thẻ: bấm **Y** trong danh sách nhạc rồi quét
mã QR bằng điện thoại cùng mạng.

## Free và Pro

Bản Free giữ nguyên tập tính năng hiện tại: sửa lỗi, không thêm tính năng.
**Truepod Pro** đang lên kế hoạch và chưa phát hành — chưa có gì dưới đây được
bán.

| | Free | Pro |
|---|:---:|:---:|
| **Phát nhạc** | | |
| Bit-perfect qua USB DAC cổng trên | ✅ | ✅ |
| FLAC, MP3, WAV, OGG, Opus, M4A / AAC / ALAC | ✅ | ✅ |
| Nhãn BIT-PERFECT / CONVERTED đọc từ sound card | ✅ | ✅ |
| Shuffle, repeat all / one / off | ✅ | ✅ |
| Gapless | ❌ | ✅ |
| EQ | ❌ | ✅ |
| Đổi nóng USB DAC ở cổng dưới | ❌ | ✅ |
| **Thư viện** | | |
| Duyệt theo thư mục, hiện sample rate và bit depth thật của từng bài | ✅ | ✅ |
| Cover art nhúng trong file | ✅ | ✅ |
| Xoá bài, nhớ thư mục lần trước | ✅ | ✅ |
| Duyệt theo nghệ sĩ và album (index tag) | ❌ | ✅ |
| Tìm kiếm | ❌ | ✅ |
| Playlist lưu được dạng `.m3u` | ❌ | ✅ |
| Yêu thích | ❌ | ✅ |
| Hàng đợi sửa được | ❌ | ✅ |
| Nhớ vị trí từng bài | ❌ | ✅ |
| **Đưa nhạc vào máy** | | |
| Upload qua Wi-Fi bằng QR code | ✅ | ✅ |
| Đồng bộ Telegram | ❌ | ✅ |
| **Màn hình và thiết bị** | | |
| Hiển thị phổ nhạc, LED nháy theo nhịp | ✅ | ✅ |
| Tắt màn hình mà nhạc vẫn chạy | ✅ | ✅ |
| Chạy trên spruceOS và firmware TrimUI gốc | ✅ | ✅ |
| Nhiều layout màn hình để chọn | ❌ | ✅ |
| Nhiều chế độ LED | ❌ | ✅ |
| Hẹn giờ tắt | ❌ | ✅ |
| Giao diện tiếng Việt | ❌ | ✅ |

Pro sẽ không khoá chất lượng đầu ra. Bản Free không có trần chất lượng và sẽ
không bao giờ có — đó chính là lý do trình phát này tồn tại.

## Báo lỗi

Mở issue, ghi firmware, phiên bản, và đính kèm `truepod.log` trong thư mục app
trên thẻ. Mấy dòng đầu của nó nói firmware của bạn có sẵn những gì, thường chỉ
cần vậy là đủ giải thích vì sao hai máy chạy khác nhau.


---

Chỉ chứa bản phát hành và tài liệu; mã nguồn chưa công khai. Truepod là phần
mềm mã nguồn đóng — xem [LICENSE](LICENSE).
