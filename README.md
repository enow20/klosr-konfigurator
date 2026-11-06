# Konfigurator Klosr

Halaman mockup tag grafir untuk strap jam dan tali sepatu. Cari model jam supaya lebar strap terisi otomatis, ketik teks, ganti bentuk, finishing, dan font, lalu cek tinggi huruf dan ukuran asli di layar.

Buka di laptop atau HP: https://enow20.github.io/klosr-konfigurator/

Repo ini dulu bernama `lifetag-konfigurator`. Link lama (`/lifetag-konfigurator/`) sudah tidak berlaku. Kalau sudah dipasang di layar utama HP, hapus lalu pasang lagi dari link baru.

Tampilan tim (alat internal untuk wawancara: bentuk usulan, plat pembanding, sumber data, detail teknis, perbandingan, ukuran asli) dibuka lewat link yang sama dengan akhiran `#tim`.

Tidak perlu login. Setelah sekali dibuka, halaman tetap jalan tanpa sinyal. Di HP bisa dipasang ke layar utama lewat menu browser ("Tambahkan ke layar utama" atau "Add to Home Screen").

## Isi repo

| File | Isi |
| --- | --- |
| `index.html` | Halaman konfigurator. Tampilan dan logika ada di satu file ini. |
| `lebar-strap-jam.csv` | Lebar strap bawaan per model jam, dengan sumber per baris. |
| `sw.js` | Menyimpan salinan halaman dan data di perangkat supaya tetap jalan tanpa sinyal. |
| `manifest.webmanifest`, `icon-192.png`, `icon-512.png` | Supaya bisa dipasang ke layar utama HP. |

## Mengubah data jam

1. Edit `lebar-strap-jam.csv`. Bisa langsung di GitHub: buka file, klik ikon pensil, lalu commit.
2. Kolom: `merek`, `model`, `varian`, `lebar_strap_mm` (kosongkan kalau belum tahu), `pemasangan`, `keyakinan` (`spek pabrikan`, `daftar kompatibilitas`, atau `lemah, ukur`), `alias` (kata kunci pencarian, dipisah `|`), `sumber`.
3. Situs ikut terbarui sekitar satu menit setelah commit. Di HP, buka ulang halaman sekali supaya salinan offline ikut terbarui.

## Penting

Repo dan situs ini publik. Jangan taruh harga, vendor, angka penjualan, atau rencana bisnis di sini. Halaman memakai tag `noindex` supaya tidak muncul di mesin pencari.
