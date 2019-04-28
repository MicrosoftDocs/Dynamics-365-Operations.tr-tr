---
title: Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (10 Eylül 2018)
description: Bu konuda, Microsoft Dynamics 365 for Talent Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: 6682e4d013f006696b45e644b7b4861b34faa9bf
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "857419"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a>Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (10 Eylül 2018)

[!include [banner](includes/banner.md)]

**Derleme 8.1.138.0**

Bu konuda, Microsoft Dynamics 365 for Talent Core HR'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>İzin isteklerinde günün belirli zamanına izin verme (yarım günler)

İzin ve devamsızlık, bunların gün şeklinde gönderileceği gibi ayarlandıysa, yarım gün tanımı da etkinleştirebilirsiniz. Daha sonra, kullanıcılar izin talebi gönderdiklerinde, günün ilk yarısını mı yoksa ikinci yarısını mı izinli olmak istediklerini belirtebilirler.

Varsayılan olarak, bu seçenek kapalıdır. Çalışanların günün ilk veya ikinci yarısını izin isteyebilmeleri için bu özelliği İnsan kaynakları **İzin ve devamsızlık** parametrelerinde açmanız gerekir.

Bu özelliğin güvenlik ayrıcalığı İnsan Kaynakları Parametrelerini Koruma'dır.

## <a name="validation-of-leave-and-absence-entries"></a>İzin ve devamsızlık girişlerinin doğrulaması

İznin nasıl yapılandırıldığına bağlı olarak, çalışma günlerinden daha uzun izin isteyen çalışanlara bir uyarı mesajı gösterilebilir. Başka bir deyişle, bunlar üzerinde belirli bir tarihte tam bir günden daha fazla izin isterlerse, uyarı verilir.

Bu doğrulamayı her zaman açıktır. Tanımlanan gün eşiğini aşan çalışanları, izin isteklerinde bir uyarı alırlar.

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>İş akışlarındaki koşul deyimleri için ek alanlar

Ek alanla, koşul ifadelerine ve yer tutuculara Core HR içindeki çeşitli iş akışları için eklenmiştir.

Aşağıdaki alanlar ücret, işten çıkarma ve transfer iş akışları için eklenmiştir:

- EmploymentType
- LegalEntity
- AdjustedWorkerStartDate
- EmployerNoticeAmount
- EmployerUnitOfNotice
- TransitionDate
- WorkerNoticeAmount
- WorkerStartDate
- WorkerUnitOfNotice
- ProbationEndDate
- Bölme
- Birlik
- Departman
- PositionType
- CompLocation
- Ünvan
- İş
- JobType
- JobFamily
- JobFunction

Aşağıdaki alanlar konum iş akışına eklendi:

- Bölme
- Birlik
- Departman
- PositionType
- CompLocation
- Ünvan
- İş
- JobType
- JobFamily
- JobFunction

Koşul ifadelerindeki alanlar ve yer tutucular, önceden belirtilen iş akışlarını düzenlemeye erişime sahip tüm kullanıcılara açıktır.

## <a name="navigation-to-attract-from-personnel-management"></a>Kişisel yönetimden Attract'e gezinti

Personel yönetiminde, Attract kurulmamışsa, **İşe alım adayları** bölümü, kullanıcıları "Burada gösterecek bir şey bulamadık" mesajı yerine Attract kullanmaya başlamaya yönlendirir.

## <a name="other-changes"></a>Diğer değişimler

Bu sürüm çeşitli hatalara yönelik düzeltmeler içerir:

- Bir alt yüklenici işe alındığında **Ücret** sekmesi, istek/eylem sayfasında kullanılabilir olmamalıdır.
- İstek sonlandırma işleminde, tüm alanlar veri içerene kadar devam edemezsiniz.
- Personel yönetimi analizlerindeki sıralama düzeni ve tarih göstergesi sorunları giderilmiştir.
