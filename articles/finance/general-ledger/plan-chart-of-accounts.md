---
title: Hesap planınızı planlama
description: Bu konuda, kuruluşunuzun hesap planını yapmanıza yardımcı olacak bilgiler verilmektedir.
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e568fca70ea2048d881681ff7ab8ebc6fad6450
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990376"
---
# <a name="plan-your-chart-of-accounts"></a>Hesap planınızı planlama

[!include [banner](../includes/banner.md)]

Bu konuda, kuruluşunuzun hesap planını yapmanıza yardımcı olacak bilgiler verilmektedir.

Bir kuruluşun finansal bilgilerini takip etmek ve kaydetmek için bir hesap planı ayarlayabilirsiniz. Hesap planı bir finansal çerçeveyi tanımlayan bir hesaplar topluluğudur. Bu hesaplardaki hareketleri daha da ayrıntılı izlemek için segmentler ekleyebilirsiniz. Bu segmentler mali boyutlar olarak bilinir. Örneğin, bir gider hesabı Departman, Maliyet merkezi ve Amaç adlı finansal boyutlar içerebilir. Kullanıcı tanımlı kurallar finansal boyutların ana hesaplara ve diğer finansal boyutlara nasıl ekleneceğini ve ayrıca işlemlerin nasıl girileceğini belirler. Kullanıcı tanımlı kurallar hesap yapıları ve gelişmiş kurallar olarak bilinir.

Hesap planı bir tüzel kişiliğin genel muhasebe hesaplarının yapılandırılmış bir listesidir. Liste, yetkililer ve sahipler için mali raporlar hazırlamak için kullanılır. Hesaplar, önce hesap türlerine göre gruplanır ve daha büyük kategorilere daha birleştirilir. En genel düzeyde, hesaplar gelirler ve maliyetler (çalışan hesaplar) ile varlıklar ve borçlar (bilanço hesapları) olarak gruplanır.

Hesap planı paylaşılabilir ve kuruluştaki herhangi bir tüzel kişilik tarafından kullanılır. Tüzel kişilik tarafından kullanılan hesap planı **Genel muhasebe** sayfasında tanımlanır.

Burada kurumunuz için hesap planının yapısını planlarken mutlaka göz önünde bulundurmanız gereken bazı faktörler açıklanmıştır:

- Kurulumunuzun bulunduğu ülkenin veya bölgenin raporlama gereksinimleri.
- Yasal biriminizin raporlama gereksinimleri
- Hem dış kurumlar hem kendi kurumunuz için gerekli olan tanımlama derecesi

**Hesap planı** sayfasından hesap planınızı oluşturun. Ana hesapları **Hesap planı** sayfasından veya **Ana hesaplar** sayfasından oluşturabilirsiniz. Ana hesaplarınız, hesap planı sınırlayıcıları olarak kullanılan hiçbir özel karakteri kullanmamalıdır. Aksi takdirde, tutarsızlıkla karşılaşabilir veya hesap ve boyut birleşimleri girerken her zaman aramaları veya iletişim kutusunu kullanmak zorunda kalabilirsiniz. Daha fazla bilgi için bkz. [Ana hesap oluşturma](tasks/create-main-account.md).

> [!NOTE]
> Dynamics 365 for Finance and Operations sürüm 8.0'da (Nisan 2018), hesap planı sınırlayıcısını **Genel muhasebe parametreleri** sayfasından değiştirebilirsiniz.

Ana hesapların ana hesap kategorileriyle ilişkilendirilmesi iyi bir fikirdir, böylece herhangi bir değişiklik yapmak zorunda kalmadan varsayılan finansal raporları istediğiniz gibi kullanabilirsiniz. Böylece, raporları daha hızlı ve kolay bir şekilde tasarlayabilir ve tutabilirsiniz.

Hesap yapılarını **Hesap yapıları oluştur** sayfasından oluşturun. Hesap yapıları geçerli kombinasyonları tanımlar. Bu birleşimler, ana hesaplarla birlikte bir hesap planı oluşturur. Daha fazla bilgi için bkz. [Hesap yapıları oluşturma](tasks/create-account-structures.md).

**Tüzel varlık geçersiz kılmaları**

Tüm tüzel kişilikler için her ana hesap geçerli değildir, bazı ana hesaplar sadece belirli bir dönem için geçerli olabilir. Bu senaryoda, **Tüzel varlık geçersiz kılmaları** bölümünü, ana hesabın askıya alınacağı şirketleri, sahibini ve boyutun etkin olacağı dönemi belirlemek için kullanabilirsiniz. Paylaşılan düzeydeki öncelikler, yasal birim düzeyindeki önceliklerden daha kısıtlayıcı olamaz.

Daha fazla bilgi için aşağıdaki konulara bakın:

- [Mali boyutlar](financial-dimensions.md)
- [Gelişmiş kural yapıları oluşturma ve atama](tasks/create-assign-advanced-rule-structures.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]