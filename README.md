# OpenClaw 🦞 — Trợ lý AI hỗ trợ phát triển Linh Đạo

<p align="center">
  <img src="https://raw.githubusercontent.com/openclaw/openclaw/main/docs/assets/openclaw-banner-dark.png" alt="OpenClaw — Trợ lý AI trên thiết bị của bạn" width="760">
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/Giấy_phép-MIT-green" alt="Giấy phép MIT"></a>
  <img src="https://img.shields.io/badge/Tài_liệu-Tiếng_Việt-blue" alt="Tài liệu tiếng Việt">
  <img src="https://img.shields.io/badge/Linh_Đạo-Đang_lên_kế_hoạch-orange" alt="Ứng dụng Linh Đạo đang lên kế hoạch">
</p>

**Bản fork cá nhân của Bùi Trung Sơn**, phục vụ học tập, tìm hiểu AI Agent và nghiên cứu ứng dụng OpenClaw vào quá trình phát triển game **Linh Đạo**.

> Repository này chứa nền tảng OpenClaw. Phần ứng dụng vào Linh Đạo hiện là ý tưởng và kế hoạch thử nghiệm, chưa phải một hệ thống hỗ trợ làm game đã được triển khai hoặc kiểm chứng. Tài liệu này không xác nhận repository đã chứa mã nguồn game.

[Dự án gốc](https://github.com/openclaw/openclaw) · [Tài liệu chính thức](https://docs.openclaw.ai) · [Hướng dẫn bắt đầu](https://docs.openclaw.ai/start/getting-started) · [Repository cá nhân](https://github.com/buitrungson09-maker/openclaw)

## Mục lục

1. [OpenClaw là gì?](#openclaw-la-gi)
2. [Mục tiêu bản fork](#muc-tieu)
3. [Ý tưởng game Linh Đạo](#linh-dao)
4. [Ứng dụng OpenClaw vào phát triển game](#ung-dung)
5. [Các vai trò AI](#vai-tro)
6. [Cài đặt và bắt đầu](#cai-dat)
7. [Làm việc với mã nguồn bản fork](#ma-nguon)
8. [Quy trình thực hiện một tính năng](#quy-trinh)
9. [Thử nghiệm linh khí và đột phá](#thu-nghiem)
10. [Lộ trình và đánh giá](#lo-trinh)
11. [Nguyên tắc sử dụng](#nguyen-tac)
12. [Trạng thái, tài liệu và giấy phép](#trang-thai)

<a id="openclaw-la-gi"></a>
## 1. OpenClaw là gì?

OpenClaw là trợ lý AI mã nguồn mở có thể chạy trên máy tính của người dùng. Nền tảng kết nối mô hình AI với công cụ, dữ liệu và các kênh giao tiếp đã cấu hình.

Các thành phần chính:

| Thành phần | Chức năng |
| --- | --- |
| Gateway | Quản lý phiên làm việc, công cụ, sự kiện và kết nối kênh |
| Control UI | Giao diện web để tương tác với hệ thống |
| CLI và TUI | Làm việc qua dòng lệnh hoặc giao diện terminal |
| Kênh giao tiếp | Kết nối trợ lý với dịch vụ nhắn tin được hỗ trợ |
| Công cụ, skills và plugins | Mở rộng khả năng thực hiện nhiệm vụ |
| Nhà cung cấp mô hình | Cung cấp mô hình AI cục bộ hoặc qua dịch vụ |

Khả năng đọc file, sửa mã nguồn, chạy lệnh hoặc thao tác GitHub phụ thuộc vào công cụ, quyền truy cập và cấu hình thực tế. Fork repository không tự động thiết lập những khả năng này.

<a id="muc-tieu"></a>
## 2. Mục tiêu bản fork

Một người tự làm game phải đảm nhiệm thiết kế, lập trình, kiểm thử, tài liệu và quản lý tiến độ. Bản fork này hướng đến xây dựng quy trình trợ lý AI bằng tiếng Việt để hỗ trợ các công việc đó.

Mục tiêu cụ thể:

- Chuyển ý tưởng thành yêu cầu có thể triển khai.
- Chia công việc thành những bước nhỏ, phù hợp với người mới học.
- Hỗ trợ viết và giải thích code.
- Đề xuất tình huống kiểm thử và phân tích lỗi.
- Ghi lại tiến độ, quyết định thiết kế và thay đổi.
- Đánh giá hiệu quả hỗ trợ dựa trên kết quả thực tế.

Phần đóng góp cá nhân dự kiến gồm tài liệu tiếng Việt, hướng dẫn vai trò, mẫu yêu cầu và quy trình thử nghiệm. OpenClaw và các thành phần gốc thuộc về tác giả, tổ chức và cộng đồng phát triển tương ứng.

<a id="linh-dao"></a>
## 3. Ý tưởng game Linh Đạo

### Bối cảnh và phong cách

**Linh Đạo** là ý tưởng game nhập vai hành động góc nhìn từ trên xuống. Người chơi vào vai một người tu luyện trẻ, khám phá vùng đất có linh khí, yêu thú, bí cảnh và môn phái.

Định hướng hình ảnh là pixel art, với nhân vật, trang bị và kỹ năng mang phong cách kiếm hiệp, tu luyện.

### Vòng lặp chơi chính

1. Chọn nhiệm vụ hoặc khu vực khám phá.
2. Chiến đấu và thu thập tài nguyên.
3. Trở về khu vực an toàn để hồi phục, chuẩn bị trang bị.
4. Hoàn thành điều kiện hoặc thử thách đột phá.
5. Mở khóa kỹ năng và khu vực mới.

Linh khí phục vụ tiến trình tu luyện. Việc phát triển nhân vật dự kiến kết hợp chiến đấu, khám phá và thử thách, tránh phụ thuộc hoàn toàn vào thời gian chờ.

### Các hệ thống dự kiến

| Hệ thống | Nội dung |
| --- | --- |
| Nhân vật | Di chuyển, máu, năng lượng và chỉ số |
| Chiến đấu | Đánh thường, né tránh, kỹ năng |
| Linh khí | Thu thập, tích lũy và sử dụng để đột phá |
| Cảnh giới | Mốc phát triển cùng điều kiện mở khóa |
| Trang bị | Vũ khí, vật phẩm hỗ trợ và nguyên liệu |
| Nhiệm vụ | Mục tiêu khám phá, chiến đấu, thu thập |
| Bản đồ | Khu vực an toàn, bãi quái, bí cảnh |
| Lưu tiến độ | Khôi phục dữ liệu nhân vật khi chơi lại |

### Phạm vi bản chơi thử

Bản đầu tiên dự kiến có một nhân vật, một bản đồ nhỏ, một loại quái, một đòn đánh, hệ thống máu, thu thập linh khí, một lần đột phá và lưu tiến độ.

Mục tiêu là hoàn thành một vòng chơi ngắn có thể trải nghiệm. Chơi trực tuyến, nhiều môn phái và thế giới rộng là hướng mở rộng sau khi nền tảng ổn định. Công nghệ làm game sẽ được lựa chọn và ghi lại khi triển khai.

<a id="ung-dung"></a>
## 4. Ứng dụng OpenClaw vào phát triển game

| Công việc | Đầu vào | Đầu ra mong muốn |
| --- | --- | --- |
| Thiết kế tính năng | Ý tưởng gameplay | Quy tắc, phạm vi và tiêu chí hoàn thành |
| Lập trình | Yêu cầu và mã nguồn liên quan | Đề xuất hoặc thay đổi code kèm giải thích |
| Phân tích lỗi | Thông báo lỗi, bước tái hiện | Nguyên nhân cần kiểm tra và hướng sửa |
| Kiểm thử | Quy tắc của tính năng | Test phù hợp và checklist chơi thử |
| Quản lý tiến độ | Kết quả đã xác nhận, thời gian có thể dành | 2–4 nhiệm vụ ưu tiên mỗi tuần |
| Tài liệu và GitHub | Thay đổi thực tế | Hướng dẫn, nội dung commit hoặc pull request |

Ví dụ yêu cầu: “Tôi muốn nhân vật thu thập linh khí và đột phá cảnh giới.”

Trợ lý cần làm rõ nguồn linh khí, điều kiện đột phá, lượng tài nguyên tiêu hao, thay đổi chỉ số và cách hiển thị trước khi đề xuất code.

<a id="vai-tro"></a>
## 5. Các vai trò AI

| Vai trò dự kiến | Trách nhiệm | Kết quả bàn giao |
| --- | --- | --- |
| Thiết kế game | Làm rõ cơ chế và giới hạn phạm vi | Tài liệu tính năng |
| Lập trình | Hỗ trợ cấu trúc và sửa code | Bản thay đổi có giải thích |
| Kiểm thử | Xác định tình huống lỗi, kiểm tra kết quả | Test, checklist và báo cáo lỗi |
| Quản lý tiến độ | Sắp xếp nhiệm vụ theo phụ thuộc | Kế hoạch và cập nhật tiến độ |

Ban đầu có thể sử dụng một trợ lý thực hiện lần lượt các vai trò. Việc triển khai nhiều agent riêng là bước mở rộng, cần cấu hình và đánh giá sau.

<a id="cai-dat"></a>
## 6. Cài đặt và bắt đầu

Các lệnh dưới đây dựa trên README gốc tại thời điểm viết. Khi phiên bản thay đổi, đối chiếu [hướng dẫn cài đặt chính thức](https://docs.openclaw.ai/install).

### Cài trên Windows

Mở PowerShell và chạy:

```powershell
iwr -useb https://openclaw.ai/install.ps1 | iex
```

### Cài trên Linux, macOS hoặc Ubuntu trong WSL2

Chạy trong terminal của môi trường tương ứng:

```bash
curl -fsSL https://openclaw.ai/install.sh | bash
```

Chọn một môi trường làm việc để dễ quản lý cài đặt và cấu hình. Nếu dùng WSL2, chạy các lệnh Linux trong terminal Ubuntu.

### Cài bằng npm nếu đã quản lý Node.js

Theo README gốc, sử dụng Node.js 24.16+ thuộc nhánh 24 hoặc 26.1+ thuộc nhánh được hỗ trợ; Node.js 26 được khuyến nghị. Xem tài liệu chính thức để xác nhận hỗ trợ cho phiên bản khác.

Với npm 12 hoặc npm 11.16+:

```bash
npm install -g openclaw@latest --allow-scripts=openclaw
```

Với npm 11.15 trở xuống, README gốc hướng dẫn bỏ tùy chọn `--allow-scripts=openclaw`.

### Thiết lập lần đầu

Trình cài đặt tự mở bước thiết lập trên bản cài mới. Nếu cài trực tiếp bằng trình quản lý gói, chạy:

```bash
openclaw onboard --install-daemon
```

Sau khi hoàn thành:

```bash
openclaw gateway status
openclaw dashboard
```

Bước thiết lập kiểm tra truy cập mô hình, tạo workspace và cấu hình Gateway. Gửi một tin nhắn trong giao diện để xác nhận hệ thống hoạt động. Quyền sử dụng và chi phí mô hình phụ thuộc vào nhà cung cấp được chọn.

<a id="ma-nguon"></a>
## 7. Làm việc với mã nguồn bản fork

Phần này dành cho việc nghiên cứu hoặc chỉnh sửa OpenClaw từ mã nguồn.

Chuẩn bị Git, Node.js phù hợp và pnpm theo [hướng dẫn phát triển từ mã nguồn](https://docs.openclaw.ai/start/setup).

```bash
git clone https://github.com/buitrungson09-maker/openclaw.git
cd openclaw
pnpm install --frozen-lockfile
pnpm build
pnpm ui:build
```

Repository sử dụng pnpm workspace. Không dùng `npm install` tại thư mục gốc để thay thế bước cài dependency.

Nếu đã cài lệnh VS Code, có thể mở thư mục bằng:

```bash
code .
```

Cài package phát hành và build bản fork là hai cách làm việc khác nhau. Chỉnh sửa bản fork không tự cập nhật bản `openclaw` đã cài toàn cục; xem hướng dẫn nguồn để chạy và phát triển đúng bản checkout.

<a id="quy-trinh"></a>
## 8. Quy trình thực hiện một tính năng

1. Gửi yêu cầu, mã nguồn liên quan và trạng thái hiện tại.
2. Xác định quy tắc, phạm vi và tiêu chí hoàn thành.
3. Chia tính năng thành những bước nhỏ theo thứ tự phụ thuộc.
4. Thực hiện thay đổi trong phạm vi nhiệm vụ.
5. Chạy kiểm tra và ghi lại kết quả thực tế.
6. Chơi thử để đánh giá thao tác và cảm giác chơi.
7. Cập nhật tài liệu và lưu thay đổi bằng Git.

### Mẫu yêu cầu dành cho trợ lý

```text
Tôi đang phát triển game Linh Đạo.

Tính năng cần làm:
[Ví dụ: thu thập linh khí]

Trạng thái hiện tại:
[Mô tả phần đã chạy được và mã nguồn liên quan]

Quy tắc:
[Điều kiện, giá trị, giới hạn]

Yêu cầu:
- Giải thích bằng tiếng Việt, phù hợp người mới học.
- Chia thành từng bước nhỏ.
- Nêu file hoặc hàm cần thay đổi dựa trên mã nguồn được cung cấp.
- Đề xuất cách kiểm tra.
- Phân biệt rõ kết quả đã kiểm chứng và đề xuất chưa thử.
```

Một nhiệm vụ chỉ hoàn thành khi đạt tiêu chí kiểm tra đã thống nhất.

<a id="thu-nghiem"></a>
## 9. Thử nghiệm linh khí và đột phá

Đây là kịch bản đề xuất đầu tiên để đánh giá quy trình hỗ trợ.

### Quy tắc minh họa

- Nhân vật bắt đầu với 0 linh khí.
- Mỗi quái bị hạ cho 10 linh khí, trao thưởng một lần.
- Đột phá cần và tiêu hao 100 linh khí.
- Đột phá tăng một bậc cảnh giới.
- Máu tối đa tăng từ 100 lên 120.
- Bản thử nghiệm chỉ cho phép đột phá một lần.

Các con số chỉ phục vụ thử nghiệm, chưa phải thiết kế cân bằng cuối cùng.

### Các bước triển khai

1. Thêm dữ liệu linh khí, cảnh giới và trạng thái đã đột phá.
2. Cộng phần thưởng khi quái bị hạ.
3. Hiển thị tiến độ trên giao diện.
4. Kiểm tra điều kiện và thực hiện đột phá.
5. Cập nhật chỉ số.
6. Lưu và tải lại trạng thái nhân vật.

### Tiêu chí kiểm tra

| Tình huống | Kết quả mong đợi |
| --- | --- |
| Có 90 linh khí | Chưa được đột phá |
| Có 100 linh khí | Thành công, còn 0 linh khí |
| Có 120 linh khí | Thành công, còn 20 linh khí |
| Nhấn đột phá nhiều lần | Không vượt giới hạn một lần |
| Sự kiện quái chết bị gọi lại | Không cộng phần thưởng lần hai |
| Lưu và tải lại | Giữ đúng linh khí, cảnh giới, máu tối đa |

<a id="lo-trinh"></a>
## 10. Lộ trình và đánh giá

| Giai đoạn | Công việc | Tiêu chí hoàn thành |
| --- | --- | --- |
| 1. Thiết lập | Cài OpenClaw, cấu hình mô hình, mở giao diện | Gửi và nhận được yêu cầu thử |
| 2. Hướng dẫn | Xây dựng mẫu yêu cầu và vai trò bằng tiếng Việt | Tạo được kế hoạch rõ ràng cho một tính năng |
| 3. Áp dụng | Thực hiện kịch bản linh khí và đột phá | Chức năng chạy được, có kết quả kiểm tra |
| 4. Hoàn thiện | Kết nối vòng chơi và lưu tiến độ | Có bản chơi thử nhỏ |
| 5. Đánh giá | Ghi nhận hiệu quả và điều chỉnh quy trình | Có báo cáo kết quả cùng hạn chế |

Theo dõi thời gian hoàn thành, số lần sửa lại, lỗi phát hiện khi chơi thử và khả năng tự giải thích code. Chưa đặt mức cải thiện cụ thể khi chưa có dữ liệu thực nghiệm.

<a id="nguyen-tac"></a>
## 11. Nguyên tắc sử dụng

- Giao nhiệm vụ nhỏ với đầu vào và tiêu chí rõ ràng.
- Cung cấp bước tái hiện và thông báo lỗi thực tế.
- Kiểm tra code trước khi sử dụng hoặc hợp nhất.
- Chỉ cấp quyền công cụ phù hợp với nhiệm vụ.
- Không đưa khóa API, mật khẩu hoặc dữ liệu riêng tư vào repository.
- Phân biệt bài kiểm tra đã chạy với checklist mới đề xuất.
- Người phát triển quyết định thiết kế và chịu trách nhiệm về sản phẩm.

Theo tài liệu gốc, công cụ trong phiên chính có thể chạy trực tiếp trên máy chủ nếu chưa cấu hình sandbox. Đọc [hướng dẫn bảo mật](https://docs.openclaw.ai/gateway/security) và [sandbox](https://docs.openclaw.ai/gateway/sandboxing) trước khi mở quyền thao tác hoặc kết nối thêm người dùng.

<a id="trang-thai"></a>
## 12. Trạng thái, tài liệu và giấy phép

### Tiến độ

- [x] Có repository cá nhân OpenClaw.
- [x] Chọn tên game Linh Đạo.
- [x] Xác định ý tưởng ứng dụng và viết README tiếng Việt.
- [ ] Xác nhận cài đặt và cấu hình OpenClaw thành công.
- [ ] Thiết lập hướng dẫn cho trợ lý.
- [ ] Thực hiện kịch bản linh khí và đột phá.
- [ ] Kiểm thử và ghi nhận kết quả.
- [ ] Hoàn thành bản chơi thử đầu tiên.

### Tài liệu tham khảo

| Nhu cầu | Tài liệu |
| --- | --- |
| Bắt đầu sử dụng | [Getting started](https://docs.openclaw.ai/start/getting-started) |
| Cài đặt | [Install](https://docs.openclaw.ai/install) |
| Phát triển từ mã nguồn | [Setup](https://docs.openclaw.ai/start/setup) |
| Mô hình AI | [Model providers](https://docs.openclaw.ai/concepts/model-providers) |
| Công cụ | [Tools](https://docs.openclaw.ai/tools) |
| Skills | [Skills](https://docs.openclaw.ai/tools/skills) |
| Plugins | [Plugins](https://docs.openclaw.ai/plugins) |
| Cấu hình Gateway | [Configuration](https://docs.openclaw.ai/gateway/configuration) |
| Đóng góp mã nguồn | [CONTRIBUTING.md](CONTRIBUTING.md) |
| Báo cáo lỗ hổng | [SECURITY.md](SECURITY.md) |

### Ghi nhận và giấy phép

OpenClaw được xây dựng bởi Peter Steinberger và cộng đồng, được quản lý bởi OpenClaw Foundation. Cảm ơn tác giả, người đóng góp và các đơn vị hỗ trợ dự án gốc.

Mã nguồn OpenClaw tuân theo [giấy phép MIT](LICENSE) © OpenClaw Foundation. Xem [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) để biết thông tin về mã nguồn được tích hợp hoặc điều chỉnh.

Ý tưởng ứng dụng vào Linh Đạo và nội dung định hướng của bản fork do Bùi Trung Sơn phát triển. Tài nguyên hình ảnh, âm thanh và phần bổ sung cho game cần được kiểm tra giấy phép và ghi nhận nguồn riêng.
