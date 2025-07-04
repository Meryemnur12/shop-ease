# ShopEase

name: Flutter CI

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2
    - uses: subosito/flutter-action@v2
      with:
        flutter-version: 'latest'
    - run: flutter pub get
    - run: flutter analyze
    - run: flutter test


ShopEase, Flutter tabanlı yenilikçi bir alışveriş uygulamasıdır.  
Akıllı arama, AR ürünü yerleştirme ve topluluk filtreleri ile öne çıkar.

---

## Özellikler

- Kategori & Ürün Listeleme  
- Detay Sayfası & AR Deneme  
- Akıllı Arama & Sesli Komut  
- Sepet & Ödeme Akışı  
- Fiyat Karşılaştırma & İndirim Bildirimi  
- Kullanıcı Profili & Favoriler

---

## Teknoloji ve Kullanılan Paketler

| Kategori             | Paket / Teknoloji                         |
|----------------------|-------------------------------------------|
| State Management     | riverpod                                  |
| HTTP & API           | dio                                       |
| AR Deneme            | arcore_flutter_plugin                     |
| Ödeme                | flutter_stripe                            |
| Bildirimler          | firebase_messaging                        |
| Local Storage        | hive                                      |
| Harita & Konum       | google_maps_flutter, location             |

---

## Kurulum ve Çalıştırma

1. Depoyu klonla  
   ```bash
   git clone https://github.com/kullanici_adin/shop_ease.git
   cd shop_ease

