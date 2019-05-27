---
title: Ambar yönetiminde stoğu ilişkili işle birlikte taşıma
description: Bu konu bir mobil cihazdan parça çekme onayının nasıl ayarlanacağını ve uygulanacağını açıklamaktadır.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 618942ff22b6a81c75bd472955e4add14e6f4d84
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548872"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a>Ambar yönetiminde stoğu ilişkili işle birlikte taşıma

[!include [banner](../includes/banner.md)]

Stok hareketini kullanarak, hangi ambar çalışanlarının rezerve edilmiş stoku taşımaya izni olduklarına karar verebilirsiniz. Bu, bir çalışanın halihazırda oluşturulmuş olan bir çekme işi için yeni bir çekme konumu seçmesine izin vermemeyi seçtiğiniz, düzenlenmiş ambarlarda esneklik sağlar. Ayrıca, ambar yöneticilerinin, daha az deneyimli çalışanların hangi yeterliklere sahip olması gerektiğini kontrol etmesine yardım eder.

Ambar çalışanlarının günlük faaliyetlerini yönetme esnekliği, şu gibi senaryolarda yararlı olabilir:

## <a name="scenario-1"></a>Senaryo 1
Bir şirket, nispeten küçük bir alma bölgesine sahiptir ve bu alan, yerine koyulmayı bekleyen kutular ve paletlerle doludur. Geçerli gün içerisinde büyük bir sevkiyat beklenmektedir, bu yüzden de alma işinden sorumlu çalışanın, alma alanını bazı paletleri ikincil giriş hazırlama alanına taşıyarak yer açması gerekmektedir.

## <a name="scenario-2"></a>Senaryo 2
Deneyimli bir ambar çalışanı, maddeleri az miktarda yakında bulunan 3 farklı alana bölmektense, tek bir konumda birleştirme fırsatını fark eder. Çalışan, miktarı bu konumların her birinden aynı konuma ve aynı plakaya taşıyarak birleştirmek istemektedir.

## <a name="scenario-3"></a>Senaryo 3
Palet, hazırlama konumunda sevkiyatı beklemektedir; BAYDOOR01 yakınında bulunan STAGE01 gibi. Ancak, plandaki değişiklik sebebiyle, kamyonun BAYDOOR04'e varması planlanır. Sevk memuru bunun farkındadır ve kamyonun STAGE01 üzerinden yüklenmek için beklemesinden emin olması gerekir. Sevk memuru, sevkiyattaki maddeleri, STAGE01'den yeni hedefe daha yakın olan STAGE04'e taşımaya karar verir.

### <a name="current-limitations"></a>Geçerli sınırlamalar

Taşıyabileceğiniz iş rezervasyonları, satış siparişiyle, Transfer emri çıkışı, Transfer emri alış irsaliyesi, Satınalma siparişi ve Stok yenileme işi ile sınırlıdır.

İş satırlarının bölünmesini önlemek için maddelerin taşınması kısıtlanmıştır. Bu, Loc1 konumundaki A maddesinin 100 adetini içeren bir iş satırına sahipseniz, yalnızca 30 maddeyi A konumundan başka bir konuma taşıyamayacağınız anlamına gelir. Bu, konumların farklı olmasından dolayı mevcut iş satırının 30 ve 70 şeklinde parçalanmasına yol açar.

Maddeleri aldığınız plakanın, maddeleri taşıdığınız plakadan farklı olduğu, bir iş siparişi için Hedef LP olarak ayarlandığı hazırlama senaryoları için, Hedef LP'nin bölünmemesi için yalnızca tüm LP'nin taşınmasına izin verilir.
Şu anda yalnızca geçici hareket desteklenir. Bu da, rezerve edilmiş stoku, şablona göre taşıma mobil cihaz menü öğeleri aracılığıyla taşıyamayacağınız anlamına gelir.

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a>Tek tek çalışanlar için rezerve stoku taşıma izni ayarlayın

Rezerve edilmiş stoku taşımasına izin verilecek çalışan için **İlişkilendirilen iş ile stok taşınmasına izin ver** onay kutusunu **Ambar yönetimi** > **Kurulum** > **Çalışan** içerisinden seçin.  

### <a name="backported"></a>Backported

Bu özellik Microsoft Dynamics AX 2012 R3'e geri aktarılmıştır ve CU12'nin parçası olarak kullanılabilecektir.
KB numarası 3192548 ile tek olarak da indirilebilir. 

