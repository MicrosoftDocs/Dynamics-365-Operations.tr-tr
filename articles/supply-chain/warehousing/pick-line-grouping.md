---
title: Malzeme çekme satırı gruplandırması
description: Bu konu, çekme satırı gruplandırmasına genel bakış sağlamaktadır.
author: Mirzaab
manager: tfehr
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: e70244d46ec2787fefdb097d0354af7910b55e9c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989730"
---
# <a name="pick-line-grouping"></a>Malzeme çekme satırı gruplandırması

[!include [banner](../includes/banner.md)]

Malzeme çekme satırı gruplandırması, aynı madde ve yerleşime sahip birden çok iş satırı mobil cihazda kullanıcıya sunulan tek bir çekmede birleştirilebilir. Bu nedenle, ambar çalışanları olası en etkili yönergeleri alabilir, ancak sistemdeki iş satırlarının gerekli ayrımı da (örneğin, farklı konteynerler, siparişler vb. için) sürdürülür.

## <a name="turn-on-the-pick-line-grouping-feature"></a>İş çekme satırı gruplandırma özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Malzeme çekme satırı gruplandırma*

## <a name="set-up-pick-line-grouping"></a>Çekme satırı gruplandırması ayarlama

### <a name="create-a-mobile-device-menu-item"></a>Mobil cihaz menü öğesi oluşturma

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Menü madde adı** alanında, *Satış grubu satırı malzeme çekme*'yi girin.
1. **Başlık** alanında, *Satış grubu satırı malzeme çekme*'yi girin. Bu başlık, mobil cihaz menüsünde gösterilir.
1. **Mod** alanında, *İş*'i seçin.
1. **Mevcut işi kullan** seçeneğinde *Evet*'i işaretleyin.
1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Yöneten** alanında *Kullanıcı tarafından yönetilen*'i seçin.
    - **Lisans kalıbı oluştur** seçeneğini *Evet* olarak ayarlayın.
    - **Grup çekme** seçeneğini *Evet* olarak ayarlayın.
    - Kalan seçenekler için varsayılan değerleri kabul edin.

1. Mobil cihaz menü öğesi için geçerli iş sınıflarını yapılandırmak üzere aşağıdaki adımları izleyin:

    1. **İş sınıfları** hızlı sekmesinde, **Yeni**'yi seçin.
    2. **İş sınıfı kimliği** alanında, kullanacağınız ambara göre *Satış*'ı veya *Satış Siparişi Çekme*'yi seçebilirsiniz. Bu senaryo için *Satış Siparişi Çekme*'yi seçin.

        **İş emri türü** alanı, otomatik olarak *Satış siparişleri* olarak ayarlanır.

### <a name="set-up-a-mobile-device-menu"></a>Mobil cihaz menüsü ayarlama

Az önce oluşturduğunuz menü öğesini **Giden** menüsüne eklemek için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. Liste bölmesi, mevcut tüm mobil cihaz menülerini gösterir. Listede, *Giden*'i seçin.
1. **Kullanılabilir menüler ve menü öğeleri** listesinde, yeni oluşturduğunuz *Satış grubu satırı malzeme çekme* menü öğesini bulun ve seçin.
1. *Satış grubu satırı malzeme çekme* menü öğesini **Menü yapısı** listesine taşımak için sağ ok düğmesini seçin.
1. Menü öğesini menü yapısında istenen konuma taşımak için yukarı ok ve aşağı ok düğmelerini kullanın.
1. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="set-up-a-work-template"></a>İş şablonu ayarla

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. **İş siparişi türü** alanında *Satış siparişi*'ni seçin.
1. **Özet** ızgarasında, bu işlevle kullanılması gereken çalışma şablonunu bulun ve seçin. Bu senaryo için *51 malzeme çekme* şablonunu seçin.
1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. Sorgu düzenleyicisi iletişim kutusundaki **Sıralama** sekmesinde **Ekle**'yi seçin ve ardından yeni satır için aşağıdaki değerleri ayarlayın:

    - **Tablo** sütununda *Geçici iş hareketleri*'ni seçin.
    - **Türetilmiş tablo** sütununda *Geçici iş hareketleri*'ni seçin.
    - **Alan** sütununda, *Öğe numarası*'nı seçin.
    - **Arama yönü** sütununda, *Artan*'ı seçin.

1. İletişim kutusunu kapatmak için **Tamam**'ı seçip seçiminizi kaydedin.
1. Aşağıdaki iletiyi alırsınız: "Gruplama sıfırlanacak, devam edilsin mi?" Devam etmek için **Eve**'i seçin.

> [!IMPORTANT]
> Satır gruplama çekme işlevinin çalışması için, iş satırlarının madde koduna göre sıralanması gerekir. Aynı maddeleri içeren satırlar başka bir satırdan sonra sıralanmamışsa, gruplandırılmaz.

## <a name="example"></a>Örnek

### <a name="create-picking-work"></a>Malzeme çekme işi oluştur

Çekme satırı gruplandırmasını ayarlamadan önce, uygun bazı giden işler oluşturmanız gerekir.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Satış siparişi oluşturmak için **Yeni**'yi seçin.
1. **Müşteri hesabı** alanında *US-004*'ü seçin.
1. **Genel** hızlı sekmesinde, **ambar** alanında, *51*'i seçin.
1. **Tamam**'ı seçin.
1. **Satış siparişi satırları** hızlı sekmesinde, aşağıdaki altı satırı ekleyin:

    - **Satır 1:** **Öğe numarası** alanında, *M9200*'ü seçin. **Miktar** alanına *3* yazın.
    - **Satır 2:** **Öğe numarası** alanında, *M9201*'ü seçin. **Miktar** alanına *3* yazın.
    - **Satır 3:** **Öğe numarası** alanında, *M9202*'ü seçin. **Miktar** alanına *2* yazın.
    - **Satır 4:** **Öğe numarası** alanında, *M9200*'ü seçin. **Miktar** alanına *1* yazın.
    - **Satır 5:** **Öğe numarası** alanında, *M9200*'ü seçin. **Miktar** alanına *3* yazın.
    - **Satır 6:** **Öğe numarası** alanında, *M9202*'ü seçin. **Miktar** alanına *7* yazın.

    İşte her madde için toplam miktarların Özeti:

    - **Madde M9200:** her biri *7*
    - **Madde M9201:** her biri *3*
    - **Madde M9202:** her biri *9*

1. Siparişleri ambara serbest bırakmadan önce, çekme yerleşimlerinin tüm siparişlerdeki tüm maddeler için yeterli stok içerdiğinden emin olmanız gerekir. Satış siparişi çekme için hangi malzeme çekme konumlarının kullanıldığını belirlemek için **yerleşim yönergesi** ayarını gözden geçirin. *51* ambarı için Contoso tanıtım veri ortamını kullanıyorsanız, kullanılabilir stok olduğundan emin olun.

    Şimdi her bir satır için stoku rezerve etmelisiniz.

1. **Satış siparişi satırları** hızlı sekmesinde, rezerve edilmesi gereken satırlardan birini seçin.
1. Kılavuzun üzerindeki **stok** menüsünde **rezervasyon**'yı seçin.
1. **Rezervasyon** sayfasındaki Eylem Bölmesi'nde rezervasyonu uygulamak için **Lotu rezerve et**'i seçin. Ardından sayfayı kapatın.
1. Rezerve edilmesi gereken kalan satırlar için 8 ile 10 arasındaki adımları yineleyin.

    Şimdi satış siparişini ambara serbest bırakmalısınız.

1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.

    Bir sevkiyat ve dalganın oluşturulduğunu ve dalganın toplu iş halinde çalıştırılmak üzere gönderildiğini bildiren bir ileti alırsınız.

    Dalga ve tüm aşağı akış işleri tamamlandığında, altı satıra sahip bir iş için bir iş kodu oluşturulur. Satırlar madde numarasına göre sıralanır.

1. Oluşturulan işi görüntülemek için **Ambar yönetimi \> İş \> Tüm işler**'e gidin. Bir sonraki yordamda kullanmanız gerekeceğinden **İş kodu** değerini not edin.

### <a name="initiate-picking-from-the-mobile-device"></a>Mobil cihazdan malzeme çekme işlemini başlatma

1. Ambar *51* için ayarlanmış olan bir kullanıcı olarak mobil cihazda oturum açın.
1. Mobil cihazda, yeni mobil aygıt menü öğesini içeren menüyü seçin. Bu senaryo için **Giden**'i seçin.
1. Malzeme çekmeyi başlatmak için **Satış grubu satırı malzeme çekme** menü öğesini seçin.
1. Önceki yordamda not aldığınız **İş Kodu** değerini girin.

    *M9200* öğesinin tüm malzeme çekme satırlarının gruplandırıldığı bir malzeme çekme adımı görmeniz ve her bir *M9200* maddesi için *7* adet çekmeniz gerektiğini bildiren bir yönerge almanız gerekir.

    > [!IMPORTANT]
    > Mobil cihazda, üç malzeme çekme iş satırı için malzeme çekme işi kullanıcı için tek bir malzeme çekme adımında toplanır.

1. Çekme adımını onaylayın.
1. İş kodunun iş sayfasına gidin ve madde *M9200* için üç çekme satırının aynı anda kapatıldığına dikkat edin.
1. Mobil cihaza geri dönün ve çekme işlemine devam edin. *M9201* için iş satırı 4 gösterilmelidir. Siparişte yalnızca bir iş satırı bulunduğundan, toplanacak bir şey yoktur.
1. Çekme adımını onaylayın.
1. Mobil aygıttaki son çekme adımı, iş emrinden alınan son iki çekme satırını toplar.
1. *M9202* maddesi için *9* adet malzeme çekme adımını tamamlayın.
1. İşi tamamlamak için Yerine Koyma adımını ve ek çekme/yerine koyma çiftlerini onaylayın.

> [!IMPORTANT]
>
> - İş satırları yalnızca sıralı olduklarında gruplandırılabilir.
> - Aşağıdaki işlevsellik desteklenmez:
>
>   - Fiili ağırlık maddeleri
>
>    İşte herhangi bir fiili ağırlık öğesi varsa, çekmeyi başlatmak için başlamadan önce bir hata iletisi alırsınız.
>
>   - Parça çekme
>   - Bitmemiş stok yenileme işi olan iş satırları
>   - Fazla malzeme çekme
>   - Yeniden tahsisatla eksik malzeme çekme
