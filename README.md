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

## Result

### **<span style="color:lightblue">En iyi model: </span>**
| En iyi model | RMSE:0.3853 | 

### Proje yapısı

### Temel Özellikler:
- **Eksik Değer Yönetimi:** Eksik veriler, basit ortalama ataması yerine **LightGBM (Regressor & Classifier)** modelleri kullanılarak akıllı bir şekilde doldurulmuştur.
- **Model Seçimi:** Çoklu Doğrusal Regresyon'un veriye uygun olmadığı tespit edildikten sonra **Ensemble** yöntemlerine (Random Forest, XGBoost, Bagging) odaklanılmıştır.

## 🛠️ Kurulum
Projeyi yerelinizde çalıştırmak için aşağıdaki adımları izleyebilirsiniz:

1. Depoyu klonlayın:
   ```bash
   git clone [https://github.com/kullaniciadi/yzta-2026-datathon-cognitive-score.git](https://github.com/kullaniciadi/yzta-2026-datathon-cognitive-score.git)
