---
title: Malzeme çekme satırı gruplandırması
description: Bu konu, çekme satırı gruplandırmasına genel bakış sağlamaktadır.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 4b9cd7dac680c1691fb4c6dd4078f109254be784
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215614"
---
# <a name="pick-line-grouping"></a>Malzeme çekme satırı gruplandırması

[!include [banner](../includes/banner.md)]

Çekme satırı gruplandırmasında, aynı madde ve yerleşime sahip birden çok iş satırı mobil cihazda kullanıcıya sunulan tek bir çekmede birleştirilebilir. Bu nedenle, ambar çalışanları olası en etkili yönergeleri alabilir, ancak sistemdeki iş satırlarının gerekli ayrımı da sürdürülür (örneğin, farklı kapsayıcılar ve siparişler için).

## <a name="set-up-pick-line-grouping"></a>Çekme satırı gruplandırması ayarlama

### <a name="create-a-mobile-device-menu-item"></a>Mobil cihaz menü öğesi oluşturma

1. **Ambar Yönetimi \> kurulum \> mobil cihaz \> mobil cihaz menüsü öğeleri**'ne gidin ve **Satış grubu satırı malzeme çekme – Kullanıcı yönlendirilen** adlı yeni bir menü öğesi oluşturun.
2. **Mobil cihaz için menü öğeleri** altında, aşağıdaki değerleri ayarla:

    - **Menü madde adı** alanında, **satış çekme- grup satırı**'nı girin.
    - **Başlık** alanında, **satış çekme- grup satırı**'nı girin.
    - **Mod** alanında, **İş**'i seçin.
    - **Mevcut işi kullan** seçeneğinde **Evet**'i işaretleyin.

3. **Genel** Hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Yöneten** alanında **Kullanıcı tarafından yönetilen**'i seçin.
    - **Lisans kalıbı oluştur** seçeneğini **Evet** olarak ayarlayın.
    - **Grup çekme** seçeneğini **Evet** olarak ayarlayın.

4. **İş sınıfları** hızlı sekmesinde, mobil aygıt menü öğesi için geçerli iş sınıflarını konfigüre etmek üzere aşağıdaki adımları izleyin:

    1. **Yeni**'yi seçin.
    2. **İş sınıfı kimliği** alanında, kullanacağınız ambara göre **satış**'ı veya **satış siparişi çekme**'yi seçin.
    3. **İş siparişi türü** alanında **Satış siparişi**'ni seçin.

### <a name="set-up-a-mobile-device-menu"></a>Mobil cihaz menüsü ayarlama

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin. 
1. Yeni oluşturduğunuz menü öğesini istenen menüye ekleyin.

### <a name="set-up-a-work-template"></a>İş şablonu ayarla

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. Bu işlevle kullanılması gereken çalışma şablonunu bulun. Bu örnek için, standart **51 malzeme çekme** Contoso iş şablonu ' nu seçin.
1. Menüde, **Düzenle sorgu** seçeneğini belirleyin.
1. **Sıralama** sekmesinde **Ekle**'yi seçin ve sonra aşağıdaki değerleri ayarlayın:

    - **Tablo** alanında **Geçici iş hareketleri**'ni seçin.
    - **Türetilmiş tablo** alanında **Geçici iş hareketleri**'ni seçin.
    - **Alan** alanında, **Öğe numarasını** seçin.
    - **Arama yönü** alanında, **artan**'ı seçin.

> [!NOTE]
> Satır gruplama çekme işlevinin çalışması için, iş satırlarının madde koduna göre sıralanması gerekir. Aynı maddeleri içeren satırlar başka bir satırdan sonra sıralanmamışsa, gruplandırılmaz.

## <a name="example"></a>Örnek

### <a name="create-picking-work"></a>Malzeme çekme işi oluştur

Çekme satırı gruplandırmasını ayarlamadan önce, uygun bazı giden işler oluşturmanız gerekir.

1. **Satış ve Pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
2. Satış siparişi oluşturmak için **Yeni**'yi seçin. 
3. **Müşteri hesabı** alanından bir AB müşterisini seçin. 
4. **Genel** hızlı sekmesinde, **ambar** alanında, **51**'i seçin. Daha sonra **Tamam**'ı seçin.
5. **Satış siparişi satırları** altında, aşağıdaki altı satırı ekleyin:

    - **Satır 1:** **Öğe numarası** alanında, **M9200**'ü seçin. **Miktar** alanına **3** yazın.
    - **Satır 2:** **Öğe numarası** alanında, **M9201**'ü seçin. **Miktar** alanına **3** yazın. 
    - **Satır 3:** **Öğe numarası** alanında, **M9202**'ü seçin. **Miktar** alanına **2** yazın. 
    - **Satır 4:** **Öğe numarası** alanında, **M9200**'ü seçin. **Miktar** alanına **1** yazın. 
    - **Satır 5:** **Öğe numarası** alanında, **M9200**'ü seçin. **Miktar** alanına **3** yazın.
    - **Satır 6:** **Öğe numarası** alanında, **M9202**'ü seçin. **Miktar** alanına **7** yazın. 

    İşte her madde için toplam miktarların Özeti:

    - **Madde M9200:** her biri 7
    - **Madde M9201:** her biri 3
    - **Madde M9202:** her biri 9

6. Siparişleri ambara serbest bırakmadan önce, çekme yerleşimlerinin tüm siparişlerdeki tüm maddeler için yeterli stok içerdiğinden emin olmanız gerekir. Satış siparişi çekme için hangi malzeme çekme konumlarının kullanıldığını belirlemek için **yerleşim yönergesi** ayarını gözden geçirin.
7. Stoku rezerve edin ve ambara serbest bırakın. Altı satıra sahip bir iş kodu oluşturulur. Satırlar madde numarasına göre sıralanır.

### <a name="run-the-mobile-device-flow"></a>Mobil cihaz akışı çalıştır

1. Mobil cihazda, yeni mobil aygıt menü öğesini içeren menüyü seçin.
1. **Satış çekme – Grup satırı** menü öğesini seçin ve çekmeyi başlatın.

    Menüyü seçtikten ve iş kodunu girdikten sonra, madde M9200 için tüm çekme satırlarının gruplandırılacağı çekme adımını görürsünüz. 7 tane Madde M9200 öğesini çekmek için bir talimat alırsınız.

1. Çekme adımını onaylayın. 
1. Süren işin istemci ekranına gidin ve madde M9200 için üç çekme satırının aynı anda kapatıldığına dikkat edin.

    İş satırı 4 gösterilir.

1. Çekme adımını onaylayın.

    Mobil aygıttaki son çekme adımı, iş emrinden alınan son iki çekme satırını toplar.

1. 9 tane her Madde M9202 için çekme adımını tamamlayın.
1. İşi tamamlamak için Yerine Koyma adımını ve ek çekme/yerine koyma çiftlerini onaylayın.

> [!NOTE]
> - İş satırları yalnızca sıralı olduklarında gruplandırılabilir.
> - Aşağıdaki işlevsellik desteklenmez:
>
>    - Fiili ağırlık maddeleri. İşte herhangi bir fiili ağırlık öğesi varsa, çekmeyi başlatmak için başlamadan önce bir hata iletisi alırsınız.
>    - Parça çekme.
>    - Bitmemiş stok yenileme çalışması olan iş satırları.
>    - Fazla malzeme çekme.
