---
title: Personeli sabit ücret planına kaydetme
description: Tazminat ve kazançlar yöneticisi, personelin ödeme oranlarını yönetmek amacıyla, personeli sabit ücret planlarına atayabilir.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bd9c39bb3b5e221694fe20a8085c9099040cb422
ms.sourcegitcommit: a8ac6d9b63eb67d14dd17a086ef4f1eccd7f9fc1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/27/2021
ms.locfileid: "7431142"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>Personeli sabit ücret planına kaydetme

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tazminat ve kazançlar yöneticisi, personelin ödeme oranlarını yönetmek amacıyla, personeli sabit ücret planlarına atayabilir. Bu prosedürde, sabit bir plan oluşturulduğu, planın etkin olduğu ve plan için uygunluk kurallarının ayarlandığı varsayılmaktadır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Yordamı başlatmak için **İnsan kaynakları** > **Çalışanlar** > **Personel** > **Ücret** > **Sabit plan**'a gidin.

1. **Yeni**'ye tıklayın.
2. **Eylem** alanında, personelin ücretindeki değişikliği açıklamak için **İşe alma/Yeniden işe alma** türünde bir Sabit ücret eylemi seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. **Pozisyon** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listede, seçili satırdaki bağlantıya tıklayın.
    * Görüntülenen düzey, Pozisyondaki İşin Maaş Düzeyi'ndendir. Çalışana maaş atanabilmesi için önce İş üzerinde düzeyin ayarlanması gerekir.  
6. **Plan** alanında, personel için sabit ücret planını seçin. Plan arama, yalnızca, Uygunluk kurallarına göre personelin uygun olduğu planları gösterecek biçimde filtre edilir.
7. Listede, istenen kaydı bulun ve seçin.
    * Maaşın **Yürürlük** ve **Bitiş** tarihlerinin varsayılan değerleri, çalışanın pozisyon atamasının başlangıç ve bitiş tarihlerinden alınır. Bu tarihleri gerektiği gibi ayarlayabilirsiniz.  
    * Sabit ücret planı bir adım planıysa, personel için doğru ödeme oranını içeren adım seçin. Sabit ücret planı bir kademeli plan veya bant planıysa, personel için doğru ödeme oranını girin. Ödeme oranı, planın toleransı ayarlarına ve iş maaş düzeyinin minimum maksimum referans noktalarına bakılarak doğrulanır.  
8. **Tamam**'a tıklayın.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
