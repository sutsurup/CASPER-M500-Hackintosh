# Casper M500  | Intel i5 (9. Nesil)

[![macOS](https://img.shields.io/badge/macOS-11.1-orange)](https://www.apple.com/tr/macos/big-sur/)
[![OpenCore](https://img.shields.io/badge/OpenCore-0.6.5-9cf)](https://github.com/acidanthera/OpenCorePkg)
[![release](https://img.shields.io/badge/indir-son%20sürüm-blue.svg)](https://github.com/sutsurup/CASPER-M500-Hackintosh/releases)

<img align="right" src="Images/casper.png" alt="Casper">

Türkçe | [English](README_EN.md)

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
| Model İsmi      | Casper M500      |
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

# Kurulum sonrası yararlanabileceğiniz rehber/araçlar (İsteğe bağlı)
* Önerilir: iCloud'a giriş yapacaksanız veya iMessage, FaceTime kullanmak istiyorsanız, bu rehberi harfiyen uygulayın: [OpenCore ile iMessage ve Apple Servislerini Aktif Etmek](https://osxinfo.net/konu/opencore-ile-imessage-ve-apple-servislerini-aktif-etmek.16297/). (Bu rehberde Clover Configurator gösterilmiş; siz OpenCore Configurator kullanacaksınız. Clover Configurator üzerinden takip edip verileri OpenCore Configurator aracılığıyla `config.plist` dosyanıza girin.)
* [ProperTree](https://osxinfo.net/konu/propertree-opencore-bootloader-icin-config-duzenleyici.12919/) (config.plist düzenlemek için)
* Hackintool ([Forum thread](https://www.insanelymac.com/forum/topic/335018-hackintool-v286/) | [Direct download link](http://headsoft.com.au/download/mac/Hackintool.zip)) (Detaylı sistem bilgileri öğrenme ve düzenlemeleri için)
* Hackintool ([İndir](https://github.com/headkaze/Hackintool/releases/tag/3.5.3))

## Dual Boot
Bu cihazı sadece iş amaçlı kullandığımdan dolayı Dual Boot (hem macOS hem Windows) yapmam gerekiyordu. Catalina ile birlikte Apple'ın dosya sistemi HFS'den APFS'ye geçti (Windows'taki FAT32/NTFS benzeri). Bu nedenle Catalina ve Big Sur için, Windows kurduktan sonra macOS kurmak genellikle mümkün olmuyor. Eğer zaten Windows kuruluysa ve macOS kullanmak istiyorsanız, daha eski sürümler (Sierra / High Sierra / Mojave) tercih edilebilir.

Big Sur için kullandığım yöntem şu şekildedir (tamamen zararsız olduğunu gözlemledim ama ideal bir yöntem değildir):

1. macOS Big Sur'u depolama birimine (HDD/SSD) öncelikli olarak yükleyin.
2. Kurulum sırasında, Windows için ayıracağınız alanı FAT formatında oluşturun. (Ben örnek olarak 100 GB ayırdım — ekran görüntüsünde bu görünür.)
3. Geri kalan diski APFS olarak formatlayıp macOS'u normal şekilde kurun.
4. macOS kurulumu tamamlandıktan sonra Windows kurulumunu başlatın ve disk bölümleme ekranına gelin. Daha önce ayırdığınız 100 GB'lık FAT bölüm görünür olacaktır.
5. Windows 10 FAT formatlı bir bölüme kurulamaz; bu nedenle o 100 GB'lık bölümü "Sil" yaparak boş alan haline getirin.
6. Boş alan (100 GB) gözükecektir; Windows'u bu boş alana kurun. Kurulum sırasında Windows, kendi boot dosyalarını depolama birimine yazacaktır.

Not: Bu işlemi tamamladıktan sonra macOS'u 11.0.1'den 11.1'e başarılı şekilde güncelledim.

## İletişime geçin
Herhangi bir adımda sorun yaşıyorsanız, öncelikli olarak [issue](https://github.com/sutsurup/CASPER-M500-Hackintosh/issues) bölümüne destek talebi açın. Diğer soru ve talepleriniz için: Website: https://sutsurup.tr // Mail: [veysel@sutsurup.tr](mailto:veysel@sutsurup.tr)

## Ekran Görüntüleri
![](Screenshots/BigSur.png)

</details>

## Destek olun.
Projeyi faydalı bulduysanız, kaynak bulma konusunda bana yardımcı olmak için bağış yapabilirsiniz:
```
₿ 1Q8CEMHTuecxPUJpEdpRiG6Bg2GVtzw4bN
``` 
<a href='https://github.com/sutsurup/sutsurup/blob/main/Donate.md'><img alt='Bağış' src='https://github.com/sutsurup/MSI-Hackintosh-Build/blob/main/Images/donate.png?raw=true' height='360px' width='375px'/></a>
```
QR koda tıklayarak alternatif seçeneklere ulaşabilirsiniz
``` 

Kolay gelsin!
