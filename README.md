# Zeyn Eczane Uygulaması

Zeyn, eczane iş akışlarını dijitalleştirmek ve operasyonel verimliliği artırmak amacıyla geliştirilmiş, akıllı veri tarama ve yönetim çözümüdür. Uygulama, özellikle toplu veri işleme ve güvenli belge paylaşımı konularında eczacıların ihtiyaçlarına yönelik optimize edilmiştir.

---

## 🚀 Temel Amaç ve Çözümler

* **Çoklu QR Yönetimi:** Tek seferde birden fazla QR kodu tarayarak ortak veri havuzuna aktarma ve diğer eczanelerle paylaşma imkanı sunar.
* **Hızlı Stok Envanteri:** Manuel süreçleri ortadan kaldırarak kamera üzerinden saniyeler içinde stok sayımı yapılmasını sağlar.
* **Güvenli Belge Transferi:** Fiziksel belgelerin dijitalleştirilmesini ve şifrelenmiş (encrypted) bir altyapı üzerinden güvenli transferini gerçekleştirir.

---

## 📱 Uygulama Bölümleri

### 1. Uygulama Girişi (Authentication)
Uygulama güvenliğini en üst düzeyde tutmak amacıyla kayıt işlemleri yalnızca merkezi panel üzerinden gerçekleştirilir. Kullanıcılar, sistemde kayıtlı olan kullanıcı adı ve şifreleri ile sisteme güvenli erişim sağlar; mobil uygulama üzerinden doğrudan kayıt oluşturulmaz.

### 2. Anasayfa (Dashboard)
Eczanenin günlük operasyonel durumunu anlık olarak takip edebileceğiniz merkezi yönetim alanıdır.
* **Veri Takibi:** Okutulan toplam kod sayısı ve bugün gönderilen veri hacmi.
* **Grup Bilgileri:** Bağlı bulunan eczane grubu ve gruptaki diğer eczane sayısı.
* **Durum Bildirimleri:** Sisteme henüz gönderilmemiş, yerel hafızada bekleyen QR kodların takibi.

### 3. QR Okutma (Multi-Scan)
Gelişmiş görüntü işleme teknolojisi sayesinde, kamera açısındaki birden fazla ilacı aynı anda tanımlar ve hızlıca listeye aktarır.
> **Not:** Uygulamanın en büyük avantajı, tek bir kamera açısıyla birden fazla ürünü aynı anda okuyabilmesidir.

### 4. QR Listesi
Taranan ilaçların detaylı (Barkod, İsim vb.) listelendiği yönetim panelidir.
* **Düzenleme:** Seçili kodları kopyalama, silme veya toplu işlem yeteneği.
* **QR Birleştirme:** Listedeki tüm verileri tek bir QR koda dönüştürür. Bu karekod okutulduğunda, içerdiği tüm ilaçların barkodları toplu olarak işlenir.

### 5. Stok Sayımı
Hızlı okuma moduyla stok sayım süreçlerini optimize eder.
* **Çıktı Seçenekleri:** Sayım sonuçlarını doğrudan merkezi sisteme aktarabilir veya **Excel** formatında dışa aktarım sağlayabilirsiniz.

### 6. Belge ve QR Çözümleme
* **Arşivleme:** Fiziksel evrakları tarayarak şifreli protokoller üzerinden sisteme yükler.
* **Fotoğraf Çözümleme:** Anlık olarak taranmayan veya daha önce fotoğrafı çekilmiş olan QR kodları, galeri üzerinden seçerek sisteme dahil etme imkanı sunar.

---

## 🛠 Teknik Avantajlar

* **Hız:** Çoklu nesne algılama ile saniyeler içinde onlarca veri girişi.
* **Güvenlik:** Belge gönderiminde uçtan uca şifreleme.
* **Esneklik:** Excel entegrasyonu ve gelişmiş toplu işlem yetenekleri.

---

## 📸 Uygulama Görselleri
![Android+Emulator+-+Medium_Phone_API_36_5554+2025-12-09+10-44-04 (1)](https://github.com/user-attachments/assets/6cb936ba-8a75-4662-b86b-6d66bbda5a81)

