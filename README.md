# 🧭 Kâşif — macOS İçin Işık Hızında APFS Derin Dosya & İçerik Arama Motoru ⚡

<div align="center">
  <img src="https://caneser.com/images/kasif-logo.webp" width="128" height="128" alt="Kâşif Logo" />
  <br />
  <h2>Milisaniyeler İçinde 5.000.000+ Dosya, WhatsApp, Apple Mail, Outlook ve Telegram Arşivlerinde Arama</h2>
  <p><b>Apple Silicon (M1/M2/M3/M4) ve Intel (Universal 2) Mimarisiyle Sıfır Gecikmeli Arama Deneyimi</b></p>

  [![macOS](https://img.shields.io/badge/macOS-14.0%2B%20(Sonoma%20%26%20Sequoia)-black.svg?style=for-the-badge&logo=apple)](https://caneser.com/kasif)
  [![Apple Notarized](https://img.shields.io/badge/Apple%20Security-Resmi%20Noter%20Onaylı%20✓-10B981.svg?style=for-the-badge&logo=apple)](https://caneser.com/kasif)
  [![Architecture](https://img.shields.io/badge/Mimari-Universal%202%20(arm64%20%2B%20x86__64)-0284C7.svg?style=for-the-badge)](https://caneser.com/kasif)
  [![Companion](https://img.shields.io/badge/Kardeş%20Uygulama-İhyâ%20(Mac%20Arınma)-10B981.svg?style=for-the-badge&logo=apple)](https://github.com/skorcu/ihya)
  [![License](https://img.shields.io/badge/Lisans-Sarkaç%20Adam%20Özel%20•%20Freeware%20Hediye-8B5CF6.svg?style=for-the-badge)](https://caneser.com/kasif)
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

| Metrik & Standart | 🧭 **Kâşif (v2.5.2 Universal 2)** | 🍎 **Dahili Sistem Arama** | 📦 **Ağır Launcher Araçları** |
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

## ✨ Sürüm Geçmişi & Yenilikler (Changelog)

### [v2.5.2] — 24 Ekim 2026 (Apple Noter Onaylı Güncel Sürüm)
- **15 Günlük Ücretsiz Pro Deneme Mimarisi:** İlk çalıştırmada başlayan ve macOS Keychain ile korunan 15 günlük tam Pro deneme motoru entegre edildi.
- **Canlı Sayaç & Hile Koruması:** Arayüzde kalan gün sayacı ve sistem saatinin geriye alınmasını engelleyen anti-tampering koruması devreye alındı.
- **Doğal Pencere Yönetimi:** Standart seviye pencere ile alttaki uygulamalara tıklandığında doğal arkaya düşme, Option+Space ile anında öne gelme sağlandı.
- **Video & PDF Küçük Resimleri:** Liste satırlarında AVFoundation ve QLThumbnailGenerator ile gerçek kare önizlemeleri ve QuickLook desteği getirildi.

### [v2.5.1] — 24 Ekim 2026
- **Sıfır Kayma ve Tek Satır Kuralı:** Sıralama butonlarında ("Ad A-Z") oluşan metin kırılması ve yükseklik bozulması giderildi; butonlar tek satır ("A-Z"), sabit 24px yükseklik ve taşma korumasıyla kilitlendi.
- **Dinamik Responsive Pencere:** Hardcoded sabit boyut yerine ekran çözünürlüğüne (MacBook 13"/14"/16", iMac, harici geniş ekran) göre otomatik ölçeklenen altın oranlı responsive pencere açılışı kuruldu.
- **Doğal macOS Pencere Yönetimi:** Pencere seviyesi standart (`.normal`) seviyeye alındı; alttaki veya arkadaki bir uygulamaya tıklandığında Kâşif doğal olarak arkaya düşer, `Option + Space` kısayoluna basıldığında anında en öne çağrılır.
- **Video ve PDF Küçük Resim Önizlemeleri:** Apple `AVFoundation` (`AVAssetImageGenerator`) ve `QLThumbnailGenerator` motoru ile liste satırlarında video (`.mp4`, `.mov`, `.3gp`, `.mkv`) ve PDF dosyaları için gerçek kare önizlemeleri aktifleştirildi.
- **Anında QuickLook Önizleme:** Satırdaki "Önizle" butonuna tıklandığında veya klavyeden `Space` tuşuna basıldığında yerel macOS QuickLook penceresi anında açılır.
- **Kalıcı Sağ Önizleme Paneli:** Önizleme paneli tercihi `@AppStorage` ile kalıcı yapıldı; ilk aramada ilk sonuç otomatik seçilerek detay kartının anında dolu gelmesi sağlandı.

### [v2.5.0] — 24 Ekim 2026
- **Sıfır Sürtünmeli Onboarding:** İlk çalıştırmada interaktif adım adım izin ve hızlı başlangıç rehberi.
- **Kalıcı Tam Disk Erişimi (FDA):** Güvenlik izinleri güncellemeler sonrasında kalıcı olarak korunur.
- **Özelleştirilebilir Global Kısayol:** Ayarlar ekranından Option+Space veya istenen tuş kombinasyonuyla anında eşleme.

### [v2.4.9] — 24 Ekim 2026
- **Apple HIG Squircle İkon:** macOS HIG standartlarında tam boy squircle ikon entegrasyonu; Launchpad ve Finder'da oluşan beyaz çerçeve ve boşluklar kalıcı olarak giderildi.

---

## 🤝 Kusursuz İkili: İhyâ ile Mac'inizi Arındırın & Hafifletin 💎

Kâşif ile aradığınız her şeye milisaniyeler içinde ulaşırken, Mac'inizin de ilk günkü saf hızına, ferahlığına ve temizliğine kavuşmasını ister misiniz?

Kâşif'in kardeş uygulaması olan **[İhyâ (Mac)](https://github.com/skorcu/ihya)**; arka planda sistemi yoran hantal temizleyicilere, gizli telemetri takibine ve aylık abonelik tuzaklarına son veren yeni nesil bir **macOS Arınma & Canlanma Motorudur**.

- 🧹 **Akıllı Arınma (Smart Clean):** Xcode, Node, Docker derleme çöplerini, sistem artıklarını ve gizli önbellekleri tek dokunuşla temizler.
- ⚡ **Başlangıç & Arka Plan Yöneticisi:** Mac açılışını yavaşlatan gereksiz servisleri ve silinmiş program kalıntılarını anında süpürür.
- 🧠 **Canlı Bellek Röntgeni:** Darwin VM baskı döngüsüyle root yetkisi gerektirmeden RAM'i anında ferahlatır.
- 🔍 **Çift Dosya Avcısı:** 3 aşamalı SHA-256 algoritmasıyla mükerrer dosyaları güvenle temizler.
- 🍎 **Saf Yerel Mimari:** Yalnızca 2.8 MB boyut, beklemede 0.0 MB RAM harcaması ve Apple Silicon M1-M4 tam desteği.

👉 **[İhyâ'yı GitHub'da İnceleyin & İndirin ➔](https://github.com/skorcu/ihya)**

---

## 📄 Lisans & Güvenlik

Kâşif, **Sarkaç Adam** tarafından Mac ekosistemine özel olarak geliştirilmiş kapalı kaynaklı (özel mülkiyet / proprietary), resmi Apple Noter güvenlik onaylı ve ömür boyu hediyeli bir arama motorudur.  
Tüm fikrî mülkiyet, kaynak kodları ve marka hakları **Sarkaç Adam** ekosistemine aittir.  
Doğal kristal koleksiyonumuzu incelemek ve çalışma masanıza saf enerji katmak için [sarkacadam.com](https://sarkacadam.com) adresini ziyaret edebilirsiniz.
