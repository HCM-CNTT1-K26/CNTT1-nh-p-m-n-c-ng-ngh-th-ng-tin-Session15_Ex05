# CNTT1-nh-p-m-n-c-ng-ngh-th-ng-tin-Session15_Ex05
### 1. Tin nhắn mẫu (Chuẩn Asynchronous & Không No-Hello)

Gửi team, tớ ghim lại chi tiết lỗi login ở đây để các bạn ở bên Nhật với Mỹ lúc vào ca làm việc xem giúp tớ nhé, không gấp đâu.

* **Hiện trạng:** Bị crash lỗi 500 ở API `/api/v1/auth/login` ngay sau khi merge nhánh `feature/oauth`.
* **Chi tiết log:** Báo `NullPointerException` tại dòng 45 file `AuthService.java`.
* **Cách test lại lỗi:** Chạy branch `main` trên máy local, gửi request POST login bình thường là bị văng. Tớ có chụp lại log terminal với xuất file `error.log` vứt trong folder Drive chung của nhóm rồi.
* **Đã thử xử lý:** Tớ check lại biến môi trường trong `.env` thì thấy khai báo chuẩn rồi, chắc kẹt ở luồng xử lý token.

Lúc nào mọi người online làm việc thì ngó qua hỗ trợ tớ nha!

---

### 2. Lịch trình gửi tin nhắn (Schedule Send)

Để tránh nhảy notification làm phiền lúc đồng đội đang ngủ, tớ cài Schedule Send trên Slack/Teams/Gmail theo các mốc sau:

* **Gửi cho bạn ở Nhật Bản (GMT+9 - Nhanh hơn VN 2 tiếng):**
* *Tình huống:* Nếu tớ viết tin nhắn lúc 22:00 giờ VN (bên Nhật là 24:00 đêm).
* *Lịch hẹn gửi (Schedule Send):* Cài **08:15 sáng giờ Nhật** (tương đương 06:15 sáng giờ VN). Vừa kịp lúc bạn ấy dậy chuẩn bị vào ca, mở máy lên là thấy ngay thông tin đầy đủ.


* **Gửi cho bạn ở Mỹ (Giờ Bờ Tây PDT - Chậm hơn VN 14 tiếng):**
* *Tình huống:* Viết tin nhắn lúc 22:00 giờ VN (bên Mỹ đang là 08:00 sáng cùng ngày, họ bắt đầu làm việc). Nhưng nếu viết lúc 14:00 chiều VN (bên Mỹ là 00:00 đêm).
* *Lịch hẹn gửi (Schedule Send):* Cài **08:30 sáng giờ Mỹ** (tương đương 22:30 đêm giờ VN). Tin nhắn sẽ nằm ngay đầu hòm thư khi bạn ấy ngủ dậy mở máy làm ca mới.
