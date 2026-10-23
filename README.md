# MotionLyn

**MotionLyn** adalah aplikasi *web-based* 3D motion graphic dan visual effect (VFX) editor yang berjalan langsung di browser tanpa perlu instalasi *software* tambahan.

🌐 **Website / Live Demo:** [motionlyn.my.id](https://motionlyn.my.id)

---

## 🚀 Fitur Utama

* **3D Rendering & Camera Control**  
  * Mendukung pemuatan dan manipulasi model 3D.
  * Kontrol kamera 3D interaktif (*orbit*, *pan*, *zoom*, dan *free camera*).
* **Bone Groups & Animation System**  
  * Pengelompokan struktur tulang (*bones*) untuk kebutuhan rig dan animasi karakter/objek 3D.
* **FX & Motion Engine**  
  * Mesin pemroses efek visual bawaan dengan dukungan prasetel kustom (*FX Defs* & *FX Extra*).
* **Media Player & Real-time Preview**  
  * Pratinjau animasi dan efek secara langsung (*real-time*) sebelum proses rendisi.
* **WebM Alpha Export**  
  * Fitur ekspor video berformat WebM dengan *transparent background* (jalur alfa) untuk kemudahan *compositing*.
* **Penyimpanan & Manajemen Berkas**  
  * Sistem penyimpanan lokal (*local storage*) untuk menyimpan proyek langsung di browser.
  * Dukungan kompresi/dekompresi berkas `.zip` untuk *import* dan *export* proyek.

---

## 🛠️ Arsitektur & Struktur Berkas

Aplikasi ini dibangun menggunakan arsitektur modular JavaScript murni (Vanilla JS) yang terbagi ke dalam beberapa modul spesifik:

```text
MotionLyn/
├── index.html                  # Antarmuka utama aplikasi
├── css/
│   └── style.css               # Tata letak dan tema antarmuka
├── img/                        # Aset gambar, ikon, dan sampel
└── js/
    ├── 01-core.js              # Inisialisasi logika inti sistem
    ├── 02-storage.js           # Pengelolaan penyimpanan lokal (Local Storage)
    ├── 03-zip.js               # Handler kompresi & ekstraksi berkas ZIP
    ├── 04-model.js             # Struktur data model
    ├── 05-fx-engine.js         # Mesin pemroses efek visual
    ├── 06-fx-defs.js           # Definisi & parameter efek visual
    ├── 07-model3d.js           # Parser & pengolah objek 3D
    ├── 08-3d-camera.js         # Sistem manipulasi kamera 3D
    ├── 09-renderer.js          # Core rendering pipeline
    ├── 10-media-player.js      # Kontrol linimasa & pemutar media
    ├── 11-export.js            # Logika ekspor proyek
    ├── 12-home.js              # Navigasi & antarmuka beranda
    ├── 13-panels.js            # Pengaturan panel antarmuka pengguna
    ├── 14-editor.js            # Logika workspace & editor animasi
    ├── 15-download-aio.js      # Handler pengunduhan berkas gabungan
    ├── 16-model-format.js      # Spesifikasi format model 3D
    ├── 17-bone-groups.js       # Pengaturan grup hirarki tulang/rigging
    ├── 18-fx-extra.js          # Efek visual tambahan
    ├── 19-init.js              # Inisialisasi aplikasi awal
    ├── 20-settings.js          # Pengaturan aplikasi & preferensi pengguna
    ├── 21-export-screen.js     # Antarmuka modul rendisi/ekspor
    └── 22-webm-alpha.js        # Encoder video WebM dengan dukungan kanal Alpha
