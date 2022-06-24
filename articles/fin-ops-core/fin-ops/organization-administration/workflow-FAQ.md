---
title: İş akışıyla ilgili SSS
description: Bu makalede, iş akışı sistemi hakkında sık sorulan sorular yanıtlanmaktadır.
author: ChrisGarty
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a72fd141bb1178a3a83385c512d1a655064d5b00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896593"
---
# <a name="workflow-faq"></a>İş akışıyla ilgili SSS

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Bu makalede, iş akışı sistemi hakkında sık sorulan sorular yanıtlanmaktadır.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Bir iş öğesi reddedildiğinde neden birden fazla uyarı alınır?
Bir iş öğesi reddedildiğinde, bu iş maddesi reddedildi olarak tamamlanır. Başka bir iş öğesi oluşturulur ve başlatıcıya atanır. Bu, reddedilen iş öğesi için başlatan bir uyarı olacağı ve ayrı bir uyarının, yeni "değişim talebi" iş öğesine atanan kullanıcıya gönderileceği anlamına gelir. 

Her bir uyarı farklı bir iş öğesi içindir, ancak benzerlik karışıklığa neden olabilir. Gelecekteki bir sürümde bunu iyileştirmenin yollarını arıyoruz.

## <a name="why-are-my-workflow-exports-failing"></a>İş akışı dışa aktarma işlemlerin neden başarısız oluyor?
İş akışı dışa aktarma özelliğinde, iş akışı adlarının 48 karakter sınırını aşmasını önleyen bir sınırlama vardır. 48 karakterden daha uzun bir ad kullanmak, "Sunucu isteği doğrulayamadı" hatasına neden olabilir ve/veya dosya türü olmadan bir dosyanın dışa aktarılmasını önleyebilir. [İş Akışı Dışa Aktarma Sorunlarını Giderme](https://community.dynamics.com/365/financeandoperations/b/elandaxdynamicsaxupgradesanddevelopment/posts/workflow-export-troubleshooting) blog gönderisinde daha fazla ayrıntı verilmektedir.

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Bir iş akışının sağlayıcısı da iş akışını onaylayabilir mi?
Evet, iş akışı bu şekilde yapılandırılırsa iş akışını da onaylayabilir. Bu davranışı engellemek için **Sistem yönetimi > İş akışı > İş akışı parametreleri > Genel > Onaylayan > Gönderen onayına izin verme**'yi **Evet** olarak ayarlayın–.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Kullanıcılara bildirim sağlamak için iş akışlarına uyarı ekleyebilir miyim?
Bildirim sağlamak amacıyla iş akışlarına uyarı ekleme hakkında dikkat edilecek bir kaç kilit alan şunlardır:
- Uyarılar ve iş akışı bildirim mekanizmaları
    - Kayıt değişiklikleri için uyarılar ayarlanabilir. İş akışları kayıtları değiştirir, bu nedenle bir iş akışının neden olduğu bir kayıt değişikliğiyle ilgili bir uyarı ayarlamak mümkündür. Ancak, iş akışlarının farklı yerleşik bildirim seçenekleri olduğundan, uyarılar kullanılması ideal değildir.
- İş akışlarından ilişkin standart bildirimler 
    - İş akışları yerleşik e-posta bildirimlerine sahiptir. Bir müşteri e-posta göndermek için bildirimleri yapılandırabilir. Bu bildirimler, kullanıcılar için Eylem Merkezi iletilerine neden olmaz.
    - Gelecekteki bir güncelleştirmede, kullanıcıya bir iş akışı iş maddesi atanacak bir İşlem Merkezi iletisi ekleyeceğiz. 
- İş akışına bildirim ekleme
    - X++içindeki bir iş akışından oluşturulan ileti gibi belirli kullanıcılar için işlem merkezi iletileri oluşturulabilir.
    - [İş Akışının İş Olayları](../../dev-itpro/business-events/business-events-workflow.md) Müşterinin Akışları tetiklemek için kullanabileceği, aradıkları bildirimlere sahiptir.   

Özetle, bir Kullanıcı bir iş akışı iş maddesi atandığında eylem merkezinden uygun bildirimi alamazsanız ek veya farklı bildirimler sağlamak için [İş Akışının iş olayları](../../dev-itpro/business-events/business-events-workflow.md) ile Microsoft Power Automate'u ek ya da farklı bildirimler sağlamak için kullanın.

## <a name="why-is-workflow-editor-not-able-to-start-under-ad-fs"></a>İş akışı düzenleyicisi AD FS altında niçin başlatılamıyor?
Yükseltilmiş bir ortamda Active Directory Federasyon Hizmetleri (AD FS) altında çalışırken, iş akışı Düzenleyicisi başlatılırken sorun olabilir. Varsa, ADFS ayarlarındaki **Microsoft Dynamics 365 for Operations şirket içi-iş akışı-yerel uygulama** özelliğine "https://dynamicsaxworkfloweditor/" URL'si eklenmiş olduğundan emin olun.

## <a name="why-am-i-getting-sql-deadlocks-on-workflow-processing"></a>İş akışı işlemede niçin SQL kilitlenmeleri alıyorum? 
**İş akışı parametreleri** sayfasındaki **toplu iş başına madde sayısı** için varsayılan alan değeri 0'dır. 0 değeri, varsayılan değerin toplu iş başına 20 öğe değiştirmesine neden olur. Toplu iş (> 40) başına yüksek sayıda madde SQL kilitlenmesine neden olabileceği için, bu değeri ayarlarken dikkatli olun.

## <a name="what-is-the-workflow-enhanced-error-feature"></a>İyileştirilmiş İş Akışı Hatası özelliği nedir?
10.0.13 sürümündeki Gelişmiş İş Akışı Hatası özelliği, farklı iş akışı hatalarının sınıflarını ayırt edebilmek için hata kodları ekler. Bildirilen hata iletileri, daha anlaşılır hale getirmek için küçük farklılıklar içerse de çoğunlukla benzer olacaktır.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
