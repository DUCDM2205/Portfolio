# Portfolio Đỗ Minh Đức — Hướng dẫn sử dụng

Website HTML/CSS/JavaScript thuần, không cần npm, không có backend. Mở index.html bằng trình duyệt để xem; có thể dùng extension Live Server trong VS Code. Google Fonts cần Internet; khi offline website dùng font hệ thống.

## File cần biết
- index.html: cấu trúc, giới thiệu, kinh nghiệm, liên hệ. Nội dung song ngữ nằm trong data-en và data-vi.
- styles.css: giao diện, responsive và hiệu ứng.
- script.js: chuyển ngôn ngữ, bộ lọc, dialog và ước tính giờ tiết kiệm.
- project-data.js: nội dung case study thực tế được website dùng. Sửa file này khi cập nhật dự án. Không cần chỉnh projects.json (bản tham khảo dữ liệu).
- assets/: hình minh họa và CV Anh–Việt đã đính kèm.

## 1. Thay ảnh cá nhân
Đưa ảnh vào assets/profile.jpg. Trong index.html tìm:

```html
<span class="monogram">đ.</span>
```

Thay bằng:

```html
<img src="assets/profile.jpg" alt="Đỗ Minh Đức" width="500" height="600">
```

Có thể dùng ảnh JPG/PNG/WebP; nếu đổi tên file phải sửa src tương ứng. CSS tự căn ảnh theo khung.

## 2. Email, điện thoại, LinkedIn và GitHub
Trong index.html tìm `EDIT CONTACT LINKS HERE`.

```html
<a href="mailto:YOUR_EMAIL">YOUR_EMAIL ↗</a>
<a href="tel:+84777800720">0777 800 720 ↗</a>
<a href="https://www.linkedin.com/in/YOUR_PROFILE/" target="_blank" rel="noopener noreferrer">LinkedIn ↗</a>
<a href="https://github.com/YOUR_USERNAME" target="_blank" rel="noopener noreferrer">GitHub ↗</a>
```

Email và LinkedIn hiện được điền từ CV/thông tin đã cung cấp. GitHub chưa có tài khoản xác nhận nên chưa hiển thị: bỏ comment quanh dòng ADD GITHUB và điền username.

## 3. Thay hình dự án
Hình hiện tại là SVG minh họa workflow được thiết kế cho portfolio, KHÔNG phải ảnh chụp tool thật. Không tìm được ảnh gốc trong lần truy xuất này.

Cách nhanh: đưa ảnh thật vào assets/commerce.png, assets/migration.png, assets/nexus.png. Trong script.js tìm hai chỗ `assets/${p.id}.svg` và thay `.svg` bằng `.png`. Tên ID:
- commerce: KTP / Thành Nhân.
- migration: VA Schools URL Auditor.
- nexus: Nexus Intelligence.

Sau khi toàn bộ hình đã là ảnh thật: sửa nhãn `ILLUSTRATIVE INTERFACE...`, `GIAO DIỆN MINH HỌA...` cùng các alt tương ứng trong script.js; bỏ nhãn minh họa khỏi ảnh gốc nếu còn. Ưu tiên ảnh ngang khoảng 1600×1000. Che API key, dữ liệu khách hàng, lead và thông tin nhạy cảm trước khi đăng.

## 4. Cập nhật CV
Thay assets/cv-en.pdf và assets/cv-vi.pdf bằng bản mới giữ nguyên tên. Nút tải tự chọn theo ngôn ngữ website.
Lưu ý: CV Anh người dùng cung cấp có phần mô tả Trường Thịnh/Thành Nhân lặp lại từ vị trí TLT; portfolio dùng mô tả tương ứng trong CV Việt. Nên rà CV Anh trước khi gửi nhà tuyển dụng. Hai PDF đính kèm được giữ nguyên.

## 5. Upload GitHub Pages
1. Giải nén ZIP, mở thư mục portfolio.
2. Tạo repository trên GitHub, ví dụ `portfolio`.
3. Upload NỘI DUNG bên trong thư mục portfolio vào gốc repository: index.html, styles.css, script.js, project-data.js, assets/... Không upload cả ZIP.
4. Vào Settings → Pages → Build and deployment → Source: Deploy from a branch.
5. Chọn branch main, thư mục /(root), bấm Save.
6. Khi GitHub hoàn tất, dùng URL Pages được hiển thị ở đó. Nếu repository tên YOUR_USERNAME.github.io thì website ở domain gốc; repo khác có thêm đường dẫn tên repo.

Không cần cấu hình build. Đường dẫn tương đối hỗ trợ cả hai kiểu URL.

## Nội dung và phạm vi
Định hướng theo JD AI Transformation Consultant, Intrepid: https://intrepid.bamboohr.com/careers/1515 (đọc ngày 21/10/2026). Không trình bày là nhân viên hay đối tác Intrepid.
- Dự án: workflow sản phẩm, migration SEO, Nexus Intelligence.
- Trạng thái được tách thành workflow áp dụng, prototype và roadmap.
- Hơn 2/3 thời gian: ước tính tự báo cáo tổng thể, chưa benchmark từng dự án.
- Chỉ số WESET lấy từ CV, không tự thêm kết quả AI/ROI.
- Không tự nhận kinh nghiệm production n8n, Langflow hoặc AI agent khi chưa xác nhận.
- Bộ tính giờ là minh họa; không phải ROI ròng hay số liệu dự án.
- Không có form gửi dữ liệu hoặc tính năng upload công khai; liên hệ qua email/điện thoại.

## Kiểm tra
Đã kiểm tra cú pháp JS và mở website trên trình duyệt desktop; chuyển EN→VI, đổi CV theo ngôn ngữ và mở case study hoạt động. Responsive được cài đặt bằng CSS; chưa kiểm thử trực tiếp trên thiết bị điện thoại thật. Không có build step.
