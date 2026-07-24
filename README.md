# 📷 Kalakini — Free Photobooth

Photobooth gratis berbasis web dengan fitur lengkap: kamera live, filter foto, strip 3 foto, dan download instan.

---

## 🚀 Cara Menjalankan

### Windows
```
double-click run.bat
```

### Mac / Linux
```bash
pip install -r requirements.txt
python app.py
```

Buka browser: **http://localhost:5000**

Admin dashboard: **http://localhost:5000/admin**

---

## ✨ Fitur

| Fitur | Detail |
|-------|--------|
| 📷 Kamera Live | Akses kamera dengan izin browser |
| 🔄 Flip Kamera | Ganti antara kamera depan & belakang |
| ⏱️ Countdown | 3 detik sebelum foto |
| 🎨 12 Filter | Original, Noir, Warm, Cool, Vintage, Fade, Vivid, Rose, Dreamy, Dramatic, Lomo, Matte |
| 🖼️ Strip 3 Foto | Kertas foto elegan dengan branding Kalakini |
| ⬇️ Download | Download langsung ke device |
| 📱 Responsive | HP, tablet, laptop — semua oke |
| 🔒 Tracking | Simpan data user ke SQLite via Flask |
| 📊 Admin | Dashboard admin di `/admin` |

---

## 🗂️ Struktur

```
kalakini/
├── app.py                 ← Flask backend (Python)
├── requirements.txt
├── kalakini.db            ← SQLite database (auto-created)
├── run.bat                ← Windows launcher
├── run.sh                 ← Mac/Linux launcher
├── templates/
│   ├── index.html         ← Halaman utama photobooth
│   └── admin.html         ← Admin dashboard
└── static/
    ├── css/
    │   └── style.css      ← Design system
    └── js/
        └── app.js         ← Camera, filters, strip generator
```

---

## 🔒 Data yang Tersimpan

Setiap sesi menyimpan:
- Nama & email (input user)
- Device info & IP address
- Filter yang dipakai
- Waktu mulai & selesai
- Status download

> Data hanya tersimpan di server lokal — tidak dikirim kemana-mana.
