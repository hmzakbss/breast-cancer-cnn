Projenin Amacı

Bu projenin amacı, mikroskop altında çekilmiş meme kanseri hücre görsellerini derin öğrenme yöntemleri kullanarak normal (benign) ve tümörlü (malignant) hücreler olarak sınıflandırmaktır. Böylece bilgisayar destekli teşhis sistemlerine katkı sağlayarak erken tanıya yardımcı olunması hedeflenmektedir.
*Veri Seti :* [Breast Histopathology Images](https://www.kaggle.com/datasets/paultimothymooney/breast-histopathology-images)  
İçerik: Orijinal veri setinde 277.524 adet 50x50 piksel histopatoloji görüntüsü bulunmaktadır.

Bu Projede Kullanılan Alt Küme: Her sınıftan 5000 örnek seçilerek toplam 10.000 görüntü ile eğitim yapılmıştır.

Sınıflar:

0: Benign (normal) hücreler

1: Malignant (tümörlü) hücreler

⚙ Kullanılan Yöntemler

Ön İşleme:

Görseller 128x128 boyutuna ölçeklendi.

Piksel değerleri [0,1] aralığına normalize edildi.

Eğitim ve test verisi %80 / %20 oranında ayrıldı.

Veri Artırma (Data Augmentation):

Döndürme, kaydırma, yakınlaştırma, yatay/dikey çevirme.

Model Mimarisi (CNN):

3 adet Conv2D + MaxPooling katmanı

1 adet Tam Bağlantılı (Dense) katman

Dropout ile aşırı öğrenme (overfitting) azaltıldı.

Çıkış katmanında sigmoid aktivasyon fonksiyonu kullanıldı.

Hiperparametre Optimizasyonu:

keras-tuner ile filtre sayısı, dense katman nöron sayısı, dropout oranı ve optimizer seçenekleri test edilerek en iyi model seçildi.
