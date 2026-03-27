# 📱 Zeyn Eczane - Mobil Tarama ve Yönetim Uygulaması

![Flutter](https://img.shields.io/badge/Flutter-%2302569B.svg?style=for-the-badge&logo=Flutter&logoColor=white)
![Dart](https://img.shields.io/badge/dart-%230175C2.svg?style=for-the-badge&logo=dart&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)

> **⚠️ Önemli Not:** Güvenlik ve gizlilik politikaları gereği, bu deponun (repository) kaynak kodları kapalı tutulmaktadır (Closed-Source).

## ⚙️ Backend & API
Bu uygulama, ASP.NET Core ve Clean Architecture ile geliştirilmiş ZeynEczane RESTful API'sini tüketmektedir.
👉 **[ZeynEczane Backend Deposunu incelemek için buraya tıklayın](https://github.com/Nartkansat/ZeynEczane)**

---

## 🚀 Temel Amaç ve Çözümler
Zeyn, eczane iş akışlarını dijitalleştirmek ve operasyonel verimliliği artırmak amacıyla geliştirilmiş akıllı veri tarama ve yönetim çözümüdür. Uygulama, eczacıların toplu veri işleme ve güvenli belge paylaşımı ihtiyaçları için özel olarak optimize edilmiştir.

*   **Çoklu QR Yönetimi:** Tek seferde birden fazla QR kodu tarayarak ortak veri havuzuna aktarma ve diğer eczanelerle sorunsuz paylaşım imkanı sunar.
*   **Hızlı Stok Envanteri:** Manuel süreçleri ortadan kaldırarak cihaz kamerası üzerinden saniyeler içinde stok sayımı yapılmasını sağlar.
*   **Güvenli Belge Transferi:** Fiziksel belgelerin dijitalleştirilmesini ve şifrelenmiş altyapı üzerinden güvenli transferini sağlar.

---

## 🏗️ Mobil Mimari ve Klasör Yapısı

Uygulama, Flutter ekosistemi içerisinde ölçeklenebilirliği ve bakım kolaylığını sağlamak amacıyla özellik odaklı (feature-based) bir mimari ile yapılandırılmıştır:

```text
📂 zeyn_mobile_app
 ┣ 📂 lib
 ┃ ┣ 📂 core               # Sabitler, Temalar, Ağ Yapılandırmaları ve Araçlar
 ┃ ┣ 📂 features           # QR Tarayıcı, Kimlik Doğrulama, Anasayfa, Envanter Modülleri
 ┃ ┣ 📂 shared             # Ortak Widget'lar, Arayüz Bileşenleri ve Yardımcı Sınıflar
 ┃ ┗ 📜 main.dart          # Uygulama Başlangıç Noktası
 ┣ 📂 assets               # Görseller, İkonlar ve Fontlar
 ┗ 📜 pubspec.yaml         # Proje Bağımlılıkları ve Konfigürasyonları
```

## 🧩 Uygulama Modülleri

### 1. Kimlik Doğrulama (Authentication)
Uygulama güvenliğini en üst düzeyde tutmak amacıyla kayıt işlemleri yalnızca merkezi admin paneli üzerinden gerçekleştirilir. Kullanıcılar, önceden kaydedilmiş kimlik bilgileriyle sisteme güvenli bir şekilde erişir; mobil uygulama üzerinden doğrudan kayıt işlemi kapalıdır.

### 2. Anasayfa (Dashboard)
Eczanenin günlük operasyonel durumunu gerçek zamanlı olarak izlemek için merkezi yönetim alanıdır.
*   **Veri Takibi:** Taranan toplam kod sayısı ve bugün iletilen veri hacmi.
*   **Grup Bilgileri:** Bağlı bulunulan eczane grubu ve ağdaki diğer eczanelerin sayısı.
*   **Durum Bildirimleri:** Yerel hafızada depolanan ve henüz sisteme iletilmemiş bekleyen QR kodların takibi.

### 3. Çoklu Tarama (Multi-Scan)
Gelişmiş görüntü işleme teknolojisi kullanılarak, kameranın görüş alanındaki birden fazla ilaç aynı anda tanımlanır ve hızla listeye aktarılır.
> **Not:** Uygulamanın en büyük avantajı, tek bir kamera açısıyla birden fazla ürünü aynı anda okuyabilmesidir.

### 4. QR Listesi
Taranan ilaçların (Barkod, İsim vb.) detaylandırıldığı yönetim panelidir.
*   **Düzenleme:** Seçilen kodları kopyalama, silme veya toplu işlem yapma yeteneği.
*   **QR Birleştirme:** Listedeki tüm verileri tek ve birleşik bir QR koda dönüştürür. Oluşturulan bu QR okutulduğunda, içerdiği tüm ilaçların barkodları toplu olarak işlenir.

### 5. Stok Sayımı
Hızlı tarama moduyla stok sayım süreçlerini optimize eder.
*   **Dışa Aktarma Seçenekleri:** Sayım sonuçlarını doğrudan merkezi sisteme aktarın veya **Excel** formatında cihazınıza indirin.

### 6. Belge ve QR Çözümleme
*   **Arşivleme:** Fiziksel belgeleri tarar ve şifreli protokoller üzerinden sisteme yükler.
*   **Fotoğraf Çözümleme:** Kullanıcıların, cihaz galerisinden daha önce çekilmiş fotoğrafları seçerek içlerindeki QR kodları çözümlemesine olanak tanır.

---

## 🛠 Teknik Avantajlar
*   **Hız:** Çoklu nesne algılama ile saniyeler içinde onlarca veri girişi.
*   **Güvenlik:** Belge iletimi sırasında uçtan uca şifreleme.
*   **Esneklik:** Kusursuz Excel entegrasyonu ve gelişmiş toplu işlem yetenekleri.

---

## 📸 Ekran Görüntüleri

<img src="https://github.com/user-attachments/assets/6cb936ba-8a75-4662-b86b-6d66bbda5a81" alt="Zeyn Mobile App Screenshot" width="300">
