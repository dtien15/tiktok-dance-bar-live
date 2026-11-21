# TikTok Live Studio

Game sàn nhảy tương tác TikTok LIVE: nhân vật GIF, cánh/bảng hiệu, sân khấu LED, video DJ, nhạc và hiệu ứng.

## Cài đặt nhanh (Windows 10/11)

Chỉ cần **Node.js 20 trở lên** ([tải tại đây](https://nodejs.org/)). Game đã build sẵn trong `Build`, dữ liệu mẫu có sẵn trong `Data`, không cần cài Unity.

1. Tải repo về (nút **Code → Download ZIP**, giải nén; hoặc `git clone`).
2. Nhấp đúp **`run.bat`**.

`run.bat` tự cài thư viện Node ở lần chạy đầu (cần mạng), khởi động Bridge, mở game và mở trang điều khiển http://127.0.0.1:3000/control.html.

Vào tab **Kết nối LIVE**, nhập username TikTok đang phát rồi bấm **Kết nối**.

## Tùy chọn

- **FFmpeg**: chỉ cần khi tự thêm nhân vật từ GIF/PNG/JPG. Có thể đặt `FFMPEG_PATH` trong `TikTokBridge/.env`.
- **Python 3 + Pillow** (`python -m pip install -r tools/requirements-media.txt`): chỉ cần khi nhập WebP.
- **`.env`**: không bắt buộc. Muốn đổi cổng hoặc nguồn live, sao chép `TikTokBridge/.env.example` thành `TikTokBridge/.env` rồi sửa.
- Game đóng gói sẵn chỉ kết nối cổng 3000. Nếu đổi `PORT`, game sẽ không tự mở.

## Quản lý asset

Trong tab **Assets** bạn có thể quản lý nhân vật, cánh, bảng hiệu, video màn DJ, phông nền và âm nhạc. Dữ liệu tải lên được lưu trong `Data`; sao lưu cả thư mục này khi chuyển máy. Repo kèm sẵn một bài nhạc mẫu trong `Data/Music`.

## Phát triển

- Node: `cd TikTokBridge`, `npm ci`, `npm test`.
- Unity: mở `UnityProject` bằng Unity 6000.2.10f1; `build.bat` tạo lại game Windows trong `Build`.
- Chi tiết đường dẫn, build C# và sao lưu: [docs/PROJECT_STRUCTURE.md](docs/PROJECT_STRUCTURE.md).
- Hướng dẫn sử dụng: [docs/usage/HUONG_DAN_SU_DUNG.txt](docs/usage/HUONG_DAN_SU_DUNG.txt).

Giấy phép mã nguồn: [MIT](LICENSE). Thông tin nguồn và giấy phép tài nguyên bên thứ ba được giữ cạnh asset.
