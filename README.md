Müşteri Terk Davranışlarının Veri Madenciliği Yöntemleri ile Analizi
Bu proje, telekomünikasyon sektöründeki müşteri kaybını (churn) tahmin etmek amacıyla makine öğrenmesi algoritmalarını kullanır. Proje, veri ön işlemeden model değerlendirmeye kadar uçtan uca bir veri bilimi sürecini kapsar.
Veri Seti
Projede kullanılan veri seti Kaggle üzerinden temin edilmiştir: Customer Churn Records Dataset

Veri seti, müşteri demografisi, hizmet kullanım bilgileri ve müşteri sadakatine dair çeşitli öznitelikler içermektedir.

Kullanılan Teknolojiler ve Yöntemler
Diller: Python

Kütüphaneler: Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn, Imbalanced-learn (SMOTE)

Yöntemler: * Veri Ön İşleme & Eksik Veri Analizi

Özellik Ölçeklendirme (StandardScaler)

Dengesiz Veri Yönetimi (SMOTE - Synthetic Minority Over-sampling Technique)

Hiperparametre Optimizasyonu (GridSearchCV)

Kullanılan Modeller ve Performans
Proje kapsamında üç farklı sınıflandırma algoritması eğitilmiş ve performansları karşılaştırılmıştır:

Model,Accuracy    (Doğruluk)   Recall (Duyarlılık)
XGBoost              %50.34      %50.31
Random Forest        %50.07      %50.04
Lojistik Regresyon   %49.52      %51.86

Not: Müşteri kaybını önceden yakalamanın kritik olduğu bu problemde, terk edenleri (1 sınıfı) en iyi yakalayan Lojistik Regresyon modeli, yüksek Recall değeri ile öne çıkmaktadır.

Öne Çıkan Bulgular
Veri setindeki gürültü (noise) seviyesinin yüksekliği, modellerin genel doğruluğunu baseline seviyesine yakın tutmuştur.

SMOTE kullanımı, modelin azınlık sınıfı (terk eden müşteriler) tanıma kapasitesini artırmıştır.

GridSearchCV ile yapılan optimizasyonlar, modellerin aşırı öğrenmesini (overfitting) engellemek için kritik rol oynamıştır.
