# Casper M500  | Intel i5 (9. Nesil)

[![macOS](https://img.shields.io/badge/macOS-11.1-orange)](https://www.apple.com/tr/macos/big-sur/)
[![OpenCore](https://img.shields.io/badge/OpenCore-0.6.5-9cf)](https://github.com/acidanthera/OpenCorePkg)
[![release](https://img.shields.io/badge/indir-son%20sürüm-blue.svg)](https://github.com/sutsurup/CASPER-M500-Hackintosh/releases)

<img align="right" src="Images/casper.png" alt="Casper">

Türkçe | [English](https://github.com/sutsurup/ASUS-K555UB-Hackintosh/blob/master/README_EN.md)

**macOS Versiyonu: 11.1**

**OpenCore Versiyonu: 0.6.5**

Yardımcı olabilecek kaynaklar: 

- [OpenCore Yükleme Rehberi](https://dortania.github.io/OpenCore-Install-Guide)


# Detaylar

    Tarih:        Ocak 20, 2021
    Durum:        Stabil
    Destek:       BIOS (5.12)
    Yapı:         OpenCore

![](Images/Hackintosh.png)

## Donanım

| **CASPER** | Detay                                                  |
| ------------------- | ------------------------------------------- |
| Model Ismi      | Casper M500      |
| Anakart           | 	Intel Kaby Point H310C     |
| CPU              | Intel(R) Core(TM) i5-9400 CPU @ 2.90GHz (max. 4.10GHz) Coffee Lake-S              |
| RAM           | Kingston 4GB+4GB (9905713-019.A00G) 2666 MHz DDR4 SDRAM   |
| Dahili Grafik Kartı | Intel(R) UHD Graphics 630 (1 GB)                     |
| Ses       | Realtek ALC662 (Layout: 13)                        |
| BIOS Versiyonu      | 5.12                   |

![](Screenshots/info.png)

## Uyumluluk
**macOS Big Sur 11.1** sürümünü desteklemektedir.
Releases bölümünde EFI klasörü için zip dosyası paylaştım. macOS kurulum belleğinizdeki EFI için ayrılan disk bölümünde, EFI adında bir klasör oluşturun ve zip içerisindeki BOOT ve OC klasörlerini EFI klasörü içerisine kopyalayınız.
macOS High Sierra 10.13.6, Mojave 10.14.6 veya Catalina 10.15.7 sürümlerinde çalıştırmayı deneyebilirsiniz

### Çalışıyor

- [x] Uyku
- [x] Ethernet (Yama yapıldı)
- [x] Ses (Layout: 13)

### Çalışmıyor (henüz)
- [ ] Ekran parlaklığı

![](Screenshots/update.png)

# Kurulum sonrası yararlanabileğiniz rehber/araçlar (Isteğe bağlı)
* önerilir: iCloud'a giriş yapacaksanız veya iMessage, FaceTime kullanmak istiyorsanız, bu rehberi harfiyen uygulayın: [OpenCore ile iMessage ve Apple Servislerini Aktif Etmek](https://osxinfo.net/konu/opencore-ile-imessage-ve-apple-servislerini-aktif-etmek.16297/) (Bu rehberde Clover Configurator gösterilmiş, siz OpenCore Configurator kullanacaksınız, Clover Configurator üzerinden takip edin, verileri OpenCore Configurator aracılığıyla config.plist dosyanıza girin)
* [ProperTree](https://osxinfo.net/konu/propertree-opencore-bootloader-icin-config-duzenleyici.12919/) (config.plist düzenlemek için)
* Hackintool ([Forum thread](https://www.insanelymac.com/forum/topic/335018-hackintool-v286/) | [Direkt indirme linki](http://headsoft.com.au/download/mac/Hackintool.zip)) (Detaylı sistem bilgileri öğrenme ve düzenlemeleri için)
* Hackintool ([Indir](https://github.com/headkaze/Hackintool/releases/tag/3.5.3)

## Dual Boot
Bu cihazı sadece iş amaçlı kullandığımdan dolayı Dual Boot yani hem macOS, hem de Windows olması gerekiyordu. Maalesef macOS Catalina ile birlikte kullanılan dosya sistemi (Apple HFS) tamamen değişti ve APFS formatına geçti (Windows'taki FAT32 ve NTFS gibi düşünebiliriz). Bu sebeple artık Windows kurduktan sonra macOS kurmak mümkün değil. En azından Catalina ve Big Sur için. Windows'unuz kurulu ve macOS kullanmak istiyorsanız, Sierra - High Sierra ve Mojave gibi alt sürümleri tercih edebilirsiniz.

Peki Big Sur'da nasıl Dual Boot yapacağız? Pek sağlıklı bir yöntem olmasa da bir zararını görmediğim bir yöntemle. Bu yöntemi kullanabilmek için macOS Big Sur'u öncelikli olarak depolama birimine (HDD - SSD) yüklemeniz gerekiyor. macOS'i yüklerken kurulum ekranında Windows için kullanacağınız alanı FAT formatını seçerek ayırın. Ben bu sistemde 100 GB ayırdım, ekran görüntüsünün alt kısmında görünüyor. Sonrasında macOS'i diğer APFS olarak formatladığınız diske normal bir şekilde kurun.

macOS kurulumu bittikten sonra, Windows kurulumunu başlatın ve disk bölümüne kadar gelin. Ben 100GB olarak ayırmıştım, dolasıyla bundan sonraki yazımda "100GB Windows diski" olarak telaffuz edeceğim. 100GB ayırdığımız FAT diski, Windows format ekranı (ÖZEL - disk bölümünde) gözüküyor fakat FAT formatlı disklere Windows 10 kurulamıyor! Bu sebeple 100GB ayırdığımız diskimizi "Sil" diyoruz ve siliyoruz. Şimdi boş alan 100GB olarak gözüküyor ve buraya kurulumu yapabiliriz. Kurulum sırasında Windows, kendine özgü boot dosyalarını depolama biriminize yükleyecektir. Bu kadar!

Not: Bu işlemi yaptıktan sonra macOS'i 11.0.1 sürümünden 11.1 sürümüne güncelledim, başarılı oldu.

## İletişime geçin
Herhangi bir adımda sorun yaşıyorsanız, öncelikli olarak [issue](https://github.com/sutsurup/CASPER-M500-Hackintosh/issues) bölümüne destek talebi açın! Diğer soru ve talepleriniz için; Website: https://sutsurup.com // Mail: [contact@sutsurup.com](contact@sutsurup.com)

## Ekran Görüntüleri
![](Screenshots/BigSur.png)

</details>

## Destek olun.
Projeyi faydalı bulduysanız, kaynak bulma konusunda bana yardımcı olmak için bağış yapabilirsiniz:
```
₿ 1Q8CEMHTuecxPUJpEdpRiG6Bg2GVtzw4bN
Papara ➜ 1801475764
``` 
<a href='https://github.com/sutsurup/sutsurup/blob/main/Donate.md'><img alt='Bağış' src='https://github.com/sutsurup/MSI-Hackintosh-Build/blob/main/Images/donate.png?raw=true' height='360px' width='375px'/></a>
```
QR kodu tarayarak alternatif seçeneklere ulaşabilirsiniz
``` 

Kolay gelsin!
