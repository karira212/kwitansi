# Aplikasi Cetak Kwitansi

Aplikasi berbasis web untuk membuat, mengelola, meninjau, mengekspor, mencadangkan, memulihkan, dan mencetak kwitansi kegiatan PKK secara cepat dan rapi.

## Ringkasan

- Pencatatan transaksi tanggal, nomor, penerima, nominal, dan keterangan.
- Pratinjau kwitansi berukuran **16 cm × 8 cm**.
- Nominal otomatis ditulis dalam bentuk terbilang Rupiah.
- Pengaturan kop vertikal, logo, kota, nama Ketua, nama Bendahara, dan tanda tangan.
- Import/export data Excel.
- Backup dan restore SQLite.
- Pencetakan satu lembar atau beberapa lembar sekaligus.
- Penyimpanan lokal pada browser.

## File Utama

Buka:

```text
KWITANSI-PKK-REVISI-V2-3.html
```

Dokumentasi lengkap tersedia pada [DOCS.md](DOCS.md).

## Menjalankan Aplikasi

### Cara Termudah dengan XAMPP

1. Letakkan folder aplikasi di `C:\xampp\htdocs\kwitansi`.
2. Jalankan Apache pada XAMPP.
3. Buka browser dan kunjungi:

```text
http://localhost/kwitansi/KWITANSI-PKK-REVISI-V2-3.html
```

### Cara Browser Langsung

Klik dua kali file HTML untuk membukanya melalui browser. Untuk hasil yang paling stabil, gunakan server lokal XAMPP.

## Cara Penggunaan Singkat

### Menambah transaksi

1. Pilih **Tambah Transaksi**.
2. Isi tanggal, nomor, pihak penerima, nominal, dan keterangan.
3. Pilih **Simpan Transaksi**.

### Mengubah atau mencetak

- Pilih ikon **mata** untuk melihat pratinjau.
- Pilih ikon **pensil** untuk mengubah transaksi.
- Pilih ikon **printer** untuk mencetak satu kwitansi.
- Tandai beberapa transaksi lalu pilih **Cetak Yang Dipilih** untuk mencetak sekaligus.

### Mengatur kop dan tanda tangan

Pilih **Pengaturan & Asset**, lalu atur:

- Teks dan font kop vertikal.
- Logo.
- Nama Ketua dan Bendahara.
- Kota lokasi kwitansi.
- Tanda tangan dan gambar kop.

Pilih **Simpan Pengaturan** setelah selesai.

### Import Excel

1. Pilih **Import Excel**.
2. Unduh template Excel.
3. Isi kolom `Tanggal`, `Nomor`, `Sudah Terima Dari`, `Nominal`, dan `Keterangan`.
4. Pilih file Excel.
5. Pilih **Proses Import**.

### Ekspor Excel

Pilih **Ekspor Ke Excel**. Jika kotak pilihan transaksi ditandai, aplikasi hanya mengekspor transaksi terpilih.

### Backup SQLite

1. Pilih **Backup & Restore SQLite**.
2. Pilih **Unduh File Backup SQLite (.sqlite)**.
3. Simpan file di lokasi aman.

Untuk memulihkan data, pilih file `.sqlite` atau `.db`, lalu pilih **Proses Restore Database**.

## Pengaturan Cetak

- Orientasi: **Portrait**
- Ukuran kwitansi: **16 cm × 8 cm**
- Satu lembar berisi satu kwitansi atau susunan beberapa kwitansi sesuai pilihan.
- Periksa hasil pada area pratinjau sebelum mencetak.

## Penyimpanan dan Keamanan Data

Data transaksi dan pengaturan disimpan di Local Storage browser. Data dapat hilang jika data browser dihapus atau browser/gadget diganti. Disarankan melakukan backup SQLite secara berkala.

## Teknologi

- HTML5
- CSS dan Tailwind CSS
- JavaScript
- Local Storage
- SQL.js
- SheetJS/XLSX
- Font Awesome
