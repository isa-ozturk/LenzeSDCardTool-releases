<div align="center">

# Lenze SD Card Tool

**Lenze lisanslı cihazlar için SD kart yönetim aracı — temizleme, kontrol ve yapılandırma tek uygulamada.**

[![Release](https://img.shields.io/github/v/release/isa-ozturk/LenzeSDCardTool-releases?style=flat-square&color=blue)](https://github.com/isa-ozturk/LenzeSDCardTool-releases/releases/latest)
[![Platform](https://img.shields.io/badge/platform-Windows-lightgrey?style=flat-square)](https://github.com/isa-ozturk/LenzeSDCardTool-releases/releases/latest)
[![Latest Downloads](https://img.shields.io/github/downloads/isa-ozturk/LenzeSDCardTool-releases/latest/total?style=flat-square&color=blue&label=latest%20downloads)](https://github.com/isa-ozturk/LenzeSDCardTool-releases/releases/latest)
[![Total Downloads](https://img.shields.io/github/downloads/isa-ozturk/LenzeSDCardTool-releases/total?style=flat-square&color=green&label=total%20downloads)](https://github.com/isa-ozturk/LenzeSDCardTool-releases/releases)

[⬇️ Son Sürümü İndir](https://github.com/isa-ozturk/LenzeSDCardTool-releases/releases/latest)

</div>

---

## Nedir?

Lenze SD Card Tool, Lenze markalı PLC ve HMI cihazlarında kullanılan SD kartları yönetmek için geliştirilmiş bir Windows masaüstü uygulamasıdır.

Uygulama; SD kart temizleme, kart üzerindeki **kredi (lisans) durumunu kontrol etme**, **cihaz IP adresini değiştirme** ve karta yazılı projeler/reçeteler hakkında ayrıntılı bilgi alma gibi işlemleri tek bir arayüzde toplar. Hem **Yeni Jenerasyon** (Linux tabanlı, easyui / CODESYS — c5x0, c750, i950) hem de **Eski Jenerasyon** (Windows CE tabanlı, VisiWinNET — c300, p300, 3200C, p500) cihazlarla uyumludur.

Tek bir EXE dosyası olarak dağıtılır, kurulum gerektirmez, harici bağımlılığı yoktur.

---

## Özellikler

### Temizleme
- **Akıllı Temizleme** — Yalnızca SD kartları algılar, USB bellek gibi diğer çıkarılabilir sürücüleri yok sayar
- **Lisans Dosyası Koruması** — Lenze kredi/lisans dosyaları otomatik tespit edilip silme işleminin dışında tutulur
- **Paralel Silme Motoru** — Çoklu iş parçacığıyla hızlandırılmış dosya silme
- **Canlı İlerleme Takibi** — Gerçek zamanlı ilerleme çubuğu ve kalan süre tahmini
- **Otomatik Çıkartma** — İşlem sonrası kartı güvenle çıkartır *(opsiyonel)*
- **Temizlik Durumu Hafızası** — Kartın daha önce temizlenip temizlenmediğini hatırlar

### SD Kart Bilgi Görünümü
- **Otomatik Jenerasyon Tespiti** — Karta bakarak Yeni / Eski jenerasyon olarak işaretler
- **4 Sekmeli Detay Görünümü**:
  - **Genel** — Dosya sistemi, doluluk yüzdesi, kredi durumu, IP dosyaları
  - **Cihaz** — Cihaz modeli, firmware versiyonu, aktif IP yapılandırması, MAC adresi, seri numarası, CPU bilgisi
  - **Projeler** — Server / Client projeleri (yeni jenerasyon) veya VisiWinNET uygulamaları (eski jenerasyon)
  - **Reçeteler** — Kart genelinde bulunan tüm `.txtrecipe` dosyaları, klasörlere göre gruplanmış
- **Kredi Doğrulama** — Yeni / Eski jenerasyon için ayrı ayrı geçerlilik kontrolü; kredi miktarını lisans dosyasından otomatik okur

### IP Yapılandırması
- Cihaz IP adresini, subnet mask ve gateway değerlerini doğrudan SD kart üzerinden değiştirme
- IP geçerlilik kontrolü ve otomatik gateway hesaplama
- Önceki yapılandırma bilgisini (ip_old.txt) görüntüleme ve geri yükleme
- Hem Yeni hem Eski jenerasyon IP dosya formatlarını destekler

### Kullanıcı Deneyimi
- **Modern Arayüz** — Custom Windows 11 stili pencere chrome'u, drop shadow, yumuşak köşeler
- **Açık / Koyu Tema** — İki tema arasında anında geçiş
- **Çift Tıkla Aç** — Kart üzerinde çift tıklayarak Windows Gezgini'nde açma
- **Bağlam Menüsü** — Sağ tıkla hızlı eylemler (Aç, Bilgi, IP, Çıkar)
- **Otomatik Güncelleme** — Footer'daki tek tıkla GitHub üzerinden güncelleme kontrolü

---

## Sistem Gereksinimleri

| Gereksinim | Minimum |
|------------|---------|
| İşletim Sistemi | Windows 10 (64-bit) |
| .NET Framework | 4.7.2 veya üzeri |
| RAM | 50 MB |
| Disk | 10 MB |
| Bağlantı | İnternet (yalnızca güncelleme kontrolü için) |

---

## Kurulum

Lenze SD Card Tool kurulum gerektirmez.

1. [Releases](https://github.com/isa-ozturk/LenzeSDCardTool-releases/releases/latest) sayfasından `SDCardCleaner.exe` dosyasını indir
2. İstediğin bir klasöre koy
3. Çift tıklayarak çalıştır

İlk çalıştırmada Windows Defender veya SmartScreen uyarısı görebilirsin. **Daha fazla bilgi → Yine de çalıştır** seçeneğiyle devam edebilirsin.

---

## Kullanım

### Temizleme
1. SD kartı bilgisayara tak — uygulama otomatik olarak algılar
2. Listeden kartı seç
3. **Temizle** butonuna tıkla ve onay ver
4. İşlem tamamlandığında kart otomatik çıkartılır *(ayara bağlı)*

### Kart Bilgisi Görüntüleme
- Kart üzerinde **Info** butonuna ya da sağ tık menüsüne tıkla
- 4 sekmede karta dair tüm bilgiler: dosya sistemi, cihaz, projeler, reçeteler
- Kredi durumu ve lisans miktarı otomatik olarak hesaplanır

### IP Yapılandırması
- Kart üzerinde **IP** butonuna tıkla
- Yeni IP adresini gir; gateway otomatik hesaplanır
- Kaydet — yeni yapılandırma `ip.txt` olarak yazılır, kart cihaza takıldığında uygulanır

### Hızlı Erişim
- Kart üzerinde **çift tıkla** → Windows Gezgini'nde açılır
- Karta **sağ tıkla** → Bağlam menüsü (Aç, Info, IP, Çıkar)

> **Not:** Temizleme işlemi geri alınamaz. İşlem öncesinde önemli verilerinizi yedeklediğinizden emin olun.

---

## Desteklenen Cihazlar

| Jenerasyon | Platform | Cihazlar |
|------------|----------|----------|
| **Yeni Jenerasyon** | Linux / easyui / CODESYS | c5x0, c750, i950 |
| **Eski Jenerasyon** | Windows CE / VisiWinNET | c300, p300, 3200C, p500 |

---

## Otomatik Güncelleme

Uygulama başlangıçta yeni sürüm olup olmadığını kontrol eder. Footer'daki **Güncel mi?** butonuyla manuel kontrol de yapılabilir. Güncelleme varsa bir bildirim gösterilir; onay vermeniz hâlinde yeni sürüm indirilip otomatik olarak kurulur. Bu işlem sırasında uygulama kapanır ve yeni sürüm açılır.

---

## Sürüm Notları

Tüm sürüm değişiklikleri için [Releases](https://github.com/isa-ozturk/LenzeSDCardTool-releases/releases) sayfasını inceleyin.

---

## Lisans

Bu uygulama **Lenze** dahili kullanımı için geliştirilmiştir. Kaynak kodu kapalıdır.

---

<div align="center">
  <sub>Geliştiren: <a href="https://github.com/isa-ozturk">isa-ozturk</a> · Lenze için özel üretim</sub>
</div>
