# ⚡ Quick Start Guide

Panduan cepat untuk mulai menggunakan template portfolio ini dalam 10 menit!

## 🎯 Langkah Cepat (10 Menit)

### 1️⃣ Buka File HTML (1 menit)

```bash
# Buka di VS Code atau editor favorit Anda
code index.html

# Atau double-click index.html untuk preview di browser
```

### 2️⃣ Replace Data Penting (5 menit)

Gunakan Find & Replace (Ctrl+H) di editor Anda:

| Cari Ini | Ganti Dengan | Jumlah |
|----------|--------------|--------|
| `[Nama Lengkap]` | Nama lengkap Anda | 5x |
| `[Email Saya]` | email@example.com | 2x |
| `[NomorWhatsApp]` | 628123456789 | 1x |
| `[Link LinkedIn]` | https://linkedin.com/in/username | 2x |
| `[Link Instagram]` | https://instagram.com/username | 2x |

**💡 Tip:** Untuk WhatsApp, format nomor: `628xxxxxxxxxx` (62 = kode Indonesia, tanpa +, 0, atau spasi)

### 3️⃣ Replace Data Pendidikan (2 menit)

| Cari Ini | Ganti Dengan |
|----------|--------------|
| `[Nama SMK]` | Nama sekolah SMK Anda |
| `[Nama SD]` | Nama SD Anda |
| `[Nama SMP]` | Nama SMP Anda |
| `[Tempat, Tanggal Lahir]` | Jakarta, 1 Januari 2005 |
| `[Alamat Lengkap Siswa]` | Alamat lengkap Anda |

### 4️⃣ Update Project Links (2 menit)

Cari dan ganti:

```
[GITHUB_URL_BANK_MELASA]   → https://github.com/username/bank-melasa
[GITHUB_URL_EVENTTY]       → https://github.com/username/eventty
[GITHUB_URL_ECOMMERCE]     → https://github.com/username/ecommerce
```

**❓ Belum punya repository?** Bisa di-skip dulu atau gunakan `#` sebagai placeholder.

### 5️⃣ Test & Preview

```bash
# Buka di browser
# Double-click index.html

# ATAU gunakan Live Server (VS Code extension)
# Right-click index.html → Open with Live Server
```

---

## 🚀 Deploy Cepat ke GitHub Pages (5 Menit)

### A. Setup Git & GitHub

```bash
# 1. Init Git
git init

# 2. Add files
git add .

# 3. Commit
git commit -m "Initial commit: My portfolio"

# 4. Buat repo di GitHub (via browser)
#    - Buka github.com
#    - Click New repository
#    - Nama: portfolio
#    - Public
#    - Jangan init with README (karena sudah ada)

# 5. Connect & Push
git remote add origin https://github.com/USERNAME/portfolio.git
git branch -M main
git push -u origin main
```

### B. Aktifkan GitHub Pages

1. Buka repository di GitHub
2. **Settings** → **Pages**
3. Source: **main** branch, **/ (root)** folder
4. **Save**
5. Tunggu 2-3 menit ✨

**Portfolio Anda online di:**
```
https://USERNAME.github.io/portfolio/
```

---

## 📝 Checklist Minimal

Sebelum publish, pastikan:

- [ ] Nama lengkap sudah diganti (cek di 5 tempat)
- [ ] Email berfungsi (test klik link email)
- [ ] WhatsApp link berfungsi (test di HP)
- [ ] Social media links valid
- [ ] Data pendidikan benar
- [ ] Test di mobile (Chrome DevTools - F12)
- [ ] Test semua navigation links

---

## 🎨 Personalisasi Lanjutan (Opsional)

### Ganti Foto Profil

1. Siapkan foto (square, min 500x500px)
2. Taruh di folder portfolio: `foto-profil.jpg`
3. Edit line ~252 di `index.html`:

```html
<!-- Dari: -->
<img src="https://lh3.google..." />

<!-- Jadi: -->
<img src="foto-profil.jpg" />
```

### Tambah Skill Baru

Cari section Skills (line ~440), copy-paste block ini:

```html
<div class="flex items-center justify-between p-2 rounded bg-surface border border-outline-variant/20">
  <span class="font-label-sm text-label-sm text-on-surface">React JS</span>
  <span class="w-1.5 h-1.5 rounded-full bg-tertiary"></span>
</div>
```

### Edit Project

Cari section Projects (line ~470), edit:
- Nama project
- Deskripsi
- Tech stack pills
- URLs

---

## 🆘 Troubleshooting Cepat

### ❌ Website tampil blank
```bash
# Check console error (F12 di browser)
# Biasanya: path file salah atau CDN blocked
```

### ❌ CSS tidak load
```bash
# Pastikan internet aktif (butuh Tailwind CDN)
# Hard refresh: Ctrl + Shift + R
```

### ❌ Icons tidak muncul
```bash
# Material Symbols butuh internet
# Check Google Fonts CDN
```

### ❌ Mobile menu tidak juga
```bash
# Check JavaScript di bagian bawah file
# Pastikan tidak ada error di console
```

---

## 📚 File Yang Perlu Dibaca

Baca **sesuai kebutuhan**:

| File | Kapan Dibaca | Durasi |
|------|--------------|--------|
| `QUICKSTART.md` | 🔥 **Sekarang!** | 10 min |
| `CHECKLIST.md` | Sebelum personalisasi detail | 5 min |
| `README.md` | Untuk dokumentasi lengkap | 15 min |
| `DEPLOYMENT.md` | Sebelum deploy ke hosting | 20 min |

---

## 🎯 Next Steps

Setelah quick start ini:

1. ✅ **Deploy dulu** ke GitHub Pages
2. 📱 **Test share** link ke teman
3. 🎨 **Personalisasi lanjut** pakai CHECKLIST.md
4. 📊 **Improve** pakai Lighthouse suggestions
5. 🚀 **Share** portfolio di LinkedIn/Instagram!

---

## 💡 Pro Tips

### Untuk Editor
- **VS Code** recommended (gratis)
- Install extension: Live Server, Prettier
- Format on save untuk kode lebih rapi

### Untuk Testing
- Test di **Chrome DevTools** (F12)
- Device toolbar untuk mobile preview
- Network tab untuk check loading

### Untuk Konten
- Keep it **professional** tapi tetap **personal**
- Foto profil **formal** tapi **approachable**
- Project descriptions **clear** dan **concise**

---

## 🎊 Congratulations!

Jika sudah sampai sini, portfolio Anda harusnya sudah:
- ✅ Personalized dengan data Anda
- ✅ Tested di browser
- ✅ Ready to deploy!

**Selamat!** Portfolio Anda siap membantu karir di dunia teknologi! 🚀

---

## 📞 Butuh Bantuan?

1. Check **README.md** untuk detail
2. Check **DEPLOYMENT.md** untuk hosting
3. Check **CHECKLIST.md** untuk personalisasi lengkap
4. Google error message di console
5. Ask di forum/komunitas (Stack Overflow, etc)

---

**Last updated:** November 2026
**Template version:** 1.0

*Happy coding! 💻*
