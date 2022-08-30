---
title: Konteyner paketleme stratejileri
description: Bu makalede konteyner paketleme stratejileri arasındaki farklar açıklanmakta ve örnekler verilmektedir.
author: GalynaFedorova
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5a9a0066abaa76294faebcb15d5091ba36e8a60d
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335780"
---
# <a name="container-packing-strategies"></a>Konteyner paketleme stratejileri

[!include [banner](../includes/banner.md)]

*Konteyner paketleme stratejisi*, konteynerler arasında madde tahsisatlarını tanımlamak için kullanabileceğiniz bir stratejidir. Bu makalede, *Tüm açık konteynerlere paketle* ve *Yalnızca geçerli konteynerde paketle* stratejileri arasındaki farklar açıklanmaktadır.

- **Tüm açık konteynerlere paketle** - Sistem, maddenin bunlardan birine uygun olacağından emin olmak için konteyner kullanımı döngüsü sırasında zaten oluşturulmuş olan tüm açık konteynerleri kontrol etmelidir. Paketleme sırasında sistem, önceden oluşturulmuş konteynerlerden herhangi birine uyup uymayacağını belirlemek için her maddeyi denetler. Madde mevcut bir konteynere uymuyorsa, sistem yeni bir konteyner oluşturur ve tüm siparişi paketlemeyi tamamlayana kadar devam eder.

    Örneğin, sipariş edilmiş *n* madde için konteyner kullanımı gerekmektedir. En kötü durumda, sistem mevcut herhangi bir konteynere uygun olmayan bir maddeyi her işlediğinde, maddenin mevcut konteynerlere uyup uymadını değerlendirmek için toplam (\[(*n* – 1) × (*n* + 1)\] ÷ 2) denetim yapacaktır.

- **Yalnızca geçerli konteynere paketle**: Sistemin, maddenin uygun olup olmadığından emin olmak için yalnızca en son oluşturulan konteyneri kontrol etmesi gerekir. Paketleme sırasında sistem, en son oluşturulan konteynere uyup uymayacağını belirlemek için her maddeyi denetler. Madde bu konteynere uymuyorsa, sistem yeni bir konteyner oluşturur ve tüm siparişi paketlemeyi tamamlayana kadar devam eder.

    Örneğin, sipariş edilmiş *n* madde için konteyner kullanımı gerekmektedir. En kötü durumda, sistem maddenin kapsayıcılara uygun olup olmadığını değerlendirmek için toplam (*n* – 1) denetim yapar.

## <a name="example-of-the-flow-for-container-packing-strategies"></a>Konteyner paketleme stratejileri için akış örneği

Konteynet oluşturma için aşağıdaki öğeleri ayarlarsınız.

| Ürün | Fiziksel boyutlar (genişlik × derinlik × yükseklik) | Ağırlık |
|---|---|---|
| HDMI Kablosu 6' | 1 × 1 × 1 | 1 |
| HDMI Kablosu 12' | 2 × 1 × 1 | 1 |
| HDMI Kablosu 18' | 3 × 1 × 1 | 2 |

Ayrıca, paketleme için kullanılacak aşağıdaki kutuyu da ayarlarsınız.

| Konteyner | Fiziksel boyutlar (uzunluk × genişlik × yükseklik) | Ağırlık | Hacim |
|---|---|---|---|
| Orta Kutu | 6 × 3 × 2 | 10 | 100 |

Son olarak, aşağıdaki ürün ve miktarlara sahip bir sipariş ayarlarsınız.

| Satış sipariş satırı | Miktar |
|---|---|
| HDMI Kablosu 12' | 9 |
| HDMI Kablosu 18' | 8 |
| HDMI Kablosu 6' | 13 |

Aşağıdaki tabloda, *Tüm açık konteynerlere paketle* stratejisini ve *Yalnızca geçerli kontenyere paketle* stratejisini kullandığınızda konteyner kullanımının nasıl çalıştığı özetlenmektedir.

| Tüm açık konteynerlere ambalajla | Geçerli konteynere paketle |
|---|---|
| <p>HDMI Kablosu 12':</p><ol><li>Yeni konteyner (CONT0001) oluşturun.</li><li>CONT0001 kontenyerine 9 ea koyun.</li></ol> | <p>HDMI Kablosu 12':</p><ol><li>Yeni konteyner (CONT0001) oluşturun.</li><li>CONT0001 kontenyerine 9 ea koyun.</li></ol> |
| <p>HDMI Kablosu 18':</p><ol><li>Maddenin CONT0001 konteynerine uyup uymadığını denetleyin.</li><li>Yeni konteyner (CONT0002) oluşturun.</li><li>CONT0002 kontenyerine 5 ea koyun.</li><li>Yeni konteyner (CONT0003) oluşturun.</li><li>CONT0003 kontenyerine 3 ea koyun.</li></ol> | <p>HDMI Kablosu 18':</p><ol><li>Maddenin CONT0001 konteynerine uyup uymadığını denetleyin.</li><li>Yeni konteyner (CONT0002) oluşturun.</li><li>CONT0002 kontenyerine 5 ea koyun.</li><li>Yeni konteyner (CONT0003) oluşturun.</li><li>CONT0003 kontenyerine 3 ea koyun.</li></ol> |
| <p>HDMI Kablosu 6':</p><ol><li>Maddenin CONT0001 konteynerine uyup uymadığını denetleyin.</li><li>CONT0001 kontenyerine 1 ea koyun.</li><li>Maddenin CONT0002 konteynerine uyup uymadığını denetleyin.</li><li>Maddenin CONT0003 konteynerine uyup uymadığını denetleyin.</li><li>CONT0003 kontenyerine 4 ea koyun.</li><li>Yeni konteyner (CONT0004) oluşturun.</li><li>CONT0004 kontenyerine 8 ea koyun.</li></ol> | <p>HDMI Kablosu 6':</p><ol><li>Maddenin CONT0003 konteynerine uyup uymadığını denetleyin.</li><li>CONT0003 kontenyerine 4 ea koyun.</li><li>Yeni konteyner (CONT0004) oluşturun.</li><li>CONT0004 kontenyerine 9 ea koyun.</li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a>Örnek senaryo: Her konteynere tekli siparişleri paketleme

Bu bölüm, sistemin birden çok siparişi tek bir sevk sevkiyatta birleştirmek üzere ayarlandığı bir senaryo sunar. Bu nedenle, birden fazla ürün içeren her siparişin kendi konteynerine paketlenmesi için konteynerleme satış siparişinden yapılacaktır.

Bu işlev, dağıtım merkezinin tam konteynerlerin perakende mağazaları arasında çapraz sevkini yapabilmesi için her konteynere yalnızca bir satış siparişi paketlemeniz gereken senaryoları uygulamanızı sağlar. Perakende senaryolarına ek olarak (perakende mağazası başına sipariş ve çapraz sevkiyat için dağıtım merkezine sevkiyat) bu teknik yalın tedarik zincirlerinde de yaygın olarak kullanılır (tam zamanında üretim hattı başına satış siparişi).

Bu senaryo, konteynerleme için *Yalnızca geçerli konteynere paketle* stratejisi kullanıarak paketleme sırasında değerlendirilen kenteyner sayısını nasıl düşürebileceğinizi gösterir.

### <a name="prerequisites"></a>Önkoşullar

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a>Sisteminizde Sevkiyatları konsolide et özelliğini açma

Bu senaryo *Sevkiyatları konsolide et* özelliğini kullanır. Supply Chain Management sürüm 10.0.29 itibarıyla, özellik zorunludur ve kapatılamaz. 10.0.29 sürümünden daha eski bir sürümü çalıştırıyorsanız, yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Sevkiyatları konsolide et* özelliğini aratarak bu işlevi açabilir veya kapatabilir.

#### <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Bu senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur. Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği **USMF** olarak ayarladığınızdan emin olun.

### <a name="inspect-or-create-container-types"></a>Konteyner türlerini inceleme veya oluşturma

Konteyner türlerinizi incelemek veya gerekirse yeni kapsayıcı türleri oluşturmak için şu adımları izleyin.

1. **Ambar yönetimi** \> **Kurulum** \> **Konteynerler** \> **Konteyner türleri** öğesine gidin.
1. Aşağıdaki konteyner türlerinin her birinin tanıtım verilerinizde kullanılabilir olduğundan emin olun. Konteyner türlerini gerektiği gibi düzenleyin veya oluşturun.

    - Konteyner türü 1:

        - **Konteyner türü kodu:** *Kutu-Büyük*
        - **Açıklama:** *Büyük Kutu*
        - **Maksimum net ağırlık:** *100*
        - **Hacim:** *400*
        - **Uzunluk:** *4*
        - **Genişlik:** *10*
        - **Yükseklik:** *10*

    - Konteyner türü 2:

        - **Konteyner türü kodu:** *Kutu-Orta*
        - **Açıklama:** *Orta Kutu*
        - **Maksimum net ağırlık:** *50*
        - **Hacim:** *200*
        - **Uzunluk:** *2*
        - **Genişlik:** *10*
        - **Yükseklik:** *10*

    - Konteyner türü 3:

        - **Konteyner türü kodu:** *Kutu-Küçük*
        - **Açıklama:** *Küçük Kutu*
        - **Maksimum net ağırlık:** *20*
        - **Hacim:** *100*
        - **Uzunluk:** *1*
        - **Genişlik:** *10*
        - **Yükseklik:** *10*

### <a name="inspect-or-create-container-groups"></a>Konteyner gruplarını inceleme veya oluşturma

Konteyner gruplarınızı incelemek veya gerekirse yeni konteyner grupları oluşturmak için şu adımları izleyin.

1. **Ambar yönetimi** \> **Kurulum** \> **Konteynerler** \> **Konteyner grupları** öğesine gidin.
1. Aşağıdaki konteyner grubunun tanıtım verilerinizde kullanılabilir olduğundan emin olun. Kullanılamıyorsa, oluşturmak için **Yeni**'yi seçin.

    - **Konteyner grubu kodu:** *Kutular*
    - **Açıklama:** *Kutu boyutları*

1. **Kutular** konteyner grubunun *Ayrıntılar* hızlı sekmesinde, aşağıdaki satırların varoldğundan emin olun. Yoksa, eklemek için **Yeni**'yi seçin.

    - Satır 1:

        - **Sıra numarası:** *1*
        - **Konteyner türü:** *Kutu-Büyük*
        - **Konteyner kullanım yüzdesi:** *100*

    - Satır 2:

        - **Sıra numarası:** *2*
        - **Konteyner türü:** *Kutu-Orta*
        - **Konteyner kullanım yüzdesi:** *100*

    - Satır 3:

        - **Sıra numarası:** *3*
        - **Konteyner türü:** *Kutu-Küçük*
        - **Konteyner kullanım yüzdesi:** *100*

### <a name="create-a-new-container-build-template"></a>Yeni bir konteyner oluşturma şablonu oluşturma

Yeni konteyner oluşturma şablonu oluşturmak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi** \> **Kurulum** \> **Konteynerler** \> **Konteyner yapı şablonu** öğesine gidin.
1. Aşağıdaki ayarlara sahip bir konteyner oluşturma şablonu oluşturmak için **Yeni**'yi seçin:

    - **Sıra numarası:** *1*
    - **Konteyner şablonu kodu:** *Kutu*
    - **Konteyner grubu kodu:** *Kutular*
    - **Temel sorgu türleri:** *Satış tahsisat satırı*
    - **Dalga adım kodu:** *234*
    - **Bölünmüş çekmelere izin ver:** *Evet*
    - **Konteyner paketleme stratejisi:** *Yalnızca geçerli konteynere paketle*
    - **Yönerge birimine göre paketle:** *Hayır*

1. Yeni şablon için satır seçiliyken, Eylem Bölmesinde **Sorguyu düzenle**'yi seçin.
1. Standart sorgu düzenleyicisi iletişim kutusu görüntülenir. Aşağıdaki ayarlara sahip bir satır eklemek için **Tasnif** sekmesinde **Ekle**'yi seçin:

    - **Tablo:** *geçici iş hareketleri*
    - **Türetilmiş tablo:** *geçici iş hareketleri*
    - **Alan:** *Sipariş numarası*
    - **Arama yönü:** *Artan*

    > [!IMPORTANT]
    > Diğer tüm açık konteynerlerde döngü yapılmasını önlemek ve bir kerede tek bir konteyneri denetleyerek işlemi hızlandırmak için, sipariş numarasına göre sıralamaya ek olarak *Yalnızca geçerli konteynere paketle* stratejisini kullanın. Bu birleşim, bir iş şablonundaki bir iş sonu gibi çalışır.

1. Sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni şablon için satır seçiliyken, Eylem Bölmesinde **Konteyner karıştırma sınırlamaları**'nı seçin.

    Şimdi, maddeleri tek bir siparişten tek bir kapsayıcıya koyan bir sınırlama ekleyeceksiniz. Başka bir siparişten gelen maddeler ayrı bir konteynere konulacaktır.

1. Aşağıdaki ayarlara sahip bir karıştırma sınırlaması oluşturmak için **Yeni**'yi seçin:

    - **Tablo:** *Satış siparişleri*
    - **Alan seçimi:** *SalesId* (Alan, ızgarada *Satış siparişi* olarak görünecektir.)

1. Sınırlamayı eklemek için **Tamam**'ı seçin.
1. Sayfayı kapatın.

### <a name="set-up-a-wave-template-for-containerization"></a>Konteynerleme için dalga şablonu oluşturma

Dalga şablonu ayarlamak için aşağıdaki adımları takip edin.

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.
1. Liste bölmesinde, **Dalga şablonu türü** alanını *Sevkiyat* olarak ayarlayın.
1. Listeden **63 Konteynerleme** şablonunu seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Yöntemler** hızlı sekmesinde, **Seçili yöntemler** sütununda, aşağıdaki satırı bulun:

    - **Yöntem adı:** *konteynerleme*
    - **Ad:** *Konteynerleme*

1. Satır için **Dalga adımı kodu** alanını *234* olarak ayarlayın.

### <a name="set-up-a-work-template"></a>İş şablonu ayarla

İş şablonu ayarlamak için aşağıdaki adımları takip edin.

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. **İş emri türü** alanını,*Satış siparişleri* olarak ayarlayın.
1. **Genel bakış** ızgarasında, konteyner başına tekli siparişleri paketleme için kullanılması gereken iş şablonunu bulun ve seçin. Bu senaryo için **63 Konteynere çekme** şablonunu seçin.
1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. Standart sorgu düzenleyicisi iletişim kutusu görüntülenir. **Tasnif** sekmesinde, aşağıdaki satırları ekleyin:

    - Satır 1:

        - **Tablo:** *geçici iş hareketleri*
        - **Türetilmiş tablo:** *geçici iş hareketleri*
        - **Alan:** *Sevkiyat kodu*
        - **Arama yönü:** *Artan*

    - Satır 2:

        - **Tablo:** *geçici iş hareketleri*
        - **Türetilmiş tablo:** *geçici iş hareketleri*
        - **Alan:** *Sipariş numarası*
        - **Arama yönü:** *Artan*

    - Satır 3:

        - **Tablo:** *geçici iş hareketleri*
        - **Türetilmiş tablo:** *geçici iş hareketleri*
        - **Alan:** *Konteyner Kimliği*
        - **Arama yönü:** *Artan*

1. Sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Aşağıdaki iletiyi alırsınız: "Gruplama sıfırlanacak, devam edilsin mi?" Devam etmek için **Eve**'i seçin.
1. **63 Konteynere çekme** hala seçiliyken, Eylem Bölmesinde **İş başlığı sonları**'nı seçin.

    Şimdi, siparişteki her konteynerin bir iş emrine bağlanması için işi bölmek üzere ayarları uygulayacaksınız.

1. **Çalışma başlığı sonları** sayfasındaki her satır için **Bu alana göre grupla** onay kutusunu seçin (**Sevkiyat kodu**, **Sipariş numarası** ve **Konteyner kodu**).
1. Sayfayı kapatın.

### <a name="set-up-shipment-consolidation-policies"></a>Sevkiyat konsolidasyonu ilkelerini ayarlama

Sevkiyat konsolidasyonu ilkesi ayralamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambara serbest bırakma \> Sevkiyat konsolidasyon ilkeleri** seçeneğine gidin.
1. Liste bölmesinde **İlke türü** alanını *Satış siparişleri* olarak ayarlayın.
1. Listeden **Varsayılan** ilkeyi seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Konsolidasyon alanları** hızlı sekmesinde **Seçili alanlar** listesinde, **Alan adı** alanının *Sipariş numarası* olarak ayarlandığı satırı seçin.
1. **Kaldır** düğmesini ![sol ok.](media/backward-button.png) seçerek alanı **Kalan alanlar** listesine taşıyın.
1. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="set-up-physical-dimensions-for-the-product"></a>Ürün için fiziksel boyutlar ayarlama

Bu senaryoda kullanılacak ürünlerle ilgili fiziksel boyutları ayarlamak için, aşağıdaki adımları izleyin.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. **Madde numarası** alanının *A0001* olarak ayarlandığı ürünü seçin.
1. Eylem Bölmesinde, **Stoğu yönet** sekmesindeki **Ambar** grubunda, **Fiziksel boyutlar**'ı seçin.
1. **Fiziksel boyutlar** sayfasında, ızgarada aşağıdaki satırı görmelisiniz:

    - **Birim:** *adet*
    - **Brüt ağırlık:** *3,00*
    - **Genişlik:** *2,00*
    - **Derinlik:** *2,00*
    - **Yükseklik:** *4,00*
    - **Hacim:** *16,00*

1. Sayfayı kapatın.
1. **Madde numarası** alanının *A0002* olarak ayarlandığı ürünü seçin.
1. Eylem Bölmesinde, **Stoğu yönet** sekmesindeki **Ambar** grubunda, **Fiziksel boyutlar**'ı seçin.
1. **Fiziksel boyutlar** sayfasında, ızgarada aşağıdaki satırı görmelisiniz:

    - **Birim:** *adet*
    - **Brüt ağırlık:** *4,00*
    - **Genişlik:** *3,00*
    - **Derinlik:** *1,00*
    - **Yükseklik:** *3,00*
    - **Hacim:** *9,00*

### <a name="create-sales-order-1"></a>Satış siparişi oluşturma 1

Bir satış siparişi oluşturmak için şu adımları izleyin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Yeni bir satış siparişi oluşturmak için bir iletişim kutusu görüntülenir. Aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-001*
    - **Ambar:** *63*

1. Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesinde, aşağıdaki satış satırlarını ekleyin:

    - Satır 1:

        - **Madde numarası:** *A0001*
        - **Miktar:** *2*

    - Satır 2:

        - **Madde numarası:** *A0002*
        - **Miktar:** *2*

1. İlk satırı seçin ve **Stok \> Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, **Lot rezerve et** 'i seçin. Ardından sayfayı kapatın.
1. İkinci satır için önceki iki adımı tekrarlayın.
1. Sayfayı kapatın.

### <a name="create-sales-order-2"></a>Satış siparişi oluşturma 2

İkinci bir satış siparişi oluşturmak için şu adımları izleyin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Yeni bir satış siparişi oluşturmak için bir iletişim kutusu görüntülenir. Aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-001*
    - **Ambar:** *63*

1. Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesinde, aşağıdaki satış satırlarını ekleyin:

    - Satır 1:

        - **Madde numarası:** *A0001*
        - **Miktar:** *4*

    - Satır 2:

        - **Madde numarası:** *A0002*
        - **Miktar:** *4*

1. İlk satırı seçin ve **Stok \> Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, **Lot rezerve et** 'i seçin. Ardından sayfayı kapatın.
1. İkinci satır için önceki iki adımı tekrarlayın.
1. Sayfayı kapatın.

### <a name="create-the-load"></a>Yük oluşturma

Bu senaryo için oluşturduğunuz her sipariş için bir yük oluşturmak ve sonra bunu ambara serbest bırakmak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Yükler \> Yük planlama çalışma ekranı** öğesine gidin.
1. **Satış satırları** sekmesinde, bu senaryo için oluşturduğunuz satış siparişlerindeki tüm satış siparişi satırlarını bulun ve seçin.
1. Eylem Bölmesinde **Arz ve talep** sekmesindeki **Ekle** grubunda **Yeni yüke**'yi seçin. Seçili sipariş satırları yeni bir yüke eklenir.
1. **Yük şablonu ataması** iletişim kutusundaki **Yük şablonu kimliği** alanında, *40' Konteyner* gibi bir yük şablonu seçin.
1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. **Yükler** bölümünde, az önce oluşturduğunuz yükü bulun ve seçin.
1. **Serbest bırak \> Ambara serbest bırak**'ı seçin.
1. Seçili yükü ambara serbest bırakmak için **Ambara serbest bırak** iletişim kutusunda **Tamam**'ı seçin.

### <a name="verify-the-shipments-and-containers"></a>Sevkiyatları ve konteynerleri doğrulama

Aşağıdaki prosedür, oluşturulan sevkiyatları doğrulamanıza olanak verir. İstenen sonuçları elde ettiğinizden emin olmak için bu senaryo için oluşturduğunuz siparişi incelemek için kullanın.

1. **Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.
1. Az önce serbest bıraktığınız yük için oluşturulan sevkiyatı bulun ve seçin.
1. Eylem Bölmesinde, **Taşıma** sekmesinde **Konteynerleri görüntüle**'yi seçin.
1. Satış siparişlerindeki maddelerin iki farklı konteynere yerleştirildiğini doğrulayın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Konteyner kullanımı](wave-containerization.md)
