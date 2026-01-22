# İstanbul Trafik Yoğunluğu – Zaman Serisi Analizi

Bu proje, İstanbul genelindeki **trafik sensörlerinden elde edilen zaman serisi verilerini** kullanarak trafik yoğunluğunu analiz etmek ve **gelecekteki trafik durumunu tahmin etmek** amacıyla geliştirilmiştir.  
Çalışma; **veri ön işleme**, **istatistiksel analiz**, **modelleme** ve **görselleştirme** aşamalarını kapsayan **uçtan uca bir veri bilimi iş akışı** sunmaktadır.

---

## 📋 Proje Özeti

Projenin temel amacı:

- Trafik yoğunluk verilerindeki **günlük ve haftalık periyodik desenleri** belirlemek
- **Trend**, **mevsimsellik** ve **durağanlık (stationarity)** bileşenlerini analiz etmek
- Bu bileşenleri kullanarak **isabetli trafik tahminleri** üretmektir

Analiz sürecinde zaman serilerinin istatistiksel özellikleri detaylı biçimde incelenmiştir.

---

## 🛠 Kullanılan Teknolojiler

- **Python**  
  Veri analizi ve modelleme için temel programlama dili

- **Pandas & NumPy**  
  Veri temizleme, dönüştürme ve sayısal işlemler

- **Matplotlib & Seaborn**  
  Zaman serisi grafikleri ve yoğunluk görselleştirmeleri

- **Statsmodels**  
  ARIMA ve SARIMA modellerinin istatistiksel analizi

- **Scikit-learn**  
  Model değerlendirme metrikleri (MSE, RMSE, MAE)

---

## 📊 Veri Seti

**Dosya:** `traffic.csv`

Veri seti, İstanbul’un farklı bölgelerindeki trafik sensörlerinden toplanan aşağıdaki sütunları içermektedir:

| Sütun | Açıklama |
|-----|---------|
| `DateTime` | Ölçümün yapıldığı zaman damgası |
| `Junction` | Trafik yoğunluğunun ölçüldüğü kavşak |
| `Vehicles` | İlgili zaman dilimindeki araç sayısı (**hedef değişken**) |

---

## 🔄 Analiz ve Modelleme Süreci

### 1. Veri Ön İşleme
- Eksik veri kontrolü
- Tarih/zaman formatlarının düzenlenmesi
- Verilerin kavşak bazlı ayrıştırılması

---

### 2. Durağanlık Analizi
- **ADF (Augmented Dickey-Fuller) Testi** ile durağanlık kontrolü
- Gerekli durumlarda **fark alma (differencing)** işlemleri

---

### 3. ACF ve PACF Analizi
- Otokorelasyon (ACF) ve kısmi otokorelasyon (PACF) grafiklerinin incelenmesi
- ARIMA/SARIMA parametrelerinin belirlenmesi:
  \[
  (p, d, q)
  \]

---

### 4. Tahmin Modelleri

- **SARIMA (Seasonal ARIMA)**  
  Günlük ve haftalık mevsimsel etkileri dikkate alan zaman serisi modeli

- **Prophet**  
  - Trend ve mevsimselliği otomatik modelleyen yaklaşım  
  - Tatil ve özel gün etkilerini dahil edebilme avantajı

---

## 📈 Model Değerlendirme

Modeller aşağıdaki metrikler kullanılarak değerlendirilmiştir:

- **MSE** – Mean Squared Error  
- **RMSE** – Root Mean Squared Error  
- **MAE** – Mean Absolute Error  

Gerçek değerler ile tahminler karşılaştırılarak performans analizleri yapılmıştır.

---

## 🎯 Projenin Amacı

- Büyük şehirlerde trafik problemlerini **veri odaklı** analiz etmek
- Zaman serisi modelleme tekniklerini **gerçek dünya verisi** üzerinde uygulamak
- Akıllı şehir (Smart City) uygulamalarına yönelik **öngörüsel analiz** altyapısı oluşturmak

