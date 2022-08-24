---
title: Kanala göre otomatik masrafları etkinleştirme ve yapılandırma
description: Bu makale, Microsoft Dynamics 365 Commerce'ta otomatik masrafların kanala göre nasıl etkinleştirileceğini ve yapılandırılacağını açıklamaktadır.
author: gvrmohanreddy
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 079d2bc1a5edb499181ecd69fa6448b672decbdf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275744"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a>Kanala göre otomatik masrafları etkinleştirme ve yapılandırma

Bu makale, Microsoft Dynamics 365 Commerce'ta otomatik masrafların (oto masraflar) kanala göre nasıl etkinleştirileceğini ve yapılandırılacağını açıklamaktadır.

## <a name="overview"></a>Özet

Belirli bir eyaletteki tüm veya bazı mağazalarda satılan bir ürün grubuna geri dönüşüm ücretleri veya başka ücretlerin uygulanması gereken senaryolarınız olabilir (örneğin, California). Commerce'taki **Kanala göre otomatik masrafları filtrelemeyi etkinleştirme** özelliği, kanala göre otomatik masrafları belirtmenize olanak sağlar (örneğin, belirli bir fiziksel mağaza kanalı). Bu özellik Dynamics 365 Commerce 10.0.10 sürümü ve sonrasında bulunur.

Otomatik masrafları kanal bazında etkinleştirmek ve yapılandırmak için aşağıdaki görevleri tamamlamanız gerekir:

- **Kanal bazında otomatik masrafları filtrelemeyi etkinleştir** özelliğini açın.
- Kuruluş hiyerarşisi amacını yapılandırın.
- Kanala göre otomatik masrafları tanımlayın.

> [!NOTE]
> **Kanala göre otomatik masrafları filtrelemeyi etkinleştirme** özelliği yalnızca gelişmiş otomatik masraflar özelliği açıksa çalışır. Gelişmiş otomatik masrafları özelliğini etkinleştirme hakkında bilgi için bkz. [Çok yönlü kanal gelişmiş otomatik masrafları](omni-auto-charges.md).

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a>Kanala göre otomatik masrafları filtrelemeyi etkinleştir özelliğini açın

Otomatik masrafları Commerce'ta kanala göre etkinleştirmek için aşağıdaki adımları izleyin.

1. **Sistem Yönetimi \> Çalışma alanları \> Özellik yönetimi** seçeneğine gidin.
1. **Etkin değil** sekmesinde **Özellik adı** listesinde, **Kanala göre otomatik masraf filtrelemeyi etkinleştir**'i bulun ve seçin.
1. Sağ alt köşede, **Şimdi etkinleştir**'i seçin. Özellik etkinleştirildikten sonra, **Tümü** sekmesindeki listede görünür.
1. **Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.
1. Sol bölmede **1110** (**Global yapılandırma**) işini bulun ve seçin.
1. Eylem Bölmesinde, yapılandırma değişikliklerini yaymak için **Şimdi çalıştır**'ı seçin.

> [!WARNING]
> Daha önce kullandıktan sonra **Kanala göre otomatik masraf filtrelemeyi etkinleştir** özelliğini kapatırsanız, **Otomatik masraflar** altındaki **Perakende kanalı ilişkisi** artık görünmez ve varolan tüm yapılandırmalarla ilgili değişiklikleri kaybedersiniz. **Perakende kanalı ilişkisi** yapılandırmalarının kaldırılması otomatik masraf kurallarının yinelenmesine neden olacaksa, özelliği kapatma girişimi başarısız olacaktır. Özelliği kapatmadan önce tüm otomatik masraf kurallarını gözden geçirmeyi ve gerekli değişiklikleri yapmayı unutmayın.

## <a name="configure-the-organization-hierarchy-purpose"></a>Kuruluş hiyerarşisi amacını yapılandırın

Kanala göre otomatik masraflar için hiyerarşiyi yönetmek **Perakende otomatik masraf** adlı yeni bir kuruluş hiyerarşisi amacı oluşturulur.

Commerce'ta bir kuruluş hiyerarşisi amacına varsayılan bir hiyerarşi atamak için aşağıdaki adımları izleyin.
        
1. **Kuruluş yönetimi \> Kuruluşlar \> Kuruluş hiyerarşisi amaçları**'na gidin.
1. Sol bölmede, **Perakende otomatik masraf**'ı seçin.
1. **Atanan hiyerarşiler** altında **Ekle**'yi seçin.
1. **Kuruluş hiyerarşileri** iletişim kutusunda bir kuruluş hiyerarşisi seçin (örneğin, **Bölgeye göre Perakende Mağazalar**) ve sonra **Tamam**'ı seçin.
1. **Atanan hiyerarşiler** altında **Varsayılan olarak ayarla**'yı seçin.
1. **Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.
1. Sol bölmede **1040** (**Ürünler**) işini bulun ve seçin.
1. Eylem Bölmesinde **Şimdi çalıştır**'ı seçin.
1. **1070** **(Kanal yapılandırması**) ve **1110** (**Genel yapılandırma**) işlerini çalıştırmak için önceki iki adımı tekrarlayın.

![Perakende otomatik masraf kuruluşu hiyerarşi amacı yapılandırması.](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a>Kanala göre otomatik masrafları tanımlama

**Kanala göre otomatik masraf filtrelemeyi etkinleştir** özelliğini etkinleştirip **Perakende otomatik masraf** kuruluş hiyerarşisi amacını yapılandırdıktan sonra, kanala göre otomatik masraflar, sipariş başlığı düzeyinde veya sipariş satırı düzeyinde tanımlanabilir.

Otomatik masrafları Commerce'ta kanala göre tanımlamak için aşağıdaki adımları izleyin.

1. Sırasıyla **Alacak hesapları \> masraflar kurulumu \> Otomatik masraflar** seçimlerini yapın.
1. Sol bölmede, iş gereksinimlerinize bağlı olarak **Düzey** alanında **Başlık** ya da **Satır** seçeneğini belirleyin.
1. **Perakende kanal kodu** alanında, uygun kanal kodunu seçin (örneğin, **Tablo** veya **Grup**). Varsayılan ayar olan **Tümü** kullanılırsa, masraf kuralları tüm kanallara uygulanır.

    - **Grup** öğesini seçerseniz, **Retail ve Commerce \> Kanal kurulumu \> Masraflar \> Perakende kanal masraf grupları**'nda bir perakende kanal masraf grubunun oluşturulduğundan emin olun.
    - **Tablo** seçeneğini belirlersniz **Perakende kanal ilişkisi** alanında özel bir kanal (örneğin **San Francisco**) seçebilirsiniz.

1. **Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.
1. Sol bölmede **1040** (**Ürünler**) işini bulun ve seçin.
1. Eylem Bölmesinde **Şimdi çalıştır**'ı seçin.
1. **1070** **(Kanal yapılandırması**) ve **1110** (**Genel yapılandırma**) işlerini çalıştırmak için önceki iki adımı tekrarlayın.
    
![Kanala göre tanımlanan otomatik masraflar.](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a>Örnek senaryo

Aşağıdaki örnekte, bir ürünü, ürün San Franscisco'daki bir fiziksel mağaza kanalı aracılığıyla satıldığında geri dönüşüm masrafları ücretlendirilecek şekilde, yapılandırmak için gerekli olan adımlar gösterilmektedir. Bu örnek ayrıca otomatik masrafların Commerce satış noktası (POS) uygulamasında nasıl göründüğünü de gösterir.

Kuruluş, aşağıdaki çizimde gösterildiği gibi, **GERİ DÖNÜŞÜM** olarak adlandırılan bir masraf kodu tanımlar.

![GERİ DÖNÜŞÜM masraf kodu.](media/Auto-charges-charge-code.png)

Satır düzeyinde otomatik masraf oluşturulur. Aşağıdaki yapılandırmaya sahiptir:

- **Hesap kodu** alanı **Tümü** olarak ayarlanır.
- **Madde kodu** alanı **Tablo** olarak ayarlanır.
- **Madde ilişkisi** alanı ürün kodu **91001** olarak ayarlanır.
- **Teslimat modu kodu** alanı **Tümü** olarak ayarlanır.
- **Perakende kanalı kodu** alanı **Tablo** olarak ayarlanır.
- **Perakende kanalı ilişki** alanı **San Francisco**  mağazası olarak ayarlanır.

Otomatik masraf satırı oluşturulur. Aşağıdaki yapılandırmaya sahiptir:

- **Para birimi** alanı **USD** olarak ayarlanır.
- **Masraf kodu** alanı **GERİ DÖNÜŞÜM** olarak ayarlanır.
- **Kategori** alanı **Sabit** olarak ayarlanır.
- **Masraf** alanı **6,25 $** olarak ayarlanır.

![Satır düzeyi otomatik masraf ve otomatik masraflar satırı yapılandırması.](media/Auto-charges-recyclingfee-line-fee.png)

POS uygulamasında **San Francisco** mağaza kanalında bir satış siparişi oluşturulur. **Masraflar** satırı, **6,25 $** tutarındaki geri dönüşüm ücretini gösterir.

POS uygulamasında **Hareket seçenekleri \> Masraflar \> Masrafları yönet**'i seçerek geri dönüşüm masrafına ait masraf kodunu ve açıklamayı görüntüleyebilirsiniz.

![POS uygulamasındaki geri dönüşüm ücreti.](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Çok yönlü kanal gelişmiş otomatik masrafları](omni-auto-charges.md)

[Başlık masraflarını eşleşen satış satırlarına eşit dağıtma](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
