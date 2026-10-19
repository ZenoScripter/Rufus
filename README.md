
# Cara Membuat Bootable Windows Menggunakan Rufus

## 📌 Deskripsi

Bootable Windows adalah media instalasi Windows yang dapat dijalankan melalui flashdisk. Salah satu aplikasi yang digunakan untuk membuat bootable adalah **Rufus**.

Rufus membantu memformat flashdisk dan membuat media USB yang dapat digunakan untuk instalasi Windows.

## 🛠️ Alat dan Bahan

- Flashdisk dengan kapasitas yang cukup.
- File ISO Windows.
- Aplikasi Rufus.
- Komputer atau laptop.

> **Peringatan:** Proses pembuatan bootable akan menghapus data pada flashdisk. Cadangkan data penting sebelum memulai.

## 📥 1. Download Rufus

1. Buka browser di komputer.
2. Kunjungi situs resmi Rufus: https://rufus.ie/
3. Cari bagian **Download**.
4. Pilih versi Rufus yang diinginkan, termasuk versi portable.
5. Tunggu hingga proses download selesai.

## 💿 2. Membuat Bootable Windows

1. Hubungkan flashdisk ke komputer.
2. Jalankan aplikasi Rufus.
3. Klik **Yes** jika muncul permintaan izin.
4. Pada bagian `Device`, pilih flashdisk yang akan digunakan.
5. Pada bagian `Boot selection`, klik `SELECT`.
6. Pilih file ISO Windows yang sudah disiapkan.
7. Atur `Partition scheme` sesuai dengan sistem komputer:
   - `GPT` untuk sistem UEFI.
   - `MBR` untuk sistem Legacy BIOS.
8. Periksa kembali pengaturannya.
9. Klik `START`.
10. Konfirmasikan peringatan yang muncul setelah memastikan perangkat yang dipilih sudah benar.
11. Tunggu hingga proses selesai.
12. Klik `CLOSE` jika proses telah berhasil.

## ⚙️ 3. Mengatur Boot Priority di BIOS

1. Hubungkan flashdisk bootable ke komputer tujuan.
2. Nyalakan komputer dan masuk ke BIOS atau UEFI.
3. Gunakan tombol yang sesuai dengan perangkat, misalnya `F2`.
4. Buka menu `Boot`.
5. Pilih flashdisk sebagai perangkat boot pertama, atau gunakan Boot Menu untuk memilihnya.
6. Pastikan mode boot sesuai dengan media instalasi.
7. Simpan pengaturan melalui `Exit Saving Changes` jika diperlukan.
8. Komputer akan mencoba menjalankan installer Windows dari flashdisk.

## ✅ 4. Memulai Instalasi Windows

Jika komputer berhasil melakukan boot dari flashdisk, menu instalasi Windows akan muncul.

Ikuti petunjuk pada layar untuk melanjutkan instalasi. Pastikan data penting pada penyimpanan komputer sudah dicadangkan sebelum melakukan instalasi ulang.

## ⚠️ Hal yang Perlu Diperhatikan

- Gunakan flashdisk yang berfungsi dengan baik.
- Pastikan file ISO berasal dari sumber tepercaya.
- Jangan sampai salah memilih perangkat pada Rufus.
- Sesuaikan GPT/MBR dan UEFI/Legacy dengan kebutuhan komputer.
- Membuat bootable tidak sama dengan menyelesaikan instalasi Windows.

## 📝 Kesimpulan

Rufus merupakan aplikasi untuk membuat media USB bootable dari file ISO. Dengan mengikuti langkah-langkah di atas, flashdisk dapat disiapkan sebagai media instalasi Windows.

---

**Referensi:**
- [Situs Resmi Rufus](https://rufus.ie/)
- [Rufus README di GitHub](https://github.com/pbatard/rufus/blob/master/README.md)
