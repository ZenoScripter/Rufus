
<div align="center">

# ⌁ Windows Bootable Creator

### Craft your Windows installation USB with Rufus.

<p>
  <img src="https://img.shields.io/badge/Platform-Windows-0078D4?style=for-the-badge&logo=windows&logoColor=white" alt="Windows"/>
  <img src="https://img.shields.io/badge/Tool-Rufus-6C63FF?style=for-the-badge" alt="Rufus"/>
  <img src="https://img.shields.io/badge/Guide-Installation-2EA44F?style=for-the-badge" alt="Installation Guide"/>
</p>

*A practical guide to creating a bootable Windows USB flash drive.*

</div>

---

## ◈ Overview

Panduan ini menjelaskan cara membuat **bootable installer Windows** menggunakan Rufus. Flashdisk bootable dapat digunakan untuk menjalankan installer Windows pada komputer atau laptop yang kompatibel.

## ⌘ Requirements

Sebelum memulai, siapkan beberapa hal berikut:

- ◉ **USB Flash Drive** — flashdisk dengan kapasitas yang cukup.
- ◉ **Windows ISO** — file installer Windows dari sumber tepercaya.
- ◉ **Rufus Utility** — aplikasi untuk membuat media bootable.
- ◉ **PC / Laptop** — perangkat untuk menyiapkan flashdisk.

> [!CAUTION]
> Proses ini akan menghapus data pada flashdisk yang dipilih. Cadangkan seluruh file penting sebelum melanjutkan.

## 01 · Download Rufus

1. Buka situs resmi [Rufus](https://rufus.ie/).
2. Gulir ke bagian **Download**.
3. Pilih versi Rufus yang diinginkan.
4. Tunggu hingga unduhan selesai.

## 02 · Prepare the USB

1. Hubungkan flashdisk ke komputer.
2. Jalankan Rufus.
3. Pilih **Yes** jika muncul permintaan izin.
4. Pada bagian `Device`, pilih flashdisk yang benar.
5. Pada bagian `Boot selection`, klik `SELECT`.
6. Cari dan pilih file ISO Windows.

## 03 · Configure Partition Scheme

Sesuaikan pengaturan dengan firmware komputer tujuan.

| Partition Scheme | Boot Mode |
| :--- | :--- |
| `GPT` | `UEFI` |
| `MBR` | `Legacy BIOS` |

> [!IMPORTANT]
> Tabel di atas merupakan panduan umum. Kompatibilitas bergantung pada konfigurasi perangkat. Untuk komputer UEFI modern, GPT biasanya menjadi pilihan yang tepat.

## 04 · Create Bootable USB

Setelah semua pengaturan benar:

1. Klik tombol `START`.
2. Periksa peringatan yang ditampilkan Rufus.
3. Konfirmasikan proses jika sudah yakin.
4. Tunggu hingga indikator proses selesai.
5. Klik `CLOSE`.

**Status:** Flashdisk siap digunakan sebagai media instalasi jika Rufus menyelesaikan proses tanpa error.

## 05 · Boot from USB

1. Hubungkan flashdisk ke komputer tujuan.
2. Nyalakan komputer dan buka BIOS/UEFI atau Boot Menu.
3. Gunakan tombol sesuai perangkat, misalnya `F2`, `F12`, `Esc`, atau `Del`.
4. Pilih flashdisk sebagai perangkat boot.
5. Simpan perubahan jika diperlukan.
6. Tunggu hingga Windows Setup muncul.

## 06 · Windows Setup

Setelah installer berhasil dimuat:

- Pilih bahasa dan pengaturan yang tersedia.
- Ikuti petunjuk Windows Setup.
- Cadangkan data penting sebelum melakukan instalasi.
- Periksa kembali disk dan partisi sebelum membuat perubahan.

## ⛨ Troubleshooting

| Problem | Possible Solution |
| :--- | :--- |
| Flashdisk tidak terdeteksi | Periksa port USB dan koneksi flashdisk. |
| Tidak bisa boot | Periksa Boot Menu dan kompatibilitas UEFI/Legacy. |
| File ISO tidak terbaca | Periksa file ISO dan unduh ulang jika rusak. |
| Rufus menampilkan error | Baca pesan error dan periksa flashdisk serta pengaturan. |

## ⌬ References

- [Rufus Official Website](https://rufus.ie/)
- [Rufus GitHub Repository](https://github.com/pbatard/rufus)
- [Microsoft Windows Download](https://www.microsoft.com/software-download/)

---

<div align="center">

### ✦ End of Documentation ✦

*Learn · Prepare · Install*

</div>
