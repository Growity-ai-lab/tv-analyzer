# TV Analyzer PWA - Deployment Rehberi

## 📱 Proje Özellikleri

- **PWA (Progressive Web App)**: Çevrimdışı çalışma, app olarak yükleme
- **Service Worker**: Caching strategy ile hızlı yükleme
- **Responsive Design**: Desktop, tablet, mobile uyumlu
- **Standalone Mode**: Native app gibi kullanım

---

## 🚀 Vercel'e Deploy Etme (Önerilen)

### Adım 1: Git Repository'e Push Et

```bash
git add .
git commit -m "Add PWA deployment configuration for Vercel/Render"
git push origin main
```

### Adım 2: Vercel'de Deploy Et

1. [Vercel.com](https://vercel.com) adresine git
2. **"New Project"** butonuna tıkla
3. GitHub'dan **tv-analyzer** repo'nu seç
4. Aşağıdaki ayarları yap:
   - **Framework**: Other
   - **Root Directory**: `./`
   - **Build Command**: `npm install` (varsayılan)
   - **Start Command**: `npm start`

5. **Deploy** butonuna tıkla

✅ Vercel size otomatik bir URL verecek: `https://tv-analyzer-xxx.vercel.app`

---

## 🚀 Render'e Deploy Etme

### Adım 1: Git'e Push Et

```bash
git add .
git commit -m "Add PWA deployment configuration for Vercel/Render"
git push origin main
```

### Adım 2: Render'de Deploy Et

1. [Render.com](https://render.com) adresine git
2. **"New +"** butonuna tıkla ve **"Web Service"** seç
3. GitHub repo'nu bağla
4. **tv-analyzer** repo'nu seç
5. Aşağıdaki ayarları yap:
   - **Name**: `tv-analyzer-pwa`
   - **Runtime**: Node
   - **Build Command**: `npm install`
   - **Start Command**: `node server.js`

6. **Create Web Service** butonuna tıkla

✅ Render size otomatik bir URL verecek: `https://tv-analyzer-pwa-xxx.onrender.com`

---

## 📘 Lokal Test Etme

Deployment öncesi lokal olarak test et:

```bash
npm install
npm start
```

Tarayıcını aç: `http://localhost:3000`

---

## ✨ PWA Özelliklerini Kontrol Et

1. **Chrome DevTools → Application → Manifest**
   - Manifest dosyası yüklü mü?

2. **Chrome DevTools → Application → Service Workers**
   - Service worker aktif mi?

3. **PWA Install Banner**
   - "Install app" mesajı görünüyor mu?

4. **Offline Mode**
   - DevTools → Network → Offline işaretle
   - Sayfayı refresh et
   - Uygulama çalışmaya devam mi ediyor?

---

## 🔧 Özelleştirme

Manifest.json dosyasında aşağıdaki ayarları yapabilirsin:

- **Tema Rengi**: `"theme_color": "#E91E8C"`
- **App Adı**: `"name": "TV Analyzer"`
- **Arka Plan**: `"background_color": "#0a0a0f"`

---

## 📊 Kontrol Listesi

- [x] PWA Meta Tags (index.html)
- [x] Service Worker
- [x] package.json
- [x] server.js
- [x] vercel.json
- [x] render.yaml
- [x] .gitignore

---

## 🎯 Deployment Sonrası

1. **HTTPS Kontrolü**
   - ✅ Otomatik olarak yapılıyor (Vercel/Render)

2. **Performance Check**
   - [PageSpeed Insights](https://pagespeed.web.dev) kullan

3. **PWA Audit**
   - Chrome DevTools → Lighthouse → PWA

---

## 🚨 Sorun Giderme

### "Service Worker Register Failed"
→ Console'da (F12) hatayı kontrol et

### "Cache Issues"
→ Browser cache'i temizle (Ctrl+Shift+Delete)

### "App Yüklenmiyor"
→ Browser console'da (F12) hatayı kontrol et

---

## 📞 Destek

Sorularınız varsa:
- [Vercel Docs](https://vercel.com/docs)
- [Render Docs](https://render.com/docs)
- [PWA Best Practices](https://web.dev/progressive-web-apps/)
