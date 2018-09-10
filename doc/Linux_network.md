# Kết nối mạng DH-FPT trên Linux
Hướng dẫn này dùng cho các Linux họ Debian (Debian, Ubuntu, Linux Mint, ...)

## 1. Cài đặt WPA Supplicant
Phiên bản mới sẽ không thể kết nối vào mạng của ĐH-FPT,
cần cài đặt bản cũ hơn tại [đây](https://drive.google.com/open?id=1b2g3TPX12x4dwUrdpxARrZFveI2obdo0).

```
sudo dpkg -i wpa*.deb
```


## 2. Bỏ qua cập nhật WPA Supplicant
Để luôn giữ bản cũ này trong máy tính.
```
sudo apt-mark hold wpasupplicant
```

### 3. Tạo network profile

