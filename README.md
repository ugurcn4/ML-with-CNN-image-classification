**Veri Kümesi Hikayesi ve Bağlantıları

Bu çalışma, çocukluk çağı kanserlerinin en yaygın türü olan Akut Lenfoblastik Lösemi'yi (ALL) ele almaktadır.
ALL, çocukluk çağı kanserlerinin yaklaşık %25'ini oluşturur ve erken teşhisin çocuklar üzerindeki olumlu etkisi çok önemlidir. 
Bu veri seti, uzman onkologlar tarafından etiketlenmiş mikroskobik hücre görüntülerinden oluşmakta ve kanserli B-lenfoblast hücreleri ile normal B-lenfositleri ayırmayı hedeflemektedir. 
Veri seti, mikroskop altında çekilen görüntülerdeki boyama gürültüleri ve aydınlatma hataları düzeltilerek hazırlanmıştır.

Toplamda 118 hastaya ait 15.135 görüntü bulunmaktadır ve görüntüler iki sınıfa ayrılmıştır:

Normal Hücreler

Lösemi Blastları (Kanserli Hücreler)

Veri Seti Bağlantıları:

Veri seti: Kaggle – Leukemia Classification

Veri seti belgesi: CNMC ReadMe.pdf

Yayın referansı: Gupta, A., & Gupta, R. (2019). ISBI 2019 ALL Challenge veri seti. Kanser Görüntüleme Arşivi. https://doi.org/10.7937/tcia.2019.dc64i46r

Projenin Amacı
Bu çalışmanın temel amacı, lösemik B-lenfoblast hücrelerini normal B-lenfositlerden ayırabilen bir görüntü sınıflandırma modeli oluşturmaktır. 
Model, kanserli hücrelerin erken teşhisi ve tedavi planlamasında kullanılabilecek bir aracı desteklemek üzerine odaklanmıştır.

Yapılan Teknikler

Veri Setinin Yüklenmesi ve İşlenmesi:

Kaggle API kullanılarak veri seti indirildi ve ayrıştırıldı.

Görüntüler 64x64 piksel olarak yeniden boyutlandı.

Normalizasyon işlemi ile görüntü verileri 0-1 aralığına dönüştürüldü.

Etiketleme:

Görüntüler, dosya adına ve klasör yapısına göre iki kategoriye ayrıldı: “ALL” (kanserli) ve “Normal”.

Etiketler sayısal hale getirilerek makine öğrenmesi modeli için hazırlandı.

Model Oluşturma:

CNN (Convolutional Neural Network) mimarisi tasarlandı.

Modelin yapısı:

3 adet konvolüsiyon katmanı (Conv2D) ve max-pooling katmanları.

Fully-connected (tam bağlı) katmanlar.

Softmax çıkış katmanı.

Model, Adam optimizer ve sparse categorical crossentropy kayıp fonksiyonu ile derlendi.

Modelin Eğitimi:

Model 10 epoch boyunca eğitildi.

Validation verisi ile modelin performansı test edildi.

Performans Değerlendirmesi:

Modelin eğitim ve validation doğruluk/kayıp grafikleri oluşturuldu.

Validation doğruluğu: %70,1

Validation kaybı: 0.768

Sonuçlar ve Kayıt:

Model, lösemik hücreleri tespit edebilme konusunda umut verici bir başarıya ulaştı.

Model kayıt altına alınarak gelecekteki çalışmalar için hazır hale getirildi.

Sonuçların Değerlendirilmesi
Validation verisi üzerinde %70,1 doğruluk elde edilmiştir. Bu sonuç, mikroskop altındaki morfolojik benzerliklerin zorluğu düşünüldüğünde başarılı bir performansı işaret etmektedir. İleride, ağırıklı veri artırma teknikleri ve daha karmaşık model mimarilerinin kullanılması ile doğruluğun daha da artması beklenmektedir.
