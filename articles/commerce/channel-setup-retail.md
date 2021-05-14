---
title: Perakende kanalı ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir perakende kanalı oluşturma yöntemi açıklanmıştır.
author: samjarawan
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3f1f5dc2c8402d9b6b68a049f804932812eb74c0
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937546"
---
# <a name="set-up-a-retail-channel"></a>Perakende kanalını ayarlama

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir perakende kanalı oluşturma yöntemi açıklanmıştır.

Dynamics 365 Commerce birden fazla perakende kanalı destekler. Bu perakende kanalları çevrimiçi mağazaları, çağrı merkezlerini ve perakende mağazalarını (tuğla dibek mağazalar olarak da bilinir) içerir. Her perakende mağaza kanalının kendi ödeme türleri, fiyat grupları, satış noktası (POS) kasaları, gelir hesapları ve gider hesapları ve personeli olabilir. Bir perakende mağaza kanalı oluşturabilmeniz için tüm bu öğeleri ayarlamanız gerekir. 

Bir perakende kanalı oluşturulmadan önce, [kanal önkoşullarını izlediğinizden](channels-prerequisites.md) emin olun.

## <a name="create-and-configure-a-new-retail-channel"></a>Yeni bir perakende kanalı oluşturma ve yapılandırma

1. Gezinti bölmesinde **Modüller \> Kanallar \> Mağazalar \> Tüm mağazalar**'a gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Ad** alanına yeni kanal için bir ad girin.
1. **Mağaza numarası** alanına benzersiz bir mağaza numarası girin. Numara yalnızca alfasayısal karakterlerden oluşabilir ve en fazla 10 karakter olabilir.
1. **Tüzel kişilik** açılır listesinde, uygun tüzel kişiliği girin.
1. **Ambar** açılır listesinde, ilgili ambarı girin.
1. **Mağaza saati dilimi** alanında, ilgili saat dilimini seçin.
1. **Satış vergisi grubu** açılır listesinde, mağaza için uygun satış vergisi grubunu seçin.
1. **Para birimi** alanında uygun para birimini seçin.
1. **Müşteri adres defteri** alanında, geçerli bir adres defteri girin.
1. **Varsayılan müşteri** alanında, geçerli bir varsayılan müşteri girin.
1. **İşlevsellik profili** alanında, varsa bir işlevsellik profili seçin.
1. **E-posta bildirimi profili** alanında, geçerli bir e-posta bildirimi profili girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde yeni bir perakende kanalının oluşturulması gösterilmektedir.

![Yeni perakende kanalı](media/channel-setup-retail-1.png)

Aşağıdaki resimde örnek bir perakende kanalı gösterilmektedir.

![Örnek perakende kanalı](media/channel-setup-retail-2.png)

## <a name="other-settings"></a>Diğer ayarlar

Perakende mağazasının gereksinimlerine göre **Ekstre/kapanış** ve **Çeşitli** bölümlerinde ayarlanabilecek isteğe bağlı birçok başka ayar vardır.

Ek olarak, **Ekran düzeni** bölümünde varsayılan ekran düzenini ayarlama hakkında bilgi için bkz. [Satış noktası (POS) için ekran düzenlerine](pos-screen-layouts.md) ve **Donanım istasyonları** bölümü hakkında kurulum bilgileri için bkz. [Retail Hardware Station'ı yapılandırma ve yükleme](retail-hardware-station-configuration-installation.md).

Aşağıdaki resimde örnek bir perakende kanalı kurulum yapılandırması gösterilmektedir.

![Örnek perakende kanalı yapılandırması](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a>Ek kanal ayarları

Bir kanal için, **Ayarla** bölümünün altındaki Eylem Bölmesi'nde bulunabilecek, kanal için ayarlanması gereken ek öğeler vardır.

Çevrimiçi kanal kurulumu için gerekli ek görevler şunların ayarlanmasını içerir: Ödeme yöntemleri, kasa bildirimi, teslimat şekilleri, gelir/gider hesabı, bölümler, karşılama grubu ataması ve kasalar.

Aşağıdaki resimde, **Ayarla** sekmesindeki çeşitli ek perakende kanal kurulum seçenekleri gösterilmektedir.

![Kanalı ayarlama](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a>Ödeme yöntemlerini ayarlama

Ödeme yöntemlerini ayarlamak için, bu kanalda desteklenen her ödeme türü için bu adımları izleyin.

1. Eylem Bölmesi'nde, **Ayarla** sekmesini ve ardından **Ödeme yöntemleri**'ni seçin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Gezinti bölmesinde, istediğiniz bir ödeme yöntemini seçin.
1. **Genel** bölümünde bir **İşlem adı** belirtin ve istediğiniz diğer ayarları yapılandırın.
1. Ödeme türü için gereken ek ayarları yapılandırın.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde bir nakit ödeme yöntemi örneği gösteriliyor.

![Örnek ödeme yöntemleri](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a>Kasa bildirimini ayarlama

1. Eylem Bölmesi'nde, **Ayarla** sekmesini ve ardından **Kasa bildirimi**'ni seçin.
1. Eylem Bölmesi'nde, **Yeni**'yi seçin ve tüm mevcut **Bozuk para** ve **Banknot** para birimlerini oluşturun.

Aşağıdaki resimde bir kasa bildirimi örneği gösteriliyor.

![Kasa bildirimlerini ayarlama](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a>Teslimat şekillerini ayarla

Yapılandırılan teslimat şekillerini, Eylem Bölmesi'ndeki **Ayarla** sekmesinden **Teslimat şekilleri**'ni seçerek görebilirsiniz.  

Bir teslimat şekli eklemek veya değiştirmek için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Stok yönetimi \> Teslimat şekilleri**'ne gidin.
1. Eylem Bölmesi'nde, yeni bir teslimat şekli oluşturmak için **Yeni**'yi seçin veya varolan bir şekli seçin.
1. **Perakende kanalları** bölümünde, kanalı eklemek için **Satır ekle**'yi seçin. Kanalları tek tek eklemek yerine kuruluş düğümleri kullanarak eklemek, kanal eklemeyi kolaylaştırabilir.

Aşağıdaki resimde bir teslimat şekli örneği gösteriliyor.

![Teslimat şekillerini ayarla](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a>Gelir/gider hesabını ayarlama

Gelir/gider hesabını ayarlamak için bu adımları izleyin.

1. Eylem Bölmesi'nde, **Ayarla** sekmesini ve ardından **Gelir/Gider hesabı**'nı seçin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Ad** altında bir ad girin.
1. **Arama adı** altında bir arama adı girin.
1. **Hesap türü** altında bir hesap türü girin.
1. **İleti satırı 1**, **İleti satırı 2**, **İrsaliye metni 1** ve **İrsaliye metni 2** için metni gerektiği şekilde girin.
1. **Deftere nakil** altında, deftere nakil bilgilerini girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde bir gelir/gider hesabı örneği gösteriliyor.

![Gelir/gider hesaplarını ayarlama](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a>Bölümleri ayarlama

Bölümleri ayarlamak için bu adımları izleyin.

1. Eylem Bölmesi'nde, **Ayarla** sekmesini seçin ve ardından **Bölümler**'e tıklayın.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Bölüm numarası** altında bir bölüm numarası girin.
1. **Açıklama** altında bir açıklama girin.
1. **Bölüm boyutu** altında bir bölüm boyutu girin.
1. Gerekirse **Genel** ve **Satış istatistikleri** için ek ayarlar yapılandırın.
1. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="set-up-a-fulfillment-group-assignment"></a>Karşılama grubu atamasını ayarlama

Bir karşılama grubu ataması ayarlamak için bu adımları izleyin.

1. Eylem Bölmesi'nde, **Ayarla** sekmesini ve ardından **Karşılama grubu ataması**'nı seçin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Karşılama grubu** açılır listesinde bir karşılama grubu seçin.
1. **Açıklama** açılır listesinde bir açıklama girin.
1. Eylem Bölmesi'nde, **Kaydet**'i seçin

Aşağıdaki resimde, bir karşılama grubu ataması kurulum örneği gösterilmektedir.

![Karşılama grubu atamalarını ayarlama](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a>Kasaları ayarlama

Kasaları ayarlamak için bu adımları izleyin.

1. Eylem Bölmesi'nde, **Ayarla** sekmesini seçin ve **Kasalar**'a tıklayın.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Kasa için bir ad girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="ensure-unique-transaction-ids"></a>Hareket kodlarının benzersiz olduğundan emin olun

Commerce sürüm 10.0.18 itibariyle, satış noktası (POS) için oluşturulan hareket kodları sıralıdır ve aşağıdaki bölümleri içerir:

- Mağaza kodu ve terminal kodu birleşimi olan sabit bir bölüm. 
- Bir numara serisi olan sıralı bölüm. 

Biçim şöyledir: *{store}-{terminal}-{numbersequence}*. 

Hareket kodları hem çevrimdışı hem çevrimiçi modlarda oluşturulabildiğinden, oluşturulan hareket kodlarında yineleme olduğu görülmüştür. Yinelenen hareket kodlarının ortadan kaldırılması, uzun süren el ile veri düzeltmeyi gerektirir. 

Commerce sürüm 10.0.19 ile birlikte hareket kodu biçimi, sıralı bölümü kaldıracak şekilde güncelleştirilmiştir. Bunun yerine, 1970'den beri zamanı milisaniye cinsinde hesaplayarak oluşturulan 13 basamaklı bir sayı kullanır. Bu değişiklikle birlikte yeni hareket kodu biçimi şöyle olmuştur: *{store}-{terminal}-{millisecondsSince1970}*. Bu güncelleştirme, hareket kodunun sıralı olmamasını sağlar ve hareket kodlarının her zaman benzersiz olmasını sağlar. 

> [!NOTE]
> Hareket kodları yalnızca dahili sistem kullanımına yöneliktir, bu nedenle sıralı olmaları gerekmez. Ancak, birçok ülke giriş kodlarının sıralı olmasını gerektirir.

Yeni hareket kodu biçim özelliği, **Özellik yönetimi** çalışma alanından etkinleştirilebilir. 

Yeni hareket kodlarının kullanımını etkinleştirmek için şu adımları izleyin:

1. Commerce genel merkezinde, **Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**'ne gidin.
1. "Reatil ve Commerce" modülüne göre filtreleyin.
1. **Yinelenen hareket kodlarından kaçınmak için yeni hareket kodunu etkinleştir** özellik adını arayın.
1. Özelliği seçin, daha sonra sağ bölmede yer alan **Şimdi Etkinleştir**'i seçin.  
1. **Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.
1. Etkinleştirilen özelliği depolarla eşitlemek için **1070 Kanal yapılandırması** ve **1170 POS görev kaydedici** işlerini çalıştırın.
1. Değişiklikler mağazalara gönderildikten sonra, yeni hareket kodu biçiminin kullanılabilmesi için POS terminallerinin kapatılıp yeniden açılması gerekir. 

> [!NOTE]
> Yeni hareket kodu biçimi özelliği etkinleştirildikten sonra bu özelliği devre dışı bırakamazsınız. Devre dışı bırakılması gerekiyorsa lütfen Commerce destek ekibiyle iletişime geçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Kanallara genel bakış](channels-overview.md)

[Kanal kurulum önkoşulları](channels-prerequisites.md)

[Çevrimiçi kanal ayarlama](channel-setup-online.md)

[Çağrı merkezi kanalını ayarlama](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
