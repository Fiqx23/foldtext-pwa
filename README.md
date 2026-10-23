# FoldText Lite PWA

PWA build terpisah untuk menguji performa tanpa menghilangkan fitur yang digunakan pada FoldText Lite.

## Source of truth
UI dan fitur inti diambil dari `Fiqx23/foldtext-app` pada saat baseline ini disiapkan. Fitur yang dipertahankan meliputi hierarki folder, editor, mode baca/edit, tema, pengaturan font/zoom/alignment, pencarian, shortcut keyboard, autentikasi Supabase, sinkronisasi manual, serta alur penanganan konflik yang ada di source.

## Perhatian data
- Repo ini memiliki origin dan storage browser yang berbeda dari `foldtext-app`; data IndexedDB/localStorage tidak otomatis ikut pindah.
- Jangan hapus repo lama atau menganggap data lokal berpindah otomatis.
- Supabase tetap menggunakan konfigurasi yang sudah tertanam atau override yang sudah digunakan source; jangan menambahkan kredensial baru ke repo.
- Service worker memiliki cache prefix tersendiri agar cache repo ini tidak bercampur dengan aplikasi lama.

## Deploy
GitHub Pages: Settings → Pages → Deploy from a branch → `main` → `/(root)`.

## Tujuan optimasi
Pertahankan perilaku dan fitur yang sudah digunakan. Optimasi berikutnya harus mengukur dan memperbaiki startup PWA secara bertahap, bukan mengganti produk dengan editor catatan minimal.
