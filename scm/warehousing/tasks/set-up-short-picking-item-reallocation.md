--- 
title: "Kısa alım maddesi yeniden tahsisini ayarlama"
description: "Bu yordam yönlendirildikleri konumda yeterli stok olmadığında alternatif konumları hızlı bir şekilde bulmak üzere ambar çalışanlarını etkinleştirmeyi gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: fedd815cddfea4e00ed61ec6e176b633468c8fb2
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-short-picking-item-reallocation"></a>Kısa alım maddesi yeniden tahsisini ayarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam yönlendirildikleri konumda yeterli stok olmadığında alternatif konumları hızlı bir şekilde bulmak üzere ambar çalışanlarını etkinleştirmeyi gösterir. Başka bir konumda kullanılabilen malları almak için konum yönergeleri kullanan otomatik yeniden tahsis işlemi kullanmak da mümkündür. Alternatif olarak, el ile yeniden tahsis kullanıldığında, kullanılabilir miktara sahip konumların listesi mobil cihazda görüntülenir ve ambar çalışanı stoğun kullanılacağı konumu seçebilir. Bu yordamı USMF demo veri şirketinde kullanabilirsiniz. Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="set-up-work-exceptions"></a>İş özel durumlarını ayarla
1. Ambar yönetimi > Kurulum > İş > İş özel durumları'na gidin.
2. Yeni'ye tıklayın.
    * Ambar çalışanının işledikleri sevkiyatın ihtiyaçlarına göre bir seçim yapabilmesi için, farklı madde yeniden tahsis ilkelerine sahip birden çok iş özel durumu tanımlamak mümkündür.  
3. İş özel durumu kodu alanına bir değer yazın.
    * İş özel durumuna ne için kullanıldığını belirten bir başlık verin. Örneğin, Kısa malzeme çekme kılavuzu.  
4. Açıklama alanına bir değer girin.
5. Özel durum türü alanında, 'Kısa çekme'yi seçin.
6. Stoğu ayarla onay kutusunu işaretleyin.
    * Bu seçenek stoğun kısa malzeme çekme konumunda 0'a otomatik olarak ayarlanacağı anlamına gelir.  
7. Varsayılan ayarlama türü kodu alanına bir değer girin veya bir değer seçin.
    * Örneğin, USMF'de 'Kaynak Res Adj Out' seçeneğini belirleyebilirsiniz.  
8. Madde yeniden tahsisi alanında 'El ile'yi seçin.
    * El ile veya Otomatik ve El ile seçeneklerini belirlerseniz, ambar çalışanının el ile yeniden tahsisi kullanmak için etkinleştirilmesi gerekir.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Çalışanı el ile madde yeniden tahsisini kullanmak üzere ayarlama
1. Sayfayı kapatın.
2. Ambar yönetimi > Kurulum > Çalışan'a gidin.
3. Düzenle öğesine tıklayın.
4. Listede, çalışan 24'ü seçin.
5. İş bölümünü genişletin.
6. El ile madde yeniden tahsisine izin ver alanında Evet'i seçin.


