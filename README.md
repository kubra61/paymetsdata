--kaggle linkim=https://www.kaggle.com/code/kbrakse/notebook1

# Dolandırıcılık Tespiti Projesi

Bu projede, finansal işlemlerden oluşan bir veri seti kullanarak iki farklı öğrenme türünü (gözetimli ve gözetimsiz öğrenme) karşılaştırdık. Amacımız dolandırıcılık tespiti yapmaktı.

## Veri Seti

Veri seti şunları içeriyor:
- **Sütunlar:** `step`, `type`, `amount`, `nameOrig`, `oldbalanceOrg`, `newbalanceOrig`, `nameDest`, `oldbalanceDest`, `newbalanceDest`, `isFraud`, `isFlaggedFraud`
- **Satır Sayısı:** 14 (örnek veri)
- **Amaç:** Finansal dolandırıcılık tespiti

## Kullanılan Algoritmalar
- **KMeans** (Gözetimsiz öğrenme)
- **KNN** (Gözetimli öğrenme)

## Sonuçlar

### Gözetimli Öğrenme Sonuçları (KNN)
- **KNN doğruluk oranı:** %85
- **Hata oranı:** %15
- Gözetimli öğrenme algoritması olan KNN, doğruluğu ve düşük hata oranı ile dolandırıcılık tespiti konusunda oldukça iyi sonuçlar verdi.

### Gözetimsiz Öğrenme Sonuçları (KMeans)
- **Küme sayısı:** 3
- **Kümeleme doğruluğu:** %75
- Gözetimsiz öğrenme algoritması olan KMeans, veri setini üç kümeye ayırdı. Dolandırıcılık tespitinde kullanıldığında, kümeleme doğruluğu %75 seviyesinde kaldı.

## Çıktılar ve Sonuçlar

### Gözetimli Öğrenme Sonuçları (KNN)
- KNN algoritması, etiketlenmiş veri kullanarak dolandırıcılığı başarılı bir şekilde tespit etti.
- [Grafikler ve analizlerin burada yer alması önerilir.]

### Gözetimsiz Öğrenme Sonuçları (KMeans)
- KMeans algoritması ise dolandırıcılığı doğrudan etiket bilgisi olmadan kümeleme yoluyla ayırt etmeye çalıştı.
- [KMeans sonuçlarının grafik ve analizleri de burada yer alabilir.]

Sonuç olarak, **KNN (gözetimli öğrenme)** algoritması, dolandırıcılık tespitinde daha iyi performans gösterdi. Çünkü bu algoritma, etiketi bilinen veri seti ile çalışarak doğrudan sınıflandırma yapabildi. **KMeans (gözetimsiz öğrenme)** ise etiket bilgisi olmadığı için kümeler oluşturarak dolandırıcılığı ayırt etmekte zorlandı. Ancak veri setinin yapısına göre kümeleme de anlamlı sonuçlar verdi.

## Sonuç

Veri setimiz üzerinde yapılan analizler sonucunda, **KNN** algoritması dolandırıcılık tespiti için daha iyi bir performans gösterdi. Bunun nedeni, veri setinin etiketli olması ve KNN algoritmasının etiketli verilerle daha iyi çalışmasıdır. **KMeans** ise daha az bilgi ile çalışmasına rağmen anlamlı kümeler oluşturarak dolandırıcılığı tespit etmeye çalıştı.

Bu sonuçlar, veri setinin yapısına ve etiketli/etiketsiz verilerin etkisine bağlıdır. Sonuçlar, finansal dolandırıcılık tespiti gibi uygulamalarda gözetimli öğrenme algoritmalarının daha etkili olduğunu göstermektedir.