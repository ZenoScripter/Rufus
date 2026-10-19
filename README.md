
<div align="center">

# ⌘ WINDOWS INSTALLATION TOOLKIT

### Complete Guide to Windows Bootable USB & Office Installers

<p>
  <img src="https://img.shields.io/badge/Windows-Installation-0078D4?style=for-the-badge&logo=windows&logoColor=white" alt="Windows Installation"/>
  <img src="https://img.shields.io/badge/Rufus-Bootable_USB-6C63FF?style=for-the-badge" alt="Rufus"/>
  <img src="https://img.shields.io/badge/Documentation-Detailed-2EA44F?style=for-the-badge" alt="Documentation"/>
</p>

**Panduan lengkap untuk menyiapkan installer Windows, membuat USB bootable, memahami BIOS/UEFI, dan melakukan instalasi sistem operasi.**

*Prepare · Configure · Boot · Install*

</div>

---

## ◈ TABLE OF CONTENTS

- [01. Tentang Proyek](#-01-tentang-proyek)
- [02. Daftar Installer Windows](#-02-daftar-installer-windows)
- [03. Daftar Installer Microsoft Office](#-03-daftar-installer-microsoft-office)
- [04. Memahami Arsitektur Windows](#-04-memahami-arsitektur-windows)
- [05. Memahami UEFI, Legacy, GPT, dan MBR](#-05-memahami-uefi-legacy-gpt-dan-mbr)
- [06. Persiapan Instalasi](#-06-persiapan-instalasi)
- [07. Download dan Persiapan Rufus](#-07-download-dan-persiapan-rufus)
- [08. Membuat Bootable USB](#-08-membuat-bootable-usb)
- [09. Mengatur BIOS dan Boot Menu](#-09-mengatur-bios-dan-boot-menu)
- [10. Proses Instalasi Windows](#-10-proses-instalasi-windows)
- [11. Instalasi Microsoft Office](#-11-instalasi-microsoft-office)
- [12. Troubleshooting](#-12-troubleshooting)
- [13. Keamanan dan Verifikasi File](#-13-keamanan-dan-verifikasi-file)
- [14. Checklist Akhir](#-14-checklist-akhir)
- [15. Referensi Resmi](#-15-referensi-resmi)

---

## ◈ 01. TENTANG PROYEK

Windows Installation Toolkit merupakan dokumentasi teknis untuk membantu pengguna memahami proses persiapan installer Windows dari awal hingga siap digunakan.

Dokumentasi ini mencakup:

- Pemilihan versi Windows yang sesuai.
- Perbedaan Windows 10, Windows 11, Windows 8.1, Windows 7, dan Windows XP.
- Perbedaan sistem 32-bit dan 64-bit.
- Perbedaan mode UEFI dan Legacy BIOS.
- Perbedaan skema partisi GPT dan MBR.
- Penggunaan Rufus untuk membuat USB bootable.
- Pengaturan prioritas boot komputer.
- Proses instalasi Windows.
- Persiapan dan instalasi Microsoft Office.
- Penanganan masalah yang sering terjadi.

> [!IMPORTANT]
> Daftar versi dan tautan di bawah berasal dari screenshot referensi yang diberikan. Tautan pihak ketiga belum diverifikasi keamanannya, keasliannya, atau status aktifnya. Untuk instalasi yang aman, prioritaskan sumber resmi Microsoft dan pengembang perangkat lunak.

## ◈ 02. DAFTAR INSTALLER WINDOWS

### ▸ Windows 11

Windows 11 merupakan sistem operasi desktop Microsoft yang ditujukan untuk perangkat modern. Persyaratan perangkat kerasnya berbeda dari Windows versi sebelumnya.

| Varian | Arsitektur | Informasi |
|:---|:---|:---|
| Windows 11 24H2 | 64-bit | Rilis yang tercantum dalam screenshot |
| Windows 11 22H2 | 64-bit | Rilis sebelumnya yang tercantum dalam screenshot |

**Tautan resmi:**

- [Windows 11 — Download resmi Microsoft](https://www.microsoft.com/software-download/windows11)

**Catatan teknis:**

- Windows 11 umumnya menggunakan UEFI dan GPT.
- Periksa kompatibilitas prosesor, TPM 2.0, Secure Boot, RAM, dan ruang penyimpanan.
- Tidak semua komputer lama memenuhi persyaratan Windows 11.
- Pastikan edisi dan bahasa installer sesuai kebutuhan.

> [!NOTE]
> Windows 11 22H2 dan 24H2 adalah nomor versi rilis, bukan arsitektur prosesor. Dukungan setiap rilis berbeda menurut edisi dan siklus pembaruannya.

### ▸ Windows 10

Windows 10 tersedia dalam beberapa edisi dan konfigurasi instalasi. Pilihan arsitektur serta metode boot harus disesuaikan dengan perangkat tujuan.

**Referensi resmi:**

- [Windows 10 — Download Microsoft](https://www.microsoft.com/software-download/windows10)

**Tautan dari screenshot:**

| Varian | Tautan |
|:---|:---|
| UEFI 64-bit | [karyawan.co.id/WIN10UEFI64](https://karyawan.co.id/WIN10UEFI64) |
| UEFI 32-bit | [karyawan.co.id/win10uefi32](https://karyawan.co.id/win10uefi32) |
| Legacy 32/64-bit | [khaddavi.net/win10legacy](https://khaddavi.net/win10legacy) |
| Paket pembaruan 64-bit, Part 1 | [sfl.gl/cl56mPI](https://sfl.gl/cl56mPI) |
| Paket pembaruan 64-bit, Part 2 | [sfl.gl/ugBTU](https://sfl.gl/ugBTU) |

**Informasi tambahan:**

- Paket pembaruan yang dibagi menjadi beberapa bagian harus mengikuti petunjuk pengarsipan dari sumbernya.
- Jangan menganggap dua file terpisah sebagai dua installer mandiri.
- Periksa checksum apabila disediakan.
- Dukungan umum Windows 10 berakhir pada 14 Oktober 2025. Periksa opsi dukungan tambahan yang berlaku sebelum menggunakannya untuk komputer yang terhubung ke internet.

### ▸ Windows 8 dan Windows 8.1

Windows 8 dan 8.1 merupakan sistem operasi generasi sebelumnya.

| Versi | Tautan referensi |
|:---|:---|
| Windows 8.0 | [karyawan.co.id/win8dsid](https://karyawan.co.id/win8dsid) |
| Windows 8.1 | [karyawan.co.id/win81dsid](https://karyawan.co.id/win81dsid) |

**Catatan:** Dukungan Windows 8.1 telah berakhir pada 10 Januari 2023. Gunakan sistem operasi ini hanya jika ada kebutuhan kompatibilitas tertentu dan pahami risiko keamanannya.

### ▸ Windows 7

Windows 7 merupakan sistem operasi lama yang masih mungkin diperlukan untuk perangkat atau aplikasi lawas.

| Varian | Tautan referensi |
|:---|:---|
| UEFI 64-bit | [karyawan.co.id/win7uefi64](https://karyawan.co.id/win7uefi64) |
| Legacy 32/64-bit | [karyawan.co.id/win7legacy](https://karyawan.co.id/win7legacy) |

**Catatan teknis:**

- Dukungan umum Windows 7 telah berakhir pada 14 Januari 2020.
- Dukungan driver USB, NVMe, dan perangkat keras modern dapat menjadi kendala.
- Instalasi pada komputer UEFI modern mungkin membutuhkan konfigurasi khusus.
- Jangan gunakan untuk aktivitas sensitif tanpa mitigasi keamanan yang sesuai.

### ▸ Windows XP SP3

Windows XP Service Pack 3 merupakan versi lawas yang sekarang hanya cocok untuk kebutuhan kompatibilitas tertentu.

- [Windows XP SP3 — tautan referensi](https://karyawan.co.id/winXPsp3)

> [!WARNING]
> Windows XP sudah tidak menerima pembaruan keamanan reguler. Jangan menggunakannya sebagai sistem operasi utama yang terhubung ke internet.

---

## ◈ 03. DAFTAR INSTALLER MICROSOFT OFFICE

Bagian ini memuat versi Microsoft Office yang terlihat pada screenshot referensi.

### ▸ Microsoft Office 2021

Pada screenshot, tersedia judul Office 2021, tetapi tautan unduh 32-bit dan 64-bit belum tercantum.

Untuk mendapatkan Office yang sesuai, gunakan:

- [Microsoft 365 dan Office — halaman resmi](https://www.microsoft.com/microsoft-365)
- [Akun Microsoft — layanan dan aplikasi](https://account.microsoft.com/)

Pilih installer berdasarkan lisensi, akun, edisi, dan kebutuhan kompatibilitas.

### ▸ Microsoft Office 2019

**Tautan dari screenshot:**

| Arsitektur | Tautan | Ukuran tercantum |
|:---|:---|:---|
| 32-bit | [sfl.gl/M0gsN](https://sfl.gl/M0gsN) | 1,5 GB |
| 64-bit | [sfl.gl/PYq0d](https://sfl.gl/PYq0d) | 1,7 GB |

Ukuran file tersebut adalah informasi yang terlihat pada screenshot, bukan hasil verifikasi ukuran unduhan saat ini.

### ▸ Microsoft Office 2016

Screenshot pertama mencantumkan Office 2016 dengan opsi single link dan part link. Namun, beberapa alamat tidak sepenuhnya terlihat atau statusnya tidak dapat dipastikan.

**Catatan:**

- Hindari mengunduh file dari mirror yang tidak dikenal.
- Pastikan installer berasal dari sumber tepercaya.
- Cocokkan versi Office dengan lisensi yang dimiliki.
- Hindari aktivator tidak resmi dan file modifikasi yang berpotensi berbahaya.

### ▸ Microsoft Office 2013

| Arsitektur | Tautan referensi | Ukuran tercantum |
|:---|:---|:---|
| 32-bit | [sfl.gl/2J2OHj](https://sfl.gl/2J2OHj) | 1 GB |
| 64-bit | [sfl.gl/TZ2eGz](https://sfl.gl/TZ2eGz) | 1,2 GB |

### ▸ Microsoft Office 2010

| Arsitektur | Tautan referensi |
|:---|:---|
| 32-bit | [sfl.gl/0gFjhq](https://sfl.gl/0gFjhq) |
| 64-bit | [sfl.gl/i8djfQ](https://sfl.gl/i8djfQ) |

### ▸ Office dengan beberapa bagian

Screenshot Office 2019 juga menampilkan paket multi-part:

| Bagian | Tautan | Status dalam screenshot |
|:---|:---|:---|
| Part 1 | [cararegistrasi.com/9WamCI](https://cararegistrasi.com/9WamCI) | Ditandai OK |
| Part 2 | [cararegistrasi.com/rAyuPXYORwc](https://cararegistrasi.com/rAyuPXYORwc) | Ditandai OK |
| Part 3 | [cararegistrasi.com/XpYSpq](https://cararegistrasi.com/XpYSpq) | Ditandai OK |
| Part 4 | [cararegistrasi.com/23i0TPv8s2cp](https://cararegistrasi.com/23i0TPv8s2cp) | Ditandai mati |

Status tersebut hanya mengikuti keterangan dalam screenshot dan tidak menjamin kondisi terkini.

> [!CAUTION]
> Microsoft Office versi lama memiliki siklus dukungan yang telah berakhir. Untuk perangkat baru, periksa dukungan sistem, persyaratan lisensi, dan opsi resmi yang masih tersedia.

---

## ◈ 04. MEMAHAMI ARSITEKTUR WINDOWS

Arsitektur menentukan jenis sistem dan aplikasi yang dapat dijalankan oleh komputer.

### 32-bit (x86)

- Umumnya digunakan pada perangkat lama.
- Memiliki batas ruang alamat memori yang lebih rendah.
- Tidak dapat menggunakan semua fitur perangkat keras modern.
- Kompatibilitas aplikasi dan driver perlu diperiksa.

### 64-bit (x64)

- Dapat menggunakan kapasitas RAM yang jauh lebih besar, bergantung pada edisi dan konfigurasi.
- Menjadi pilihan umum untuk komputer modern.
- Dapat menjalankan banyak aplikasi 32-bit, tetapi tidak semua driver atau aplikasi lama kompatibel.
- Membutuhkan prosesor yang mendukung arsitektur x64.

| Kondisi | Rekomendasi umum |
|:---|:---|
| Komputer modern | Windows 64-bit |
| Komputer lama | Periksa kemampuan CPU dan driver |
| RAM besar | 64-bit biasanya lebih sesuai |
| Aplikasi khusus lawas | Periksa persyaratan aplikasi |

**Cara memeriksa arsitektur:**

Pada Windows yang sedang berjalan:

1. Buka `Settings`.
2. Masuk ke `System`.
3. Pilih `About`.
4. Periksa bagian `System type`.

---

## ◈ 05. MEMAHAMI UEFI, LEGACY, GPT, DAN MBR

Empat istilah ini sering muncul saat membuat bootable, tetapi masing-masing mempunyai fungsi berbeda.

### UEFI

UEFI adalah firmware modern yang menginisialisasi perangkat keras dan menjalankan bootloader sistem operasi.

Karakteristik umum:

- Mendukung boot dari partisi sistem EFI.
- Umumnya digunakan bersama GPT.
- Mendukung fitur seperti Secure Boot pada perangkat yang kompatibel.

### Legacy BIOS

Legacy BIOS adalah metode firmware boot generasi sebelumnya.

Karakteristik umum:

- Sering digunakan bersama skema partisi MBR.
- Banyak ditemukan pada komputer lama.
- Dukungan dan pilihan pengaturannya bergantung pada perangkat.

### GPT

GPT adalah skema partisi yang umum digunakan pada komputer UEFI modern.

Keunggulan:

- Mendukung disk berkapasitas besar.
- Mendukung lebih banyak partisi dibandingkan batas tradisional MBR.
- Memiliki struktur tabel partisi dengan mekanisme redundansi.

### MBR

MBR adalah skema partisi lama yang masih digunakan pada konfigurasi tertentu.

Karakteristik:

- Memiliki batas tradisional ukuran disk sekitar 2 TiB dengan sektor 512 byte.
- Mendukung hingga empat entri partisi primer dalam struktur dasarnya.
- Sering digunakan untuk kompatibilitas Legacy BIOS.

### Ringkasan

| Firmware | Skema partisi umum |
|:---|:---|
| UEFI | GPT |
| Legacy BIOS | MBR |

> [!IMPORTANT]
> Tabel ini adalah panduan umum, bukan aturan mutlak untuk setiap perangkat. Pilihan boot harus sesuai dengan konfigurasi firmware, media instalasi, dan disk tujuan. Jangan mengubah skema partisi tanpa memahami dampaknya terhadap data.

---

## ◈ 06. PERSIAPAN INSTALASI

Sebelum menjalankan Rufus, pastikan semua kebutuhan tersedia.

### Hardware

- Komputer atau laptop yang kompatibel.
- Flashdisk dengan kapasitas cukup.
- Port USB yang berfungsi.
- Koneksi internet untuk mengunduh file yang dibutuhkan.

### Software

- File ISO Windows.
- Aplikasi Rufus dari situs resmi.
- Driver perangkat jika diperlukan.
- Cadangan data dan informasi lisensi.

### Pemeriksaan sebelum mulai

- [ ] Data flashdisk sudah dicadangkan.
- [ ] File ISO telah diunduh sepenuhnya.
- [ ] Arsitektur installer sesuai perangkat.
- [ ] Mode boot telah diketahui.
- [ ] Ruang penyimpanan komputer mencukupi.
- [ ] Data penting komputer sudah dicadangkan.
- [ ] Kunci pemulihan enkripsi, seperti BitLocker, tersedia jika digunakan.

---

## ◈ 07. DOWNLOAD DAN PERSIAPAN RUFUS

Rufus adalah utilitas untuk memformat USB dan membuat media bootable dari file image.

**Situs resmi:** https://rufus.ie/

### Langkah persiapan

1. Buka browser.
2. Masuk ke situs resmi Rufus.
3. Buka bagian unduhan.
4. Pilih versi yang sesuai dengan sistem operasi komputer.
5. Jalankan aplikasi yang diunduh.
6. Izinkan aplikasi berjalan jika Windows menampilkan permintaan izin.

Versi portable dapat digunakan tanpa instalasi tradisional jika tersedia.

### Mengenali bagian antarmuka

| Bagian | Fungsi |
|:---|:---|
| Device | Memilih flashdisk tujuan |
| Boot selection | Memilih ISO atau image yang digunakan |
| SELECT | Membuka pemilih file |
| Partition scheme | Menentukan GPT atau MBR |
| Target system | Menampilkan target firmware yang sesuai |
| File system | Menentukan sistem file yang digunakan |
| START | Memulai proses pembuatan media |
| CLOSE | Menutup jendela aplikasi |

Nama dan pilihan yang tampil dapat berbeda menurut versi Rufus serta file ISO yang dipilih.

---

## ◈ 08. MEMBUAT BOOTABLE USB

### Step 01 — Hubungkan flashdisk

Colokkan flashdisk ke komputer.

Periksa kapasitas dan nama perangkat untuk memastikan flashdisk yang benar terpilih.

### Step 02 — Pilih perangkat

Pada bagian `Device`, pilih flashdisk tujuan.

Jangan melanjutkan apabila nama perangkat atau kapasitasnya tidak sesuai.

### Step 03 — Pilih file ISO

1. Pada `Boot selection`, pilih `Disk or ISO image` jika tersedia.
2. Klik `SELECT`.
3. Cari file ISO Windows.
4. Pilih file tersebut.
5. Pastikan file berhasil dimuat oleh Rufus.

### Step 04 — Atur skema partisi

Tentukan skema partisi berdasarkan komputer tujuan.

- Pilih GPT untuk kebanyakan instalasi UEFI modern.
- Pilih MBR jika diperlukan untuk konfigurasi Legacy BIOS yang sesuai.

Periksa juga pilihan `Target system` yang ditampilkan.

### Step 05 — Mulai proses

1. Periksa kembali perangkat dan file ISO.
2. Klik `START`.
3. Baca peringatan yang muncul.
4. Konfirmasikan penghapusan data jika sudah yakin.
5. Tunggu proses penulisan sampai selesai.

### Step 06 — Selesaikan proses

Jika indikator selesai dan tidak ada pesan error:

1. Klik `CLOSE`.
2. Keluarkan flashdisk dengan aman.
3. Simpan flashdisk sebagai media instalasi.

> [!WARNING]
> Jangan mencabut flashdisk selama proses penulisan. Jika terjadi error, baca pesan Rufus sebelum mengulangi proses.

---

## ◈ 09. MENGATUR BIOS DAN BOOT MENU

BIOS/UEFI memungkinkan komputer menentukan perangkat yang digunakan untuk memulai sistem operasi.

### Cara masuk BIOS atau Boot Menu

1. Matikan komputer.
2. Hubungkan flashdisk bootable.
3. Nyalakan komputer.
4. Tekan tombol firmware sesuai perangkat.

Tombol yang sering digunakan:

| Tombol | Penggunaan yang umum |
|:---|:---|
| F2 | Masuk BIOS/UEFI pada sebagian perangkat |
| F12 | Boot Menu pada sebagian perangkat |
| Esc | Menu startup pada sebagian perangkat |
| Del | BIOS/UEFI pada sebagian motherboard |

Tombol yang benar bergantung pada merek dan model komputer.

### Memilih flashdisk

- Buka menu `Boot` atau gunakan Boot Menu.
- Pilih flashdisk yang sesuai.
- Jika muncul pilihan dengan awalan `UEFI:`, gunakan pilihan tersebut untuk boot UEFI.
- Simpan perubahan jika diperlukan.
- Tunggu hingga Windows Setup dimuat.

### Jika flashdisk tidak muncul

- Periksa port USB.
- Coba port USB lain.
- Pastikan Rufus selesai tanpa error.
- Periksa kompatibilitas firmware.
- Periksa pengaturan Secure Boot jika media tidak kompatibel.

Jangan menonaktifkan Secure Boot atau mengubah pengaturan keamanan firmware tanpa memahami alasan dan konsekuensinya.

---

## ◈ 10. PROSES INSTALASI WINDOWS

Setelah berhasil boot dari flashdisk, Windows Setup akan ditampilkan.

### Tahapan umum

1. Pilih bahasa, format waktu, dan keyboard jika diminta.
2. Klik `Install now`.
3. Masukkan product key jika diperlukan, atau pilih opsi yang sesuai dengan lisensi.
4. Pilih edisi yang sesuai dengan lisensi.
5. Baca dan setujui persyaratan lisensi.
6. Pilih jenis instalasi sesuai kebutuhan.
7. Periksa disk dan partisi tujuan dengan teliti.
8. Lanjutkan instalasi dan tunggu komputer melakukan restart.
9. Ikuti proses konfigurasi awal Windows.

### Risiko pada pemilihan partisi

Menghapus atau memformat partisi dapat menghilangkan data secara permanen.

Sebelum mengubah partisi:

- Pastikan disk yang dipilih benar.
- Cadangkan file penting.
- Jangan menghapus partisi pemulihan atau data tanpa mengetahui fungsinya.
- Pastikan konfigurasi GPT/MBR sesuai dengan metode boot.

### Setelah instalasi

- Jalankan Windows Update jika masih didukung.
- Instal driver dari produsen perangkat.
- Periksa Device Manager.
- Aktifkan Windows menggunakan lisensi yang sah.
- Pulihkan data cadangan.
- Instal aplikasi dari sumber resmi.

---

## ◈ 11. INSTALASI MICROSOFT OFFICE

Microsoft Office adalah rangkaian aplikasi produktivitas, seperti Word, Excel, dan PowerPoint.

### Sebelum instalasi

Periksa hal berikut:

- Versi Office yang dibutuhkan.
- Arsitektur 32-bit atau 64-bit.
- Kompatibilitas dengan Windows.
- Jenis lisensi.
- Ketersediaan akun atau product key yang sah.

### Langkah umum

1. Dapatkan installer dari akun atau sumber resmi.
2. Jalankan installer.
3. Ikuti petunjuk pemasangan.
4. Tunggu proses selesai.
5. Buka salah satu aplikasi Office.
6. Selesaikan aktivasi melalui metode resmi yang sesuai dengan lisensi.

### Memilih 32-bit atau 64-bit

Pilih arsitektur berdasarkan kompatibilitas aplikasi dan add-in yang digunakan, bukan hanya berdasarkan ukuran file installer.

Untuk penggunaan Office modern, 64-bit sering sesuai untuk perangkat modern, sedangkan 32-bit mungkin dibutuhkan untuk kompatibilitas dengan add-in lama.

> [!CAUTION]
> Hindari aktivator ilegal, installer yang telah dimodifikasi, serta file executable dari mirror tidak tepercaya. File tersebut dapat membawa malware atau mencuri data.

---

## ◈ 12. TROUBLESHOOTING

### Rufus tidak mendeteksi flashdisk

**Penyebab yang mungkin:**

- Port USB bermasalah.
- Flashdisk rusak.
- Perangkat belum dikenali oleh Windows.

**Solusi:**

1. Cabut dan hubungkan kembali flashdisk.
2. Coba port USB lain.
3. Periksa Disk Management.
4. Coba flashdisk lain jika perlu.

### Flashdisk tidak bisa boot

**Penyebab yang mungkin:**

- Mode boot tidak sesuai.
- Media bootable gagal dibuat.
- ISO tidak kompatibel.
- Pengaturan firmware membatasi media boot.

**Solusi:**

1. Periksa apakah Rufus menyelesaikan proses tanpa error.
2. Periksa pilihan UEFI atau Legacy.
3. Pastikan flashdisk dipilih dari Boot Menu.
4. Buat ulang media dari ISO yang tepercaya.

### Error GPT atau MBR

Pesan ini dapat muncul ketika mode boot atau skema partisi tidak sesuai dengan disk tujuan.

**Solusi:**

- Periksa mode boot yang digunakan.
- Periksa skema partisi disk.
- Cadangkan data sebelum mengubah struktur partisi.
- Jangan mengonversi disk secara sembarangan karena proses tertentu dapat menghapus data.

### Installer Windows tidak menemukan disk

Kemungkinan penyebab meliputi driver penyimpanan yang belum tersedia, konfigurasi controller penyimpanan, atau masalah kompatibilitas.

**Solusi:**

- Periksa pengaturan penyimpanan di firmware.
- Periksa apakah SSD/HDD terdeteksi oleh BIOS/UEFI.
- Dapatkan driver penyimpanan yang tepat dari produsen perangkat.
- Jangan mengubah mode controller secara acak.

### File ISO gagal dibaca

- Pastikan unduhan selesai.
- Periksa ukuran file.
- Cocokkan checksum dengan nilai resmi jika tersedia.
- Unduh ulang dari sumber tepercaya bila perlu.

### Windows gagal diaktifkan

- Periksa edisi Windows.
- Periksa status lisensi.
- Pastikan lisensi cocok dengan instalasi.
- Gunakan pemecah masalah aktivasi atau dukungan resmi Microsoft.

---

## ◈ 13. KEAMANAN DAN VERIFIKASI FILE

Keamanan installer sama pentingnya dengan keberhasilan proses instalasi.

### Gunakan sumber tepercaya

Prioritaskan:

- Microsoft untuk installer Windows.
- Microsoft atau portal lisensi resmi untuk Office.
- Rufus untuk utilitas bootable.
- Situs produsen perangkat untuk driver.

### Periksa integritas file

Jika sumber menyediakan checksum:

1. Catat nilai checksum resmi.
2. Hitung checksum file yang diunduh.
3. Bandingkan kedua nilai.
4. Jangan gunakan file jika nilainya berbeda.

Contoh menggunakan PowerShell:

```powershell
Get-FileHash ".\Windows.iso" -Algorithm SHA256
```

Perintah tersebut menghitung hash SHA-256 file lokal. Hasilnya harus dibandingkan dengan checksum resmi yang cocok dengan file yang diunduh.

### Hindari sumber mencurigakan

- Jangan menjalankan file yang meminta izin tidak wajar.
- Hindari installer dengan aktivator tidak resmi.
- Jangan memasukkan akun Microsoft ke situs mirror.
- Jangan menonaktifkan antivirus hanya karena diminta situs unduhan.
- Pindai file sebelum menjalankannya.

---

## ◈ 14. CHECKLIST AKHIR

### Sebelum membuat bootable

- [ ] Flashdisk berfungsi.
- [ ] Data flashdisk sudah dicadangkan.
- [ ] ISO berasal dari sumber tepercaya.
- [ ] Arsitektur sistem sudah diperiksa.
- [ ] Skema partisi sudah dipilih.
- [ ] File penting komputer sudah dicadangkan.

### Setelah membuat bootable

- [ ] Rufus selesai tanpa error.
- [ ] Flashdisk terbaca.
- [ ] Boot Menu mengenali flashdisk.
- [ ] Mode boot sesuai.
- [ ] Windows Setup berhasil dimuat.

### Setelah instalasi

- [ ] Windows berhasil masuk ke desktop.
- [ ] Driver perangkat diperiksa.
- [ ] Pembaruan keamanan diperiksa.
- [ ] Aktivasi menggunakan lisensi sah.
- [ ] Data cadangan dipulihkan.
- [ ] Aplikasi dipasang dari sumber tepercaya.

---

## ◈ 15. REFERENSI RESMI

| Resource | Link |
|:---|:---|
| Rufus | https://rufus.ie/ |
| Rufus GitHub | https://github.com/pbatard/rufus |
| Windows 11 | https://www.microsoft.com/software-download/windows11 |
| Windows 10 | https://www.microsoft.com/software-download/windows10 |
| Microsoft 365 | https://www.microsoft.com/microsoft-365 |
| Microsoft Account | https://account.microsoft.com/ |

---

<div align="center">

### ✦ DOCUMENTATION COMPLETE ✦

**Understand the system. Prepare the media. Install responsibly.**

<sub>Windows Installation Toolkit · Community Documentation</sub>

</div>
