<div align="center">

# fascan

**Market fişini tara, paranın nereye gittiğini gör.**

![iOS](https://img.shields.io/badge/iOS-26+-000000?logo=apple&logoColor=white)
![Swift](https://img.shields.io/badge/Swift-6-F05138?logo=swift&logoColor=white)
![SwiftUI](https://img.shields.io/badge/SwiftUI-0A84FF?logo=swift&logoColor=white)
![SwiftData](https://img.shields.io/badge/SwiftData-34C759)
![On-device](https://img.shields.io/badge/veri-cihazda_kalır-8E8E93)
![Durum](https://img.shields.io/badge/durum-geliştiriliyor-FF9F0A)


</div>

---

Fascan, market fişinin fotoğrafını çekmeni sağlar ve fişi **telefonun içinde** okur. Mağaza, tarih, toplam tutar ve ürünler otomatik ayrılır. Ay sonunda hangi markete ve hangi ürünlere ne kadar harcadığını tek ekranda görürsün.

Hesap yok, sunucu yok. Fişlerin telefonundan hiçbir yere gitmez.

## Nasıl çalışır

```
Tara  →  Oku  →  Ayrıştır  →  Düzelt  →  Kaydet  →  Özetle
```

| Adım | Ne oluyor | Kullanılan teknoloji |
| --- | --- | --- |
| Tara | Fiş kenarları bulunur, eğiklik düzeltilir | VisionKit |
| Oku | Türkçe metin cihazda tanınır | Vision |
| Ayrıştır | Mağaza, tarih, toplam ve ürün satırları ayrılır | Swift Regex |
| Düzelt | Kullanıcı hatalı alanları onaylar | SwiftUI |
| Kaydet | Fişler ve ürünler saklanır | SwiftData |
| Özetle | Aylık ve mağaza bazlı harcama | Swift Charts |

## Doğruluk

Ayrıştırıcı, gerçek market fişlerinden oluşan bir test setiyle ölçülür.

| Alan | Doğruluk |
| --- | --- |
| Mağaza | ölçülüyor |
| Tarih | ölçülüyor |
| Toplam | ölçülüyor |
| Ürün satırları | ölçülüyor |

<sub>Test seti: — fiş · Son ölçüm: —</sub>

## Çalıştır

Xcode 26 ile `fascan.xcodeproj` dosyasını aç ve **⌘R**'ye bas. Kamera simülatörde çalışmaz; simülatörde galeriden fiş fotoğrafı seçebilirsin.

Testler için **⌘U**.

## Kararlar

Para neden kuruş olarak saklanıyor, OCR satırları nasıl yeniden kuruluyor, yapay zekâ neden opsiyonel? Tüm teknik kararlar gerekçeleriyle birlikte [docs/kararlar.md](docs/kararlar.md) dosyasında.

---

<div align="center">
<sub>Geliştiren: <a href="https://github.com/fferhatakr">Ferhat Akar</a></sub>
</div>
