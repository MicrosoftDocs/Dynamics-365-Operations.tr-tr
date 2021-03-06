---
title: Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (15 Kasım 2018)
description: Bu konuda, Microsoft Dynamics 365 Talent - Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a7598db1dc4c11864cf5f5a73d00672ceb66e8c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462822"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-15-2018"></a>Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (15 Kasım 2018)

**Derleme 8.1.2045**

Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.

## <a name="other-changesfixes"></a>Diğer değişimler/düzeltmeler

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>Personelin geçerli konumuna gelecekteki açık bir konuma değiştirilemiyor

Konum yalnızca gelecekte kullanılabilirse, konum transferlerine olanak sağlamak için bir değişiklik yapıldı. 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>Konum, yeni bir çalışan oluşturulduğunda görüntülenmiyor

Talent içinde yeni çalışanlar işe alırken atamaya açık konumları görüntülemek için bir değişiklik yapıldı. Bu, geçmişteki pozisyonları veya gelecek tarihteki konumları dahil etmektedir. Pozisyonlar artık çalışan başlangıç tarihinde şimdi doğru olarak görüntülenecektir. 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>İşe son verme tarihi kullanıcı ayarlarına dayalı olarak görüntülenir

İşe son verme tarihini görüntülerken tercih çalışanın tercih edilen zaman dilimini denk getirmek için geçmiş çalışan listesinde bir değişiklik yapıldı.

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>Bana atanmış çalışma öğeleri bağlantıları, doğru bilgiyi göstermiyor

Bu değişiklik ile, listede tekil iş öğelerinin ayrıntılarına gezinti, seçilen öğe için doğru bilgiyi gösterecektir. Bu sorun yalnızca gelişmiş güvenlik seçenekleri ile ortaya çıkmaktaydı.


## <a name="known-issue"></a>Bilinen sorun

- **Sorun**: Bir çalışan için yeni bir eki eklerken **Yeni** ve **Düzenle** düğmeleri gridir. 
- **Çözüm:** Ek sayfasını açmadan önce **Çalışan** sayfasındaki bilgi kutularının kapalı olduğundan emin olun. **Çalışan** sayfası yüklendiğinde bilgi kutuları kapalıysa, eklentiler düğmeleri etkinleştirilmiş olacaktır. (Bu sorun sonraki platform güncelleştirmesinde giderilecektir.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]