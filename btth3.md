# báo cáo phân tích ipo: lấy lại quyền truy cập aws bằng backup codes

## input
- backup codes (mã dự phòng) đã lưu ở nơi an toàn (két, sổ giấy, trình quản lý mật khẩu mã hóa)
- tên đăng nhập và mật khẩu aws
- thiết bị mới hoặc máy tính đáng tin

## process
1. dùng máy an toàn, đăng nhập aws bằng tên đăng nhập và mật khẩu
2. ở bước mfa chọn "dùng mã dự phòng", nhập 1 backup code. mỗi mã chỉ dùng được 1 lần
3. vào được rồi thì xóa thiết bị mfa cũ (điện thoại bị mất) để kẻ nhặt được máy không dùng được
4. đổi mật khẩu và thu hồi các phiên đăng nhập, access key cũ
5. đăng ký lại mfa trên điện thoại mới
6. hủy toàn bộ backup codes cũ, tạo bộ mã mới và cất chỗ an toàn

## output
- vào lại được aws để bảo trì hệ thống
- mfa cũ và mã cũ không còn giá trị
- hệ thống an toàn, kẻ nhặt điện thoại không đăng nhập được

## tại sao không lưu backup codes dạng ảnh trong thư viện ảnh
- ảnh nằm cùng điện thoại, mất điện thoại là mất luôn mã, kẻ nhặt được chỉ cần mở thư viện là thấy
- ảnh dễ bị tự động đồng bộ lên icloud, google photos, nên nếu tài khoản đó bị hack thì lộ mã
- ảnh dễ bị app khác đọc, bị chia sẻ nhầm hoặc nằm trong bản sao lưu không mã hóa
- ảnh không có mật khẩu bảo vệ riêng