# 🎓 Portfolio Website - Siswa RPL

Portfolio website untuk siswa kelas XII Rekayasa Perangkat Lunak (RPL) dengan desain modern dan profesional menggunakan Material Design 3 (Dark Theme) dan Tailwind CSS.

## ✨ Fitur Utama

- **Desain Modern Dark Theme**: Menggunakan Material Design 3 dengan skema warna yang elegan dan eye-friendly
- **Fully Responsive**: Tampilan optimal di semua perangkat (Desktop, Tablet, Mobile)
- **Single Page Application**: Navigasi smooth scroll dengan anchoring
- **Animasi & Transitions**: Interaksi yang halus dan profesional
- **SEO Friendly**: Struktur HTML semantik dan meta tags yang lengkap
- **Performance Optimized**: Menggunakan CDN untuk library dan font loading yang optimal

## 📋 Struktur Halaman

1. **Hero Section**: Headline portofolio dengan status ketersediaan dan CTA buttons
2. **About Me**: Profil pribadi lengkap dengan foto dan data akademik terstruktur
3. **Education Journey**: Timeline riwayat pendidikan dari SD hingga SMK
4. **Skills & Technologies**: Kategori skills (Frontend, Backend, Database, Tools)
5. **Selected Projects**: Showcase project unggulan dengan detail fitur dan tech stack
6. **Contact**: Multiple contact methods dengan form pesan langsung

## 🛠️ Teknologi yang Digunakan

- **HTML5**: Struktur markup semantik
- **Tailwind CSS v3**: Utility-first CSS framework via CDN
- **JavaScript (Vanilla)**: Interaktivitas untuk mobile menu
- **Google Fonts**:
  - Inter (Body text)
  - JetBrains Mono (Labels & code-like text)
  - Plus Jakarta Sans (Headlines)
- **Material Symbols**: Icon system dari Google

## 🚀 Cara Menggunakan

### 1. Personalisasi Konten

Buka file `index.html` dan ganti placeholder berikut dengan data pribadi Anda:

#### Data Pribadi:
- `[Nama Lengkap]` - Nama lengkap Anda
- `[Tempat, Tanggal Lahir]` - Tempat dan tanggal lahir
- `[Alamat Lengkap Siswa]` - Alamat domisili
- `[Nama SMK]` - Nama sekolah SMK
- `[Nama SD]` - Nama SD
- `[Nama SMP]` - Nama SMP

#### Kontak & Social Media:
- `[Email Saya]` - Alamat email
- `[NomorWhatsApp]` - Nomor WhatsApp (format: 628xxxxxxxxxx)
- `[Link LinkedIn]` - URL profil LinkedIn
- `[Link Instagram]` - URL profil Instagram

#### Project URLs:
- `[GITHUB_URL_BANK_MELASA]` - URL repository Bank Melasa Syariah
- `[GITHUB_URL_EVENTTY]` - URL repository EVENTTY
- `[GITHUB_URL_ECOMMERCE]` - URL repository E-Commerce Sepeda

### 2. Ganti Foto Profil (Opsional)

Foto profil saat ini menggunakan placeholder dari Google. Untuk menggunakan foto Anda sendiri:

1. Siapkan foto profil dengan ukuran persegi (misal: 800x800px)
2. Simpan foto di folder yang sama atau buat folder `assets/images/`
3. Ganti URL di bagian About Me section:

```html
<img src="assets/images/foto-profil.jpg" alt="Foto profil siswa RPL" />
```

### 3. Jalankan Website

#### Metode 1: Langsung di Browser
- Double-click file `index.html`
- Website akan terbuka di browser default Anda

#### Metode 2: Menggunakan Live Server (Recommended)
Jika menggunakan VS Code:
1. Install extension "Live Server"
2. Klik kanan pada `index.html`
3. Pilih "Open with Live Server"

#### Metode 3: Local Web Server
```bash
# Menggunakan Python
python -m http.server 8000

# Menggunakan PHP
php -S localhost:8000

# Buka browser: http://localhost:8000
```

## 📝 Customization Tips

### Mengubah Warna

File ini menggunakan custom color palette dari Material Design 3. Untuk mengubah tema warna, edit bagian `colors` di dalam `<script id="tailwind-config">`:

```javascript
"primary": "#adc6ff",        // Warna utama
"secondary": "#b7c4ff",      // Warna sekunder
"tertiary": "#4cd7f6",       // Warna aksen
```

### Menambah Project Baru

Copy struktur HTML dari salah satu card project dan sesuaikan:

```html
<div class="rounded-xl border border-outline-variant/30 bg-surface-container-low p-6 flex flex-col justify-between hover:border-primary/50 transition-colors">
  <!-- Project content here -->
</div>
```

### Menambah Skill Baru

Tambahkan item di bagian Skills & Technologies:

```html
<div class="flex items-center justify-between p-2 rounded bg-surface border border-outline-variant/20">
  <span class="font-label-sm text-label-sm text-on-surface">React JS</span>
  <span class="w-1.5 h-1.5 rounded-full bg-tertiary"></span>
</div>
```

## 📱 Browser Support

- Chrome (Latest)
- Firefox (Latest)
- Safari (Latest)
- Edge (Latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📦 File Structure

```
Portofolio/
├── index.html          # File utama website
├── README.md          # Dokumentasi (file ini)
└── baca.md            # Template original (dapat dihapus)
```

## 🎨 Design Credits

- Design System: Material Design 3 (Google)
- Color Scheme: Custom dark theme based on Material You
- Icons: Material Symbols Outlined
- Typography: Inter, JetBrains Mono, Plus Jakarta Sans

## 📄 License

Template ini bebas digunakan untuk keperluan portfolio pribadi dan pendidikan.

## 🤝 Contribution

Jika Anda menemukan bug atau ingin menambahkan fitur:
1. Fork repository
2. Buat branch feature baru
3. Commit changes
4. Push ke branch
5. Buat Pull Request

## 📞 Support

Jika ada pertanyaan atau memerlukan bantuan, silakan hubungi melalui:
- GitHub Issues
- Email yang tercantum di portfolio

---

**Dibuat dengan ❤️ untuk Siswa RPL Indonesia**

*Selamat berkarya dan semoga sukses!* 🚀
