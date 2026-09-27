# Truepod

Trình phát nhạc bit-perfect cho **TrimUI Brick Pro**.

*[English](README.md)*

Mọi trình phát khác trên máy này đều bị chặn chất lượng ngay từ lúc biên dịch.
Truepod phát đúng file bạn đang có — và khi phần cứng không cho phép, nó nói
thẳng chứ không giả vờ.

## Tải về

Chọn bản đúng với firmware của bạn ở **[bản phát hành mới nhất](../../releases/latest)**:

| Firmware | File |
|---|---|
| spruceOS | `Truepod-<phiên-bản>-spruceOS.zip` |
| TrimUI gốc | `Truepod-<phiên-bản>-stockOS.zip` |

Cùng một trình phát, chỉ đóng gói theo đúng chỗ mà mỗi firmware tìm app.

## Cài đặt

1. Giải nén, bạn được đúng một thư mục.
2. Chép thư mục đó vào thư mục **`App`** ở gốc thẻ nhớ (firmware gốc thì là
   **`Apps`** — trong zip có ghi lại).
3. Bỏ nhạc vào `/mnt/SDCARD/MEDIA`. Có thư mục con thì càng tốt, đó là cách bạn
   duyệt nhạc.
4. Khởi động máy và mở **Truepod**.

## Dùng thế nào

Máy này không ghi nhãn nút nào, nên **bấm SELECT để mở màn hình Options — đó
chính là sách hướng dẫn**, mọi phím đều liệt kê ở đó.

Mấy phím cần ngay: **A** phát, **B** quay lại, **START** vào màn hình đang
phát, **L1/R1** đổi bài. Âm lượng dùng hai nút bên hông.

Muốn đưa nhạc vào mà không có đầu đọc thẻ: mở **Wi-Fi upload** trong Options
rồi quét mã QR bằng điện thoại cùng mạng.

## Hai thứ trông như lỗi nhưng không phải

**"Sao nó ghi CONVERTED?"** Loa trong máy chạy xung nhịp cố định 48 kHz, nên
nhạc 44.1 kHz — tức phần lớn nhạc — bắt buộc phải resample. Truepod báo đúng
sự thật đó. Cắm USB DAC vào cổng **trên** thì chính file đó sẽ phát
BIT-PERFECT. Chỉ báo này đọc từ kernel chứ không phải app tự đánh giá mình.

**"Để yên mà vẫn tụt pin."** Máy sẽ không ngủ khi Truepod đang mở: chế độ ngủ
của firmware này giết luôn dòng phát và chưa lần nào tỉnh lại sạch sẽ, nên
trình phát chủ động chặn. Nhấn **cần analog phải** để tắt màn hình mà nhạc vẫn
chạy, hoặc thoát bằng **MENU** thì máy ngủ bình thường.

## Dữ liệu chẩn đoán

Bản beta gửi về **file log của chính nó** sau khi bạn thoát — cái `truepod.log`
trong thư mục app, bạn đọc được. Không bao giờ gửi nhạc, không mật khẩu, và
không gửi gì trong lúc bạn đang nghe. Tên file trong log thì tắt được trong
Options. Ứng dụng sẽ hỏi bạn đồng ý trước; chi tiết ở
**[Điều khoản](TERMS.vi.md)**.

## Sắp tới

Bản Free: hẹn giờ tắt, yêu thích, nhớ vị trí từng bài, hàng đợi sửa được,
gapless.

Bản **Truepod Pro** đang lên kế hoạch, chưa phát hành — index tag để duyệt theo
nghệ sĩ/album và tìm kiếm, playlist lưu được, đồng bộ Telegram, EQ, và
hot-switch USB DAC ở cổng dưới.

Pro sẽ không bao giờ khoá chất lượng đầu ra hay các thao tác cơ bản của một
trình phát. Bản Free không có trần chất lượng và sẽ không bao giờ có — đó chính
là lý do trình phát này tồn tại.

## Báo lỗi

Mở issue, ghi firmware, phiên bản, và đính kèm `truepod.log` trong thư mục app
trên thẻ. Mấy dòng đầu của nó nói firmware của bạn có sẵn những gì, thường chỉ
cần vậy là đủ giải thích vì sao hai máy chạy khác nhau.


---

Chỉ chứa bản phát hành và tài liệu; mã nguồn chưa công khai. Truepod là phần
mềm mã nguồn đóng — xem [LICENSE](LICENSE).
