---
title: POS çevre birimleri ve hizmetleri için durum denetimi
description: Bu makale, satış noktasındaki (POS) sistem durumu denetimi işlemine genel bakış sağlar.
author: BrianShook
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 44fd4b6246d3d7947527416c2b8b447bd64f179f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863333"
---
# <a name="health-check-for-pos-peripherals-and-services"></a>POS çevre birimleri ve hizmetleri için durum denetimi

[!include [banner](includes/banner.md)]

Bu makale, satış noktasındaki (POS) sistem durumu denetimi işlemini açıklar.

## <a name="overview"></a>Özet

Perakende mağazalar, birçok uygulama ve cihazın kullanıldığı karmaşık ortamlar olabilir. İşlemler büyüdükçe, örneğin gün içinde bozulabilen veya kazara bağlantısı kesilen çevre birimleri gibi bağımlılıklar nedeniyle, işlemlerin her zaman sorunsuz çalışmasını sağlamak zor olabilir. Cihazlarla ve hizmetlerle ilgili sorunları giderme, büyük tüccarlar için maliyetli ve daha küçük işlemler için de aynı şekilde sinir bozucu olabilir.

Microsoft Dynamics 365 Commerce 10.0.10 ve sonraki sürümler, bu maliyet ve engellerin bir bölümünü önlemeye yardımcı olabilecek bir sistem durumu denetimi işlemi içerir. Bu işlem, cihazları normal işlemler dışında POS'tan doğrudan test etmek için bir yöntem sağlar. Bu nedenle, perakendecilerin sorunları ortaya çıkmadan önce saptamalarına yardımcı olabilir.

## <a name="key-terms"></a>Önemli terimler

| Vade | Tanım |
|---|---|
| Çevre birimi | POS uygulamasının hareketleri ve mağazadaki diğer işlemleri kolaylaştırmak için kullandığı herhangi bir cihaz. Örnekler arasında kasalar, barkod tarayıcıları ve ödeme terminalleri bulunur. |
| Servis | Bu makalede hizmet, POS uygulamasının hareketleri ve günlük işlemleri gerçekleştirmek için kullandığı yardımcı bir uygulamadır. Örnek olarak vergi veya sevkiyat hesaplamalarına yardımcı olan uygulamalar sayılabilir. |

## <a name="health-check-operation"></a>Sistem durumu denetimi işlemi

Sistem durumu denetimi işlemi, Commerce Headquarters'daki **POS İşlemleri** sayfasında yer alan 717 işlemidir. POS, kasa modunda olmadığında kullanılabilir. Ancak, bir donanım istasyonu etkin olmalıdır.

Varsayılan olarak, sistem durumu denetimi yalnızca, bir kayıt için etkin durumda olan donanım İstasyonu için donanım profilinde yapılandırılan cihazları sınar. Bir kayıt gün boyunca birden fazla donanım istasyonu kullanıyorsa, bunların tümünde sistem durumu denetimleri yapmak için bir seferde tek bir donanım istasyonuna bağlanılması gerekir. Mağaza düzeyinde sistem durumu denetimi yoktur. Ancak, bu tür bir denetimin Commerce Server genişletilebilirliği aracılığıyla gerçekleştirilmesi mümkündür.

### <a name="out-of-box-health-checks"></a>Kullanıma hazır sistem durumu denetimleri

| Türü | Bağlantı | Ayrıntılı |
|---|---|---|
| Yazıcı | OPOS | Bu denetim POS (OPOS) işlevleri için temel nesne bağlamayı ve katıştırmayı sınar. Burada bazı örnekler verilmiştir:<ul><li>Aç: **Aç** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Kapat: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Kapat**</li></ul> |
| Satır görüntüleme | OPOS | Bu denetim temel OPOS işlevlerini sınar. Burada bazı örnekler verilmiştir:<ul><li>Aç: **Aç** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Kapat: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Kapat**</li></ul> |
| Çift ekran | Windows | Bu denetim, işletim sisteminin ikinci bir Windows ekranı algılamasını sağlar. | 
| MSR | OPOS | Bu denetim temel OPOS işlevlerini sınar. Burada bazı örnekler verilmiştir:<ul><li>Aç: **Aç** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Kapat: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Kapat**</li></ul> |
| Keşideci | OPOS | Bu denetim temel OPOS işlevlerini sınar. Burada bazı örnekler verilmiştir:<ul><li>Aç: **Aç** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Kapat: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Kapat**</li></ul> | 
| Tarayıcı | OPOS | Bu denetim temel OPOS işlevlerini sınar. Burada bazı örnekler verilmiştir:<ul><li>Aç: **Aç** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Kapat: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Kapat**</li></ul> | 
| Ölçek | OPOS | Bu denetim temel OPOS işlevlerini sınar. Burada bazı örnekler verilmiştir:<ul><li>Aç: **Aç** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Kapat: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Kapat**</li></ul> |
| PIN pad | OPOS | Bu denetim temel OPOS işlevlerini sınar. Burada bazı örnekler verilmiştir:<ul><li>Aç: **Aç** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Kapat: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Kapat**</li></ul> |
| Ödeme terminali | Ödemeler SDK'sı | Bu denetim, Ödemeler SDK'sı tarafından sağlanan temel ödeme terminali işlevlerini sınar. <ul><li>Kilitle</li><li>BeginTransaction</li><li>EndTransaction</li><li>ReleaseDevice</li><li>Kapalı</li></ul> |

### <a name="using-the-health-check-operation-in-the-pos"></a>POS'ta sistem durumu denetimi işlemi kullanma

POS'ta sistem durumu denetimi işlemi başlatıldığında, sağdaki bir bölme yapılandırılmış cihazları listeler ve her cihazın durumunu gösterir. Tek bir cihaz için sistem durumu denetimi yapmak üzere cihazı ve ardından **Seçili olanı sına**'yı seçin. Tüm cihazlar için sistem durumu denetimi yapmak üzere **Tümünü sına**'yı seçin. **Tümünü sına** işlevi tüm cihazları tek tek test eder ve her cihazın **Durum** sütunundaki durumunu güncelleştirir.

**Son denetim** sütunu, her cihaz için sistem durumu denetiminin en son ne zaman yapıldığını gösterir.

Bir cihazın sistem durumu denetimi başarılı olursa (başka bir deyişle, hatayla karşılaşılmazsa), cihazın durumu **Tamam** olacaktır. Sistem durumu denetimi başarısız olursa, durum hata olduğunu belirtir. Bu durumda, sağdaki bölme hatayla ilgili ayrıntıları gösterir veya kullanıcıya sistem yöneticisine başvurmasını bildirir.

OPOS tuş kilidi gibi bazı cihazlarda kullanıma hazır sistem durumu denetimi testleri bulunmaz. Kullanılan herhangi bir cihaz için sistem durumu denetimi testi algılanmazsa, durum **Desteklenmiyor** olacaktır.

### <a name="extending-health-checks"></a>Sistem durumu denetimlerini genişletme

Kullanıma hazır sistem durumu denetimi testleri, tipik hatalar için kullanıcı dostu bazı iletiler sağlayacak şekilde yapılandırılmıştır. Ancak, tüm senaryoları kapsamaz. Genişletilebilirlik aracılığıyla, tüccarlar kullanıcı dostu iletileri ortamlarına özel olabilecek hatalarla eşleyebilir.

Ayrıca, kullanıma hazır olarak desteklenmeyen cihazları test etmek veya POS 'un bağımlı olduğu hizmetleri test etmek için özel durum denetimleri oluşturulabilir.

## <a name="related-articles"></a>İlgili makaleler

[Modern POS (MPOS) tetikleyicileri ve yazdırma](dev-itpro/pos-trigger-printing.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]