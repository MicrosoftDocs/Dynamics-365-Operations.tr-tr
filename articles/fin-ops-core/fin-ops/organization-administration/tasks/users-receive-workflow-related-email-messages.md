---
title: Kullanıcıların iş akışı ile ilgili e-posta iletileri almasını etkinleştirme
description: İş akışı ile ilgili olaylar gerçekleştiğinde, sistem kullanıcılara e-posta iletileri gönderecek şekilde yapılandırabilirsiniz.
author: jasongre
manager: AnnBe
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a81e01c36081ce7131ee65344f583755fa3bfd3
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564202"
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