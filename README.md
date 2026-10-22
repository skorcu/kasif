# Kâşif — macOS İçin Işık Hızında APFS Dosya & İçerik Arama Motoru ⚡

> **Milisaniyeler içinde 2.500.000+ dosya, WhatsApp mesajları, iMessage, Apple Mail, Outlook ve Telegram mesajları arasında arama yapın.**  
> Tamamen yerel, %100 gizli, offline ve Apple Silicon (M1/M2/M3/M4) ile Intel uyumlu (Universal 2).

<p align="center">
  <a href="https://caneser.com/downloads/Kasif.dmg">
    <img src="https://img.shields.io/badge/İndir-Kasif.dmg%20(v2.2.1)-blue?style=for-the-badge&logo=apple&logoColor=white" alt="Kâşif DMG İndir" />
  </a>
  <a href="https://caneser.com/kasif">
    <img src="https://img.shields.io/badge/Web%20Sitesi-caneser.com%2Fkasif-black?style=for-the-badge&logo=safari&logoColor=white" alt="Resmi Web Sitesi" />
  </a>
  <img src="https://img.shields.io/badge/Mimari-Universal%202%20(Apple%20Silicon%20%2B%20Intel)-emerald?style=for-the-badge" alt="Universal 2" />
  <img src="https://img.shields.io/badge/macOS-14.0%2B%20(Sonoma%20%26%20Sequoia)-purple?style=for-the-badge" alt="macOS 14+" />
</p>

<p align="center">
  <img src="https://caneser.com/images/kasif-preview.png" alt="Kâşif macOS Arama Motoru Arayüzü" width="100%" />
</p>

---

## 🚀 1 Dakikada Kolay Kurulum (DMG)

Kâşif son kullanıcılar için tek tıkla kurulabilecek şekilde paketlenmiştir:

1. **[Kasif.dmg İndir](https://caneser.com/downloads/Kasif.dmg)** bağlantısına tıklayarak en güncel sürümü bilgisayarınıza indirin.
2. İndirilen **`Kasif.dmg`** dosyasına çift tıklayın.
3. Açılan pencerede **Kâşif** uygulamasını **Uygulamalar (Applications)** klasörüne sürükleyip bırakın.
4. Uygulamalar'dan **Kâşif**'i açın.
5. Klavyenizden **`⌥ Boşluk` (Option + Space)** tuşlayarak dilediğiniz her an anında aramaya başlayın!

> **İpucu:** WhatsApp, iMessage, Mail ve sistem dosyaları gibi derin veri tabanlarında arama yapabilmesi için Kâşif ilk açılışta sizden *Tam Disk Erişimi (Full Disk Access)* onayı isteyecektir. Ayarlar > Gizlilik ve Güvenlik altından tek tıkla izin verebilirsiniz.

---

## ✨ Öne Çıkan Yetenekler

| Yetenek | Açıklama |
| :--- | :--- |
| ⚡ **APFS 0.001s Hız** | Apple APFS dosya sistemini doğrudan ve paralel bellek eşlemeli (mmap) mimariyle okuyarak Spotlight'tan 90 kat daha hızlı sonuç listeler. |
| 💬 **WhatsApp Derin Arama** | Bilgisayarınızdaki yerel WhatsApp SQLite veritabanını okur; kişi adları, sohbet geçmişi ve mesaj içeriklerinde anında arama yapar. |
| 💬 **iMessage & SMS** | macOS Mesajlar (`chat.db`) arşivini saniyeler içinde tarar; SMS doğrulama kodlarını ve eski mesajları anında bulur. |
| 📬 **Apple Mail & Outlook** | Hem yerel Apple Mail hem de Microsoft Outlook profillerindeki tüm e-postaları, konuları ve ekleri arar. |
| ✈️ **Telegram Arama** | Telegram masaüstü uygulamasının yerel verilerini çözümleyerek mesaj ve medya aramalarını listeler. |
| 👁️ **QuickLook Önizleme** | Bulduğunuz herhangi bir sonucun üzerindeyken **`Boşluk`** tuşuna basarak dosyayı veya mesajı açmadan tam ekran önizleyin. |
| 🔒 **%100 Yerel & Gizli** | Hiçbir veriniz, arama teriminiz veya dosya içeriğiniz internete aktarılmaz. Tamamen çevrimdışı çalışır. |
| 🍎 **Apple Universal 2** | M1, M2, M3, M4 serisi Apple Silicon ve tüm Intel tabanlı Mac modellerinde saf yerel makine kodunda çalışır. |

---

## 🥊 Neden Raycast veya Spotlight Değil? (Teknik Mimari)

Kâşif, Raycast veya Electron tabanlı araçlar gibi eklenti mağazası taşıyan hantal bir komut paleti (launcher) değildir. Doğrudan **macOS çekirdeğine bağlı, derin yerel arama motorudur**.

### Mimari Karşılaştırma Tablosu

| Metrik & Yetenek | 🧭 **Kâşif** | 🍎 **Spotlight** | ⚡ **Raycast** | 🎩 **Alfred** |
| :--- | :--- | :--- | :--- | :--- |
| **Mimari / Motor** | **Saf Swift & AppKit (Yerel)** | C++ & CoreServices | Node.js & Rust & Web | Objective-C |
| **İndirilen Paket Boyutu** | **2.7 MB** | macOS Dahili | 150+ MB | 18 MB |
| **RAM Bellek Tüketimi** | **~20 – 45 MB** | 800 MB+ (`mds`/`worker`) | 250 MB+ | 120 MB |
| **Arka Plan Pil Harcaması**| **%0.0 (Sıfır CPU)** | İndeks Sırasında Yüksek | Sürekli Aktif | Düşük |
| **WhatsApp, Telegram & SMS**| **Dahili (Yerel SQLite)** | Yalnızca iMessage | Yok | Yok |
| **Apple Mail & Outlook** | **Dahili (Envelope Index)** | Yüzeysel | Harici Eklentiyle | Harici Eklentiyle |
| **5M+ Dosya Arama Gecikmesi**| **0.001 – 0.003s** | 1.2 – 3.5s | 0.8 – 2.0s | 0.6 – 1.8s |
| **Harici SSD/HDD Desteği**| **Eksiksiz (APFS / HFS+)** | Sınırlı / Ağır | Eklentiye Bağlı | Özel İndeks |
| **Gizlilik & Çevrimdışı** | **%100 Çevrimdışı • Sıfır Takip**| Apple Sunucuları | Hesap & Telemetri | Yerel |

### 4 Temel Mühendislik Farkı:

1. **2.7 MB vs 150+ MB Şişkinlik (Sıfır Electron / Web):**  
   Raycast ve Electron araçları arkalarında devasa Chromium ve Node.js runtime taşırken, Kâşif **%100 saf Swift ve yerel AppKit** ile doğrudan metal seviyesinde derlenmiştir. 0.05 saniyede anında açılır.
2. **~20 MB RAM & Sıfır Pil Tüketimi (%0.0 CPU):**  
   Spotlight arka planda disk indekslerken fan açtırıp pili tüketir (`mds` servisi 800 MB+ RAM). Raycast arka planda sürekli 250 MB+ RAM rezerve eder. Kâşif beklemedeyken **%0.0 CPU** tüketir, pil ömrünüzü asla eksiltmez.
3. **Spotlight'ın Giremediği Derinlik (Yerel SQLite & CoreData):**  
   Raycast bir komut paletidir, Spotlight ise sadece yüzeysel dosya adlarını görür. Kâşif ise yerel SQLite ve Envelope Index motorlarına doğrudan bağlanarak WhatsApp, iMessage, SMS, Apple Mail, Outlook ve Telegram mesajlarını anında tarar.
4. **APFS Çekirdek Hızlandırması (`getattrlistbulk` & SIMD):**  
   Milyonlarca dosyayı taramak için arka planda sistemi yoran indeksleme servisleri kurmaz. Apple'ın doğrudan C API'si ile 5.000.000+ dosyayı 1 milisaniyede tarar; harici 8TB disklerde bile donma yaşatmaz.

---

## ⌨️ Klavye Kısayolları

- **`⌥ Boşluk` (Option + Space)**: Kâşif'i her yerden çağırır veya gizler.
- **`↑ / ↓`**: Sonuçlar arasında gezinir.
- **`Boşluk` (Space)**: Seçili dosya, mesaj veya e-posta için hızlı macOS QuickLook önizleme kartını açar.
- **`Enter`**: Dosyayı veya ilgili mesajı ait olduğu uygulamada açar.
- **`⌘ Enter`**: Dosyanın bulunduğu klasörü Finder'da gösterir.
- **`⌘ C`**: Seçili dosyanın tam yolunu panoya kopyalar.
- **`⌘ ,`**: Kâşif Ayarları penceresini açar (Disk filtreleri, dışlanan uzantılar, kısayol yönetimi).

---

## 👑 Lisans & Geliştirici

- **Geliştirici:** Can Eser
- **Web Sitesi:** [caneser.com](https://caneser.com) • [caneser.com/kasif](https://caneser.com/kasif)
- **E-Posta:** [info@caneser.com](mailto:info@caneser.com)
- **Telefon:** 0532 630 88 77

*Kâşif, Can Eser tarafından geliştirilmiş tescilli bir macOS masaüstü aracıdır. Tüm hakları saklıdır.*
