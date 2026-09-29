# Truepod

Trình phát nhạc bit-perfect cho **TrimUI Brick Pro**.

*[English](README.md)*

Mọi trình phát khác trên máy này đều phải hy sinh một thứ gì đó. Có cái giới
hạn đầu ra ở 44.1 kHz hoặc 16-bit, có cái resample hết về 48 kHz. Nút âm lượng
không chỉnh được volume của DAC USB. Nhạc bị giật, bị lag, bị nhảy bài. Và phải
để màn hình sáng thì nhạc mới chạy, nên rất tốn pin.

Truepod khắc phục tất cả:

- **Chất lượng đầy đủ.** Phát file đúng sample rate và bit depth của nó, và nói
  cho bạn biết khi không làm được.
- **Nút âm lượng chỉnh được DAC.** Với DAC USB, nút âm lượng chỉnh volume phần
  cứng của chính DAC, nên dữ liệu âm thanh không bị đụng tới.
- **Không giật, không nhảy bài.** Âm thanh có một nhân CPU riêng, tách khỏi phần
  còn lại của hệ thống. Tạm dừng hay cắm lại DAC không bao giờ bị tính là hết
  bài.
- **Tắt màn hình, nhạc vẫn chạy.** Tắt màn hình là CPU xuống chế độ tiết kiệm
  điện nhất, còn nhạc vẫn phát.

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

## Tính năng

✅ là có trong Free, ❌ là dự kiến cho bản **Truepod Pro**, chưa phát hành. Bản
Free giữ nguyên tập tính năng hiện tại: sửa lỗi, không thêm tính năng.

| | Free | Pro |
|---|:---:|:---:|
| Hi-res: 24-bit và sample rate cao, đã test tới 88.2 kHz | ✅ | ✅ |
| Bit-perfect qua USB DAC cổng trên | ✅ | ✅ |
| FLAC, MP3, WAV, OGG, Opus, M4A / AAC / ALAC | ✅ | ✅ |
| Nhãn BIT-PERFECT / CONVERTED đọc từ sound card | ✅ | ✅ |
| Duyệt theo thư mục, hiện rate và bit depth thật, cover art, xoá bài | ✅ | ✅ |
| Shuffle, repeat all / one / off | ✅ | ✅ |
| Upload qua Wi-Fi bằng QR code | ✅ | ✅ |
| Hiển thị phổ nhạc, LED nháy theo nhịp | ✅ | ✅ |
| Tắt màn hình mà nhạc vẫn chạy | ✅ | ✅ |
| spruceOS và firmware TrimUI gốc | ✅ | ✅ |
| Duyệt theo nghệ sĩ và album, tìm kiếm, playlist `.m3u` | ❌ | ✅ |
| Yêu thích, hàng đợi sửa được, nhớ vị trí từng bài | ❌ | ✅ |
| Gapless, EQ | ❌ | ✅ |
| Đồng bộ và stream nhạc từ Telegram, Spotify, SoundCloud… | ❌ | ✅ |
| Dùng cổng USB dưới làm DAC | ❌ | ✅ |
| Cập nhật qua mạng (OTA) | ❌ | ✅ |
| Nhiều layout màn hình, nhiều chế độ LED | ❌ | ✅ |
| Hẹn giờ tắt | ❌ | ✅ |
| Giao diện tiếng Việt | ❌ | ✅ |

## Báo lỗi

Mở issue, ghi firmware, phiên bản, và đính kèm `truepod.log` trong thư mục app
trên thẻ. Mấy dòng đầu của nó nói firmware của bạn có sẵn những gì, thường chỉ
cần vậy là đủ giải thích vì sao hai máy chạy khác nhau.

---

Chỉ chứa bản phát hành và tài liệu; mã nguồn chưa công khai. Truepod là phần
mềm mã nguồn đóng — xem [LICENSE](LICENSE).
