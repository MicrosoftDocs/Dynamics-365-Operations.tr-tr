---
title: "Hesap planınızı planlama"
description: "Bu makalede, kuruluşunuzun hesap planını yapmanıza yardımcı olacak bilgiler verilmektedir."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 1e3d582e79b98d048bf6c78fc9231b6b19040036
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="plan-your-chart-of-accounts"></a>Hesap planınızı planlama

[!include[banner](../includes/banner.md)]


Bu makalede, kuruluşunuzun hesap planını yapmanıza yardımcı olacak bilgiler verilmektedir.

Bir kuruluşun finansal bilgilerini takip etmek ve kaydetmek için bir hesap planı ayarlayabilirsiniz. Hesap planı bir finansal çerçeveyi tanımlayan bir hesaplar topluluğudur. Bu hesaplardaki işlemleri daha yakından takip etmek için finansal boyutlar olarak bilinen segmentler ekleyebilirsiniz. Örneğin, bir gider hesabı Departman, Maliyet merkezi ve Amaç adlı finansal boyutlar içerebilir. Hesap yapıları ve gelişmiş kurallar olarak bilinen, kullanıcı tanımlı kurallar finansal boyutların ana hesaplara ve diğer finansal boyutlara nasıl ekleneceğini ve ayrıca işlemlerin nasıl girileceğini belirler. 

Hesap planı bir yasal kuruluşun genel muhasebe hesaplarının yapılandırılmış bir listesidir. Liste, yetkililer ve sahipler için mali raporlar hazırlamak için kullanılır. Hesaplar, hesap türlerine göre gruplanır ve daha büyük kategorilere daha birleştirilir. En genel düzeyde, hesaplar gelirler ve maliyetler (çalışan hesaplar) ile varlıklar ve borçlar (bilanço hesapları) olarak gruplanır. 

Hesap planı paylaşılabilir ve kuruluştaki herhangi bir tüzel kişilik tarafından kullanılır. Tüzel kişilik tarafından kullanılan hesap planı **Genel muhasebe** sayfasında tanımlanır. 

Burada kurumunuz için hesap planının yapısını planlarken mutlaka göz önünde bulundurmanız gereken bazı faktörler açıklanmıştır:

-   Kurulumunuzun bulunduğu ülkenin/bölgenin raporlama gereksinimleri.
-   Yasal biriminizin raporlama gereksinimleri
-   Hem dış kurumlar hem kendi kurumunuz için gerekli olan tanımlama derecesi

**Hesap planı** sayfasından hesap planınızı oluşturun. Ana hesaplar **Hesap planı** sayfasından veya **Ana hesaplar** sayfasından oluşturulabilir. Ana hesaplarınız, hesap planı sınırlayıcıları olarak kullanılan hiçbir özel karakteri kullanmamalıdır. Hesap planı sınırlayıcınızla aynı olan bir özel karakter bulunuyorsa tutarsızlık yaşayabilir veya hesap ve boyut kombinasyonları girerken daima arama veya sorgulama özelliklerini kullanmak durumunda kalabilirsiniz. 

Ana hesapların ana hesap kategorileriyle ilişkilendirilmesi iyi bir fikirdir, böylece herhangi bir değişiklik yapmak zorunda kalmadan varsayılan finansal raporları istediğiniz gibi kullanabilirsiniz. Böylece, raporları daha hızlı ve kolay bir şekilde tasarlayabilir ve tutabilirsiniz. 

Hesap yapıları oluşturmak için **Hesap yapıları oluştur** sayfasını kullanın. Hesap yapıları geçerli kombinasyonları tanımlar. Kombinasyonlar, ana hesaplarla birlikte bir hesap planı oluşturur. 

**Tüzel kişilik geçersiz kılmaları** 

Tüm yasal birimler için her ana hesap geçerli değildir, bazı ana hesaplar sadece belirli bir zaman aralığı için geçerli olabilir. Bu senaryoda, Yasal birim önceliği bölümü, ana hesabın hangi şirketler için askıya alınması gerektiğinin, sahibinin kim olduğunun ve boyutun etkin olacağı zaman diliminin belirlenmesi için kullanılabilir. Paylaşılan düzeydeki öncelikler, yasal birim düzeyindeki önceliklerden daha kısıtlayıcı olamaz.

Daha fazla bilgi için bkz. [Mali boyutlar](financial-dimensions.md).




