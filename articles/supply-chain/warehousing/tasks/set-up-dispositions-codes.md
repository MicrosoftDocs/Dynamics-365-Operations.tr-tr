---
title: Değerlendirme kodlarını ayarlama
description: Bu yordam, iade emri alma işlemi için mobil aygıtta kullanılabilecek bir değerlendirme kodunun kurulumuna odaklanır.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85402e05d55367da5fe89b242ad8eafc727b441e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558019"
---
# <a name="set-up-dispositions-codes"></a>Değerlendirme kodlarını ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, iade emri alma işlemi için mobil aygıtta kullanılabilecek bir değerlendirme kodunun kurulumuna odaklanır. Değerlendirme kodları, maddeler alındığında kullanılabilir kurallar topluluğudur. Örneğin, kullanıcı bir iş kullanıcısı zarar görmüş maddeleri almak için mobil aygıta kullandığında, bozuk öğeler için bir değerlendirme kodu taratmalıdır. Alınan malların stok durumu, iş şablonu ve yerleşim yönergesi taranan değerlendirme kodundan belirlenebilmektedir. Satınalma siparişi alma işlemi ve bitirilmiş bir işlem olarak üretim emri raporu için değerlendirme kodu kullanımı isteğe bağlıdır. Maddeler bir taşınabilir aygıt kullanarak kayıt edilmiş ise satış siparişi iade alma işlemi için değerlendirme kodu kullanımı zorunludur.  Bu kılavuz oluşturulurken USMF demo verisi şirketi kullanılmıştır. Bu yordam ambar yöneticisi için hazırlanmıştır. 

1. Ambar Yönetimi > Kurulum > Mobil aygıt > Değerlendirme kodları menüsüne gidin.
2. Yeni'ye tıklayın.
    * Müşteri iadelerinde kullanılmak üzere yeni bir değerlendirme kodu oluşturun.  
3. Değerlendirme kodu alanına bir değer girin.
4. Stok durumu alanında, stok durdurması olan bir stok durumu seçin.
    * USMF kullanıyorsanız, 'Durdurma'yı seçin. Sipariş satırlarında varsayılan durumu geçersiz kılmak için değerlendirme koduna bir stok durumu ekleyebilirsiniz.  
5. İş şablonu alanında bir değer girin.
    * İsteğe bağlı: bir iade emri ile ilişkilendirilmiş bir iş şablonu kodu seçin. Hiçbir değer sağlanmamışsa, iş şablonu, sisteminizdeki yapılandırılmış standart kurallar kullanılarak çözümlenir. İş şablonu seçmek bu değerlendirme kodunun birlikte kullanılabileceği işlemleri sınırlar. Örneğin bir değerlendirme kodunun, satın alma türünde iş emrine sahip bir çalışma şablonu varsa, bu müşteri tarafından iade edilen maddeleri kayıtta kullanılamaz.  
6. İade değerlendirme kodu alanına bir değer girin.
    * İade değerlendirme kodu, kayıt edilen maddeler için iade siparişi işleminin kalanını belirlemekte kullanılır. Bu örnekte, müşteri bir alacak dekontu almalıdır. Eylem kredisi içeren bir iade değerlendirme kodu ekleyin.  

