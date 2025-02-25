# Hướng Dẫn Cấu Hình Livestream YouTube Bằng OBS

**Giảng Viên Giảng Dạy: Hoàng Quốc Tuấn**  

## 1. Cấu Hình Máy Tính Đề Xuất

### Mức Cơ Bản (Livestream 720p, 30fps)
- **CPU**: Intel Core i5-10400 / Ryzen 5 3600  
- **RAM**: 8GB  
- **GPU**: GTX 1650 / RX 570  
- **Internet**: Upload tối thiểu 5 Mbps  

### Mức Trung Bình (Livestream 1080p, 60fps)
- **CPU**: Intel Core i7-12700 / Ryzen 7 5800X  
- **RAM**: 16GB  
- **GPU**: RTX 3060 / RX 6700 XT  
- **Internet**: Upload tối thiểu 10 Mbps  

### Mức Cao Cấp (Livestream 4K, 60fps hoặc đa kênh)
- **CPU**: Intel Core i9-13900K / Ryzen 9 7950X  
- **RAM**: 32GB hoặc hơn  
- **GPU**: RTX 4080 / RX 7900 XTX  
- **Internet**: Upload tối thiểu 20 Mbps  

## 2. Phần Mềm Hỗ Trợ Livestream
- **OBS Studio (Miễn phí, phổ biến nhất)**  
- **Streamlabs OBS (Dễ dùng, giao diện trực quan)**  
- **vMix (Chuyên nghiệp, trả phí)**  
- **XSplit Broadcaster (Tính năng cao cấp, trả phí)**  

## 3. Cấu Hình Phần Mềm OBS Studio

### Cài đặt cơ bản:
- **Encoder**: Chọn NVIDIA NVENC (nếu dùng GPU NVIDIA) hoặc x264 (nếu dùng CPU)  
- **Bitrate**:  
  - 720p 30fps → 3,500 - 5,000 Kbps  
  - 1080p 60fps → 6,000 - 9,000 Kbps  
  - 4K 60fps → 20,000 - 50,000 Kbps  
- **Keyframe Interval**: 2 giây  
- **Preset**: Quality hoặc Max Quality (nếu GPU đủ mạnh)  
- **Audio Bitrate**: 160 Kbps trở lên  

## 4. Cấu Hình Internet
- **Kiểm tra tốc độ upload**: Dùng [Speedtest](https://www.speedtest.net/)  
- **Dùng kết nối có dây (Ethernet) thay vì Wi-Fi**  
- **Tắt các ứng dụng tiêu tốn băng thông khi livestream**  

---

# Hướng Dẫn Livestream Trực Tiếp Trên YouTube Cá Nhân Bằng OBS

## 1. Bật Chế Độ Livestream Trên YouTube  
1. **Truy cập YouTube Studio**: [https://studio.youtube.com/](https://studio.youtube.com/)  
2. **Vào phần "Phát Trực Tiếp"**:  
   - Ở menu bên trái, chọn **"Trực tiếp"**.  
   - Nếu là lần đầu tiên, YouTube sẽ yêu cầu xác minh tài khoản (mất **24 giờ** để kích hoạt).  
3. **Lấy khóa luồng (Stream Key)**:  
   - Trong tab **"Luồng"**, kéo xuống mục **Cài đặt mã hóa**.  
   - Sao chép **"Khóa luồng"** (Stream Key).  

## 2. Cài Đặt OBS Studio Để Live YouTube  

### Tải và Cài Đặt OBS Studio  
- **Tải OBS Studio tại**: [https://obsproject.com/](https://obsproject.com/)  
- Cài đặt và mở OBS Studio.

### Thêm YouTube vào OBS  
1. **Mở OBS → Chọn "Cài đặt" (Settings) → Chuyển sang tab "Stream"**  
2. **Chọn Dịch vụ**: **YouTube - RTMP**  
3. **Dán "Khóa luồng"** vào ô **Stream Key**  
4. Nhấn **OK** để lưu lại.

## 3. Thiết Lập Cảnh (Scenes) & Nguồn (Sources) Trong OBS

### Thêm Nguồn Video  
- Ở mục **Scenes**, bấm vào **"+"** để tạo một cảnh mới.  
- Ở mục **Sources**, bấm vào **"+"** để thêm nguồn:  
  - **Màn hình máy tính**: Chọn **Display Capture**.  
  - **Webcam**: Chọn **Video Capture Device**.  
  - **Game**: Chọn **Game Capture**.  
  - **Hình ảnh, video**: Chọn **Media Source**.  

## 4. Cấu Hình Chất Lượng Livestream Trong OBS

Vào **Cài đặt (Settings) → Video & Output**, thiết lập như sau:  

### Độ phân giải (Video Settings):
- **1080p, 60fps**:  
  - **Output Resolution**: 1920x1080  
  - **FPS**: 60  
  - **Bitrate**: 6.000 - 9.000 Kbps  
- **720p, 30fps**:  
  - **Output Resolution**: 1280x720  
  - **FPS**: 30  
  - **Bitrate**: 3.000 - 5.000 Kbps  

### Bộ mã hóa (Encoder Settings):
- **Nếu dùng GPU NVIDIA** → Chọn **NVENC H.264**.  
- **Nếu không có GPU mạnh** → Chọn **x264 (CPU Encode)**.  
- **Keyframe Interval**: 2 giây  
- **Preset**: Quality hoặc Max Quality  

## 5. Bắt Đầu Livestream

1. Nhấn **"Start Streaming"** trên OBS.  
2. Quay lại **YouTube Studio** để kiểm tra xem luồng đã kết nối chưa.  
3. Nhấn **"Phát Trực Tiếp"** trên YouTube để bắt đầu.  

## 6. Kết Thúc Livestream  
- Khi muốn dừng, vào OBS nhấn **"Stop Streaming"**.  
- Quay lại YouTube Studio, nhấn **Kết thúc trực tiếp** nếu cần.  

---

## Lưu Ý Khi Livestream  
✅ **Kiểm tra tốc độ mạng** (Upload từ 5 Mbps trở lên để live mượt).  
✅ **Dùng kết nối mạng dây (Ethernet)** thay vì Wi-Fi để ổn định hơn.  
✅ **Đóng các ứng dụng không cần thiết** để giảm lag.  
✅ **Test trước khi live** để tránh lỗi kỹ thuật.  

## Nộp Bài  
Truy cập đường dẫn sau để nộp bài:  
[**Nộp bài tại đây**](https://hethongnopbai.dak.edu.vn/nopbai.html)  
