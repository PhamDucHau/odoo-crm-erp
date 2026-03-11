## Odoo 18 với Docker Compose

### Cấu trúc

- **docker-compose.yml**: định nghĩa service `odoo` và `db` (PostgreSQL).
- **odoo.conf**: file cấu hình Odoo (kết nối DB, `addons_path`, v.v).
- **addons/**: nơi để custom module, được mount vào container tại `/mnt/extra-addons`.

### Cách chạy

1. Cài Docker & Docker Compose (hoặc Docker Desktop).
2. (Khuyến nghị) Tạo thư mục addons:
   ```bash
   mkdir -p addons
   ```
3. Chạy Odoo:
   ```bash
   docker compose up -d
   ```
4. Mở trình duyệt và vào:
   - `http://localhost:8069`

Database mặc định:
- **Postgres user**: `odoo`
- **Postgres password**: `odoo`
- **Postgres host**: `db`

Khi tạo database mới trong giao diện Odoo, bạn dùng user/password ở trên.

