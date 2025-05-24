# ✈️ Uçak Bilet Rezervasyon Konsol Uygulaması (Java OOP)

## 📌 Proje Açıklaması

Bu proje, Java programlama dili kullanılarak geliştirilen basit bir uçak bilet rezervasyon sistemidir. Kullanıcılar konsol arayüzü üzerinden mevcut uçuşları görüntüleyebilir ve bir uçuş için rezervasyon yapabilir. Yapılan rezervasyonlar JSON dosyasına kaydedilmektedir.

---

## 🔧 Kullanılan Yapılar

- Java OOP (Sınıflar, Nesneler, Encapsulation)
- Interface ve Abstract kullanımına açık yapı
- Konsol tabanlı kullanıcı arayüzü
- JSON formatında veri kaydı (Google Gson kütüphanesi)

---

## 🧱 Sınıflar

| Sınıf Adı       | Açıklama |
|----------------|----------|
| `Ucak`         | Uçak bilgilerini içerir (model, marka, seri no, koltuk kapasitesi). |
| `Lokasyon`     | Lokasyon bilgilerini tutar (ülke, şehir, havaalanı, aktif/pasif). |
| `Ucus`         | Bir uçuşu tanımlar. Kalkış, varış, saat ve uçak içerir. |
| `Rezervasyon`  | Bir yolcu rezervasyonu (ad, soyad, yaş, uçuş). |
| `DosyaServisi` | Rezervasyonları JSON dosyasına yazar. |
| `MainApp`      | Konsol uygulaması burada çalışır, kullanıcı etkileşimi buradan yönetilir. |

---

## ▶️ Uygulama Kullanımı

1. Konsolda mevcut uçuşlar listelenir.
2. Kullanıcı uçuş seçer.
3. Ad, soyad, yaş bilgileri girilir.
4. Uçuşta boş koltuk varsa rezervasyon yapılır.
5. Programdan çıkıldığında tüm rezervasyonlar `rezervasyonlar.json` dosyasına kaydedilir.

---

## 📂 JSON Dosya Yapısı

Rezervasyonlar şu şekilde bir JSON formatında saklanır:

```json
[
  {
    "ad": "Ayşe",
    "soyad": "Yılmaz",
    "yas": 25,
    "ucus": {
      ...
    }
  }
]
