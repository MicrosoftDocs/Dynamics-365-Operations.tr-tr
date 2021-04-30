---
title: Müşteri portalı kullanıcıları oluşturma ve yönetme
description: Bu konu, müşteri portalı Kullanıcı hesaplarının nasıl oluşturulacağını ve bunların izinlerinin nasıl ayarlanacağını açıklar.
author: dasani-madipalli
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 453c6f18c689bb8bf2f6208d9181b23a2792f41a
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907777"
---
# <a name="create-and-manage-customer-portal-users"></a>Müşteri portalı kullanıcıları oluşturma ve yönetme

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Sistemde bulunmayan uygulamada, kullanıcıların müşteri portalı kullanılarak oluşturulan Web siteleri için kendi kendine kayıt yaptırmalarına olanak yoktur. Oturum açmak ve bir Web sitesini kullanmak için, kullanıcıların yönetici tarafından davet edilmeleri gerekir. Microsoft, kullanıcıların kendi kendine kayıt yapma becerisini kasıtlı olarak engellemiştir.

Bir kullanıcının bir Web sitesini kullanabilmesi için, o Kullanıcı için bir ilgili kişi kaydı oluşturulmalıdır. Bu kayıt kullanıcının hangi müşteri hesabı ve yasal tüzel kişiliye ait olduğunu gösterir. Bu bilgiler, kullanıcının satış siparişlerini oluşturup görüntüleyebilmesi için gereklidir.

Kullanıcılar kendi kendine kayıt yaptırtığı zaman, ilgili kişi kayıtları otomatik olarak oluşturulur. Bu nedenle, kullanıcının doğru müşteri hesabını ve yasal varlığı seçmesi için emin değilseniz. Diğer taraftan, davet işlemi bir yöneticinin davet gönderilmeden önce ilgili kişi kaydına doğru müşteri hesabını ve yasal varlığı atamasına olanak tanır. Çözümü kullanıcıların kendi kendine kaydolabilmesini sağlayacak şekilde özelleştirme konusunda düşünmeniz varsa, olası sonuçları göz önünde bulundurdığınızdan emin olun.

## <a name="video"></a>Görüntü
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ADkI]

[Müşterileri müşteri portalınıza kaydolup kullanmaya davet etme](https://youtu.be/drGUYHX9QIQ) videosu (yukarıda gösterilen) YouTube'daki [Finance and Operations oynatma listesine](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) eklenmiştir.

## <a name="prerequisite-setup"></a>Ön koşul kurulumu

Power Apps portallarında bulunan ilgili kişiler, Microsoft Dataverse'teki **İlgili kişiler** tablosunda kayıtlar olarak depolanır. Çift yaz daha sonra bu kayıtları gerektiği gibi Microsoft Dynamics 365 Supply Chain Management'a eşitler .

![Müşteri Portalı ilgili kişilerinin sistem diyagramı](media/customer-portal-contacts.png "Müşteri Portalı ilgili kişilerinin sistem diyagramı")

Yeni müşterileri davet etmeye başlamadan önce, **İlgili kişi** tablosu eşlemesini çift yazılabilir olarak etkinleştirdiğinizden emin olun.

## <a name="the-invitation-process"></a>Davet işlemi

Varolan bir ilgili kişiyi müşteri portalına davet etmek için, Power Apps Portal belgelerindeki [ilgili kişileri portallarınıza davet etme](/powerapps/maker/portals/configure/invite-contacts) adımlarını izleyin.

Müşteriyi müşteri portalına katılmaya davet etmeden önce, müşterinin [ilgili kişi kaydının](/powerapps/maker/portals/configure/configure-contacts) kullanılabilir olduğundan ve aşağıdaki şekilde ayarlandığından emin olun:

1. **Şirket** alanını Supply Chain Management'a ait olmasını istediğiniz müşterinin tüzel varlığı girin.
2. **Hesap Numarası** alanını Supply Chain Management'ta ait olmasını istediğiniz kullanıcının müşteri hesap numarasına girin.

İlgili kişi oluşturulduktan sonra, Supply Chain Management'tan bunu görebilmelisiniz.

Daha fazla bilgi için, Power Apps Portal belgelerindeki [bir portalda kullanılacak ilgili kişiyi konfigüre edin](/powerapps/maker/portals/configure/configure-contacts).

## <a name="out-of-box-web-roles-and-table-permissions"></a>Kullanıma hazır web rolleri ve tablo izinleri

Power Apps portallarında kullanıcı rolleri [web rolleri](/powerapps/maker/portals/configure/create-web-roles) ve [tablo izinleri](/powerapps/maker/portals/configure/assign-entity-permissions) tarafından tanımlanır. Müşteri Portalı için birkaç rol tanımlanır. Yeni roller oluşturabilir, varolan rolleri değiştirebilir veya kaldırabilirsiniz.

### <a name="out-of-box-web-roles"></a>Yerleşik Web rolleri

Bu bölümde, müşteri portalı ile teslim edilen Web rolleri açıklanmaktadır.

Kullanıma hazır kullanıcı rollerini değiştirme hakkında daha fazla bilgi için Power Apps portalları belgelerindeki [Portallar için web rolleri oluşturma](/powerapps/maker/portals/configure/create-web-roles) ve [Portallar için tablo izinlerini kullanarak kayıt tabanlı güvenlik ekleme](/powerapps/maker/portals/configure/assign-entity-permissions) makalelerini inceleyin.

#### <a name="administrator"></a>Yönetici

Yönetici Web sitesini geçersiz görür ve bakımını yapar. Bu kişi müşteri portalını hazırlayacaktır ve ayarlar. Yönetici portalın BT ve güvenlik yönlerini korur ve herşeyin sorunsuz çalışmasına neden olur. Yönetici ayrıca yeni işlevler ekleyerek, yeni roller oluşturarak portalı özelleştirebilir ve/veya değiştirebilir.

#### <a name="customer-representative"></a>Müşteri temsilcisi

Müşteri temsilcisi bir müşteri şirketi için çalışır ve şirketin yer aldığı siparişlerin yönetiminden sorumludur. Müşteri temsilcisi, şirket ve kendilerine yerleştirilen kullanıcılar için verilen tüm siparişleri görebilir. Ek olarak, müşteri temsilcisi, söz konusu hesap adına hangi ilgili kişilerin sipariş koyabileceği ile ilgili bilgileri de görebilir.

#### <a name="authorized-users"></a>Yetkilendiren kullanıcılar

Yetkili kullanıcılar sipariş verebilir ve bulundukları siparişlerin durumunu görüntüleyebilir. Ancak, şirketlerinde diğer kullanıcıların yerleştirdiği siparişlerin durumunu görüntüleyemez.

#### <a name="unauthorized-users"></a>Yetkisiz kullanıcılar

Yetkisiz kullanıcılar hiçbir veriyi görüntüleyemez. Bunlar, hüküm ve koşullar gibi yalnızca genel bilgileri ve müşteri portalını çalıştıran şirketle ilgili ayrıntıları görebilirler.

#### <a name="example"></a>Örnek

Aşağıdaki tabloda, her bir Web rolündeki kullanıcıların sistemde hangi satış siparişlerini görebileceği gösterilmektedir.

| Satış siparişi | Yönetici | Müşteri X için müşteri&nbsp;temsilcisi | Yetkilendiren kullanıcı: Jane | Yetkilendiren kullanıcı: Sam | Yetkisiz kullanıcı: May |
|---|---|---|---|---|---|
| Müşteri&nbsp;X sipariş veren: &nbsp;Jane | Evet | Evet | Evet | No | No |
| Müşteri&nbsp;X sipariş veren: &nbsp;Sam | Evet | Evet | No | Evet | No |
| Müşteri&nbsp;Y Sipariş veren: &nbsp;May | Evet | No | No | No | No |

> [!NOTE]
> Hem Sam, hem Jane, müşteri X için çalışan ilgili kişiler olmakla birlikte, yalnızca kendilerinin yerleştirdikleri siparişleri görebilir, başka birşey görmez. May'in sistemde bir siparişi olsa da, yetkisi olmayan bir kullanıcı olduğu için müşteri portalında o siparişi göremeyebilir. (Ek olarak, siparişi müşteri portalı dışında bir kanala yerleştirmiş olmalıdır.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]