--- 
title: "Maliyet nesnesi denetleyicisi için erişim haklarını yapılandırma"
description: "Bir maliyet nesnesi denetleyicisi için erişim haklarını yapılandırmak için bu yordamı kullanın."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 9c5f79b7d9d62b29f21f2ddd1f6507ff82b381cc
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="configure-access-rights-for-a-cost-object-controller"></a>Maliyet nesnesi denetleyicisi için erişim haklarını yapılandırma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bir maliyet nesnesi denetleyicisi için erişim haklarını yapılandırmak için bu yordamı kullanın. Bu kayıt USP2 demo veri şirketini kullanır.


## <a name="assign-the-cost-object-controller-role"></a>Maliyet nesnesi denetçi rolünü ata
1. Sistem Yönetimi > Kullanıcılar > Kullanıcılar'a git.
2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Kullanıcı adı alanını 'sibel' değeriyle filtreleyin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Rolleri ata'ya tıklayın.
5. Listede, istenen kaydı bulun ve seçin.
6. Tamam'a tıklayın.

## <a name="enable-access-list-security"></a>Erişim listesi güvenliğini etkinleştir
1. Maliyet muhasebesi > Boyutlar > Boyut hiyerarşileri'ne gidin.
2. Listede, istenen kaydı bulun ve seçin.
    * Kuruluşu seçin.  
3. Düzenle öğesine tıklayın.
4. Erişim listesi hiyerarşi alanında Evet'i seçin.
5. Hiyerarşiyi görüntüle düğmesini tıklayın.

## <a name="assign-access-rights-to-user"></a>Kullanıcıya erişim haklarını ata
1. Yeni'ye tıklayın.
2. Listede, seçili satırı işaretleyin.
3. Kullanıcı kimliği alanında bir değer girin veya bir değer seçin.
    * Yönetici seçin.  
4. Ağaçta 'Kuruluş\CEO\CFO\FIM' öğesini seçin.
5. Yeni'ye tıklayın.
6. Listede, seçili satırı işaretleyin.
7. Kullanıcı kimliği alanında bir değer girin veya bir değer seçin.
    * Sibel'i seçin.  
8. Kaydet'e tıklayın.

## <a name="enable-access-rights-in-cost-accounting"></a>Maliyet muhasebesinde erişim haklarını etkinleştir
1. Maliyet muhasebesi > Kurulum > Parametreler'e gidin.
2. Genel sekmesine tıklayın.
3. Maliyet nesnesi boyut üyeleri için görüntüleme erişimini etkinleştir alanında Evet'i seçin.
4. Kaydet'e tıklayın.
5. Sayfayı kapatın.
6. Maliyet muhasebesi > Kurulum > Maliyet denetimi çalışma alanı yapılandırması'na gidin.
7. Düzenle öğesine tıklayın.
8. Yayımlanan alanında Evet'i seçin.
    * Evet'i seçerseniz, aşağıdaki dört rolden birine atanmış bir kullanıcı Maliyet kontrolü çalışma alanındaki raporları görebilir: maliyet muhasebesi yöneticisi, maliyet muhasebecisi, maliyet muhasebe memuru ve maliyet nesnesi denetleyicisi. Hayır'ı seçerseniz, yalnızca aşağıdaki rollerden birine atanmış bir kullanıcı raporları görebilir: maliyet muhasebesi yöneticisi, maliyet muhasebecisi ve maliyet muhasebe memuru.    
9. Kaydet'e tıklayın.


