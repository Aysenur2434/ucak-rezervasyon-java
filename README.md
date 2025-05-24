# ✈️ Java Uçak Bilet Rezervasyon Uygulaması

Bu proje, Java dilinde nesne yönelimli programlama prensiplerine uygun olarak geliştirilmiş basit bir uçak bileti rezervasyon uygulamasıdır. Konsol üzerinden çalışan bu sistem, kullanıcıya aktif uçuşları listeler ve koltuk uygunluğu olan uçuşlara rezervasyon yapılmasına izin verir.

---

## 🔧 Kullanılan Yapılar

- `Class`, `Encapsulation`, `Association`
- `List`, `Scanner`, `LocalDateTime`
- `Gson` ile JSON dosyaya veri yazma
- Konsol tabanlı etkileşim

---

## 📦 Sınıflar Hakkında Kısa Bilgi

| Sınıf Adı         | Açıklama |
|-------------------|----------|
| `Ucak`            | Model, marka, seri no, koltuk kapasitesi bilgilerini tutar. |
| `Lokasyon`        | Ülke, şehir, havaalanı ve aktiflik durumu içerir. |
| `Ucus`            | Kalkış, varış, saat ve uçak bilgilerini birleştirir. |
| `Rezervasyon`     | Yolcunun adı, soyadı, yaşı ve seçtiği uçuş bilgilerini barındırır. |
| `DosyaServisi`    | Rezervasyon listesini JSON formatında dosyaya yazar. |
| `MainApp`         | Konsol arayüzüdür, tüm işlemler burada yürütülür. |

---

## ▶️ Kullanım

1. Uygulama başlatıldığında mevcut uçuşlar listelenir.
2. Kullanıcı bir uçuş seçer.
3. Ad, soyad ve yaş bilgileri girilir.
4. Rezervasyon uygunluk kontrolü yapılır.
5. Başarılı rezervasyonlar `rezervasyonlar.json` dosyasına kaydedilir.

---

## 💡 Notlar

- Rezervasyon sayısı, uçak koltuk kapasitesinden fazla olamaz.
- Lokasyonlar aktif değilse uçuşta kullanılamaz.
- Program sonunda tüm rezervasyonlar otomatik olarak dosyaya kaydedilir.

---

## 📁 Örnek JSON Kaydı

```json
[
  {
    "ad": "Ayşenur",
    "soyad": "Yıldız",
    "yas": 23,
    "ucus": {
      ...
    }
  }
]
