# CU Keling Kumang — WiFi Login Redirect

Halaman redirect untuk login hotspot Mikrotik via QR Code.

## Cara kerja

QR Code berisi URL:
```
https://USERNAME.github.io/wifi-kk/?u=KODE&ip=10.10.10.1&s=AULA+KELING+KUMANG
```

Saat di-scan → halaman ini terbuka via HTTPS → redirect ke IP hotspot lokal → user login otomatis → tercatat sebagai user di Mikrotik.

## Parameter URL

| Parameter | Keterangan | Contoh |
|-----------|-----------|--------|
| `u` | Username/kode voucher | `ABC123` |
| `p` | Password (opsional, default = u) | `ABC123` |
| `ip` | IP hotspot gateway | `10.10.10.1` |
| `s` | Nama SSID (untuk tampilan) | `AULA+KELING+KUMANG` |

## Setup

1. Fork repo ini atau buat repo baru bernama `wifi-kk`
2. Upload `index.html` ke repo
3. Aktifkan GitHub Pages di Settings → Pages → Branch: main
4. Generate QR dengan URL format di atas menggunakan `qr-voucher-final.html`
