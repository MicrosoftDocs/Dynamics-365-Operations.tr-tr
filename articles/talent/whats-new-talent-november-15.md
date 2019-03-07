---
title: Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (15 Kasım 2018)
description: Bu konuda, Microsoft Dynamics 365 for Talent Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0e9de5e36e67941ab09c773a63b0e7045105a07e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "306513"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a>Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (15 Kasım 2018)

[!include [banner](includes/banner.md)]

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
