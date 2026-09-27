# Truepod 0.1.0 — first public beta

*The body of the GitHub release. Copy it into the release, or pass it with
`gh release create --notes-file RELEASE.md`. Vietnamese follows the English.*

---

A bit-perfect music player for the **TrimUI Brick Pro**. Every other player on
this handheld caps its output at compile time — 44.1 kHz, or 48, or 16-bit.
Truepod plays the file you actually have, and when the hardware cannot, it says
so instead of pretending.

Free, and the quality is not the paid part. There is no output ceiling in this
build and there will not be one.

## Download

| Your firmware | File |
|---|---|
| spruceOS | `Truepod-0.1.0-spruceOS.zip` |
| stock TrimUI | `Truepod-0.1.0-stockOS.zip` |

Same player in both. They differ only in which directory the firmware looks in,
and each archive carries an `INSTALL.txt` repeating the one below.

## Install

1. Unzip. You get a `Truepod` folder.
2. Copy it onto the SD card: **spruceOS → `/mnt/SDCARD/App/`**, **stock TrimUI →
   `/mnt/SDCARD/Apps/`**. You should end up with `…/Truepod/truepod`.
3. Put music in `/mnt/SDCARD/MEDIA`. Subfolders are how you browse it.
4. Boot, open **Truepod**, agree to the beta terms.

No installer, no patching the firmware, nothing written outside the card.
Delete the folder to uninstall.

## What it does

- **Bit-perfect** through a USB DAC on the **top** port, at the file's own rate
  and bit depth — verified to 88.2 kHz / 24-bit.
- **The fidelity badge is read from the kernel**, not from the player's opinion
  of itself: `BIT-PERFECT` and `CONVERTED` describe what the sound card actually
  negotiated.
- FLAC, MP3, WAV, OGG, Opus, M4A / AAC / ALAC.
- Folder browser showing each track's real rate and bit depth **before** you
  play it. Embedded cover art. Remembers where you were.
- **Wi-Fi upload from a QR code** — get music on without pulling the card.
- Spectrum visualiser on screen and across the **RGB LEDs**, driven by the music
  rather than by the volume. Switch them off in Options if you prefer.
- **Screen off, music on**: click the right stick.
- Runs on **spruceOS and on stock TrimUI firmware**.

The device has no manual and its buttons are unlabelled, so **SELECT opens
Options, and Options is the manual** — every binding is listed there.

## Two things that look like bugs

**"It says CONVERTED."** The built-in speaker runs a fixed 48 kHz clock, so
44.1 kHz music — most music — must be resampled for it. Truepod reports that
honestly rather than claiming otherwise. Plug a USB DAC into the top port and
the same file plays `BIT-PERFECT`.

**"The battery drains while it sits idle."** The device will not sleep while
Truepod is open: this firmware's sleep kills playback and never resumed
cleanly, so the player prevents it. Click the right stick to blank the screen
with the music playing, or quit with **MENU** and the device sleeps normally.

## Beta diagnostics

This build uploads **its own log** — the `truepod.log` in the app folder, which
you can read — after you quit. Never your music, never a credential, nothing
while you are listening. File names in it can be switched off in Options. It
asks you to agree on first launch; declining quits. See
**[Terms](TERMS.md)** ([Tiếng Việt](TERMS.vi.md)).

## Known limitations

- No sleep while the app is open; quit to let the device sleep.
- On stock firmware nothing stops the firmware suspending mid-track.
- No gapless playback yet.
- Tested to 88.2 kHz. Higher rates are untested rather than known-bad.

## Later

**Free:** sleep timer, favourites, per-track resume, an editable queue, gapless.

**Truepod Pro** — planned, not released: a tag index with artist/album browsing
and search, saved playlists, Telegram sync, EQ, and hot-switching a USB DAC on
the bottom port. Pro will never gate output quality or basic playback.

## Something broken?

Open an issue with your firmware, this version, and `truepod.log` from the app
folder. Its first lines name what your firmware provides, which usually
explains a difference between two devices immediately.

---
---

# Truepod 0.1.0 — bản beta công khai đầu tiên

Máy nghe nhạc **bit-perfect** cho **TrimUI Brick Pro**. Mọi player khác trên máy
này đều chặn chất lượng đầu ra ngay lúc biên dịch — 44.1 kHz, hoặc 48, hoặc
16-bit. Truepod phát đúng file bạn có, và khi phần cứng không làm được thì nó
**nói thẳng** thay vì giả vờ.

Miễn phí, và chất lượng không phải là phần thu phí. Bản này không có trần chất
lượng, và sẽ không bao giờ có.

## Tải về

| Firmware của bạn | File |
|---|---|
| spruceOS | `Truepod-0.1.0-spruceOS.zip` |
| TrimUI gốc | `Truepod-0.1.0-stockOS.zip` |

Cùng một player. Khác nhau duy nhất ở thư mục mà firmware tìm app, và mỗi file
nén đều kèm `INSTALL.txt` nhắc lại hướng dẫn dưới đây.

## Cài đặt

1. Giải nén. Bạn được một thư mục `Truepod`.
2. Copy vào thẻ SD: **spruceOS → `/mnt/SDCARD/App/`**, **TrimUI gốc →
   `/mnt/SDCARD/Apps/`**. Kết quả phải là `…/Truepod/truepod`.
3. Để nhạc vào `/mnt/SDCARD/MEDIA`. Các thư mục con chính là cách bạn duyệt nhạc.
4. Khởi động máy, mở **Truepod**, đồng ý điều khoản beta.

Không cần installer, không vá firmware, không ghi gì ra ngoài thẻ. Xoá thư mục
là xong gỡ.

## Có gì

- **Bit-perfect** qua USB DAC cắm cổng **trên**, đúng sample rate và bit depth
  của file — đã đo tới 88.2 kHz / 24-bit.
- **Nhãn chất lượng đọc từ kernel**, không phải từ player tự khai: `BIT-PERFECT`
  và `CONVERTED` mô tả đúng cái mà sound card thật sự đã thương lượng được.
- FLAC, MP3, WAV, OGG, Opus, M4A / AAC / ALAC.
- Browser theo thư mục, hiện sample rate và bit depth thật của từng bài **trước
  khi** phát. Cover art nhúng trong file. Nhớ thư mục lần trước đang mở.
- **Upload qua Wi-Fi bằng QR code** — đưa nhạc vào máy không cần rút thẻ.
- Spectrum hiển thị trên màn hình và trên **dàn LED RGB**, chạy theo nhạc chứ
  không theo âm lượng. Không thích thì tắt trong Options.
- **Tắt màn hình, nhạc vẫn chạy**: bấm nút cần analog phải.
- Chạy được trên **spruceOS và cả firmware TrimUI gốc**.

Máy này không có sách hướng dẫn và các nút thì không ghi nhãn, nên **SELECT mở
Options, và Options chính là sách hướng dẫn** — mọi phím đều liệt kê ở đó.

## Hai thứ trông như bug nhưng không phải

**"Nó ghi CONVERTED."** Loa trong máy chạy clock cố định 48 kHz, nên nhạc
44.1 kHz — tức là phần lớn nhạc — buộc phải resample. Truepod báo thật chuyện
đó chứ không nhận vơ. Cắm USB DAC vào cổng trên thì đúng file đó phát
`BIT-PERFECT`.

**"Để không mà vẫn tụt pin."** Máy sẽ không ngủ khi Truepod đang mở: cơ chế
sleep của firmware này giết luôn playback và chưa bao giờ resume sạch, nên
player chặn nó. Bấm cần analog phải để tắt màn hình mà nhạc vẫn chạy, hoặc
thoát bằng **MENU** thì máy ngủ bình thường.

## Diagnostics của bản beta

Bản này gửi lên **log của chính nó** — file `truepod.log` trong thư mục app, bạn
đọc được — sau khi bạn thoát. Không có nhạc của bạn, không có mật khẩu, và
không gửi gì trong lúc bạn đang nghe. Tên file trong log có thể tắt trong
Options. App hỏi bạn đồng ý ở lần mở đầu tiên; không đồng ý thì nó thoát. Xem
**[Điều khoản](TERMS.vi.md)**.

## Hạn chế đã biết

- Máy không ngủ khi app đang mở; thoát ra thì ngủ.
- Trên firmware gốc, không có gì chặn firmware suspend giữa bài.
- Chưa có gapless.
- Chỉ mới test tới 88.2 kHz. Cao hơn là *chưa test*, không phải là không chạy.

## Sắp tới

**Free:** hẹn giờ tắt, favourite, nhớ vị trí từng bài, queue sửa được, gapless.

**Truepod Pro** — đang lên kế hoạch, chưa phát hành: index theo tag để duyệt
artist/album và tìm kiếm, playlist lưu được, Telegram sync, EQ, và đổi nóng USB
DAC ở cổng dưới. Pro sẽ không bao giờ khoá chất lượng đầu ra hay thao tác phát
nhạc cơ bản.

## Gặp lỗi?

Mở issue kèm firmware bạn dùng, phiên bản này, và file `truepod.log` trong thư
mục app. Mấy dòng đầu của nó cho biết firmware của bạn cung cấp những gì —
thường giải thích ngay khác biệt giữa hai máy.
