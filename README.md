# Datahon_2026

## YZTA 2026 Datathon: Bilişsel Performans Skoru Tahmini

Bu proje, bireylerin çeşitli demografik özellikleri ve uyku verilerini kullanarak **Bilişsel Performans Skorlarını** tahmin etmeyi amaçlayan bir makine öğrenmesi çalışmasıdır.

## 📊 Proje Özeti
Proje kapsamında sunulan veri seti üzerinde kapsamlı bir veri ön işleme, eksik değer tamamlama ve regresyon modelleme süreçleri uygulanmıştır. 

### Temel Özellikler:
- **Eksik Değer Yönetimi:** Eksik veriler, basit ortalama ataması yerine **LightGBM (Regressor & Classifier)** modelleri kullanılarak akıllı bir şekilde doldurulmuştur.
- **Model Seçimi:** Çoklu Doğrusal Regresyon'un veriye uygun olmadığı tespit edildikten sonra **Ensemble** yöntemlerine (Random Forest, XGBoost, Bagging) odaklanılmıştır.

## 🛠️ Kurulum
Projeyi yerelinizde çalıştırmak için aşağıdaki adımları izleyebilirsiniz:

1. Depoyu klonlayın:
   ```bash
   git clone [https://github.com/kullaniciadi/yzta-2026-datathon-cognitive-score.git](https://github.com/kullaniciadi/yzta-2026-datathon-cognitive-score.git)


# 1. Klasörü bir Git deposu haline getir
git init

# 2. Tüm dosyaları (klasör yapısıyla birlikte) takibe al
git add .

# 3. Yaptığın işlemi onayla (Commit)
git commit -m "Proje yapısı ve ilk modelleme çalışmaları eklendi"

# 4. Ana dal ismini 'main' yap (GitHub standardı)
git branch -M main

# 5. Yerel deponu GitHub'daki boş depoya bağla 
# (Aşağıdaki URL kısmına kendi oluşturduğun reponun linkini yapıştır)
git remote add origin https://github.com/kullanici_adin/repo_adin.git

# 6. Dosyaları GitHub'a gönder
git push -u origin main
