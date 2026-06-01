# MBA Bỏ Túi - Membership Site

Đây là bản web membership/knowledge portal dạng single-file HTML, dùng để quản lý và hiển thị nội dung học tập/kiến thức.

Repo này là bản deploy sạch, được tách riêng từ file backup `membership-site.html` để đưa lên GitHub và deploy lên Vercel.

## File chính

- `index.html`: toàn bộ website nằm trong file này.
- `.gitattributes`: giữ encoding/line ending ổn định khi đưa lên GitHub.

## Tài khoản admin demo

Đăng nhập bằng tài khoản sau để vào khu vực quản trị:

- Email: `admin@learnhub.com`
- Mật khẩu: `admin123`

## Tính năng chính

- Dashboard tổng quan cho người học.
- Thư viện kiến thức theo danh mục.
- Trang chi tiết nhóm nội dung/chương/bài viết.
- Admin quản lý nội dung theo cây: danh mục, nhóm nội dung, chương, bài viết.
- Trình soạn thảo bài viết có lưu nội dung, xem trước, chèn ảnh, video, HTML, box nội dung và callout.
- Quản lý thành viên, thêm thủ công, import CSV, export CSV.
- Cài đặt giao diện: tên web, mô tả, logo, favicon, màu sắc, font, popup/banner marketing.
- Link trong mục Tổng quan có thể thêm, sửa, xóa và sắp xếp.

## Cách mở trên máy

Tải repo về máy rồi mở trực tiếp file:

```text
index.html
```

Website hiện chạy hoàn toàn trên trình duyệt, không cần cài backend.

## Lưu dữ liệu

Bản hiện tại lưu dữ liệu bằng `localStorage` của trình duyệt:

- `lh_content`: dữ liệu danh mục, nhóm nội dung, chương, bài viết.
- `lh_users`: dữ liệu tài khoản/thành viên demo.
- `lh_settings`: dữ liệu cài đặt giao diện, logo, favicon, popup, link sidebar.

Lưu ý: dữ liệu localStorage chỉ nằm trên từng trình duyệt/máy. Nếu mở bằng trình duyệt khác hoặc xóa dữ liệu web, nội dung đã chỉnh có thể không còn.

## Deploy lên Vercel

1. Vào Vercel và chọn Add New Project.
2. Import repo GitHub này.
3. Giữ cấu hình mặc định vì đây là web tĩnh.
4. Bấm Deploy.

Sau khi deploy, Vercel sẽ cấp link dạng:

```text
https://ten-project.vercel.app
```

## Hướng phát triển tiếp theo

Bản này phù hợp để demo và dùng thử nhanh. Khi muốn chạy như sản phẩm thật, nên migrate sang:

- Next.js cho frontend/app structure.
- Supabase Auth cho đăng nhập và phân quyền.
- Supabase Database để lưu nội dung, thành viên, cài đặt.
- Supabase Storage để lưu logo, favicon, ảnh popup và ảnh trong bài viết.

