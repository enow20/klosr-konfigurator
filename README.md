# Konfigurator Klosr

Halaman mockup tag grafir untuk strap jam dan tali sepatu. Cari model jam supaya lebar strap terisi otomatis, ketik teks, ganti bentuk, finishing, dan font, lalu cek tinggi huruf dan ukuran asli di layar.

Buka di laptop atau HP: https://enow20.github.io/klosr-konfigurator/

Repo ini dulu bernama `lifetag-konfigurator`. Link lama (`/lifetag-konfigurator/`) sudah tidak berlaku. Kalau sudah dipasang di layar utama HP, hapus lalu pasang lagi dari link baru.

Tampilan tim (alat internal) dibuka lewat link yang sama dengan akhiran `#tim` dan dikunci password. Isinya disimpan terenkripsi di `tim.enc.json`. Password tidak ada di repo ini.

Tampilan pembeli tidak perlu login. Setelah sekali dibuka, halaman tetap jalan tanpa sinyal. Di HP bisa dipasang ke layar utama lewat menu browser ("Tambahkan ke layar utama" atau "Add to Home Screen").

## Isi repo

| File | Isi |
| --- | --- |
| `index.html` | Halaman konfigurator untuk pembeli, plus kolom password untuk `#tim`. Dibuat oleh skrip build dari sumber yang disimpan terpisah, jadi jangan diedit langsung di sini. |
| `tim.enc.json` | Tampilan tim dalam bentuk terenkripsi (AES-GCM, kunci dari password lewat PBKDF2). Dibuat oleh skrip build yang sama. |
| `lebar-strap-jam.csv` | Lebar strap bawaan per model jam, dengan sumber per baris. |
| `sw.js` | Menyimpan salinan halaman dan data di perangkat supaya tetap jalan tanpa sinyal. |
| `manifest.webmanifest`, `icon-192.png`, `icon-512.png` | Supaya bisa dipasang ke layar utama HP. |

## Mengubah data jam

1. Edit `lebar-strap-jam.csv`. Bisa langsung di GitHub: buka file, klik ikon pensil, lalu commit.
2. Kolom: `merek`, `model`, `varian`, `lebar_strap_mm` (kosongkan kalau belum tahu), `pemasangan`, `keyakinan` (`spek pabrikan`, `daftar kompatibilitas`, atau `lemah, ukur`), `alias` (kata kunci pencarian, dipisah `|`), `sumber`.
3. Situs ikut terbarui sekitar satu menit setelah commit. Di HP, buka ulang halaman sekali supaya salinan offline ikut terbarui.

## Penting

Repo dan situs ini publik. Jangan taruh harga, vendor, angka penjualan, rencana bisnis, atau password di sini. Halaman memakai tag `noindex` supaya tidak muncul di mesin pencari.
