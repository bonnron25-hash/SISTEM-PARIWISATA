# 📘 Panduan Deployment ke Streamlit Cloud

Aplikasi Anda sudah siap untuk di-hosting! Ikuti langkah-langkah di bawah ini.

## ✅ Langkah-Langkah Deployment

### Step 1: Create GitHub Repository
1. Buka [github.com](https://github.com) dan login/sign up
2. Klik tombol **"New"** (pojok kiri atas)
3. Beri nama repository: `sistem-analisis-pariwisata`
4. Pilih **Public** (agar Streamlit Cloud bisa mengakses)
5. Jangan inisialisasi README/gitignore (sudah ada)
6. Klik **Create repository**

### Step 2: Push Code ke GitHub
Jalankan perintah di terminal PowerShell dari folder project:

```powershell
# Ganti USERNAME dan REPO dengan milik Anda
git remote add origin https://github.com/USERNAME/REPO.git
git branch -M main
git push -u origin main
```

**Contoh:**
```powershell
git remote add origin https://github.com/johndoe/sistem-analisis-pariwisata.git
git branch -M main
git push -u origin main
```

### Step 3: Deploy ke Streamlit Cloud
1. Buka [share.streamlit.io](https://share.streamlit.io)
2. Klik **"New app"**
3. Pilih:
   - **Repository**: USERNAME/REPO (contoh: johndoe/sistem-analisis-pariwisata)
   - **Branch**: main
   - **Main file path**: app.py
4. Klik **Deploy**
5. Tunggu 2-5 menit hingga selesai ✨

### Step 4: Share Aplikasi
Setelah deployment selesai, Anda akan mendapatkan URL seperti:
```
https://username-sistem-analisis-pariwisata.streamlit.app
```

Bisa dibagikan ke siapa saja!

---

## 📋 Checklist
- ✅ Project sudah di Git
- ✅ Sudah ada .gitignore
- ✅ Sudah ada .streamlit/config.toml
- ✅ requirements.txt lengkap
- ⬜ GitHub repository dibuat
- ⬜ Code di-push ke GitHub
- ⬜ Deploy ke Streamlit Cloud

---

## 🆘 Troubleshooting

**Error: "Github Credentials"?**
- GitHub akan meminta login via browser saat `git push`
- Login dengan akun GitHub Anda

**Aplikasi error setelah deploy?**
- Buka **Manage App** > **Reboot App**
- Cek bagian **Logs** untuk melihat error message
- Update code dan push ulang ke GitHub (auto-update dalam 1 menit)

**Mau custom domain?**
- Upgrade ke plan berbayar di Streamlit Cloud

---

## 📞 File Persiapan Sudah Siap
✅ `.gitignore` - Exclude unneed files
✅ `.streamlit/config.toml` - Streamlit configuration
✅ `app.py` - Main application
✅ `requirements.txt` - Dependencies
✅ `scraper.py` - Web scraping module
✅ `README.md` - Project documentation
✅ Sample data included

Siap deploy! 🚀
