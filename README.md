# My Apps — Emrah Yurttutan

Emrah Yurttutan tarafından geliştirilen uygulamalar & araçlar.

Appétit tarafından güçlendirilen kişisel uygulama katalogu — Fatih Kadir Akın'ın (FKA) App Store'dan ilham alan açık kaynak katalogu.

**Live** · [apps.yurttutan.net](https://apps.yurttutan.net) · **Kaynak:** [Appétit](https://github.com/fka/appetit)

---

Bu repo, Fatih Kadir Akın'ın (FKA) [Appétit](https://github.com/fka/appetit) projesinin bir fork'udur; Emrah Yurttutan'ın kişisel uygulama katalogu olarak özelleştirilmiştir. Framework, UI ve mimari için tüm kredi FKA'ya aittir. Bu fork yalnızca uygulama verisi, marka ve kategori yapılandırmasını değiştirmektedir.

Appétit, Apple App Store görünümünde güzel ve gezinilebilir bir uygulama katalogu. Tamamen vanilla HTML, CSS ve JS ile inşa edilmiş — framework yok, build adımı yok, bağımlılık yok. Sadece `apps.json` dosyasını düzenle ve deploy et.

## Uygulamalar

| Uygulama                                                                                                                    | Kategori                  | Platform      |
| --------------------------------------------------------------------------------------------------------------------------- | ------------------------- | ------------- |
| [Ehliyet Sınav Soruları](https://apps.apple.com/tr/app/ehliyet-s%C4%B1nav-sorular%C4%B1-2026-1/id1435728653)                | Education                 | iOS & Android |
| [KPSS Deneme Sınavları](https://apps.apple.com/tr/app/kpss-2025-deneme-s%C4%B1navlar%C4%B1-%C3%A7%C3%B6z/id1482779937)      | Education                 | iOS & Android |
| [Tarih Altın Bilgiler](https://apps.apple.com/tr/app/tarih-alt%C4%B1n-bilgiler/id1497468191)                                | Education                 | iOS & Android |
| [Prayer Times & Qibla](https://apps.apple.com/app/id6450932588)                                                             | Lifestyle                 | iOS & Android |
| [Efsun: Kahve Falı & Rüya](https://play.google.com/store/apps/details?id=com.appasoft.efsunkfrt)                            | Lifestyle & Entertainment | iOS & Android |
| [Kadın Sağlığı & Güvenlik](https://apps.apple.com/tr/app/kad%C4%B1n-sa%C4%9Fl%C4%B1%C4%9F%C4%B1-g%C3%BCvenlik/id6756342991) | Health & Fitness          | iOS           |
| [Bitki Sulama: Bakım ve Takip](https://apps.apple.com/tr/app/bitki-sulama-bak%C4%B1m-ve-takip/id6755485267)                 | Lifestyle & Productivity  | iOS & Android |
| [Derdini Dök](https://apps.apple.com/tr/app/derdini-d%C3%B6k-anonim-payla%C5%9F%C4%B1m/id6755607825)                        | Lifestyle                 | iOS & Android |
| [Çizmeli Kedi Veteriner](https://apps.apple.com/tr/app/%C3%A7izmeli-kedi-veteriner/id6759364103)                            | Lifestyle                 | iOS & Android |

## Dosya Yapısı

```
├── index.html          Ana HTML
├── style.css           Stiller (dark + light tema)
├── app.js              Routing, rendering, carousel, modaller
├── apps.json           Tüm uygulama verisi — bu dosyayı düzenle
├── logo.svg            Favicon
├── update-stats.sh     GitHub yıldız/fork sayılarını günceller
└── CNAME               GitHub Pages için özel domain
```

## Geliştirme

```bash
git clone https://github.com/emrahyurttutan/my-apps.git
cd my-apps
python3 -m http.server 8080
```

[localhost:8080](http://localhost:8080) adresinden çalıştır.

## Yeni Uygulama Eklemek

`apps.json` dosyasını düzenle:

```jsonc
{
  "id": "app-id",
  "name": "Uygulama Adı",
  "subtitle": "Kısa açıklama",
  "description": "Liste görünümü için tek satır.",
  "longDescription": "Detay sayfası için tam açıklama.",
  "icon": "https://example.com/icon.png",
  "iconStyle": { "objectFit": "cover", "borderRadius": "22%" },
  "category": ["education"],
  "platform": "iOS & Android",
  "price": "Free",
  "language": "Swift / Kotlin",
  "requirements": "iOS 15+ or Android 8+",
  "links": [
    {
      "label": "App Store",
      "url": "https://apps.apple.com/...",
      "platform": "ios",
    },
    {
      "label": "Google Play",
      "url": "https://play.google.com/...",
      "platform": "android",
    },
  ],
  "features": ["Özellik 1", "Özellik 2"],
}
```

## Deploy

GitHub Actions otomatik olarak `master` branch'ine push yapıldığında [apps.yurttutan.net](https://apps.yurttutan.net) adresine deploy eder.

## Lisans

MIT
