# FoldText PWA

Repo eksperimen terpisah untuk mengukur dan mengoptimalkan startup PWA FoldText. Tidak mengubah repo APK utama `foldtext-app`.

## Prinsip

- Offline-first: tampilan catatan tidak bergantung pada CDN atau koneksi cloud.
- Catatan disimpan di IndexedDB; autosave lokal terdebounce.
- Tidak ada SDK eksternal yang diunduh saat startup.
- Service worker shell cache-first.
- Sinkronisasi cloud belum diaktifkan pada baseline ini. Jangan memakai baseline ini sebagai pengganti aplikasi utama sampai kompatibilitas serta proses migrasi data diuji.

## Uji baseline

1. Buka GitHub Pages saat online sekali agar service worker menyimpan shell.
2. Tutup dan buka ulang; bandingkan cold/warm startup di DevTools Performance.
3. Uji offline, buat/edit/hapus catatan, lalu ekspor dan impor JSON.
4. Tambahkan cloud hanya setelah baseline lokal terukur dan stabil.

## Data

Versi baseline menggunakan IndexedDB database `FoldTextPWA` sendiri agar tidak menimpa data `FoldTextDB` aplikasi utama. Impor/ekspor JSON tersedia untuk memindahkan salinan catatan secara eksplisit.
