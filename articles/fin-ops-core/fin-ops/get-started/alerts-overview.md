---
title: Uyarılara genel bakış
description: Bu konu uyarılar hakkında genel bilgileri sağlar. Uyarıları, iş günü sırasında izlemek istediğiniz olaylardan haberdar olmak için kullanabilirsiniz.
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: a42e836c0b72798de3375c169e45b121debd55ec
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191282"
---
# <a name="alerts-overview"></a>Uyarılara genel bakış

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a>Uyarılar hakkında
Uyarılar, sistemdeki kritik olaylar için bir bildirim sistemi oluşturur. Uyarıları, iş günü sırasında izlemek istediğiniz olaylardan haberdar olmak için kullanabilirsiniz. Vadesi geçen teslimatlar, silinmiş siparişler, değişen fiyatlar veya yanıtlamanız gereken diğer olaylar hakkında uyarılar almak için kendi kurallarınızı kolaylıkla oluşturabilirsiniz.

Kurumsal kaynak planlamasında (ERP), uyarı özelliklerinin kullanılabileceği bazı tipik senaryolar vardır. Burada bazı örnekler verilmiştir.

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a>Senaryo 1: Yeni satış siparişleri için bir uyarı kuralı oluşturun

1. **Tüm satış siparişleri** sayfasını açın.
2. Eylem Bölmesinde, **Seçenekler** sekmesindeki **Paylaş** grubunda **Özel uyarı oluştur**'u seçin.
3. **Uyarı kuralı oluştur** iletişim kutusunda **Beni uyarma zamanı** hızlı sekmesinde **Olay** alanında **Kayıt oluşturuldu**'yu seçin.

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a>Senaryo 2: Bir teslimat tarihinin ertelenmesi için bir uyarı kuralı oluşturun

1. **Tüm satınalma siparişleri** sayfasını açın.
2. Satınalma siparişi ayrıntılarına erişmek için bir satınalma siparişi kimliği seçin.
3. **Satın alma siparişi başlığı** hızlı sekmesini genişletin.
4. Eylem Bölmesinde, **Seçenekler** sekmesindeki **Paylaş** grubunda **Özel uyarı oluştur**'u seçin.
5. **Uyarı kuralı oluştur** iletişim kutusunda **Beni uyarma zamanı** hızlı sekmesinde **Alan** alanında **Teslimat tarihi**'ni seçin.
6. **Olay** alanında **ertelendi**'yi seçin.
    
**Uyarı kuralı oluştur** iletişim kutusunu kapattıktan sonra kuralınız, **Uyarı kurallarını yönet** sayfasında görünür. Mevcut uyarı kurallarınızı güncelleştirmek için **Uyarı kurallarını yönet** sayfasını kullanabilirsiniz. Örneğin, olay tetikleyicilerini değiştirebilir, olay bildirimlerini güncelleştirebilir ve bitiş tarihlerini güncelleştirebilirsiniz. **Uyarı kurallarını yönet** sayfasını açmak için Eylem Bölmesinin **Seçenekler** sekmesinde **Beni uyar** düğmesini kullanın.

## <a name="what-occurs-when-an-alert-rule-is-created"></a>Uyarı kuralı oluşturulduğunda ne olur?

Uyarı kuralları oluşturduğunuzda önceden tanımlanmış bir olayı belirli bir alanla ilişkilendirebilirsiniz. Örneğin, alanda belirtilen tarih geldiğinde veya alan içeriği değiştiğinde. Alternatif olarak, bir olayı belirli bir sayfadaki kayıtlarla ilişkilendirebilirsiniz. Örneğin, bir kayıt oluşturulur veya bir kayıt silinir.

Alan veya sayfadaki bir kayıt için seçilen olay gerçekleşirse bir uyarı gönderilir. Örneğin, belirli bir satınalma sipariş satırında **Teslimat tarihi** alanını **bu kadar süre önce sona erdi** olayıyla ilişkilendirdiğiniz bir kural oluşturun. Zaman dilimini beş gün olarak ayarlayın. Bu durumda, ilgili satınalma sipariş satırının teslimat tarihinden beş gün sonra bir uyarı gönderilir.

Ayrıca uyarı kurallarını koşullar ayarlayarak daraltabilirsiniz. Örneğin, belirli satıcı hesapları için oluşturulan yeni satınalma siparişleriyle ilgili uyarı alabilirsiniz.

## <a name="preparing-for-an-alert"></a>Uyarı için hazırlanma

Uyarı kuralını ayarlamadan önce, ne zaman ve hangi durumlarda uyarı almak istediğinize karar verin. Hangi olay hakkında bilgilendirilmek istediğinizi bildiğinizde, bu olaya neden olan verilerin göründüğü sayfayı bulun. Olay, gelecek bir tarih veya meydana gelen özel bir değişiklik olabilir. Bu nedenle, tarihin belirtildiği veya değişen alanın bulunduğu ya da oluşturulan yeni kaydın göründüğü sayfayı bulmanız gerekir. Bu bilgilere sahip olduktan sonra uyarı kuralını oluşturabilirsiniz.

## <a name="components-of-an-alert-rule"></a>Uyarı kuralının bileşenleri

Uyarı kuralının beş bileşeni vardır:

- **Olay**: Uyarı kuralını tetikleyen olay, gelecek bir tarih veya meydana gelen belirli bir değişiklik olabilir. Olayları, **Uyarı kuralı oluştur** iletişim kutusunun **İş durumu değişiklikleri için e-posta uyarıları gönder** hızlı sekmesinde tanımlarsınız.
- **Koşul**: **Uyarı kuralı oluştur** iletişim kutusunun **Beni uyar** hızlı sekmesinde, olaylar hakkında ne zaman uyarılacağınızı denetlemek üzere koşulun kapsamını seçebilirsiniz. Kuralı, yalnızca geçerli kayda veya sayfadaki tüm görünür kayıtlara uygulayabilirsiniz. Kural, tüzel kişiliklerde geçerliyse **Organizasyon çapında** seçeneğini **Evet** olarak ayarlayabilirsiniz.
- **Kuralın sona ermesi**: **Uyarı kuralı oluştur** iletişim kutusunun **Beni şu tarihe kadar uyar** hızlı sekmesinde, uyarı kuralının ne kadar süreyle etkin olacağını belirtebilirsiniz.
- **İçindekiler**: **Uyarı kuralı oluştur** iletişim kutusunun **Bana gönderilecek uyarı biçimi** hızlı sekmesinde, uyarı iletisinin kullanması gereken konu metnini ve ileti metnini belirtebilirsiniz.
- **Kullanıcı**: **Uyarı kuralı oluştur** iletişim kutusunun **Uyarılacaklar** hızlı sekmesinde, uyarı iletisini hangi kullanıcının alması gerektiğini belirtebilirsiniz. Varsayılan olarak kullanıcı kimliğiniz seçilir.

    > [!NOTE]
    > Bu seçenek, kuruluş yöneticileriyle sınırlıdır.

## <a name="email-notifications-from-alerts"></a>Uyarılardan e-posta bildirimleri

Uyarılardan e-posta bildirimleri henüz etkinleştirilmedi. Gelecekteki bir güncelleştirmede etkinleştirilecektir.

## <a name="videos"></a>Videolar

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a>Filtrelenmiş verileri izlemek için uyarıları kullanma

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3DWZ3]

[Filtrelenmiş verileri izlemek için uyarıları kullanma](https://youtu.be/ZYKMcv6kl9s) videosu (yukarıda gösterilir) YouTube'daki [Finance and Operations oynatma listesine](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) eklenmiştir.

### <a name="alert-rule-options"></a>Uyarı kuralı seçenekleri

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3E4PV]

[Uyarı kuralı seçenekleri](https://youtu.be/cpzimwOjicM) videosu (yukarıda gösterilen), YouTube'da bulunan [Finance and Operations oynatma listesinde](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) bulunmaktadır.


