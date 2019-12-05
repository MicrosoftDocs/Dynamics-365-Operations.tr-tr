---
title: İş akışı SSS
description: Bu konu, iş akışı sistemi hakkında sık sorulan soruları yanıtlamaktadır.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0188e8ed3cbbfd7dbccd7d13cf6129e146a919ac
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772709"
---
# <a name="workflow-faq"></a>İş akışıyla ilgili SSS

[!include [banner](../includes/banner.md)]

Bu konu, iş akışı sistemi hakkında sık sorulan soruları yanıtlamaktadır.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Bir iş öğesi reddedildiğinde neden birden fazla uyarı alınır?
Bir iş öğesi reddedildiğinde, bu iş maddesi reddedildi olarak tamamlanır. Başka bir iş öğesi oluşturulur ve başlatıcıya atanır. Bu, reddedilen iş öğesi için başlatan bir uyarı olacağı ve ayrı bir uyarının, yeni "değişim talebi" iş öğesine atanan kullanıcıya gönderileceği anlamına gelir. 

Her bir uyarı farklı bir iş öğesi içindir, ancak benzerlik karışıklığa neden olabilir. Gelecekteki bir sürümde bunu iyileştirmenin yollarını arıyoruz.

## <a name="why-are-my-workflow-exports-failing"></a>İş akışı dışa aktarma işlemlerin neden başarısız oluyor?
İş akışı dışa aktarma özelliğinde, iş akışı adlarının 48 karakter sınırını aşmasını önleyen bir sınırlama vardır. 48 karakterden daha uzun bir ad kullanmak, "Sunucu isteği doğrulayamadı" hatasına neden olabilir ve/veya dosya türü olmadan bir dosyanın dışa aktarılmasını önleyebilir. [İş Akışı Dışa Aktarma Sorunlarını Giderme](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting) blog gönderisinde daha fazla ayrıntı verilmektedir.

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Bir iş akışının sağlayıcısı da iş akışını onaylayabilir mi?
Evet, iş akışı bu şekilde yapılandırılırsa iş akışını da onaylayabilir. Bu davranışı engellemek için **İş akışı parametreleri > Genel > Onaylayan > Gönderen onayına izin verme**'yi **Evet** olarak ayarlayın–.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Kullanıcılara bildirim sağlamak için iş akışlarına uyarı ekleyebilir miyim?
Bildirim sağlamak amacıyla iş akışlarına uyarı ekleme hakkında dikkat edilecek bir kaç kilit alan şunlardır:
- Uyarılar ve iş akışı bildirim mekanizmaları
    - Kayıt değişiklikleri için uyarılar ayarlanabilir. İş akışları kayıtları değiştirir, bu nedenle bir iş akışının neden olduğu bir kayıt değişikliğiyle ilgili bir uyarı ayarlamak mümkündür. Ancak, iş akışlarının farklı yerleşik bildirim seçenekleri olduğundan, uyarılar kullanılması ideal değildir.
- İş akışlarından ilişkin standart bildirimler 
    - İş akışları yerleşik e-posta bildirimlerine sahiptir. Bir müşteri e-posta göndermek için bildirimleri yapılandırabilir. Bu bildirimler, kullanıcılar için Eylem Merkezi iletilerine neden olmaz.
    - Gelecekteki bir güncelleştirmede, kullanıcıya bir iş akışı iş maddesi atanacak bir İşlem Merkezi iletisi ekleyeceğiz. 
- İş akışına bildirim ekleme
    - X++içindeki bir iş akışından oluşturulan ileti gibi belirli kullanıcılar için işlem merkezi iletileri oluşturulabilir.
    - [İş Akışının İş Olayları](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) Müşterinin Akışları tetiklemek için kullanabileceği, aradıkları bildirimlere sahiptir.   

Özetle, bir kullanıcı kendisine bir iş akışı iş maddesi atandığında eylem merkezinden uygun bildirimi alamazsa ek veya farklı bildirimler sağlamak için [İş Akışı İş Olayları](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) ile Microsoft Power Automate'i ek ya da farklı bildirimler sağlamak için kullanır.
