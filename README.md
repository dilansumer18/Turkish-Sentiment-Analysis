Türkçe Duygu Analizi Sınıflandırıcısı (Turkish Sentiment Analysis)
Bu proje, Türkçe metin verilerini (kullanıcı yorumları) kullanarak bir Makine Öğrenimi (ML) modeli eğitmeyi ve bir metnin içerdiği duyguyu üç ana sınıfa ayırmayı amaçlar: Olumsuz (0), Tarafsız (1) ve Olumlu (2).

Proje Hedefleri ve Özellikleri
NLP Temelleri: Türkçe karakter desteği, metin normalizasyonu ve NLTK Türkçe Stop Word çıkarma gibi Dil İşleme (NLP) adımlarını uygulamak.
Özellik Çıkarımı: Metin verilerini TF-IDF (Term Frequency-Inverse Document Frequency) yöntemiyle sayısal vektörlere dönüştürmek.
Model Eğitimi: Hızlı ve etkili bir sınıflandırıcı olan Lojistik Regresyon (Logistic Regression) ile uçtan uca bir model oluşturmak.
Hata Çözümü: Veri yükleme ve temizleme aşamasında karşılaşılan Türkçe kodlama ve eksik etiket (NaN) sorunlarını çözmek.

Kullanılan Teknolojiler
Kategori                  Kütüphane/Araç                            Amaç
Veri Manipülasyonu        pandas, numpy                             Veri temizleme, düzenleme ve sayısal işlemler.
NLP/ML                    scikit-learn, nltk                        Model eğitimi, vektörleştirme (TF-IDF), performans metrikleri
Görselleştirme            matplotlib, seaborn                       Karmaşıklık Matrisi ve sonuç görselleştirmeleri.
Çalışma Ortamı            Google Colab / Jupyter Notebook           Kod geliştirme ve çalıştırma.

precision    recall  f1-score   support
#
#          1.0       0.78      0.72      0.75       587
#          2.0       0.81      0.86      0.84       851
#
#     accuracy                           0.80      1438
#    macro avg       0.80      0.79      0.79      1438

Model, Olumlu (2.0) yorumları tespit etmede yüksek başarı (Recall: %86) göstermiştir. Geliştirme amaçlı yapılan N-Gram eklemesi, modelin Tarafsız (1.0) yorumları yakalama gücünü (Recall: %72) biraz artırmıştır.
Modelin birincil hata noktası, Tarafsız yorumları Olumlu olarak sınıflandırmaya eğilimli olmasıdır.
