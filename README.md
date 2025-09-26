Meme Kanseri Hücre Görselleri Sınıflandırması

Projenin Amacı

Bu projenin amacı, mikroskop altında çekilmiş meme kanseri hücre görsellerini derin öğrenme yöntemleri kullanarak normal (benign) ve tümörlü (malignant) hücreler olarak sınıflandırmaktır. Böylece bilgisayar destekli teşhis sistemlerine katkı sağlayarak erken tanıya yardımcı olunması hedeflenmektedir.

Veri Seti Adı:** [Breast Histopathology Images](https://www.kaggle.com/datasets/paultimothymooney/breast-histopathology-images)  

İçerik: Orijinal veri setinde 277.524 adet 50x50 piksel histopatoloji görüntüsü bulunmaktadır.
Bu Projede Kullanılan Alt Küme: Her sınıftan 5000 örnek seçilerek toplam 10.000 görüntü ile eğitim yapılmıştır.

Sınıflar:

0: Benign (normal) hücreler

1: Malignant (tümörlü) hücreler

Kullanılan Yöntemler

Veri Hazırlığı ve Ön İşleme: Görüntüler, os ve pandas kütüphaneleri kullanılarak işlenmiş ve etiketlenmiştir. Dengeli bir veri seti oluşturulmuş ve veriler eğitim ile test kümelerine ayrılmıştır.

Veri Çoğaltma (Data Augmentation): Modelin genelleme yeteneğini artırmak ve aşırı uydurmayı (overfitting) önlemek için döndürme, yatay/dikey çevirme ve yakınlaştırma gibi veri çoğaltma teknikleri uygulanmıştır.

Model Mimarisi: Proje için üç evrişim katmanı ve iki tam bağlantılı katman içeren temel bir CNN mimarisi oluşturulmuştur.

Hiperparametre Optimizasyonu: Keras Tuner kullanılarak en uygun model mimarisi otomatik olarak bulunmuştur. Filtre sayısı, yoğun katman nöron sayısı ve Dropout oranı gibi hiperparametreler optimize edilmiştir. Bu sayede modelin performansı artırılmıştır.

Model Değerlendirmesi: Eğitilen model, doğruluk (accuracy) ve kayıp (loss) grafikleriyle, ayrıca ayrıntılı bir sınıflandırma raporu (precision, recall, f1-score) ve karışıklık matrisi (confusion matrix) ile değerlendirilmiştir

Test Setindeki Sınıf Dağılımları:
<br>
<img width="1014" height="451" alt="image" src="https://github.com/user-attachments/assets/50ef5035-f1be-437b-8bb3-0d620d5e49b3" />


<br>
Sınıflandırma Raporu:
<br>
<img width="423" height="167" alt="Ekran görüntüsü 2025-09-25 233941" src="https://github.com/user-attachments/assets/05498078-1277-41cf-be27-f3913a670615" />


Karışıklık Matrisi Analizi: 
<br>
<img width="448" height="470" alt="image" src="https://github.com/user-attachments/assets/086c49a5-2c16-4a71-b15d-878f78f9671c" />



Kaggle Notebook Linki
<br>
https://www.kaggle.com/code/hamzaakbas/breast-cancer-cnn
<br>
ROC Eğrisi
<img width="702" height="549" alt="image" src="https://github.com/user-attachments/assets/d4883521-3f91-4e52-8c3f-aad4018ebb0b" />
<br>
Precision-Recall Eğrisi
<br>
<img width="691" height="547" alt="image" src="https://github.com/user-attachments/assets/e321c40f-a88e-473b-9177-4364436b88d9" />



