--- 
title: "Üretim akışı modellerini tanımlama"
description: "Üretim akışı modelleri, yalın imalat iş hücrelerinin kapasitesinin nasıl hesaplanacağını ve sürdürüleceğini tanımlar."
author: cvocph
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlowModel
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7850a121ca06f25f6c532e49e18c0b6811bd7455
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="define-production-flow-models"></a>Üretim akışı modellerini tanımlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Üretim akışı modelleri, yalın imalat iş hücrelerinin kapasitesinin nasıl hesaplanacağını ve sürdürüleceğini tanımlar. Bu nedenle, bir üretim akışı modelinin tanımı iş hücrelerinin tanımının bir önkoşuludur. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="define-a-production-flow-model"></a>Bir üretim akışı modeli tanımlayın. 
1. Üretim kontrolü > Ayarlar > Yalın imalat akışı > Üretim akışı modelleri'ne gidin.
2. Yeni'ye tıklayın.
3. Üretim akışı modeli alanında üretim akışı modeli için bir kimlik girin.
4. Model türü alanında bir seçenek belirleyin.
    * İki model türü vardır: İş çıkarma yeteneği türü ve Saat türü. İş çıkarma yeteneği türü için, bu üretim akışı modelini kullanan iş hücrelerinin kapasitesi ürün miktarı olarak belirtilir ve hesaplanır. Saat türü için, bu üretim akışı modelini kullanan iş hücrelerinin kapasitesi saat olarak belirtilir ve hesaplanır. Bu özelliğin mevcut bir üretim akışı modeli için değiştirilemeyeceğini unutmayın. Bir iş hücresinin kapasite rezervasyonları olduğunda üretim akışı modeli türü değiştirilemez.  
5. EPE Döngüsü'nde gün sayısını girin.
    * Dönem aralığı, her bir parçanın bir üretim akışı tarafından üretileceği dönemi ya da en az bir iş hücresinin üretileceği dönemi tanımlar. EPE döngüsü ne kadar kısa olursa üretim süreci de o kadar esnek olur. EPE Döngüsü = 0 ise, tüm talepler aynı gün içinde üretilebilir. EPE Döngüsü, yalın süreçli işleri zamanlamak için kullanılır. EPE döngüsü = 5 olan bir iş hücresinde bir iş zamanlarken, zamanlama işlemi ürünün bu döngüde üretileceğinden emin olmak için Vade tarihi - EPE Döngüsü (vade tarihinin 5 gün öncesi) içindeki iş hücresinin kapasitesini göz önüne alır. Bir ürünün stok sağlama süresi genellikle ilgili üretim sürecinin EPE Döngüsü ile eşit veya bundan daha uzun olur.  
6. Dönem planlama türü alanında bir seçenek belirleyin.
    * Bir iş hücresinin kapasite rezervasyonları olduğunda planlama dönemi türü değiştirilemez. Yalnızca bu belirli iş hücresiyle aynı dönem türüne sahip üretim akışı modellerini seçebilirsiniz.  
7. Planlama zaman dilimi alanında bir sayı girin.
    * Planlama zaman dilimi, ilgili iş hücreleri için kapasite rezervasyonlarının gerçekleştirileceği gün sayısını tanımlar. Planlama zaman diliminde gün sayısını girin.   Bu dönemin dışında kalan Kanban süreci işleri otomatik planlama ile planlanmaz. Planlama zaman dilimi, bir üretim akışında veya iş hücresinde üretilen ürünlerin ortalama stok sağlama süresinden iki kat fazladır. EPE Döngüsü, planlama zaman diliminin yarısından fazla olmamalıdır.     
8. Kapasite eksikliğine tepki alanında bir seçenek belirtin.
    * Seçenekler şunlardır:   Erteleme - Etkinliği zamanlamaya ilişkin tam talebi uygun bir iş çıkarma yeteneğinin olduğu sonraki uygun bir üretim gününe erteleyin. İptal etme - Etkinliği zamanlamaya ilişkin otomatik zamanlamayı sonlandırın ve planlanmamış ilgili işleri olduğu gibi bırakın.   İstenen güne ekleme - İstenen işleri istenen bir dönemde yapılacak şekilde planlayın. Bu, hücreyi bu gün için aşırı yükler ve planlayıcının gözden geçirmesini ve el ile etkili etkileşime girmesini gerektirir.   Kullanılabilir dönemlere dağıt - Planlama etkinliğinin farklı işlerini tüm kullanılabilir üretim günlerine dağıt, kullanılabilir ilk günden başlayarak. Minimum dağıtım miktarı kanban iş miktarıdır. Dağıtım, minimum planlama miktarını (kanban miktarı) yeterince uygun iş çıkarma yeteneği olan her bir güne atar.  


