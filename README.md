Forest Fire Detection CNN

Bu repo, Akbank Derin Öğrenme Bootcamp kapsamında hazırladığım orman yangını tespit projesini içermektedir.
Amaç: Görsellerden yangın (Fire) / yangın olmayan (Non-Fire) sınıflarını ayırabilen bir derin öğrenme modeli (CNN) geliştirmek.

Giriş

Veri seti: Kaggle - Forest Fire Images

Sınıflar: Fire ve Non-Fire

Kullanılan algoritma: Convolutional Neural Networks (CNN)

Ek olarak: Data Augmentation, EarlyStopping, ModelCheckpoint, Grad-CAM görselleştirme eklendi.

Projenin teknik detayları, notebook dosyası içerisinde Markdown hücreleri ile anlatılmıştır.

---

Metrikler

Modelin eğitimi sonucunda elde edilen metrikler:

Eğitim Doğruluğu (Train Accuracy): ~%96

Doğrulama Doğruluğu (Validation Accuracy): ~%94

Confusion Matrix ve Classification Report ile sınıf bazında değerlendirme yapıldı.

Loss değerleri eğitim boyunca azaldı → model başarılı şekilde öğrenmiş.

📌 Yorum: Eğitim ve doğrulama eğrilerinin yakın olması, overfitting olmadığını gösteriyor.

---

Ekler

Proje kapsamında:

Grad-CAM ile modelin görselde hangi bölgelerden karar verdiği görselleştirildi.

Hiperparametre denemeleri (dropout oranı, batch size, learning rate) yapıldı.

Kaggle GPU ortamında eğitim alındı.

---

Gelecekte:

Streamlit UI eklenerek modelin web arayüzü üzerinden test edilmesi,

Gerçek zamanlı kamera verisi ile dinamik yangın tespiti yapılması planlanıyor.

---

Sonuç ve Gelecek Çalışmalar

Model %94 doğruluk ile yangın tespitinde başarılı oldu.

Daha büyük ve çeşitli veri setleri ile performans artırılabilir.

Transfer learning (VGG16, ResNet gibi hazır modeller) eklenerek daha güçlü sonuçlar elde edilebilir.

Gelecekte bu proje IoT + kamera sistemleri ile birleştirilip, gerçek zamanlı yangın tespiti yapılabilir.

---

Linkler

Kaggle Notebook: Forest Fire Detection CNN
 (kendi linkini buraya koymalısın)

Dataset: Forest Fire Images