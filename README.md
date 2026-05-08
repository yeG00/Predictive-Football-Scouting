# ⚽ Futbolcu Piyasa Değeri Tahminleme (Football Player Market Value Prediction)

> 🚧 **Durum: Geliştirme Aşamasında (Work in Progress)** > Bu proje şu anda aktif olarak geliştirilmektedir. Hedef, farklı makine öğrenmesi algoritmalarını test ederek en düşük hata payına (RMSE) ulaşmaktır.

## 📌 Projenin Amacı
Bu projenin temel amacı, futbolcuların yaş, yetenek puanı (overall), potansiyel ve fiziksel özellikleri gibi metriklerini kullanarak piyasa değerlerini (`value_eur`) makine öğrenmesi algoritmaları ile tahmin etmektir. 

## 🛠️ Kullanılan Teknolojiler
* **Dil:** Python
* **Veri Manipülasyonu & Analizi:** Pandas, NumPy
* **Veri Görselleştirme:** Matplotlib, Seaborn
* **Makine Öğrenmesi:** Scikit-Learn (Linear Regression, StandardScaler)
* **Geliştirme Ortamı:** Jupyter Notebook

## ✅ Tamamlanan Aşamalar
- [x] **Veri Temizleme (Data Cleaning):** Eksik veriler (NaN) temizlendi, veri seti güncel tutulmak adına sadece FC 24 versiyonundaki oyuncularla sınırlandırıldı.
- [x] **Özellik Mühendisliği (Feature Engineering):** - Oyuncuların boy ve kilo verilerinden Vücut Kitle İndeksi (`BMI`) hesaplanarak yeni bir özellik olarak modele eklendi.
  - Karmaşık mevki verileri hücum, orta saha, defans ve kaleci olarak 4 ana gruba indirgendi.
- [x] **Keşifsel Veri Analizi (EDA):** Top 5 Lig'in maaş dağılımları Kutu Grafiği (Boxplot) ile incelendi ve hedef değişkeni en çok etkileyen özellikleri bulmak için Korelasyon Haritası (Heatmap) çıkarıldı.
- [x] **Taban Modelin (Baseline) Kurulması:** İlk model olarak Çoklu Doğrusal Regresyon (Multiple Linear Regression) kullanıldı. Model sonuçları:
  - **R2 Skoru:** 0.36
  - **RMSE:** ~6.9 Milyon Euro (Bu sapma, fiyatlardaki üstel artışın doğrusal bir modelle yakalanamamasından kaynaklanmaktadır, sonraki adımlarda optimize edilecektir).

## 🚀 Gelecek Adımlar (To-Do)
- [ ] **Polinom Regresyon (Polynomial Regression):** Doğrusal olmayan fiyat artışlarını yakalamak için modele uygulanacak ve RMSE değeri düşürülecek.
- [ ] **Hiperparametre Optimizasyonu:** Model parametreleri ince ayardan geçirilecek.
- [ ] **Farklı Algoritmaların Test Edilmesi:** Karar Ağaçları (Decision Trees) veya Random Forest gibi non-lineer algoritmaların denenmesi.
