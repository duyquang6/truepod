# Truepod Beta — Điều khoản

*[English](TERMS.md)* · Phiên bản 1, 27-09-2026

Đây là bản **beta**. Nó miễn phí, và thứ nó xin lại là được gửi log của chính
nó về để tìm và sửa lỗi. Dùng bản beta nghĩa là bạn đồng ý điều đó.

Nói rõ ra thì:

## Gửi cái gì

Sau mỗi phiên, khi bạn đã thoát ứng dụng, nó tải lên **file log của chính nó**
— đúng cái `truepod.log` nằm trong thư mục app trên thẻ của bạn. Bạn mở ra đọc
được bất cứ lúc nào để biết chính xác trong đó có gì.

Nếu lúc thoát không có mạng, log sẽ chờ trên thẻ của bạn, trong
`Saves/truepod/outbox`, và được gửi vào lần tới bạn mở hoặc thoát Truepod khi có
Wi-Fi. Gửi xong
thì nó bị xoá khỏi đó. Tối đa 20 log mới nhất được giữ lại chờ gửi.

Log chứa:

- Bạn đang dùng máy nào, firmware nào, và bản Truepod nào
- Phần cứng âm thanh đã làm gì: tần số, độ sâu bit, thiết bị nào được mở, đầu
  ra là bit-perfect hay đã bị chuyển đổi
- Lỗi, sự cố về thời gian, và các lần thử khôi phục
- **Tên và đường dẫn các file bạn đã phát.** Đây là phần bạn tắt được — xem
  bên dưới.

Có kèm một mã định danh ngẫu nhiên cho lần cài đặt này, để nhiều log từ cùng
một máy đọc chung được. Nó sinh ra ở lần chạy đầu tiên và không suy ra từ bất
cứ thứ gì về bạn hay phần cứng của bạn.

## Không bao giờ gửi

- Nhạc của bạn, hay bất kỳ phần nào của nó. Không âm thanh, không ảnh bìa.
- Bất kỳ thông tin đăng nhập, token, mã ghép nối hay chi tiết tài khoản nào.
- Vị trí, danh bạ, hay bất cứ thứ gì khác trên máy.

## Tắt phần nhạy cảm

Trong Options có công tắc **tên file trong log**. Tắt nó đi thì trình phát sẽ
che tên và đường dẫn nhạc của bạn trước khi log được gửi. Phần kỹ thuật —
phần cứng, định dạng, lỗi — vẫn gửi, vì đó mới là thứ khiến bản beta đáng chạy.

Phần log kỹ thuật cơ bản là một phần của việc tham gia beta và không tắt được.
Nếu bạn không muốn gửi bất cứ thứ gì, đừng cài bản beta.

## Gửi đi đâu và giữ bao lâu

Báo cáo đi tới kho lưu trữ do tác giả Truepod quản lý và được giữ **60 ngày**,
sau đó tự động xoá. Chúng dùng để sửa lỗi. Không bán, không chia sẻ cho bên thứ
ba, không dùng cho quảng cáo.

## Không bảo hành

Phần mềm beta, cung cấp nguyên trạng, không bảo hành dưới bất kỳ hình thức nào.
Nó phát nhạc trên một chiếc máy chơi game cầm tay; đừng dùng nó vào việc mà sự
cố gây hậu quả.

## Thay đổi

Nếu điều khoản thay đổi theo hướng ảnh hưởng tới những gì được thu thập, ứng
dụng sẽ hỏi lại bạn trước khi tiếp tục.

## Liên hệ

Mở một issue trên repo này.
