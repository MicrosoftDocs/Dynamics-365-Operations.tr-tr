--- 
title: "Tüzel kişilikler arasında sabit kıymet amortismanı hesaplama"
description: "Bu yordam, birden fazla tüzel kişilik için amortisman işlemini nasıl ayarlayacağınızı ve çalıştıracağınızı gösterir."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 4c45da124136b7fecb916d2ff9098c8ffeff6cb1
ms.contentlocale: tr-tr
ms.lasthandoff: 11/02/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Tüzel kişilikler arasında sabit kıymet amortismanı hesaplama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Sabit kıymet amortismanı tüzel kişilikler arasında tek bir adımda çalıştırılabilir. Bu yordam, birden fazla tüzel kişilik için işlemi nasıl ayarlayacağınızı ve çalıştıracağınızı gösterir. Muhasebeci rolünü kullanır.  

Bu kayıtta USMF demo şirketi kullanılmaktadır.


Adımlar (16) Alt görev: Şirketler arası amortisman çalıştırma günlüklerini ayarlayın. 

1. İlk olarak, her tüzel kişilikte şirketler arası amortisman çalıştırmada kullanılacak günlükleri ayarlamanız gerekir. Sabit kıymetler > Kurulum > Sabit kıymet parametreleri'ne gidin. 
2. Sabit kıymet teklifleri bölümünü genişletin. 
3. Tüzel kişilikteki her deftere nakil katmanı için kullanılacak günlük adıyla bir kayıt oluşturun. Defterler genel muhasebeye nakledilmezse, ilişkilendirilen günlükle Hiçbiri deftere nakil katmanının seçilmesi gerekir. Ekle öğesini tıklatın. 
4. Deftere nakil katmanı alanında bir değer girin veya bir değer seçin. 
5. Günlük adı alanına bir değer girin veya seçin. 
6. Her tüzel kişilik için Sabit kıymet parametreleri sayfasında günlük kurulumunu yineleyin. 

Alt görev: Amortismanı hesaplama

1. Tüzel kişilikler arasında amortisman çalıştırmayı başlatmak için Amortisman teklifi oluştur sayfasını kullanın. Sabit kıymetler > Günlük girişleri > Amortisman tekifi oluştur'a gidin. 
2. Deftere nakil katmanı alanında bir değer girin veya bir değer seçin. 
3. Günlük adı varsayılan olarak Sabit kıymet parametrelerinden alınacaktır. Burada geçerli tüzel kişilik için değiştirilebilir. 
4. Bitiş tarihi alanına bir tarih girin. 
5. Amortisman çalıştırmaya dahil edilecek tüzel kişilikleri seçin. Yalnızca Sabit kıymet parametreleri sayfasında Sabit kıymet teklifleri için ayarlanan günlükleri bulunan tüzel kişilikler listede görüntülenir. 
6. Etkinleştirildiğinde, Günlükleri deftere naklet seçeneği amortisman günlüklerini oluşturuldukları zaman otomatik olarak nakleder. Seçili değilse, günlükler oluşturulur ancak deftere nakledilmez, böylece deftere nakletmeden önce ayrıntıları inceleyebilirsiniz. Günlükleri deftere naklet alanında Evet'i seçin. 
7. Filtreleme alanları, bu amortisman çalıştırma için seçilen tüzel kişiliklerle ilgili tüm sabit kıymetleri, grupları ve defterleri içerir. 
8. Toplu işleme seçeneği varsayılan olarak etkindir. Bu seçenek etkinleştirildiğinde, amortisman günlüğü oluşturma ve deftere nakletme arka planda çalışır. 
9. Günlük oluştur'a tıklayın. 
10. İlgili tüzel kişiliklerde oluşturulan amortisman günlüklerini görüntülemeniz gerekir. Sabit kıymetler > Günlük girişler > Sabit kıymetler günlüğü'ne gidin.

