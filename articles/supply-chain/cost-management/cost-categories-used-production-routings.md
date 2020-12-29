---
title: Üretim rotasında kullanılan maliyet kategorileri
description: Bu makalede, rota kullanan imalat ortamlarına uygulanan maliyet kategorileri hakkında bilgiler sağlanmaktadır.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 78153
ms.assetid: a3fdc76c-0a27-4723-b1c7-4322f707d89e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 20697fd557fd81a0eec5a033c2c397f3918e6477
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439445"
---
# <a name="cost-categories-used-in-production-routing"></a>Üretim rotasında kullanılan maliyet kategorileri

[!include [banner](../includes/banner.md)]

Bu makalede, rota kullanan imalat ortamlarına uygulanan maliyet kategorileri hakkında bilgiler sağlanmaktadır.

Maliyet kategorileri rota kullanan imalat ortamları için geçerlidir. Maliyet kategorileri, imal edilmiş bir maddenin hesaplanmış maliyetlerindeki saatlik maliyetleri tanımlamak ve maliyet katkılarını bölümlendirmek için operasyon kaynaklarına ve rota operasyonlarına atanır. Maliyet kategorilerine atanan maliyet grupları, imalat maliyeti katkılarını operasyon kaynaklarına ve örneğin kurulum ve çalıştırma zamanı gibi faaliyetin tipine göre sınıflandırır. Maliyet grubu atamalarının özgüllüğü, imalat genel giderlerinin rota bilgilerine dayalı olarak hesaplanmasını mümkün kılar. 

**Not:** Maliyet kategorileri imalat ortamlarında işçilik ücreti kodları veya makine ücreti kodları gibi birçok başka adla bilinirler. 

Her bir maliyet kategorisinin ilişkili maliyet kayıtları ve atanmış bir maliyet grubu vardır. Farklı üretim amaçları için farklı maliyet kategorileri gereklidir.

-   Operasyon kaynağına bağlı olarak farklı saatlik maliyetler atayın. Örneğin, maliyetler çeşitli işçilik becerilerine, makinelere veya imalat hücrelerine göre farklı olabilir.
-   Bir rota operasyonuyla ilişkili kurulum zamanı veya çalıştırma zamanı için farklı saatlik maliyetler atayın.
-   Operasyon kaynağı maliyetlerini, saatlik maliyetler yerine işçilik ödemesi için parça ücretleri gibi çıktı miktarını temel alarak atayın.
-   İmal edilmiş bir maddenin hesaplanan maliyetine, maliyet katkılarının maliyet grup bölümlendirmesini sağlayın. Örneğin, işçilik ve makine maliyetlerini bölümlendirebilirsiniz.
-   Genel gider hesaplama formülleri için işçilikle ve makineyle ilişkili genel giderler veya kurulum ve çalıştırma zamanıyla ilişkili genel giderler gibi maliyet grubu temelini sağlayın.

Bir rota operasyonu için kurulum zamanına, işlem zamanına ve miktara bir maliyet kategorisi atanabilir. Örneğin, kurulum zamanı ile işlem zamanı arasındaki maliyetler veya maliyet grubu bölümlendirmesi farklı ise, kurulum zamanına ve işlem zamanına farklı maliyet kategorileri tanımlanmalı ve atanmalıdır. Kurulum zamanı, işlem zamanı ve miktar için maliyet kategorilerinin seçici kullanımı bir operasyona atanmış rota grubu tarafından belirlenir. Zamana ve miktara maliyet kategorileri atanması, **Üretim kontrol parametreleri** sayfasında tanımlı şirket geneli politikalar tarafından zorunlu kılınabilir. 

Her bir maliyet kategorisi, maliyetlerle bir maliyetlendirme sürümündeki maliyet kayıtlarının açıklamasına dayalı olarak ilişkilendirilmiştir. Belirtilen bir maliyetlendirme sürümü ve tesisi için maliyet kayıtlarını tanımlamak üzere **Maliyet kategorisi fiyatı** sayfasını kullanın. Bir maliyet kategorisi için ilk kez girilen maliyet kaydının durumu **Beklemede** olacak ve amaçlanan geçerlilik tarihine sahip olacaktır. Maliyet kaydını etkinleştirdiğinizde, durum **Geçerli etkin** olarak güncellenir ve geçerlilik tarihi aktivasyon tarihine güncellenir. Farklı maliyet kayıtları farklı tesisleri, geçerlilik tarihlerini veya durumları yansıtıyor olabilir. Gelecekteki veya geçmişteki bir tarih için yapılan ürün reçetesi (BOM) hesaplamaları ilgili geçerlilik tarihlerine sahip maliyet kayıtlarını kullanır. Geçerli etkin maliyet kaydı, üretim emri maliyetlerini tahmin etmek ve raporlanan zamanı bir üretim emrine karşılık değerlendirmek için kullanılır. 

Bir maliyet kategorisine yönelik maliyet kaydı tesise özel veya şirket çapında olabilir. Bir maliyet kaydını tesise özgü yapmak için ona bir tesis atayın. Aksi durumda, boş bir değer maliyet kaydının şirketteki tüm tesisler için geçerli olacağı anlamına gelir. Örneğin maliyetler tesisler arasında farklılık gösterebilir, bu nedenle maliyet kayıtlarının tesise özel olarak tanımlanması gerekir. 

Rota operasyonu normalde operasyon kaynağına veya master operasyona atanan maliyet kategorilerini devralır. Bir üretim emri oluşturulurken, üretim rotasındaki rota operasyonları seçilen rota sürümünü yansıtır. Üretim rotasındaki operasyonlara atanan maliyet kategorilerinin üzerine yazabilirsiniz. 

Bazı üretim iş türleri, proje süresi tahminlerine ve raporlamaya uygulanabilir. Bu durumda, üretim ve proje amaçları için bir maliyet kategorisi gereklidir. Bir maliyet kategorisi projelerde kullanılmak üzere bayrakla işaretlendiğinde projeyle ilgili ek bilgiler tanımlamanız gerekir.



