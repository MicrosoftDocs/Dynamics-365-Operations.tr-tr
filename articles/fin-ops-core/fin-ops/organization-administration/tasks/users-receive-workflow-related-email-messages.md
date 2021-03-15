---
title: Kullanıcıların iş akışı ile ilgili e-posta iletileri almasını etkinleştirme
description: İş akışı ile ilgili olaylar gerçekleştiğinde, sistem kullanıcılara e-posta iletileri gönderecek şekilde yapılandırabilirsiniz.
author: jasongre
manager: AnnBe
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 221e38cbe31e2ad24a56cb2e71206a1ebcdd619e
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2020
ms.locfileid: "4799016"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Kullanıcıların iş akışı ile ilgili e-posta iletileri almasını etkinleştirme

[!include [banner](../../includes/banner.md)]

İş akışı ile ilgili olaylar gerçekleştiğinde, sistem kullanıcılara e-posta iletileri gönderecek şekilde yapılandırabilirsiniz. Örneğin, belgeler onay için kendilerine atandığında kullanıcılara e-posta iletileri gönderilebilir. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.

1. **Gezinti bölmesi > Modüller > Sistem yönetimi > Kullanıcılar > Kullanıcılar**'a gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. **Eylem bölmesi**'nde, **Kullanıcı seçenekleri**'ne tıklayın.
4. **İş akışı** sekmesine tıklayın. **Bildirimler** bölümünün genişletilmiş olduğundan emin olun. **Bildirimler** bölümünde, kullanıcının iş akışı ile ilgili olaylar hakkında nasıl bilgilendirilmesini istediğinizi belirtebilirsiniz.  
5. **Satır maddesi iş akışı bildirim türü** alanında bir seçenek belirleyin.
    - Gruplandırıldı: Satır maddeleri için bildirimler tek bir e-posta iletisine gruplandırılır.
    - Tek tek: Her satır maddesi için bir e-posta iletisi gönderilir.  
    - Kullanıcının, istemcide bildirimler almasını istiyorsanız **E-postada bildirimler gönder** onay kutusunu seçin.  
6. **Kaydet**'e tıklayın.
7. Sayfayı kapatın.

> [!NOTE]
> İş akışı e-posta şablonları, iş akışının sistem düzeyi (şirkete özel değil) veya organizasyon düzeyi (Şirket özel) iş akışı olmasına bağlı olarak, sistem e-posta şablonlarından veya kuruluş e-posta şablonlarından kaynakdan alınır.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]