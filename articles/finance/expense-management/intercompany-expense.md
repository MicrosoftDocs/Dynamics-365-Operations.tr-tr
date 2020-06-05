---
title: Şirketlerarası giderler
description: Bir kuruluştaki bir tüzel kişilikte çalışan bir çalışan, aynı kuruluştaki başka bir tüzel kişilik için iş yapabilir. Bu durumda, şirketlerarası gider özelliğini, çalışanın giderini işin gerçekleştirildiği tüzel kişiliğe atamak için kullanabilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390896"
---
# <a name="intercompany-expenses"></a>Şirketlerarası giderler

[!include [banner](../includes/banner.md)]

Bir kuruluştaki bir tüzel kişilikte çalışan bir çalışan, aynı kuruluştaki başka bir tüzel kişilik için iş yapabilir. Bu durumda, şirketlerarası gider özelliğini, çalışanın giderini işin gerçekleştirildiği tüzel kişiliğe atamak için kullanabilirsiniz. Çalışanı çalıştıran tüzel kişilik, kiralayan tüzel kişilik olarak adlandırılır. Çalışanın gider oluşturduğu tüzel kişilik, ödünç alan tüzel kişilik olarak adlandırılır. 

Bir çalışan, kiralayan tüzel kişilikte farklı bir tüzel kişilik için gerçekleştiren işler için giderler oluşturmadan ve göndermeden önce, **Gider yönetimi parametreleri** sayfasında, **Şirketlerarası gider satırlarına izin ver** seçeneğini işaretleyin. 

## <a name="tax-posting-for-intercompany-expenses"></a>Şirketlerarası giderler için vergilerin deftere nakli

[!include [banner](../includes/banner.md)]

Gider raporunuza borç alan (hedef) tüzel varlık yerine borç veren (kaynak) tüzel varlıkla ilişkili vergi grupları kullanmak istiyorsanız bunu, Genel muhasebe satış vergisi kurulumunda yapılandırmanız gerekir. **Şirketlerarası vergilerin deftere nakli için tüzel varlık** Genel muhasebe parametresi **Kaynak** olarak ve **Satış vergisi vergilendirme kurallarını uygula** parametresi **Hayır** olarak ayarlandığında, borç veren tüzel varlığın vergi birleşimi kullanılır. Aynı parametre **Hedef** olarak ayarlandığında, borç alan tüzel varlığın vergi birleşimi kullanılır. Amerika Birleşik Devletleri'ndeki tüzel varlıklar için parametre **Kaynak** olarak ayarlandığında, **Satış vergisi alacakları** alanı da yeni **Genel muhasebe deftere nakil grupları** sayfasında yapılandırılmalıdır. Muhasebe altyapısı, vergi ile ilgili muhasebe girişi için bu alandaki bilgileri kullanır.   
Bu davranış, proje ile veya proje olmadan deftere nakledilen gider satırları için tutarlıdır.  
