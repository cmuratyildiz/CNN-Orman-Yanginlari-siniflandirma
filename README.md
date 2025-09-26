Orman Yangını Tespiti - Derin Öğrenme Projesi

Bu proje, Akbank Derin Öğrenme Bootcamp kapsamında gerçekleştirilmiştir.  
Amaç: Görüntülerden orman yangını (Fire / Non-Fire) sınıflandırması yapmak için CNN tabanlı derin öğrenme modeli geliştirmek.

---

Veri Seti
- Kullanılan veri seti:Kaggle - Forest Fire Images -- https://www.kaggle.com/datasets/mohnishsaiprasad/forest-fire-images  
- Sınıflar:  
  - 🔥 Fire 
  - 🌲 Non-Fire
- Eğitim ve test klasörleri:  
	/Data/Train_Data/Fire
        /Data/Train_Data/Non_Fire
        /Data/Test_Data/Fire
        /Data/Test_Data/Non_Fire

Veri Önişleme
- Görseller 150x150 boyutuna getirildi.  
- Normalization: `rescale=1./255`  
- Data Augmentation:  
- Rotation (15°)  
- Width/Height shift (0.1)  
- Zoom (0.1)  
- Horizontal flip  

Model Mimarisi- CNN

Conv2D (32 filtre) + MaxPooling  
Conv2D (64 filtre) + MaxPooling
Conv2D (128 filtre)+ MaxPooling
Flatten  
Dense (128 nöron, ReLU)
Dropout (0.5)
Dense (1 nöron, Sigmoid)  

Optimizer: Adam 
Loss:      Binary Crossentropy
Metrics:   Accuracy

Overfitting Önleme
- **EarlyStopping** → validation loss iyileşmediğinde eğitim durur  
- **ModelCheckpoint** → en iyi model `.h5` olarak kaydedilir  

---

##Sonuçlar
Accuracy / Loss Grafikleri
Eğitim sürecinde modelin performansı görselleştirilmiştir:

- Eğitim doğruluğu: ~%93  
- Validation doğruluğu: ~%90  

Confusion Matrix
Modelin test setindeki sınıflandırma başarımı:

![confusion-matrix](confusion_matrix.png)

Classification Report
Precision, Recall ve F1-Score değerleri raporlanmıştır.

---

Grad-CAM Görselleştirme
Modelin karar verirken odaklandığı bölgeler Grad-CAM ile gösterilmiştir:

![grad-cam](grad_cam.png)

---

Hiperparametre Denemeleri
- Dropout oranı değiştirildi (0.5 → 0.3)  
- Learning rate düşürüldü (`0.001 → 0.0005`)  
- Adam optimizer kullanıldı  

Bu denemeler sonucunda validation accuracy iyileşmiştir.


Çağatay Murat YILDIZ