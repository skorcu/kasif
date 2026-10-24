# 🧭 Kâşif — macOS İçin Işık Hızında APFS Derin Dosya & İçerik Arama Motoru ⚡

<div align="center">
  <img src="https://caneser.com/images/kasif-logo.webp" width="128" height="128" alt="Kâşif Logo" />
  <br />
  <h2>Milisaniyeler İçinde 5.000.000+ Dosya, WhatsApp, Apple Mail, Outlook ve Telegram Arşivlerinde Arama</h2>
  <p><b>Apple Silicon (M1/M2/M3/M4) ve Intel (Universal 2) Mimarisiyle Sıfır Gecikmeli Arama Deneyimi</b></p>

  [![macOS](https://img.shields.io/badge/macOS-14.0%2B%20(Sonoma%20%26%20Sequoia)-black.svg?style=for-the-badge&logo=apple)](https://caneser.com/kasif)
  [![Apple Notarized](https://img.shields.io/badge/Apple%20Security-Resmi%20Noter%20Onaylı%20✓-10B981.svg?style=for-the-badge&logo=apple)](https://caneser.com/kasif)
  [![Architecture](https://img.shields.io/badge/Mimari-Universal%202%20(arm64%20%2B%20x86__64)-0284C7.svg?style=for-the-badge)](https://caneser.com/kasif)
  [![License](https://img.shields.io/badge/Lisans-Açık%20Kaynak%20•%20Hediye-8B5CF6.svg?style=for-the-badge)](https://caneser.com/kasif)
</div>

---

## 🌿 Sarkaç Adam'dan Mac Topluluğuna Bir Arama Hediyesi

> *"Zihinsel berraklık ve odaklanma için çalışma masanızda doğal kristalleri ve sükûneti ararken, Mac'inizde bir dosyayı veya önemli bir mesajı ararken vakit kaybetmenizi istemiyoruz.*  
> *Sarkaç Adam olarak; arka planda sisteminizi yoran hantal araçlara inat, doğrudan Apple APFS çekirdeğine bağlanan ve milisaniyeler içinde arama yapan **Kâşif**'i tüm Mac kullanıcılarına **karşılıksız bir hediye** olarak sunuyoruz.*  
> *Mac'iniz aradığınız her şeye anında ulaşırken, sizleri de çalışma alanınıza odaklanma ve dinginlik katacak doğal kristallerimizle tanışmaya davet ediyoruz."*

---

## ⚡ Neden Kâşif? (Mühendislik & Performans Farkı)

Geleneksel komut paletleri ve arama araçları genellikle yüzlerce megabaytlık Node.js / Web runtime'ları (Electron) taşır, arka planda 200 MB'tan fazla bellek bağlar ve devasa harici disklerde veya mesaj arşivlerinde indeksleme sancıları yaşatır.

**Kâşif**, doğrudan macOS çekirdeğine bağlı saf Swift ve AppKit ile inşa edilmiştir:
- **Resmi Apple Noter Onaylı (Apple Notarized):** Apple Developer ID (`P5GAL325ZG`) ile resmi noter onayından geçmiştir. Gatekeeper'dan pürüzsüzce açılır.
- **Sadece 2.7 MB Boyut:** Yüzlerce megabaytlık ağır frameworkler yerine saf yerel makine kodu.
- **~20 MB RAM & Sıfır Pil Tüketimi (%0.0 CPU):** Arka planda asla fan açtırmaz, pilinizi tüketmez.
- **APFS Çekirdek Hızlandırması (`getattrlistbulk` & mmap):** Apple'ın doğrudan C API'si ile 5.000.000+ dosyayı 1 milisaniyede tarar; harici 8TB SSD disklerde bile anında yanıt verir.

---

## 📊 Bağımsız Arama & Performans Karşılaştırması

*Test Ortamı: Apple M-Serisi Apple Silicon & APFS SSD • 2.500.000 Dosya & Mesaj Havuzu*

| Metrik & Standart | 🧭 **Kâşif (v2.2 Universal 2)** | 🍎 **Dahili Sistem Arama** | 📦 **Ağır Launcher Araçları** |
| :--- | :--- | :--- | :--- |
| **Uygulama Mimarisi** | **Saf Swift & AppKit (Yerel)** | C++ & CoreServices | Node.js / Rust / Webview |
| **İndirilen Paket Boyutu** | **2.7 MB** | Dahili | 120 MB – 180 MB |
| **Arka Plan RAM Tüketimi** | **~20 MB** | 600 MB+ (`mds`/`worker`) | 200 MB – 350 MB |
| **Arka Plan Pil Harcaması**| **%0.0 (Sıfır CPU)** | İndeks Sırasında Yüksek | Sürekli Aktif Servis |
| **5M+ Dosya Arama Gecikmesi**| **0.001 – 0.003s** | 1.2 – 3.5s | 0.8 – 2.0s |
| **WhatsApp, Telegram & SMS**| **Dahili (Yerel SQLite)** | Yalnızca iMessage | Yok / Karmaşık Eklenti |
| **Apple Mail & Outlook** | **Dahili (Envelope Index)** | Yüzeysel | Harici Eklentiyle |
| **Harici SSD/HDD Desteği**| **Eksiksiz (APFS / HFS+)** | Sınırlı / Ağır | Eklentiye Bağlı |
| **Gizlilik & Çevrimdışı** | **%100 Çevrimdışı • Sıfır Takip**| Harici Sunucu Sorguları | Hesap & Telemetri Takibi |

---

## ✨ Öne Çıkan Yetenekler

| Yetenek | Açıklama |
| :--- | :--- |
| ⚡ **APFS 0.001s Hız** | Apple APFS dosya sistemini doğrudan ve paralel bellek eşlemeli (mmap) mimariyle okuyarak ışık hızında sonuç listeler. |
| 💬 **WhatsApp Derin Arama** | Bilgisayarınızdaki yerel WhatsApp SQLite veritabanını okur; kişi adları, sohbet geçmişi ve mesaj içeriklerinde anında arama yapar. |
| 💬 **iMessage & SMS** | macOS Mesajlar (`chat.db`) arşivini saniyeler içinde tarar; SMS doğrulama kodlarını ve eski mesajları anında bulur. |
| 📬 **Apple Mail & Outlook** | Hem yerel Apple Mail hem de Microsoft Outlook profillerindeki tüm e-postaları, konuları ve ekleri tek çatı altında arar. |
| ✈️ **Telegram Arama** | Telegram masaüstü uygulamasının yerel verilerini çözümleyerek mesaj ve medya aramalarını listeler. |
| 👁️ **QuickLook Önizleme** | Bulduğunuz herhangi bir sonucun üzerindeyken **`Boşluk`** tuşuna basarak dosyayı veya mesajı açmadan tam ekran önizleyin. |
| 🔒 **%100 Yerel & Gizli** | Hiçbir veriniz, arama teriminiz veya dosya içeriğiniz internete aktarılmaz. Tamamen çevrimdışı çalışır. |
| 🍎 **Apple Universal 2** | M1, M2, M3, M4 serisi Apple Silicon ve tüm Intel tabanlı Mac modellerinde saf yerel makine kodunda çalışır. |

---

## ⌨️ Klavye Kısayolları

- **`⌥ Boşluk` (Option + Space)**: Kâşif'i her yerden çağırır veya gizler.
- **`↑ / ↓`**: Sonuçlar arasında gezinir.
- **`Boşluk` (Space)**: Seçili dosya, mesaj veya e-posta için hızlı macOS QuickLook önizleme kartını açar.
- **`Enter`**: Dosyayı veya ilgili mesajı ait olduğu uygulamada açar.
- **`⌘ Enter`**: Dosyanın bulunduğu klasörü Finder'da gösterir.
- **`⌘ C`**: Seçili dosyanın tam yolunu panoya kopyalar.
- **`⌘ ,`**: Kâşif Ayarları penceresini açar.

---

## 🚀 1 Dakikada Kolay Kurulum (DMG)

1. **[Kasif.dmg İndir](https://caneser.com/downloads/Kasif.dmg)** bağlantısından güncel sürümü bilgisayarınıza indirin.
2. DMG dosyasına çift tıklayın ve **Kâşif** uygulamasını **Uygulamalar (Applications)** klasörüne sürükleyin.
3. Klavyenizden **`⌥ Boşluk` (Option + Space)** tuşlayarak anında aramaya başlayın.

---

## 📄 Lisans & Teşekkür

Bu proje açık kaynak felsefesiyle sunulmaktadır.  
Tüm hakları ve marka tasarımı **Sarkaç Adam** ekosistemine aittir.  
Doğal kristal koleksiyonumuzu incelemek ve çalışma masanıza saf enerji katmak için [sarkacadam.com](https://sarkacadam.com) adresini ziyaret edebilirsiniz.
