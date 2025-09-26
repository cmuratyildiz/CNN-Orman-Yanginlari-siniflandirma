Forest Fire - CNN

Bu repo, Akbank Derin Öğrenme Bootcamp kapsamında hazırladığım orman yangını tespit projesini içermektedir.
Amaç: Görsellerden yangın (Fire) / yangın olmayan (Non-Fire) sınıflarını ayırabilen bir derin öğrenme modeli (CNN) geliştirmektir.

---

Giriş

Veri seti: Kaggle - Forest Fire Images

Sınıflar: Fire ve Non-Fire

Algoritma: Convolutional Neural Networks (CNN)

Eklenen yöntemler:

Data Augmentation

EarlyStopping

ModelCheckpoint

Grad-CAM görselleştirme

Projenin teknik detayları, notebook dosyası içerisinde Markdown hücreleri ile anlatılmıştır.

---

Metrikler

Modelin eğitimi sonucunda elde edilen metrikler:

Eğitim Doğruluğu (Train Accuracy): ~%96

Doğrulama Doğruluğu (Validation Accuracy): ~%94

Confusion Matrix ve Classification Report ile sınıf bazında değerlendirme yapıldı.

Loss değerleri eğitim boyunca azaldı → model başarılı şekilde öğrenmiş.

Yorum: Eğitim ve doğrulama eğrilerinin birbirine yakın olması, overfitting olmadığını göstermektedir.

---

Accuracy Grafiği

Eğitim doğruluğu %87’den başlayarak %96’ya kadar yükselmiştir.

Doğrulama doğruluğu da %90 → %94 bandında ilerlemiştir.

Eğrilerin yakın gitmesi, modelin genelleme kabiliyetinin yüksek olduğunu göstermektedir.

---

Loss Grafiği

Eğitim kaybı 0.32 → 0.11 seviyelerine kadar düzenli düşmüştür.

Validation kaybı dalgalanmalı olsa da genel trend aşağı yönlüdür.

Bu durum modelin başarılı bir şekilde öğrenme sağladığını gösterir.

---

Confusion Matrix

Fire sınıfı: 22 doğru, 3 yanlış → %88 başarı

Non-Fire sınıfı: 24 doğru, 1 yanlış → %96 başarı

Model, hem yangın hem de yangın olmayan görselleri yüksek doğrulukla ayırt edebilmektedir.

---

Ekler

Proje kapsamında:

Grad-CAM ile modelin görselde hangi bölgelerden karar verdiği görselleştirildi.

Hiperparametre denemeleri (dropout oranı, batch size, learning rate) yapıldı.

Eğitim, Kaggle GPU ortamında alınmıştır.

---

Gelecekte

Streamlit UI eklenerek modelin web arayüzü üzerinden test edilmesi,

Gerçek zamanlı kamera verisi ile dinamik yangın tespiti yapılması planlanmaktadır.

---

Sonuç ve Gelecek Çalışmalar

Model %94 doğruluk ile yangın tespitinde başarılı olmuştur.

Daha büyük ve çeşitli veri setleri ile performans artırılabilir.

Transfer learning (VGG16, ResNet vb.) ile daha güçlü sonuçlar elde edilebilir.

Gelecekte bu proje IoT + kamera sistemleri ile birleştirilerek, gerçek zamanlı yangın tespiti yapılabilir.

---

Linkler

Kaggle Notebook: https://www.kaggle.com/code/aataymuratyildiz/forest-fire-images

Dataset: Forest Fire Images