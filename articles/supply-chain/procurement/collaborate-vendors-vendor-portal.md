---
title: Satıcılarla Satıcı portalını kullanarak iş birliği yapın
description: Bu konu, satın alma aracılarının satın alma sipariş onay sürecinde dış satıcılarla iş birliği yapmak için Satıcı portalının nasıl kullanabileceğini açıklar. Bu bilgiler, Dynamics AX'in yalnızca Şubat 2016 &amp; Mayıs 2016 sürümleri için geçerlidir.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b263b7c4f44871f81e8dd753f702327893f00d86
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207152"
---
# <a name="collaborate-with-vendors-by-using-the-vendor-portal"></a>Satıcı portalını kullanarak satıcılarla iş birliği yapma

[!include [banner](../includes/banner.md)]

Bu konu, satın alma aracılarının satın alma sipariş onay sürecinde dış satıcılarla iş birliği yapmak için Satıcı portalının nasıl kullanabileceğini açıklar. Bu bilgiler, Dynamics AX'in yalnızca Şubat 2016 ve Mayıs 2016 sürümleri için geçerlidir.

Bu konudaki bilgiler, Dynamics AX'in yalnızca Şubat 2016 ve Mayıs 2016 sürümleri için geçerlidir. Yeni satıcı iş birliği işlevleri hakkında daha fazla bilgi için bkz. [Harici satıcılarla satıcı iş birliği](vendor-collaboration-work-external-vendors.md).  

Satıcı portalı, satınalma siparişi (PO) bilgilerinin değiş tokuşu için Microsoft Dynamics AX ile elektronik veri değişim (EDI) tümleştirmesi olamayan satıcılar için hedeflenir. Portal, satın alma aracılarının satıcıya PO göndermelerine ve doğrudan Dynamics AX'ten Onaylandı ya da Reddedildi yanıtı almalarına olanak tanır.  

İşlem, satıcıdan gelen bir onayın sipariş otomatik olarak onaylamasını sağlayacak şekilde yapılandırılabilir. Bu durumda takip yalnızca bazı durumlarda gerekli olacaktır: Bir sipariş reddedildiğinde veya bir satıcı onayı yanıt olarak kaydedildiyse ancak PO durumu onay sürecinde bir sorun nedeniyle **Onaylandı** olarak güncellemezse.

## <a name="po-confirmation-and-rejection"></a>Satınalma siparişi onayı ve reddi
PO'lar Dynamics AX'te hazırlanır. Durumu **Onaylandı** olan bir satınalma siparişiniz olduğunda, bunu satıcıya bir onay talebi oluşturarak gönderirsiniz. Satıcının ilgisini yeni bir PO'ya çekmek istiyorsanız, PO'yu e-postayla göndermek için yazdırma yönetimi sistemini de kullanabilirsiniz. PO Satıcı portalında görüntülenir ve satıcının onaylamak veya reddetmek için kullanabileceği bir seçenek içerir. Satıcı, PO'da yapılan değişiklikler gibi bilgileri bildirmek için açıklama da ekleyebilir.  

Satıcı portalında, satıcı sipariş satırlarını görebilir. Bu satırlar harici ürün numarası, boyutlar, fiyat bilgileri, miktar, teslim tarihi ve teslimat adresi gibi bilgileri içerir. Satıcı PO bilgilerini ve toplam fiyatı gösteren bir rapor oluşturabilir. Satıcıyla ilgili giderler, satıcı başlık veya satırlardaki **Giderler** düğmesine tıkladığında görüntülenir. Satıcıları PO bilgilerini kendi sistemine **Excel'e aktar** işlevini kullanarak alabilir.  

Aşağıdaki tabloda, satıcının onay için PO gönderdiğinizde nasıl yanıt vereceğine bağlı olarak, tipik bilgi alışverişi gösterilmektedir.

| Yanıt tipi                                                                                                  | Sonuç                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Satıcı siparişi onaylar. Sistem, satıcı onayladığında PO'ları otomatik olarak onaylayacak şekilde yapılandırılmıştır.    | Siparişin durumu **Onaylandı** olarak güncellenir. Herhangi bir şey siparişin güncellenmesini engellerse, satıcı yanıtı yine de **Onaylandı** olarak kaydedilir ancak PO'nun durumu **Dış İncelemede** olarak kalır.                                                                       |
| Satıcı siparişi onaylar. Sistem, satıcı onayladığında PO'ları otomatik olarak onaylayacak şekilde yapılandırılmamıştır. | Satıcı yanıtı **Onaylandı** olarak kaydedilir ancak PO'nun durumu **Dış İncelemede** olarak kalır.                                                                                                                                                                                      |
| Satıcı siparişi reddeder.                                                                                     | Satıcı yanıtı **Reddedildi** olarak kaydedilir ve PO'nun durumu **Dış İncelemede** olarak kalır. Reddetme, bir neden ve alternatif teslim tarihi gibi bir değişiklik önerisiyle birlikte alınır. PO'yu güncelleyip yeni sürümü onay için gönderirsiniz. |

## <a name="changes-to-a-po"></a>PO değişiklikleri
Önceden onaylanmış bir PO'yu değiştirmeniz gerektiğinde, yeni PO'yu satıcıya Satıcı portalı aracılığıyla gönderebilirsiniz. Yeni SS'de önceden gönderilen SS'nin değiştirilmiş bir sürümü olduğunu belirtmek için bir sürüm soneki bulunur. Satıcı portalı satıcılara her siparişin geçmişini izleme olanağı sunar. Yeni PO onaylanana kadar, PO'nun önceden onaylanan sürümü onaylanan PO'lar listesinde kalmaya devam eder.  

Bir PO'yu iptal ettiğinizde durum yeniden **Onaylandı** olarak değiştirilir. Satıcının iptali onaylayabilmesi veya reddedebilmesi için PO'yu Satıcı portalı üzerinden satıcıya tekrar göndermeniz gerekir. İptal onaylandıktan sonra, SS satıcının onaylanan SS listesinde **İptal edildi** olarak görünür.

## <a name="versions-status-transitions-and-change-management"></a>Sürümler, geçiş durumları ve değişiklik yönetimi
PO satıcıya gönderildiğinde, sistemde satın alma siparişinin belirli bir sürümü olarak kaydedilir ve durumu **Onaylandı** yerine **Dış İncelemede** olarak değişir. PO daha sonra değiştirilirse, PO'nun yeni bir sürümü oluşturulur ve durumu tekrar **Onaylandı** olarak değiştirilir (veya değişiklik yönetimi etkin olduğunda durum **Taslak** olarak değişir).  

Aşağıdaki tablo, PO'nun geçebileceği durum ve sürüm değişikliklerine bir örnek gösterir.

| Eylem                                                   | Durum ve sürüm                                                                                    |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| PO başlangıç sürümü Dynamics AX'de oluşturulur. | Durum **Onaylandı** .                                                                           |
| PO Satıcı portalına gönderildi                     | Satıcı portalında bir sürüm kaydedilir ve durum **Dış İncelemede** olarak değiştirilir.    |
| Satıcı tarafından istenen bazı değişiklikler yaparsınız.  | Durum tekrar **Onaylandı** olarak değiştirilir.                                                            |
| Satıcı portalına PO'nun yeni sürümünü gönderirsiniz. | Satıcı portalında yeni sürüm kaydedilir ve durum **Dış İncelemede** olarak değiştirilir. |
| Satıcı PO'nun yeni sürümünü onaylar.           | Durum **Onaylandı** olarak değişir.                                                                |

Satıcıya gönderilen PO sürümlerini ve yanıtları görmek için satın alma siparişinden **Günlükler** &gt; **Onay istekleri**'ne tıklayın.  

Bir yanıt için satıcıya gönderilen ve durumu **Dış İncelemede** olan siparişler **Satıcı portalına gönderilen, yanıt bekleyen satınalma siparişleri** veya **Satıcı portalına gönderilen, eylem gerektiren satınalma siparişleri** listesinde görünür. Satıcıya gönderilmiş olan bir siparişte değişiklik yaptığınızda, durum **Onaylandı** olarak değişir ve sipariş artık bu listelerde görüntülenmez. Sipariş için daha önce satıcıdan gelen bir yanıt olup olmadığını görüntülemek için **Günlükler** &gt; **Onay istekleri**'ne tıklayın.  

Satıcılar, PO'yu Satıcı portalından onaylamak zorunda değildir. E-posta iletisi gönderebilir veya PO'yu kabul ettiklerini başka kanallar aracılığıyla bildirebilirler. Dynamics AX'de siparişi el ile onaylayabilirsiniz. Bu durumda, satıcıdan yanıt olmasa bile siparişin onaylandığını belirten bir uyarı alırsınız. Daha sonra PO Satıcı portalındaki onay geçmişinde herhangi bir yanıt alınmamış açık onaylanmış sipariş olarak görünür. Ayrıca, satıcının artık PO'yu onaylama veya reddetme seçeneği yoktur.  

**Not:** Dynamics AX'de diğer işlemler için kullanılabilir durumda olan PO sürümü, bu sürüm kaydedilmemiş olsa bile, daima en son sürümdür.

### <a name="change-management"></a>Değişiklik yönetimi

Bir PO için değişiklik yönetimini açtıysanız, PO **Onaylandı** durumuna gelmek için bir onay iş akışından geçer. Bu işlem satıcı tarafından görülmez.  

PO için değişiklik yönetimi açıldığında, sürüm PO satıcıya gönderildiği veya doğrulandığı zaman değil, onaylandığı zaman kaydedilir.  

Aşağıdaki tablo, değişim yönetimi etkinleştirildiğinde PO'nun geçebileceği durum ve sürüm değişikliklerine bir örnek gösterir:


|                                                    Eylem                                                     |                                                                                                                                                                                                                      Durum ve sürüm                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           PO başlangıç sürümü Dynamics AX'de oluşturulur.                            |                                                                                                                                                                                                            Durum <strong>Taslak</strong>'tır.                                                                                                                                                                                                             |
| PO onay işlemine yeniden gönderilir. (Bu satıcının içinde bulunmadığı dahili bir işlemdir.) |                                                                                                                        PO onay işlemi sırasında reddedilmediyse, durum <strong>Taslak</strong> yerine <strong>İncelemede</strong> ve <strong>Onay</strong> olarak değiştirilir. Onaylanan PO bir sürüm olarak kaydedilir.                                                                                                                        |
|                                      PO tedarikçi Portalı'na gönderildi                                      |                                                                                                                                                                      Sürüm Satıcı portalında kaydedilir ve durum <strong>Dış İncelemede</strong> olarak değiştirilir.                                                                                                                                                                       |
|                            Satıcı tarafından istenen bazı değişiklikler yaparsınız.                            |                                                                                                                                                                                                    Durum tekrar <strong>Taslak</strong> olarak değiştirilir.                                                                                                                                                                                                     |
|                              PO yeniden onay işlemine gönderilir.                               | SS onay işlemi sırasında reddedilmediyse, durum <strong>Taslak</strong> yerine <strong>İncelemede</strong> ve <strong>Onay</strong> olarak değiştirilir. Alternatif olarak, sistem belirli alandaki değişikliklerin yeniden onaylanması gerekmez şeklinde yapılandırılabilir. Bu durumda, durum önce <strong>Taslak</strong> olur ve ardından otomatik olarak <strong>Onaylandı</strong> şeklinde güncellenir. Onaylanan PO yeni bir sürüm olarak kaydedilir. |
|                           Satıcı portalına PO'nun yeni sürümünü gönderirsiniz.                            |                                                                                                                                                                    Yeni sürüm Satıcı portalında kaydedilir ve durum <strong>Dış İncelemede</strong> olarak değiştirilir.                                                                                                                                                                     |
|                                Satıcı PO'nun yeni sürümünü onaylar.                                 |                                                                                                                                                     Durum otomatik olarak veya satıcıdan yanıt alıp PO'yu onayladığınızda <strong>Onaylandı</strong> olarak değişir.                                                                                                                                                     |

<a name="additional-resources"></a>Ek kaynaklar
--------

[Satıcı portal kullanıcı güvenliği](configure-security-vendor-portal-users.md)

[Satıcı iş birliği faturalama çalışma alanı](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md)



