# 🎓 KULIAHKU - Portal & Portofolio Akademik Digital
### Universitas Islam Negeri Siber Syekh Nurjati Cirebon (UINSSC)

Aplikasi web profesional berbasis **Single Page Application (SPA)** siap **GitHub Pages**, terhubung secara real-time dengan backend **Google Apps Script**, penyimpanan **Google Drive**, dan database **Google Sheets**.

---

## 🎨 Komposisi & Palet Warna Profesional
Menggunakan tata letak *Floating Dark Sidebar + Material Pro Dashboard* yang dipadukan dengan 5 palet warna ceria resmi:
- **Raspberry Crimson (`#C42B5B`):** Active pill menu, panel grafik berkas, kartu tugas.
- **Emerald Pine (`#238B6E`):** Identitas akademik UINSSC, grafik aktivitas pertemuan, status selesai.
- **Warm Honey Amber (`#EAA646`):** Kartu progres, aksen catatan dosen, badge SKS.
- **Fresh Mint (`#7FE0BF`):** Aksen status pada panel gelap, bingkai foto profil mahasiswa.
- **Dark Charcoal (`#232327`) & Soft Platinum (`#CFD1D4`):** Sidebar mengambang, kartu ringkasan, dan kanvas bersih.

---

## 📁 Struktur Berkas Repositori

```text
├── assets/
│   ├── logo-uinssc.png        # Logo resmi UIN Siber Syekh Nurjati Cirebon
│   └── color-palette.png      # Referensi palet 5 warna
├── .nojekyll                  # Konfigurasi statis GitHub Pages
├── index.html                 # Aplikasi Web SPA (Siap Upload ke GitHub Pages)
├── code.gs                    # Arsip Backend Controller Google Apps Script
├── setup.gs                   # Arsip Skrip Inisialisasi Safe Migration
├── prd.md                     # Dokumen Blueprint & Master Context (Single Source of Truth)
├── ZettBOT.md                 # Sakelar Aktivasi ZettBOT
└── README.md                  # Panduan Deployment GitHub Pages & Integrasi
```

---

## 🚀 Cara Publikasi Basis Web ke GitHub Pages (3 Menit)

Karena URL API Google Apps Script Anda sudah tertanam permanen di dalam `index.html`, seluruh data Spreadsheet dan berkas Google Drive Anda yang sudah ada akan **langsung terbaca otomatis** tanpa mengubah isi Spreadsheet maupun Drive:

1. Buat repositori baru di akun **GitHub** Anda (misalnya: `kuliahku-uinssc`).
2. Unggah (push/upload) berkas berikut ke repositori GitHub Anda:
   - `index.html`
   - `.nojekyll`
   - Folder `assets/` (berisi `logo-uinssc.png`)
3. Masuk ke tab **Settings** repositori GitHub Anda ➔ pilih menu **Pages** di sebelah kiri.
4. Pada bagian **Build and deployment** (*Branch*), pilih **`main`** dan folder **`/ (root)`**, lalu klik **Save**.
5. Tunggu 1–2 menit hingga tautan website aktif muncul (contoh: `https://username.github.io/kuliahku-uinssc/`).
6. Buka tautan tersebut dari HP maupun Laptop — masukkan **PIN** Anda untuk langsung masuk!

---

## 🔧 Pembaruan Wajib Backend Google Apps Script (Untuk PIN Ketat & Notif WA)
Karena perubahan **verifikasi PIN** dan **pengingat WhatsApp** berjalan di sisi server Google Apps Script (data Spreadsheet & Google Drive Anda tetap **100% aman & tidak berubah**):
1. Buka proyek Google Apps Script Anda, lalu ganti seluruh isi file `code.gs` dengan isi terbaru dari file `code.gs` di repositori ini (*JANGAN mengubah atau menjalankan ulang `setup.gs`*).
2. Klik **Deploy ➔ Manage deployments ➔ Edit (ikon pensil) ➔ Version: New version ➔ Deploy** (URL `/exec` akan tetap sama).
3. *(Untuk jadwal otomatis WA tiap Kamis/Jumat tanpa membuka web)*: Di aplikasi web buka menu **Notif WhatsApp**, isi Nomor WA + API Key (CallMeBot gratis / Fonnte / Webhook), centang jadwal mingguan, lalu klik **Simpan Pengaturan**. Jika muncul pemberitahuan izin trigger, buka editor Apps Script ➔ pilih fungsi `pasangJadwalNotifWAJumat` di bilah atas ➔ klik **Run** 1x untuk menyetujui izin jadwal otomatis.
