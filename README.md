# breast-cancer-cnn
PROJENİN AMACI

Bu projenin amacı, mikroskop altında çekilmiş meme kanseri hücre görsellerini derin öğrenme yöntemleri kullanarak normal (benign) ve tümörlü (malignant) hücreler olarak sınıflandırmaktır. Böylece bilgisayar destekli teşhis sistemlerine katkı sağlayarak erken tanıya yardımcı olunması hedeflenmektedir.

VERİ SETİ HAKKINDA BİLGİ

Veri Seti Adı: [Breast Histopathology Images](https://www.kaggle.com/datasets/paultimothymooney/breast-histopathology-images)

içerik: Orijinal veri setinde 277.524 adet 50x50 piksel histopatoloji görüntüsü bulunmaktadır.
Bu Projede Kullanılan Alt Küme: Her sınıftan 5000 örnek seçilerek toplam 10.000 görüntü ile eğitim yapılmıştır.

Sınıflar:
0: Benign (normal) hücreler
1: Malignant (tümörlü) hücreler

KULLANILAN YÖNTEMLER

Veri Hazırlığı ve Ön İşleme: Görüntüler, os ve pandas kütüphaneleri kullanılarak işlenmiş ve etiketlenmiştir. Dengeli bir veri seti oluşturulmuş ve veriler eğitim ile test kümelerine ayrılmıştır.

Veri çoğaltma (Data Augmentation): Modelin genelleme yeteneğini artırmak ve aşırı uydurmayı (overfitting) önlemek için döndürme, yatay/dikey çevirme ve yakınlaştırma gibi veri çoğaltma teknikleri uygulanmıştır.

Model mimarisi: Proje için üç evrişim katmanı ve iki tam bağlantılı katman içeren temel bir CNN mimarisi oluşturulmuştur.

Hiperparametre Optimizasyonu (Bonus Adım): Keras Tuner kullanılarak en uygun model mimarisi otomatik olarak bulunmuştur. Filtre sayısı, yoğun katman nöron sayısı ve Dropout oranı gibi hiperparametreler optimize edilmiştir. Bu sayede modelin performansı artırılmıştır.
Model Değerlendirmesi: Eğitilen model, doğruluk (accuracy) ve kayıp (loss) grafikleriyle, ayrıca ayrıntılı bir sınıflandırma raporu (precision, recall, f1-score) ve karışıklık matrisi (confusion matrix) ile değerlendirilmiştir.


ELDE EDİLEN SONUÇLAR


En İyi Modelin Doğruluk Oranı (Test Verisi):

Eğitim Sonrası Grafiklerin Analizi: 

Sınıflandırma Raporu ve Karışıklık Matrisi Analizi:

Karışıklık Matrisi (Confusion Matrix):



KAGGLE NOTEBOOK LİNKİ 



