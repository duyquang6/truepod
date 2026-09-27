# Truepod 0.1.0 — bản beta công khai đầu tiên

*[English](https://github.com/duyquang6/truepod/blob/main/RELEASE.en.md)*

Máy nghe nhạc bit-perfect cho TrimUI Brick Pro.

Mọi player khác trên máy này đều chốt chất lượng đầu ra ngay lúc biên dịch:
44.1 kHz, hoặc 48, hoặc 16-bit. Truepod phát file đúng sample rate và bit depth
của nó, và nói cho bạn biết khi không làm được.

Miễn phí. Chất lượng không phải phần thu phí, và bản này không có trần chất
lượng.

## Tải về

| Firmware của bạn | File |
|---|---|
| spruceOS | `Truepod-0.1.0-spruceOS.zip` |
| TrimUI gốc | `Truepod-0.1.0-stockOS.zip` |

Cùng một player. Chỉ khác thư mục mà firmware tìm app.

## Cài đặt

1. Giải nén, được một thư mục `Truepod`.
2. Copy vào thẻ SD. spruceOS: `/mnt/SDCARD/App/`. TrimUI gốc: `/mnt/SDCARD/Apps/`.
   Kết quả phải là `…/Truepod/truepod`.
3. Để nhạc vào `/mnt/SDCARD/MEDIA`. Các thư mục con chính là cách bạn duyệt nhạc.
4. Khởi động máy và mở Truepod.

## Tính năng

- Bit-perfect qua USB DAC cắm cổng trên, đã test tới 88.2 kHz / 24-bit.
- FLAC, MP3, WAV, OGG, Opus, M4A / AAC / ALAC.
- Browser hiện sample rate và bit depth thật của từng bài trước khi phát, kèm
  cover art nhúng trong file. Nhớ thư mục lần trước đang mở.
- Upload qua Wi-Fi bằng QR code, thêm nhạc không cần rút thẻ.
- Hiển thị phổ nhạc trên màn hình, LED nháy theo nhịp nhạc. Tắt được trong
  Options.
- Tắt màn hình mà nhạc vẫn chạy.
- Shuffle và repeat all / one / off.
- Xoá bài ngay trong browser, có hỏi lại.
- Chạy trên spruceOS và cả firmware TrimUI gốc.

## Phím

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

## BIT-PERFECT và CONVERTED

Nhãn trên màn hình cho biết bạn đang nghe loại nào, và nó đọc từ sound card chứ
không phải từ player tự khai.

**BIT-PERFECT** — đúng những mẫu trong file đi tới DAC. Không có phần mềm nào
can thiệp.

**CONVERTED** — phần mềm phải sửa gì đó trên đường đi, thường là sample rate.
Loa trong máy chạy cố định 48 kHz, nên nhạc 44.1 kHz buộc phải resample. Cắm USB
DAC vào cổng trên thì nó nhận đúng rate của file, và bài đó phát bit-perfect.

## Hạn chế đã biết

- Máy không ngủ khi Truepod đang mở, nên vẫn tốn pin. Thoát bằng MENU thì máy
  ngủ bình thường.
- Trên firmware gốc, không có gì chặn firmware suspend giữa bài.
- Chưa có gapless.
- Chỉ mới test tới 88.2 kHz. Cao hơn là chưa test, không phải là không chạy.

## Sắp tới

Bản Free giữ nguyên tập tính năng hiện tại. Sửa lỗi, không thêm tính năng.

Truepod Pro, đang lên kế hoạch và chưa phát hành: hẹn giờ tắt, favourite, nhớ vị
trí từng bài, queue sửa được, gapless, index theo tag để duyệt theo artist và
album, tìm kiếm, playlist lưu được, Telegram sync, EQ, đổi nóng USB DAC ở cổng
dưới, nhiều layout màn hình để chọn, và thêm nhiều chế độ LED. Pro sẽ không khoá
chất lượng đầu ra.

## Gặp lỗi?

Mở issue kèm firmware bạn dùng, phiên bản này, và file `truepod.log` trong thư
mục app. Mấy dòng đầu của nó cho biết firmware của bạn cung cấp những gì, thường
giải thích ngay khác biệt giữa hai máy.

