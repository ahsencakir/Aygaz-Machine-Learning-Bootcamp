# Google Play Store Apps - Churn Analysis and Noise & Anomaly Detection

Bu proje, Google Play Store Apps verisini kullanarak iki farklı problem üzerine odaklanmıştır: **Churn Analysis (Kullanıcı Kaybı Analizi)** ve **Noise and Anomaly Detection (Gürültü ve Anomali Tespiti)**. Verinin öne çıkan özellikleri ve yapılan analizler aşağıda detaylandırılmıştır.

## Kaggle Notebook Link

https://www.kaggle.com/code/ahsencakir/churn-analysis-noise-and-anomaly-detection

## Veri Seti Açıklaması

Google Play Store Apps veri seti şu sütunları içermektedir:

- **App Name**: Uygulamaların isimleri.
- **App Id**: Uygulamaların eşsiz değerleri.
- **Category**: Uygulamaların kategorileri.
- **Rating**: Uygulamaların 1 ile 5 arasında aldığı puanlar.
- **Rating Count**: Uygulamaların kaç kez oylandığını gösterir.
- **Installs**: Uygulamaların indirilme sayısı.
- **Minimum Installs**: Minimum indirilme sayısı.
- **Maximum Installs**: Maksimum indirilme sayısı.
- **Free**: Uygulamanın ücretsiz olup olmadığını gösterir (True/False).
- **Price**: Uygulamaların ücreti.
- **Currency**: Ücretli uygulamaların para birimi.
- **Size**: Uygulamanın boyutu.
- **Minimum Android**: Desteklenen minimum Android sürümü.
- **Developer Id**: Geliştirici kimliği.
- **Developer Website**: Geliştirici websitesi.
- **Developer Email**: Geliştirici e-posta adresi.
- **Released**: Uygulamanın yayınlanma tarihi.
- **Privacy Policy**: Gizlilik politikası.
- **Last Updated**: Uygulamanın son güncellenme tarihi.
- **Content Rating**: İçeriğin hangi kitleye yönelik olduğunu gösterir.
- **Ad Supported**: Reklam desteklenip desteklenmediğini belirtir (True/False).
- **In-app Purchases**: Uygulama içi satın alım olup olmadığını gösterir (True/False).
- **Editors Choice**: Editörlerin önerip önermediğini belirtir (True/False).

## Kullanılan Sütunlar
Projelerde aşağıdaki sütunlar kullanılmıştır:

- **App Name**
- **Rating**
- **Rating Count**
- **Installs**
- **Price**
- **Category**
- **Last Updated**
- **Free**

## Churn Analysis Projesi Sonuçları
Churn Analysis projemizde, model performansını şu metriklerle değerlendirdik:

- **Mean Squared Error (MSE)**: 0.005553778039120735
- **Mean Absolute Error (MAE)**: 0.005553778039120735
- **Confusion Matrix**:
  [[246653    663]
  [  1906 213346]]
 - **Accuracy**: 0.9944462219608793
- **Precision**: 0.9969019994486213
- **Recall**: 0.9911452622972144
- **F1**: 0.9940152960553137

## Noise and Anomaly Detection Projesi Sonuçları
Noise and Anomaly Detection projemizin final çıktısı:

- **Davies-Bouldin Skoru**: 12.782790832582085

Bu proje için Davies-Bouldin skoru, kümeleme algoritmalarının performansını değerlendirmek amacıyla kullanılmıştır. Bu indeks, her bir kümenin merkezi ile o kümedeki örneklerin birbirine yakınlığını ölçer. Düşük Davies-Bouldin skoru, daha iyi bir kümeleme performansını gösterir.

## Projenin Amacı ve Uygulanan Yöntemler
Veri setimiz, Google Play Store'daki Android uygulamalarının kategorilerini tahmin etmek için denetimli öğrenme yöntemlerinden sınıflandırma algoritmalarının kullanımına uygundur. Özellikle her uygulamanın sahip olduğu "Kategori" etiketi, sınıflandırma modelleri eğitmek için kullanılmıştır.

Bu projede, çeşitli sınıflandırma algoritmaları (Lojistik Regresyon, Doğrusal Regresyon vb.) test edilmiştir. Verinin karmaşıklığı, boyutu ve doğruluk düzeyi gibi faktörler göz önünde bulundurularak uygun algoritmalar seçilmiş ve deneysel bir yaklaşımla sonuçlar karşılaştırılmıştır.

**Özellik mühendisliği**, model doğruluğunu artırmak için önemli bir adım olarak kabul edilmiştir. Model değerlendirme metrikleri, düzenleme teknikleri ve aşırı öğrenmeyi önleme yöntemleri kullanılarak daha başarılı sonuçlar elde edilmiştir.

