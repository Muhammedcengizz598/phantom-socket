# 🔮 Phantom Socket Premium v2.0

<div align="center">

![Python Version](https://img.shields.io/badge/python-3.6%2B-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Platform](https://img.shields.io/badge/platform-Linux%20%7C%20Termux-lightgrey.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

**Gelişmiş Port Tarama ve Güvenlik Analiz Aracı**

[Özellikler](#-özellikler) • [Kurulum](#-kurulum) • [Kullanım](#-kullanım) • [Örnekler](#-kullanım-örnekleri) • [Uyarılar](#-önemli-uyarilar)

</div>

---

## 📋 İçindekiler

- [Hakkında](#-hakkında)
- [Özellikler](#-özellikler)
- [Sistem Gereksinimleri](#-sistem-gereksinimleri)
- [Kurulum](#-kurulum)
- [Kullanım](#-kullanım)
- [Kullanım Örnekleri](#-kullanım-örnekleri)
- [Tarama Tipleri](#-tarama-tipleri)
- [Önemli Uyarılar](#-önemli-uyarilar)
- [Yasal Sorumluluk](#-yasal-sorumluluk)
- [Katkıda Bulunma](#-katkıda-bulunma)
- [Lisans](#-lisans)
- [İletişim](#-iletişim)

---

## 🔍 Hakkında

**Phantom Socket Premium**, ağ güvenliği uzmanları ve sistem yöneticileri için geliştirilmiş profesyonel bir port tarama ve güvenlik analiz aracıdır. Gelişmiş özellikler ve detaylı raporlama yetenekleri ile sistemlerinizin güvenlik durumunu kapsamlı bir şekilde analiz etmenizi sağlar.

### 🎯 Amaç

Bu araç, **eğitim ve test amaçlı** olarak geliştirilmiştir. Sistem yöneticilerinin ve güvenlik araştırmacılarının kendi sistemlerini test etmelerine yardımcı olmak için tasarlanmıştır.

---

## ✨ Özellikler

### 🚀 Temel Özellikler

- **🔥 Hızlı Çoklu Thread Tarama**: 2000'e kadar eşzamanlı thread desteği
- **🎯 Gelişmiş Servis Tanıma**: 50+ yaygın servis için detaylı bilgi
- **🏷️ Banner Grabbing**: Servis versiyonu ve bilgi toplama
- **📊 Detaylı Risk Analizi**: Otomatik güvenlik risk değerlendirmesi
- **💾 JSON Export**: Tarama sonuçlarını JSON formatında kaydetme
- **🎨 Renkli Terminal Çıktısı**: Kolay okunabilir ve profesyonel görünüm

### 🔐 Güvenlik Özellikleri

- **Risk Seviyesi Belirleme**: Her port için risk değerlendirmesi (Düşük, Orta, Yüksek, Çok Yüksek)
- **Güvenlik Önerileri**: Port bazlı detaylı güvenlik tavsiyeleri
- **Kategori Bazlı Analiz**: Servisleri kategorilere ayırarak analiz
- **Kapsamlı Raporlama**: Detaylı güvenlik raporu oluşturma

### 📈 Tarama Modları

1. **Hızlı Tarama**: En yaygın 21 port
2. **Standart Tarama**: 1-1000 arası + kritik portlar
3. **Tam Tarama**: Tüm portlar (1-65535)
4. **Web Servisleri**: HTTP/HTTPS portları
5. **Veritabanı Servisleri**: Veritabanı portları
6. **Uzak Erişim**: RDP, SSH, VNC, Telnet portları

---

## 💻 Sistem Gereksinimleri

### Minimum Gereksinimler

- **İşletim Sistemi**: Linux, Termux (Android), macOS
- **Python**: 3.6 veya üzeri
- **RAM**: 512 MB (önerilen: 1 GB+)
- **İnternet Bağlantısı**: Gerekli

### Desteklenen Platformlar

| Platform | Durum | Notlar |
|----------|-------|--------|
| 🐧 Linux | ✅ Tam Destek | Ubuntu, Debian, Kali, Arch vb. |
| 📱 Termux | ✅ Tam Destek | Android cihazlar için |
| 🍎 macOS | ✅ Tam Destek | macOS 10.12+ |
| 🪟 Windows | ⚠️ Kısıtlı | WSL kullanımı önerilir |

---

## 📦 Kurulum

### Linux Kurulumu

```bash
# Depoyu klonlayın
git clone https://github.com/Muhammedcengizz598/phantom-socket.git
cd phantom-socket

# Gerekli paketleri yükleyin
pip3 install -r requirements.txt

# Çalıştırma izni verin
chmod +x phantom_socket.py

# Aracı çalıştırın
python3 phantom_socket.py
```

### Termux Kurulumu (Android)

```bash
# Termux'u güncelleyin
pkg update && pkg upgrade

# Python ve Git'i yükleyin
pkg install python git

# Depoyu klonlayın
git clone https://github.com/Muhammedcengizz598/phantom-socket.git
cd phantom-socket

# Gerekli paketleri yükleyin
pip install -r requirements.txt

# Aracı çalıştırın
python phantom_socket.py
```

### Manuel Kurulum

```bash
# Python 3'ün yüklü olduğundan emin olun
python3 --version

# Dosyayı indirin
wget https://raw.githubusercontent.com/Muhammedcengizz598/phantom-socket/main/phantom_socket.py

# Çalıştırın
python3 phantom_socket.py
```

---

## 🎮 Kullanım

### Temel Kullanım

```bash
python3 phantom_socket.py
```

Araç çalıştırıldığında sizden şu bilgileri isteyecektir:

1. **Hedef Domain/IP**: Taramak istediğiniz hedef (örn: example.com, 192.168.1.1)
2. **Tarama Tipi**: 1-6 arası seçim (varsayılan: Hızlı Tarama)
3. **Export Seçeneği**: Sonuçları JSON olarak kaydetmek ister misiniz? (e/h)
4. **Etik Kullanım Onayı**: Aracı sadece kendi sistemlerinizde kullandığınızı onaylayın

### Komut Satırı Parametreleri

```bash
# Doğrudan çalıştırma
python3 phantom_socket.py

# Arka planda çalıştırma (Linux)
nohup python3 phantom_socket.py &

# Screen ile çalıştırma
screen -S phantom python3 phantom_socket.py
```

---

## 📚 Kullanım Örnekleri

### Örnek 1: Hızlı Tarama

```bash
$ python3 phantom_socket.py

🎯 Hedef domain veya IP adresini girin: example.com

📋 Tarama tipini seçin:
1. Hızlı Tarama (Yaygın portlar)
Seçiminiz (1-6, varsayılan 1): 1

Sonuçları JSON dosyasına export etmek istiyor musunuz? (e/h): e

Bu aracı sadece kendi sistemlerinizde kullandığınızı onaylıyor musunuz? (e/h): e
```

### Örnek 2: Web Servisleri Taraması

```bash
$ python3 phantom_socket.py

🎯 Hedef domain veya IP adresini girin: 192.168.1.100

📋 Tarama tipini seçin:
4. Web Servisleri
Seçiminiz (1-6, varsayılan 1): 4

Sonuçları JSON dosyasına export etmek istiyor musunuz? (e/h): h

Bu aracı sadece kendi sistemlerinizde kullandığınızı onaylıyor musunuz? (e/h): e
```

### Örnek 3: Tam Port Taraması

```bash
$ python3 phantom_socket.py

🎯 Hedef domain veya IP adresini girin: localhost

📋 Tarama tipini seçin:
3. Tam Tarama (1-65535)
Seçiminiz (1-6, varsayılan 1): 3

Sonuçları JSON dosyasına export etmek istiyor musunuz? (e/h): e

Bu aracı sadece kendi sistemlerinizde kullandığınızı onaylıyor musunuz? (e/h): e
```

---

## 🎯 Tarama Tipleri

### 1️⃣ Hızlı Tarama (Quick Scan)

**Tarama Süresi**: ~10-30 saniye  
**Port Sayısı**: 21 port  
**Kullanım Alanı**: Hızlı güvenlik kontrolü

**Taranan Portlar**:
- Web: 80, 443, 8080
- FTP: 21
- SSH: 22
- Telnet: 23
- Email: 25, 110, 143, 993, 995
- DNS: 53
- Windows: 135, 139, 445
- Veritabanı: 1433, 3306, 5432, 6379, 27017
- Uzak Erişim: 3389, 5900

### 2️⃣ Standart Tarama (Common Scan)

**Tarama Süresi**: ~2-5 dakika  
**Port Sayısı**: 1000+ port  
**Kullanım Alanı**: Kapsamlı güvenlik analizi

### 3️⃣ Tam Tarama (Full Scan)

**Tarama Süresi**: ~10-30 dakika  
**Port Sayısı**: 65535 port  
**Kullanım Alanı**: Detaylı penetrasyon testi

### 4️⃣ Web Servisleri

**Tarama Süresi**: ~5-10 saniye  
**Port Sayısı**: 8 port  
**Kullanım Alanı**: Web sunucu güvenlik kontrolü

### 5️⃣ Veritabanı Servisleri

**Tarama Süresi**: ~5-10 saniye  
**Port Sayısı**: 7 port  
**Kullanım Alanı**: Veritabanı güvenlik kontrolü

### 6️⃣ Uzak Erişim Servisleri

**Tarama Süresi**: ~5-10 saniye  
**Port Sayısı**: 6 port  
**Kullanım Alanı**: Uzak erişim güvenlik kontrolü

---

## ⚠️ Önemli Uyarılar

### 🚨 Etik Kullanım

> **UYARI**: Bu araç yalnızca **eğitim ve test amaçlı** geliştirilmiştir.

#### ✅ İzin Verilen Kullanımlar

- ✔️ Kendi sistemlerinizi test etmek
- ✔️ İzin aldığınız sistemleri taramak
- ✔️ Laboratuvar ortamında eğitim amaçlı kullanım
- ✔️ Güvenlik araştırmaları (yasal çerçevede)
- ✔️ Penetrasyon testi (yazılı izinle)

#### ❌ Yasak Kullanımlar

- ❌ İzinsiz sistemleri taramak
- ❌ Kötü amaçlı kullanım
- ❌ Yasadışı aktiviteler
- ❌ Başkalarının sistemlerine zarar vermek
- ❌ Yetkisiz erişim denemesi

### 🔒 Güvenlik Notları

1. **VPN Kullanımı**: Kendi sistemlerinizi bile taramadan önce VPN kullanmanız önerilir
2. **İzin Belgesi**: Kurumsal sistemlerde mutlaka yazılı izin alın
3. **Log Kayıtları**: Tüm tarama aktivitelerinizi kayıt altına alın
4. **Sorumluluk**: Aracın kullanımından kaynaklanan tüm sorumluluk kullanıcıya aittir

### 📜 Yasal Uyarı

```
⚖️ YASAL SORUMLULUK REDDİ

Bu araç, bilgisayar ağlarının güvenliğini test etmek ve eğitim amaçlı 
kullanılmak üzere geliştirilmiştir. Aracın kullanımından doğabilecek 
her türlü yasal sorumluluk kullanıcıya aittir.

Geliştiriciler (Muhammed Cengiz ve katkıda bulunanlar), bu aracın 
yanlış kullanımından, yasadışı aktivitelerden veya herhangi bir 
zarardan sorumlu tutulamaz.

Aracı kullanarak, yalnızca yasal ve etik çerçevede kullanacağınızı 
kabul etmiş olursunuz.
```

---

## 📊 Çıktı Formatları

### Terminal Çıktısı

Araç, renkli ve detaylı terminal çıktısı sağlar:

- 🟢 **Yeşil**: Başarılı işlemler ve düşük riskli portlar
- 🟡 **Sarı**: Uyarılar ve orta riskli portlar
- 🟠 **Turuncu**: Yüksek riskli portlar
- 🔴 **Kırmızı**: Kritik riskli portlar ve hatalar
- 🔵 **Mavi**: Bilgilendirme mesajları

### JSON Export

Tarama sonuçları JSON formatında kaydedilebilir:

```json
{
  "scan_info": {
    "target": "example.com",
    "scan_time": "2024-01-15T10:30:00",
    "duration": 45.23,
    "total_ports_scanned": 1021
  },
  "results": {
    "open_ports": 5,
    "closed_ports": 1015,
    "filtered_ports": 1
  },
  "detailed_results": {
    "80": {
      "port": 80,
      "status": "open",
      "service": "HTTP",
      "risk": "ORTA",
      "banner": "Apache/2.4.41"
    }
  }
}
```

---

## 🛠️ Sorun Giderme

### Yaygın Hatalar ve Çözümleri

#### Hata: "Permission Denied"

```bash
# Çözüm: Root yetkisi ile çalıştırın
sudo python3 phantom_socket.py
```

#### Hata: "Module not found"

```bash
# Çözüm: Gereksinimleri yeniden yükleyin
pip3 install -r requirements.txt --upgrade
```

#### Hata: "Connection timeout"

```bash
# Çözüm: Timeout süresini artırın veya daha az thread kullanın
# Kod içinde socket.settimeout() değerini artırın
```

#### Hata: "Too many open files"

```bash
# Linux için çözüm:
ulimit -n 4096

# Termux için çözüm:
# Thread sayısını azaltın (kod içinde max_threads değerini düşürün)
```

---

## 🤝 Katkıda Bulunma

Projeye katkıda bulunmak isterseniz:

1. Projeyi fork edin
2. Yeni bir branch oluşturun (`git checkout -b feature/yeniOzellik`)
3. Değişikliklerinizi commit edin (`git commit -am 'Yeni özellik eklendi'`)
4. Branch'inizi push edin (`git push origin feature/yeniOzellik`)
5. Pull Request oluşturun

### Katkı Kuralları

- ✅ Temiz ve okunabilir kod yazın
- ✅ Yorum satırları ekleyin
- ✅ Test edin
- ✅ Dokümantasyon güncelleyin
- ✅ Etik kullanım prensiplerine uyun

---

## 📝 Değişiklik Geçmişi

### v2.0 (Mevcut)
- ✨ Gelişmiş servis tanıma sistemi
- ✨ Banner grabbing özelliği
- ✨ JSON export desteği
- ✨ Risk analizi ve güvenlik önerileri
- ✨ Kategori bazlı port analizi
- ✨ Çoklu tarama modu
- 🐛 Performans iyileştirmeleri

### v1.0
- 🎉 İlk sürüm
- ⚡ Temel port tarama
- 🎨 Renkli terminal çıktısı

---

## 📄 Lisans

Bu proje MIT Lisansı altında lisanslanmıştır. Detaylar için [LICENSE](LICENSE) dosyasına bakın.

```
MIT License

Copyright (c) 2024 Muhammed Cengiz

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 👨‍💻 Geliştirici

**Muhammed Cengiz**

- 🌐 GitHub: [@Muhammedcengizz598](https://github.com/Muhammedcengizz598)
- 📧 E-posta: [İletişim için GitHub profilini ziyaret edin]
- 💼 LinkedIn: [Profil bağlantınız]

---

## 🌟 Teşekkürler

Bu projeyi kullandığınız için teşekkür ederiz! Eğer faydalı bulduysanız:

- ⭐ Projeye yıldız verin
- 🐛 Hata bildirin
- 💡 Önerilerde bulunun
- 🤝 Katkıda bulunun

---

## 📞 İletişim ve Destek

### Destek Kanalları

- 🐛 **Hata Bildirimi**: [GitHub Issues](https://github.com/Muhammedcengizz598/phantom-socket/issues)
- 💬 **Tartışmalar**: [GitHub Discussions](https://github.com/Muhammedcengizz598/phantom-socket/discussions)
- 📧 **E-posta**: GitHub profili üzerinden ulaşın

### Sık Sorulan Sorular (SSS)

**S: Bu araç yasal mı?**  
C: Evet, kendi sistemlerinizde veya izin aldığınız sistemlerde kullanmak yasaldır.

**S: Termux'ta çalışır mı?**  
C: Evet, Termux'ta sorunsuz çalışır. Kurulum talimatlarını takip edin.

**S: Root yetkisi gerekli mi?**  
C: Bazı portları taramak için root yetkisi gerekebilir.

**S: Kaç port tarayabilirim?**  
C: Tam tarama modunda 65535 porta kadar tarama yapabilirsiniz.

**S: Sonuçları nasıl kaydedebilirim?**  
C: JSON export özelliğini kullanarak sonuçları kaydedebilirsiniz.

---

## 🔗 Faydalı Bağlantılar

- 📚 [Python Dokümantasyonu](https://docs.python.org/3/)
- 🔒 [OWASP Port Scanning](https://owasp.org/www-community/vulnerabilities/Port_scanning)
- 🛡️ [Nmap Referansı](https://nmap.org/book/man.html)
- 📖 [Siber Güvenlik Kaynakları](https://www.cybrary.it/)

---

<div align="center">

### 🌟 Projeyi Beğendiyseniz Yıldız Vermeyi Unutmayın! 🌟

**Phantom Socket Premium v2.0**

*Güvenli taramalar dileriz!* 🔐

---

**© 2024 Muhammed Cengiz | Tüm Hakları Saklıdır**

*Bu araç eğitim amaçlıdır. Sorumlu ve etik kullanın.*

</div>
