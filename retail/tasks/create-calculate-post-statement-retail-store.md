--- 
title: " Perakende mağazasına yönelik bir ekstre oluşturma, hesaplama ve deftere nakletme"
description: "Bu yordam bir mağaza için el ile ekstre oluşturma, hesaplama ve deftere nakletme adımlarını açıklar."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 60bcafffc922e6d57e52a5dff104a0fbb252f6ce
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a> Perakende mağazasına yönelik bir ekstre oluşturma, hesaplama ve deftere nakletme

[!include[task guide banner](../includes/task-guide-banner.md)]

Bu yordam bir mağaza için el ile ekstre oluşturma, hesaplama ve deftere nakletme adımlarını açıklar. Aynı görevler için yapılandırılabilecek toplu işler de vardır. Toplu işleri yapılandırma ve çalıştırmayla ilgili adımlar diğer konularda bulunabilir. Bu yordamı tamamlamak için POS'ta tamamlanan ve ardından Dynamics AX uygulamasına çekilen hareketleriniz olmalıdır. Bu kayıt USRT demo veri şirketini kullanır. Bu yordam, Microsoft Dynamics AX'e başvuru içerebilir. Dynamics AX'in artık Microsoft Dynamics 365 for Operations olarak adlandırıldığını unutmayın.

1. Tüm çalışma alanları > .. > Perakende mağazası mali öğeleri'ne gidin.
2. Yeni ekstre'ye tıklayın.
3. Mağaza numarası alanında, aramayı açmak için açılır menü düğmesine tıklayın.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Tamam'a tıklayın.
    * Kurulum grubunda, ekstreye hangi hareketlerin dahil edileceğini ve bunların ekstre satırlarında nasıl gruplandırılacağını denetleyen ayarlar bulunur. Kurulum grubunu açarak bu ayarları değiştirebilir veya varsayılanları kullanabilirsiniz.  
    * Ekstre yöntemi alanı ekstre satırlarının nasıl gruplandırılacağını belirtir.  
    * Ekstreyi yalnızca belirli bir personel üyesi ya da kayıt için hesaplamak istiyorsanız bir personel üyesi veya kayıt seçin.  
6. Kapanış yöntemi alanında bir seçenek seçin.
7. Ekstreyi hesapla'ya tıklayın.
8. Evet'i tıklatın.
    * Ekstreyi hesaplandıktan sonra, kullanılan her ödeme ve ekstre yöntemi için toplam tutarları içeren satırlar oluşturulmalıdır.  
    * Girilmesi veya güncelleştirilmesi gerekiyorsa her satıra sayılmış bir tutar girin. Sayılan alanı POS'ta yapılan kasa sayımlarından alınan tutarlarla doldurulur.  
9. Ekstreyi deftere naklet'e tıklayın.
10. Kapat’a tıklayın.
11. Perakende ve ticaret > Kanallar > Perakende mağaza finansmanları'na gidin.
12. Deftere nakledilen ekstreler sekmesine tıklayın.


