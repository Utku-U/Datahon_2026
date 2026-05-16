# Datahon_2026

## YZTA 2026 Datathon: Bilişsel Performans Skoru Tahmini

Bu proje, bireylerin çeşitli demografik özellikleri ve uyku verilerini kullanarak **Bilişsel Performans Skorlarını** tahmin etmeyi amaçlayan bir makine öğrenmesi çalışmasıdır.

## 📊 Proje Özeti
Proje kapsamında sunulan veri seti üzerinde kapsamlı bir veri ön işleme, eksik değer tamamlama ve regresyon modelleme süreçleri uygulanmıştır. 

|  | Değer 
| :--- | :---: | 
| Görev | Regresyon | 
| Hedef | bilissel_performans_skoru | 
| Birincil Metrik | RMSE |
| Train | 56000,24 | 
| Test| 24000,23 | 
| En iyi model | RMSE: 0.3853 | 

### Data Cleaning
Elimizdeki ham veri setlerinde(train,test), eksik değeri olan değişkenlerin sınıflandırma modeli ile (LGBM) doldurulabilmesi adına elimizde daha fazla gözlem olması adına bu aşama için train ve test verileri birleştirilmiştir. Bu sayede elimizde 80000 gözlemli tek bir veri setinde eksik değeri olmayan gözlemler kullanılarak, eksik gözlemi olan bütün değişken değerlerine uygun tahminler değerleri üretilir ve indexlerine göre uygun verilere(train,test) atama işlemi gerçekleştirilir. Daha sonra, artık eksik gözlemi bulunmayan verilerin kategorik ve numerik olarak gözlenmesi işlemlerini içerir. 

### EDA
- Numerik değişkenlerin histogram grafikleri, bağımsız değişkenlerin hedef değişkene göre saçılımları ve Box-plot grafikleri incelenerek, veride aykırı değerlerin varlığı ve uygun regresyon model seçimlerine dair bir ön izlenim barındırması amaçlanmıştır. 
- Ve Korelasyon grafiği ile değişkenler arası ilişkiler incelenmiştir. "hafta_sonu_uyku_farki_saat" ilişkisiz olduğu için noise azaltmaya yönelik bu değişken çıkartılmıştır.

### Data Manipulation
- Kategorik değişkenlerin regresyon modellerinde kullanılabilmesi adına dummy değişkenler üretilmiştir.
- Kurulması planlanan ağaç tabanlı ve parametrik olmayan modellerin (Decision Tree, Random Forest, LightGBM) matematiksel olarak ölçek varyasyonlarından etkilenmediği bilinmesine rağmen veri setindeki aykırı değerlerin (outliers) olumsuz etkilerini minimize etmek adına RobustScaler kullanılmıştır. Çünkü bu problemde bizim için önemli olan RMSE değeri aykırı değerlerden oldukça etiklenir.Ve verideki gürültünün azaltılması amaçlanmıştır. 
- Ham train ve test verilerimizin hem ölçeklenmiş ve ölçeklenmemiş (train,test), verileri ayrı ayrı oluşturulmuştur.

### Daha preprocessing
- Train veri setinde eğitilecek olan modelin doğruluğunun ve metriklerinin testinin yapılabilmesi için ham train verimiz, train ve valid olarak ayrılmıştır. 

### Modelleme
| LGBM | Valid setindei Metrikler
| :--- | :---: | 
| R2 | 0.7015 | 
| MSE | 0.1484 | 
| RMSE | 0.3853 |

| Out_of_Bagging | Valid setindei Metrikler
| :--- | :---: | 
| R2 | 0.6736 | 
| MSE | 0.1623 | 
| RMSE | 0.4029 |

| XBG | Valid setindei Metrikler
| :--- | :---: | 
| R2 | 0.6993 | 
| MSE | 0.1495 | 
| RMSE | 0.3867 |



## 🛠️ Kurulum
Projeyi yerelinizde çalıştırmak için aşağıdaki adımları izleyebilirsiniz:

   ```bash
   pip install -r requirements.txt
   git clone [https://github.com/kullaniciadi/yzta-2026-datathon-cognitive-score.git](https://github.com/kullaniciadi/yzta-2026-datathon-cognitive-score.git)
