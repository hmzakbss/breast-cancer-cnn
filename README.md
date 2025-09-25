🧬 Breast Cancer Classification with CNN

Bu proje, mikroskop altında çekilmiş meme kanseri hücre görsellerini derin öğrenme yöntemleriyle sınıflandırmayı amaçlamaktadır.
Amaç, bilgisayar destekli teşhis sistemlerine katkı sağlayarak erken tanıya yardımcı olmak 🚑.

📊 Veri Seti

Veri Seti Adı: Breast Histopathology Images

Toplam Görsel (Orijinal): 277.524 adet (50x50 piksel histopatoloji görüntüsü)

Bu Projede Kullanılan Alt Küme:

Her sınıftan 5000 örnek → Toplam 10.000 görüntü

🔹 Sınıflar
Etiket	Açıklama
0	Benign (Normal hücreler)
1	Malignant (Tümörlü hücreler)
⚙️ Kullanılan Yöntemler

Veri Hazırlığı ve Ön İşleme

os ve pandas kütüphaneleri ile görseller işlendi ve etiketlendi

Dengeli veri seti oluşturuldu

Eğitim/Test kümelerine ayrıldı

Veri Çoğaltma (Data Augmentation)

Döndürme

Yatay/Dikey çevirme

Yakınlaştırma

→ Amaç: Overfitting’i önlemek ve genelleme yeteneğini artırmak

CNN Model Mimarisi

3 Evrişim Katmanı (Conv2D)

2 Tam Bağlantılı Katman (Dense)

Aktivasyon: ReLU + Softmax

Dropout ile düzenlileştirme

Hiperparametre Optimizasyonu (Bonus 🚀)

Keras Tuner ile filtre sayısı, nöron sayısı, dropout oranı optimize edildi

En iyi model seçildi

Model Değerlendirmesi

Accuracy & Loss grafikleri

Sınıflandırma raporu (Precision, Recall, F1-score)
              precision    recall  f1-score   support

    Benign       0.80      0.86      0.83      1000
 Malignant       0.85      0.79      0.82      1000

    accuracy                           0.83      2000
   macro avg       0.83      0.83      0.83      2000
weighted avg       0.83      0.83      0.83      2000

Karışıklık matrisi (Confusion Matrix)

📈 Elde Edilen Sonuçlar
✅ Test Verisi Doğruluk Oranı

%83

🔹 Sınıf Dağılımları
<img width="448" height="470" alt="data-distribution" src="https://github.com/user-attachments/assets/39fc6b9d-4475-41e2-ac26-e9aab04b0d27" />

🔹 Karışıklık Matrisi
<img width="448" height="470" alt="confusion-matrix" src="https://github.com/user-attachments/assets/2ed5c3fc-baf9-4113-8bf4-e150abaf7e46" />

                CNN MODEL MİMARİSİ
-------------------------------------------------
 Girdi (50x50x3)  →  Renkli hücre görüntüsü
-------------------------------------------------
 Conv2D (32 filtre, 3x3, ReLU) 
 MaxPooling2D (2x2)
-------------------------------------------------
 Conv2D (64 filtre, 3x3, ReLU)
 MaxPooling2D (2x2)
-------------------------------------------------
 Conv2D (128 filtre, 3x3, ReLU)
 MaxPooling2D (2x2)
-------------------------------------------------
 Flatten
 Dense (128 nöron, ReLU)
 Dropout (0.5)
 Dense (64 nöron, ReLU)
 Dropout (0.5)
-------------------------------------------------
 Çıkış Katmanı → Dense (2 sınıf, Softmax)
-------------------------------------------------
