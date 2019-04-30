---
title: Personeli sabit ücret planına kaydetme
description: Tazminat ve kazançlar yöneticisi, personelin ödeme oranlarını yönetmek amacıyla, personeli sabit ücret planlarına atayabilir.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee0ba197ee47d2a2da2372b12291e5625ddc9ba1
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "859955"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>Personeli sabit ücret planına kaydetme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tazminat ve kazançlar yöneticisi, personelin ödeme oranlarını yönetmek amacıyla, personeli sabit ücret planlarına atayabilir. Bu prosedürde, sabit bir plan oluşturulduğu, planın etkin olduğu ve plan için uygunluk kurallarının ayarlandığı varsayılmaktadır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Prosedüre başlamak için İnsan Kaynakları > Çalışanlar > Personel > Ücret > Sabit plan'a gidin

1. Yeni'ye tıklayın.
2. Eylem alanında, personelin ücretindeki değişikliği açıklamak için, Kirala/Yeniden Kirala türünde bir Sabit ücret eylemi seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Posizyon alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listede, seçili satırdaki bağlantıya tıklayın.
    * Görüntülenen düzey, Pozisyondaki İşin Maaş Düzeyi'ndendir. Çalışana maaş atanabilmesi için önce İş üzerinde düzeyin ayarlanması gerekir.  
6. Plan alanında personel için sabit ücret planını seçin. Plan arama, yalnızca, Uygunluk kurallarına göre personelin uygun olduğu planları gösterecek biçimde filtre edilir.
7. Listede, istenen kaydı bulun ve seçin.
    * Maaşın Yürürlük ve Bitiş tarihlerinin varsayılan değerleri, çalışanın pozisyon atamasının başlangıç ve bitiş tarihlerinden alınır. Bu tarihleri gerektiği gibi ayarlayabilirsiniz.  
    * Sabit ücret planı bir adım planıysa, personel için doğru ödeme oranını içeren adım seçin. Sabit ücret planı bir kademeli plan veya bant planıysa, personel için doğru ödeme oranını girin. Ödeme oranı, planın toleransı ayarlarına ve iş maaş düzeyinin minimum maksimum referans noktalarına bakılarak doğrulanır.  
8. Tamam'a tıklayın.

