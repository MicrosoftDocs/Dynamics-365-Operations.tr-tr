---
title: Müşteri portalı kullanıcıları oluşturma ve yönetme
description: Bu konu, müşteri portalı Kullanıcı hesaplarının nasıl oluşturulacağını ve bunların izinlerinin nasıl ayarlanacağını açıklar.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: c56e41b8ea5039531205083b5b42aff05e05cf66
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/01/2020
ms.locfileid: "3414019"
---
# <a name="create-and-manage-customer-portal-users"></a>Müşteri portalı kullanıcıları oluşturma ve yönetme

Sistemde bulunmayan uygulamada, kullanıcıların müşteri portalı kullanılarak oluşturulan Web siteleri için kendi kendine kayıt yaptırmalarına olanak yoktur. Oturum açmak ve bir Web sitesini kullanmak için, kullanıcıların yönetici tarafından davet edilmeleri gerekir. Microsoft, kullanıcıların kendi kendine kayıt yapma becerisini kasıtlı olarak engellemiştir.

Bir kullanıcının bir Web sitesini kullanabilmesi için, o Kullanıcı için bir ilgili kişi kaydı oluşturulmalıdır. Bu kayıt kullanıcının hangi müşteri hesabı ve yasal tüzel kişiliye ait olduğunu gösterir. Bu bilgiler, kullanıcının satış siparişlerini oluşturup görüntüleyebilmesi için gereklidir.

Kullanıcılar kendi kendine kayıt yaptırtığı zaman, ilgili kişi kayıtları otomatik olarak oluşturulur. Bu nedenle, kullanıcının doğru müşteri hesabını ve yasal varlığı seçmesi için emin değilseniz. Diğer taraftan, davet işlemi bir yöneticinin davet gönderilmeden önce ilgili kişi kaydına doğru müşteri hesabını ve yasal varlığı atamasına olanak tanır. Çözümü kullanıcıların kendi kendine kaydolabilmesini sağlayacak şekilde özelleştirme konusunda düşünmeniz varsa, olası sonuçları göz önünde bulundurdığınızdan emin olun.

## <a name="prerequisite-setup"></a>Ön koşul kurulumu

Power Apps Portallarda bulunan ilgili kişiler , Common Data Service'deki **ilgili kişiler** varlığında kayıtlar olarak depolanır . Çift yaz daha sonra bu kayıtları gerektiği gibi Microsoft Dynamics 365 Supply Chain Management'a eşitler .

![![Müşteri Portalı ilgili kişilerinin sistem diyagramı](media/customer-portal-contacts.png "Müşteri Portalı ilgili kişilerinin sistem diyagramı")](media/customer-portal-contacts.png "System diagram for Customer portal contacts")

Yeni müşterileri davet etmeye başlamadan önce, **ilgili kişi** varlığı eşlemesini çift-yazılabilir olarak etkinleştirdiğinizden emin olun.

## <a name="the-invitation-process"></a>Davet işlemi

Varolan bir ilgili kişiyi müşteri portalına davet etmek için, Power Apps Portal belgelerindeki [ilgili kişileri portallarınıza davet etme](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts) adımlarını izleyin.

Müşteriyi müşteri portalına katılmaya davet etmeden önce, müşterinin [ilgili kişi kaydının](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) kullanılabilir olduğundan ve aşağıdaki şekilde ayarlandığından emin olun:

1. **Şirket** alanını Supply Chain Management'a ait olmasını istediğiniz müşterinin tüzel varlığı girin.
2. **Hesap Numarası** alanını Supply Chain Management'ta ait olmasını istediğiniz kullanıcının müşteri hesap numarasına girin.

İlgili kişi oluşturulduktan sonra, Supply Chain Management'tan bunu görebilmelisiniz.

Daha fazla bilgi için, Power Apps Portal belgelerindeki [bir portalda kullanılacak ilgili kişiyi konfigüre edin](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts).

## <a name="out-of-box-web-roles-and-entity-permissions"></a>Yerleşik Web rolleri ve varlık izinleri

Power Apps Portallarda Kullanıcı rolleri [Web rolleri](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) ve [varlık izinleri](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions) tarafından tanımlanır. Müşteri Portalı için birkaç rol tanımlanır. Yeni roller oluşturabilir, varolan rolleri değiştirebilir veya kaldırabilirsiniz.

### <a name="out-of-box-web-roles"></a>Yerleşik Web rolleri

Bu bölümde, müşteri portalı ile teslim edilen Web rolleri açıklanmaktadır.

Sistemde bulunmayan Kullanıcı rollerini değiştirme hakkında daha fazla bilgi için, Power Apps portal belgelerindeki [portallar için web rolleri oluştur](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) ve [Portallar için varlık izinlerini kullanarak kayıt tabanlı güvenlik ekleme](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions)'ye bakın.

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