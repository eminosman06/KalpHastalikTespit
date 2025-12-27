## 🫀 Kalp Hastalığı Tespit Projesi 
Bu proje, UCI Cleveland kalp hastalığı veri setini kullanarak, bir hastanın klinik özelliklerine göre kalp hastalığı riskini tahmin eden uçtan uca bir makine öğrenmesi boru hattıdır (pipeline).

Projenin en belirgin özelliği, sınıflandırma işlemi için hazır kütüphane kullanmak yerine Lojistik Regresyon algoritmasının sıfırdan (from scratch) Python ile kodlanmış olmasıdır.

## 🚀 Öne Çıkan Özellikler
OOP Mimari: Tüm süreç VeriMadenciligiProjesi sınıfı altında modüler bir yapıda kurgulanmıştır.

Özel Lojistik Regresyon: LojistikRegresyon sınıfı; sigmoid fonksiyonu, ağırlık/sapma (weight/bias) güncellemeleri ve L2 regülarizasyonu içerecek şekilde manuel olarak implement edilmiştir.

Kapsamlı Veri Ön İşleme: * Eksik değerlerin medyan ile doldurulması.

IQR (Interquartile Range) yöntemi ile aykırı değer tespiti ve temizlenmesi.

Manuel Min-Max normalizasyonu.

Görsel Analiz: Matplotlib ve Seaborn ile Boxplot, Histogram ve Confusion Matrix görselleştirmeleri.

## 🛠️ Kullanılan Teknolojiler
Dil: Python

Kütüphaneler: * Pandas & NumPy (Veri manipülasyonu ve matris işlemleri)

Matplotlib & Seaborn (Veri görselleştirme)

Scikit-learn (Sadece veri bölme ve performans metrikleri için)

## 📊 Veri Seti: Cleveland Heart Disease
Veri seti, kalp hastalığı teşhisi için 14 temel klinik özellik içerir:

| age |, sex, cp (göğüs ağrısı), trestbps (kan basıncı), chol (kolesterol), fbs, restecg, thalach, exang, oldpeak, slope, ca, thal. |

Hedef (Target): 0 (Normal) ve 1 (Hastalık Var) olarak ikili sınıflandırmaya dönüştürülmüştür.

## 📂 Proje Yapısı ve Akışı
Proje dört ana aşamadan oluşmaktadır:

- Veri Yükleme (veri_yukle): processed.cleveland.data dosyası okunur, eksik veriler temizlenir ve hedef değişken binary formata getirilir.

- Veri Analizi (veri_analizi): Boxplot ile aykırı değerler, histogramlar ile veri dağılımı incelenir.

- Ön İşleme (veri_on_isleme): Aykırı değerler veri setinden atılır ve tüm özellikler 0-1 arasına normalize edilir.

- Model Eğitimi (model_egitimi): Özel yazılmış Lojistik Regresyon modeli 2000 iterasyon boyunca eğitilir.

## 📉 Model Performansı
Kodun çıktı olarak ürettiği analizler şunları içerir:

- Doğruluk (Accuracy)

- Hassasiyet (Precision) & Duyarlılık (Recall)

- F1 Skoru

Özellik Önemlilik Sıralaması: Modelin karar verirken hangi klinik bulguya (örn: thal, ca, cp) ne kadar ağırlık verdiği gösterilir.

## ⚙️ Kurulum

Depoyu klonlayın:
- git clone "https://github.com/eminosman06/KalpHastalikTespit.git"

 
Gerekli kütüphaneleri yükleyin:
- pip install numpy pandas matplotlib seaborn scikit-learn


processed.cleveland.data dosyasının ana dizinde olduğundan emin olun ve kodu çalıştırın:
- python main.py
