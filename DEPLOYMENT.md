# 🚀 Panduan Deployment Portfolio

Dokumen ini berisi panduan lengkap untuk mendeploy portfolio website Anda ke berbagai platform hosting gratis.

## 📋 Daftar Isi

1. [GitHub Pages](#github-pages) - **Recommended**
2. [Netlify](#netlify)
3. [Vercel](#vercel)
4. [Cloudflare Pages](#cloudflare-pages)

---

## 🌟 GitHub Pages

**Gratis • Mudah • Cepat**

### Langkah-langkah:

#### 1. Persiapan Repository

```bash
# Inisialisasi Git (jika belum)
git init

# Tambahkan semua file
git add .

# Commit pertama
git commit -m "Initial commit: Portfolio website"

# Buat repository di GitHub (via web)
# Kemudian hubungkan dengan repository lokal
git remote add origin https://github.com/username/portfolio.git
git branch -M main
git push -u origin main
```

#### 2. Aktifkan GitHub Pages

1. Buka repository di GitHub
2. Klik **Settings** → **Pages**
3. Di **Source**, pilih:
   - Branch: `main`
   - Folder: `/ (root)`
4. Klik **Save**
5. Tunggu beberapa menit, website Anda akan aktif di:
   ```
   https://username.github.io/portfolio/
   ```

#### 3. Custom Domain (Opsional)

Jika punya domain sendiri:

1. Buat file `CNAME` di root folder:
   ```
   portfolio.namadomain.com
   ```

2. Setting DNS di provider domain:
   ```
   Type: CNAME
   Name: portfolio (atau @)
   Value: username.github.io
   ```

3. Di GitHub Pages settings, masukkan custom domain

### Update Website

```bash
# Setiap kali ada perubahan
git add .
git commit -m "Update portfolio content"
git push
```

---

## 🎯 Netlify

**Gratis • Fitur Lengkap • CI/CD Otomatis**

### Metode 1: Drag & Drop (Termudah)

1. Buka [netlify.com](https://www.netlify.com/)
2. Login/Sign up (bisa pakai GitHub)
3. Klik **Add new site** → **Deploy manually**
4. Drag & drop folder portfolio Anda
5. Website langsung online! 🎉

URL otomatis: `random-name-123.netlify.app`

### Metode 2: Git Integration (Recommended)

1. Push code ke GitHub (lihat panduan GitHub Pages)
2. Di Netlify, klik **Add new site** → **Import from Git**
3. Pilih GitHub → Pilih repository
4. Setting build:
   ```
   Build command: (kosongkan)
   Publish directory: .
   ```
5. Klik **Deploy site**

### Custom Domain di Netlify

1. Di dashboard Netlify → **Domain settings**
2. Klik **Add custom domain**
3. Ikuti instruksi DNS yang diberikan

### Update Website
- Jika pakai Drag & Drop: Upload ulang folder
- Jika pakai Git: Push ke GitHub, Netlify auto-deploy

---

## ⚡ Vercel

**Gratis • Super Cepat • Next.js Friendly**

### Langkah-langkah:

1. Push code ke GitHub
2. Buka [vercel.com](https://vercel.com/)
3. Login dengan GitHub
4. Klik **Add New** → **Project**
5. Import repository portfolio
6. Setting:
   ```
   Framework Preset: Other
   Build Command: (kosongkan)
   Output Directory: .
   ```
7. Klik **Deploy**

URL otomatis: `portfolio-username.vercel.app`

### Custom Domain

1. Di project dashboard → **Settings** → **Domains**
2. Add domain Anda
3. Update DNS sesuai instruksi

### Update Website
Auto-deploy setiap push ke GitHub

---

## 🔷 Cloudflare Pages

**Gratis • CDN Global • Unlimited Bandwidth**

### Langkah-langkah:

1. Push code ke GitHub
2. Buka [pages.cloudflare.com](https://pages.cloudflare.com/)
3. Login/Sign up
4. Klik **Create a project**
5. Connect GitHub account
6. Pilih repository
7. Setting:
   ```
   Production branch: main
   Build command: (kosongkan)
   Build output directory: .
   ```
8. Klik **Save and Deploy**

URL otomatis: `portfolio.pages.dev`

### Custom Domain

1. Di Cloudflare Pages dashboard
2. **Custom domains** → **Set up a custom domain**
3. Follow instruksi

### Update Website
Auto-deploy setiap push ke GitHub

---

## 📊 Perbandingan Platform

| Feature | GitHub Pages | Netlify | Vercel | Cloudflare |
|---------|--------------|---------|---------|------------|
| **Harga** | Gratis | Gratis | Gratis | Gratis |
| **Bandwidth** | Soft limit | 100GB/bulan | 100GB/bulan | Unlimited |
| **Build Minutes** | - | 300 menit/bulan | - | 500/bulan |
| **Custom Domain** | ✅ | ✅ | ✅ | ✅ |
| **HTTPS** | ✅ Auto | ✅ Auto | ✅ Auto | ✅ Auto |
| **Auto Deploy** | ✅ | ✅ | ✅ | ✅ |
| **Forms** | ❌ | ✅ (100 submit/bulan) | ❌ | ✅ |
| **Analytics** | ❌ | ✅ Basic | ✅ Basic | ✅ |
| **Edge Functions** | ❌ | ✅ | ✅ | ✅ |

## 🎯 Rekomendasi

### Untuk Pemula:
**GitHub Pages** - Paling simple, langsung dari repository

### Untuk Portfolio Profesional:
**Netlify** - Fitur lengkap, forms, analytics

### Untuk Performa Maksimal:
**Vercel** atau **Cloudflare Pages** - CDN global, super cepat

---

## 🔧 Tips Optimasi Sebelum Deploy

### 1. Validasi HTML
```bash
# Gunakan W3C Validator
https://validator.w3.org/
```

### 2. Test Responsiveness
- Chrome DevTools (F12) → Device toolbar
- Test di berbagai ukuran layar

### 3. Check Lighthouse Score
1. Buka Chrome DevTools (F12)
2. Tab **Lighthouse**
3. Click **Generate report**
4. Target: 90+ untuk semua metrics

### 4. Compress Images (Jika Ada)
- Gunakan TinyPNG atau ImageOptim
- Format WebP untuk modern browsers

### 5. Minify Code (Opsional)
Untuk production, bisa gunakan:
- HTML Minifier
- CSS Minifier
- JavaScript Minifier

---

## 🚨 Troubleshooting

### Website tidak muncul/blank:
- Check console browser (F12) untuk error
- Pastikan semua path file benar
- Clear cache browser (Ctrl+Shift+R)

### CSS tidak load:
- Pastikan Tailwind CDN link benar
- Check network tab di DevTools

### Form tidak berfungsi:
- Form di template ini adalah dummy
- Untuk form nyata, butuh backend atau gunakan:
  - Netlify Forms
  - Formspree
  - Google Forms embed

### Custom Domain tidak kerja:
- DNS propagation butuh waktu 24-48 jam
- Check DNS dengan: `nslookup namadomain.com`

---

## 📚 Resource Tambahan

- [GitHub Pages Documentation](https://docs.github.com/pages)
- [Netlify Documentation](https://docs.netlify.com/)
- [Vercel Documentation](https://vercel.com/docs)
- [Cloudflare Pages Documentation](https://developers.cloudflare.com/pages/)

---

## 🎓 Kesimpulan

Semua platform di atas excellent untuk portfolio static website. Pilih yang paling sesuai dengan kebutuhan dan skill level Anda.

**Quick Start untuk Pemula:**
1. Personalisasi `index.html`
2. Push ke GitHub
3. Deploy ke GitHub Pages
4. ✨ Portfolio online!

Selamat mencoba! 🚀

---

**Last Updated:** November 2026
**Author:** Portfolio Template for SMK RPL Students
