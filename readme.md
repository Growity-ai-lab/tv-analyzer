# TV Analyzer by Time & Growity

TV reklamlarının etkinliğini ölçmek ve planlamak için geliştirilmiş interaktif analiz aracı.

![TV Analyzer Screenshot](screenshot.png)

## 🎯 Özellikler

### Modelleme Kapasiteleri
- **Adstock (Carry-over):** Reklamın zamanla taşan etkisini hesaplar
- **Saturation (Diminishing Returns):** Harcama arttıkça azalan verimliliği modeller
- **Response Model:** TV'nin satışlara etkisini tahmin eder

### Giriş Modları
- **💰 Harcama Bazlı:** Post-campaign analiz için TL cinsinden harcama girişi
- **📺 GRP Bazlı:** Planlama için hedef GRP girişi, otomatik bütçe hesaplama

### Analiz Çıktıları
- Haftalık Adstock değerleri
- Saturation eğrisi ve optimal bütçe noktası
- TV kaynaklı satış artışı
- TV Efficiency Index
- ROI analizi
- CSV export

### Senaryo Karşılaştırma
Hazır parametre setleri ile hızlı karşılaştırma:
- 🐢 **Muhafazakar:** Düşük carry-over, yüksek doygunluk eşiği
- ⚖️ **Dengeli:** Tipik TV kampanyası parametreleri
- 🚀 **Agresif:** Yüksek carry-over, hızlı doygunluk

## 🚀 Kurulum

### GitHub Pages ile (Önerilen)

1. Bu repo'yu fork edin veya clone edin
2. Repository Settings → Pages → Source: `main` branch
3. Birkaç dakika içinde `https://kullaniciadin.github.io/tv-analyzer/` adresinde yayında

### Lokal Kullanım

Herhangi bir web tarayıcısında `index.html` dosyasını açın. Sunucu gerektirmez.

## 📊 Kullanım

### 1. Veri Girişi
Harcama veya GRP bazlı mod seçin ve haftalık değerleri virgülle ayırarak girin.

```
Örnek (Harcama): 500000, 750000, 1000000, 800000, 600000
Örnek (GRP): 200, 300, 400, 320, 240
```

### 2. Parametre Ayarları

| Parametre | Açıklama | Tipik Değer |
|-----------|----------|-------------|
| Decay Rate (λ) | Reklamın hafızada kalma süresi | 0.5 - 0.8 |
| Alpha (α) | Doygunluk noktası | 1.0 - 3.0 |
| Gamma (γ) | Eğri şekli | 0.6 - 1.2 |
| Baseline | TV olmadan haftalık satış | Sektöre göre |
| Max Lift | TV'nin max katkı potansiyeli (%) | 15 - 40 |

### 3. Analizi Çalıştır
"Analizi Çalıştır" butonuna tıklayın ve sonuçları inceleyin.

## 📈 Metrikler

### TV Efficiency Index
```
TV Efficiency = (TV Kaynaklı Satış / Harcama) × 100
```
Her 1 TL harcama için ne kadar incremental satış yaratıldığını gösterir.

### Optimal Bütçe
Saturation eğrisinde diminishing returns başlamadan önceki en verimli harcama noktası.

## 🛠️ Teknolojiler

- Vanilla JavaScript (framework yok)
- Chart.js (grafikler)
- Chart.js Annotation Plugin (optimal nokta işaretleme)
- CSS3 (modern UI)

## 📁 Dosya Yapısı

```
tv-analyzer/
├── index.html      # Ana uygulama
├── README.md       # Bu dosya
├── LICENSE         # MIT lisansı
└── screenshot.png  # Ekran görüntüsü (opsiyonel)
```

## 🤝 Katkıda Bulunma

1. Fork edin
2. Feature branch oluşturun (`git checkout -b feature/yeni-ozellik`)
3. Commit edin (`git commit -m 'Yeni özellik eklendi'`)
4. Push edin (`git push origin feature/yeni-ozellik`)
5. Pull Request açın

## 📄 Lisans

MIT License - Detaylar için [LICENSE](LICENSE) dosyasına bakın.

## 👥 Geliştiriciler

**Time & Growity** - Digital Marketing & Media Strategy Consulting

---

⭐ Bu projeyi faydalı bulduysanız yıldız vermeyi unutmayın!
