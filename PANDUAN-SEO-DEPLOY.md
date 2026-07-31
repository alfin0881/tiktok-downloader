# Panduan SEO Off-Page, Indeksasi Cepat & Deploy — SnapTok

> File pendukung: `seo-head-additions.html`, `robots.txt`, `sitemap.xml`.
> Ganti semua contoh `https://snaptok.app` dengan domain asli Anda sebelum publish.

---

## 1. Verifikasi Situs di Google Search Console (GSC)

1. **Buka** https://search.google.com/search-console dan login dengan akun Google.
2. **Tambah properti** → pilih tipe **"Awalan URL" (URL prefix)**, masukkan `https://snaptok.app/` (lebih mudah diverifikasi daripada tipe "Domain" yang butuh akses DNS).
3. **Metode verifikasi** — pilih salah satu yang paling praktis untuk hosting Anda:
   - **HTML tag**: salin meta tag yang diberikan GSC, tempel ke placeholder `google-site-verification` di file `seo-head-additions.html`, lalu deploy ulang.
   - **File HTML**: unduh file `google[xxxxx].html` dari GSC, upload ke root folder situs (sejajar dengan `index.html`), pastikan bisa diakses di `https://snaptok.app/google[xxxxx].html`.
   - **DNS TXT record** (paling stabil, tidak hilang saat ganti hosting): tambahkan TXT record di panel DNS domain Anda.
4. Klik **Verify**. Setelah berhasil, buka menu **Sitemaps** di sidebar kiri → masukkan `sitemap.xml` → **Submit**.
5. Cek menu **Page indexing** secara berkala untuk memantau status crawl & error.

## 2. Verifikasi Situs di Bing Webmaster Tools

1. Buka https://www.bing.com/webmasters dan login (bisa pakai akun Microsoft).
2. **Cara tercepat**: gunakan fitur **"Import from Google Search Console"** — Bing akan otomatis menarik data properti & sitemap dari GSC yang sudah Anda verifikasi. Ini menghemat waktu verifikasi manual.
3. Jika verifikasi manual: tambahkan meta tag `msvalidate.01` (sudah disiapkan di `seo-head-additions.html`) atau upload file XML verifikasi ke root domain.
4. Setelah terverifikasi, buka **Sitemaps** → submit `https://snaptok.app/sitemap.xml`.
5. Yandex Webmaster (opsional, jika menyasar trafik Rusia/Asia Tengah): https://webmaster.yandex.com — proses serupa, gunakan meta tag `yandex-verification`.

## 3. Request Indexing agar Terindeks dalam 24–48 Jam

**Google:**
1. Di GSC, buka menu **URL Inspection** (ikon kaca pembesar di atas).
2. Masukkan URL penuh, contoh `https://snaptok.app/`.
3. Tunggu hasil pengecekan → jika status "URL is not on Google", klik **Request Indexing**.
4. Ulangi untuk setiap halaman penting (maksimal ~10-12 URL/hari agar tidak dianggap spam quota).
5. **Percepat crawl tambahan**: bagikan link situs di 2-3 platform berdomain otoritas tinggi (lihat bagian backlink di bawah) — Googlebot sering menemukan halaman baru lebih cepat lewat referral link dibanding menunggu crawl terjadwal.

**Bing:**
1. Bing Webmaster Tools punya kuota **URL Submission API** — di menu **URL Submission**, masukkan URL dan submit langsung (kuota harian cukup besar, ratusan URL/hari untuk situs baru).
2. Bing biasanya mengindeks lebih cepat dari Google untuk situs baru jika sitemap sudah valid.

**Catatan realistis:** 24–48 jam adalah target yang mungkin tercapai untuk *crawling* awal (Googlebot mengunjungi & membaca halaman), tapi **ranking di halaman 1** untuk keyword kompetitif seperti "download video tiktok" butuh waktu jauh lebih lama (biasanya berbulan-bulan) karena niche ini sangat kompetitif dan didominasi situs-situs lama dengan ribuan backlink.

---

## 4. Strategi Target Keyword

### Kelompok keyword inti (head terms — persaingan sangat tinggi)
| Keyword | Estimasi Kesulitan | Prioritas |
|---|---|---|
| download video tiktok | Sangat tinggi | Jangka panjang |
| tiktok downloader | Sangat tinggi | Jangka panjang |
| download tiktok tanpa watermark | Tinggi | Jangka menengah |

### Kelompok keyword long-tail (persaingan lebih rendah, lebih cepat naik)
Ini yang sebaiknya **jadi prioritas awal** karena situs baru sulit bersaing langsung di head terms:
- "cara download video tiktok tanpa watermark di hp"
- "download video tiktok kualitas hd gratis"
- "download mp3 dari video tiktok"
- "download foto slideshow tiktok"
- "situs download tiktok tanpa aplikasi"
- "download video tiktok tanpa watermark online"
- "tiktok downloader tanpa login"

### Cara eksekusi
1. Buat 1 halaman/artikel khusus per keyword long-tail (bukan cuma landing page tunggal) — ini sudah direfleksikan di contoh `sitemap.xml` di atas (`/cara-download-video-tiktok-tanpa-watermark`, `/download-mp3-tiktok`, dll). Masing-masing halaman: 600–1000 kata, jawab pertanyaan spesifik, sisipkan tool SnapTok di dalamnya.
2. Gunakan **Google Search Console → Performance** setelah 2-3 minggu untuk melihat query apa yang sudah mulai muncul (impression), lalu perkuat halaman terkait.
3. Riset gratis tambahan: Google Autocomplete, "Orang juga bertanya" (People Also Ask), dan Google Trends untuk variasi musiman (misal saat ada tren TikTok baru).
4. Pantau kompetitor (savefrom, snaptik, ssstik, musicaldown) lewat pencarian manual — lihat struktur H1/H2 dan FAQ mereka sebagai referensi konten (jangan menyalin langsung).

---

## 5. Strategi Backlink Berkualitas Awal (Niche Web Tool/Downloader)

Backlink adalah faktor terbesar untuk bersaing di niche downloader yang sangat kompetitif. Fokus **kualitas & relevansi**, bukan kuantitas — backlink spam justru berisiko penalti.

1. **Direktori tools/software legit** — daftarkan SnapTok ke direktori seperti AlternativeTo, Product Hunt (khusus produk baru), SaaSHub, dan direktori software Indonesia. Ini backlink dofollow berkualitas dengan effort rendah.
2. **Forum & komunitas relevan** — jawab pertanyaan asli terkait "cara download video tiktok" di forum seperti Kaskus, Reddit (r/indonesia, r/TikTokHelp), Quora — sisipkan link SnapTok hanya jika benar-benar relevan dan jawaban Anda bermanfaat (bukan spam link kosong).
3. **Guest post / kolaborasi konten** — tawarkan artikel tamu ke blog teknologi/tips-trik Indonesia (misalnya blog niche gadget, tutorial HP) dengan topik seperti "5 cara download video TikTok tanpa watermark 2026" yang menyertakan link ke SnapTok.
4. **Press release / listing startup lokal** — situs seperti Startup Indonesia atau media teknologi lokal kadang meliput tools baru; ajukan press release singkat.
5. **Social signal** — buat akun resmi di X/Twitter, Instagram, TikTok itu sendiri (ironis tapi efektif), dan bagikan tool secara organik. Ini bukan backlink langsung tapi mendorong traffic + brand search yang membantu SEO.
6. **Backlink dari YouTube/TikTok** — buat video tutorial singkat "cara pakai SnapTok" dengan link di deskripsi; video di YouTube sering ranking tinggi untuk query "cara download tiktok" dan mengarahkan trafik + link.
7. **Hindari**: PBN (Private Blog Network) berbayar murah, backlink farm otomatis, dan direktori spam — ini berisiko manual action dari Google dan justru menurunkan trust situs baru.

**Kecepatan wajar**: bangun 5-10 backlink berkualitas per bulan secara konsisten jauh lebih aman dan efektif daripada 100 backlink instan dari sumber tidak jelas.

---

## 6. Panduan Deploy & Hosting — Shared Hosting atau VPS?

### Karakteristik situs SnapTok
Berdasarkan file yang Anda upload: situs ini adalah **single-page static site** (HTML/CSS/JS murni, Tailwind via CDN, tanpa backend server sendiri) yang memanggil API pihak ketiga (`tikwm.com`) langsung dari browser (client-side fetch). Ini artinya **tidak butuh server aplikasi/backend Anda sendiri** untuk menjalankan fitur utamanya.

### Rekomendasi: gunakan **Static Hosting / CDN**, bukan shared hosting maupun VPS

Untuk kasus spesifik SnapTok, opsi terbaik sebenarnya di luar dua pilihan yang Anda sebutkan:

| Opsi | Cocok untuk SnapTok? | Alasan |
|---|---|---|
| **Static hosting (Cloudflare Pages, Vercel, Netlify, GitHub Pages)** | ✅ **Paling direkomendasikan** | Gratis/murah, HTTPS otomatis, CDN global (loading cepat di seluruh Indonesia), auto-scaling saat trafik viral, tanpa maintenance server |
| **Shared Hosting** | ⚠️ Bisa, tapi kurang optimal | Cukup untuk trafik rendah-menengah, murah, tapi loading lebih lambat & rawan down saat trafik tiba-tiba naik (tool viral rentan lonjakan trafik mendadak) |
| **VPS** | ❌ Berlebihan untuk saat ini | Butuh maintenance manual (security patch, konfigurasi Nginx/Apache, SSL), biaya lebih mahal, tidak diperlukan karena situs tidak punya backend sendiri |

### Kenapa static hosting/CDN lebih unggul untuk niche ini:
1. **Kecepatan** — Core Web Vitals (LCP, INP, CLS) adalah faktor ranking Google. CDN global membuat TTFB jauh lebih rendah dibanding shared hosting satu server.
2. **Tahan lonjakan trafik** — tools downloader sering viral mendadak (misal dibagikan di grup WhatsApp/TikTok); static hosting dengan CDN auto-scale tanpa server down, sementara shared hosting sering kena "resource limit exceeded".
3. **Biaya** — Cloudflare Pages, Vercel, dan Netlify punya tier gratis yang sangat cukup untuk static site seperti ini; jauh lebih hemat dibanding VPS bulanan.
4. **Keamanan** — tidak ada server backend berarti permukaan serangan (attack surface) jauh lebih kecil; tidak perlu pusing patch OS/PHP/MySQL seperti di shared hosting/VPS.

### Kapan sebaiknya pindah ke VPS?
Pertimbangkan VPS **hanya jika** ke depannya Anda menambah:
- Backend sendiri (misal proxy API sendiri agar tidak bergantung ke `tikwm.com`, sistem cache/database, rate limiting server-side)
- Sistem user account/login
- Traffic sangat tinggi dengan kebutuhan kontrol server penuh

Untuk kondisi situs saat ini (client-side tool), itu belum diperlukan.

### Langkah deploy singkat (contoh: Cloudflare Pages — gratis)
1. Push kode (`index.html`, `robots.txt`, `sitemap.xml`) ke repository GitHub.
2. Login ke https://dash.cloudflare.com → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
3. Pilih repo, biarkan build command kosong (situs ini static, tanpa build step), set output directory ke root (`/`).
4. Deploy → Cloudflare otomatis memberi subdomain `*.pages.dev` + HTTPS gratis.
5. Hubungkan domain custom (`snaptok.app`) di menu **Custom domains**, arahkan DNS sesuai instruksi.
6. Setelah live, lanjutkan ke Bagian 1–3 di atas (verifikasi GSC/Bing, submit sitemap, request indexing).

---

## Ringkasan Checklist Go-Live

- [ ] Tempel isi `seo-head-additions.html` ke `<head>` index.html, isi kode verifikasi Search Console/Bing
- [ ] Upload `robots.txt` dan `sitemap.xml` ke root domain
- [ ] Deploy ke static hosting (Cloudflare Pages/Vercel/Netlify) + domain custom + HTTPS
- [ ] Verifikasi & submit sitemap di Google Search Console
- [ ] Verifikasi & submit sitemap di Bing Webmaster Tools (import dari GSC)
- [ ] Request Indexing untuk homepage via URL Inspection
- [ ] Validasi semua JSON-LD di https://search.google.com/test/rich-results
- [ ] Cek kecepatan situs di https://pagespeed.web.dev
- [ ] Mulai bangun 5-10 backlink berkualitas/bulan sesuai Bagian 5
- [ ] Buat halaman konten long-tail keyword tambahan (lihat Bagian 4) secara bertahap
