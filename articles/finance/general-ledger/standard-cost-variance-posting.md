---
title: Standart maliyet farkını deftere nakletme
description: Bu konuda, standart maliyetlendirme için deftere nakil profilleri ayarlama hakkında bilgi sağlanır.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: bc4f1bd7c1bf7a8f214f20460b10d371d8f3c790
ms.sourcegitcommit: 1ea145dc606e243c7f51d91a5c0dd9e385bbda4a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804628"
---
# <a name="standard-cost-variance-posting"></a>Standart maliyet farkını deftere nakletme

Kuruluşunuzda bir veya daha fazla ürün için standart maliyetlendirme kullandığınızda, [standart maliyetlendirmeye yönelik ön koşulları](/supply-chain/cost-management/prerequisites-standard-costs.md) yapılandırmalısınız. Bu konuda, ön koşulların 3. adımı ("Madde nakillerine, standart maliyet farklarıyla ilişkili genel muhasebe hesapları atayın") için gerekli olan deftere nakil hesapları açıklanmaktadır.

Satınalmalar ve üretim emirleri için çeşitli türlerde farklar olabilir. Üretim farklarına örnekler için bkz. [Üretim farklarının ortak kaynakları](/supply-chain/cost-management/common-sources-of-production-variances.md). Satınalma siparişi fiyat farkları, satın alınan bir madde için standart maliyet kullandığınızda ve ürünün standart maliyeti ile satınalma siparişindeki faturalanan tutar arasında fark olduğunda oluşur.

## <a name="sample-posting-profile-configuration"></a>Örnek deftere nakil profili yapılandırması

Aşağıdaki tabloda, varsayılan deftere nakil türlerine örnekler gösterilmiştir. Buna örnek ana hesaplar ve açıklamalar dahildir.

- "Borç/Alacak?" sütun, hareketin genellikle bir borç veya alacak olduğunu gösterir. Bazı durumlarda, bir hareket borç veya alacak nakledebilir.
- "Kliring hesabı" sütunu, deftere nakil türünün bir kliring hesabı olduğunu belirtir. Diğer bir ifadeyle, sonraki bir hareket deftere nakledildiğinde, bu hesapta deftere nakledilen tutar için otomatik olarak ters işlem uygulanır.
- "P/F" sütunu deftere nakil türünü gösterir. "P" fiziksel deftere nakilleri, "F" mali deftere nakilleri temsil eder.
- "İzle" sütunu, deftere nakil türü ana hesabının genellikle başka bir deftere nakil türü ana hesabıyla aynı olup olmadığını gösterir. Özel olarak, genellikle kullanılan deftere nakil türünü gösterir.

> [!NOTE]
> Tablodaki bu ana hesaplar ve ana hesap adları önerilerdir. İş gereksinimleriniz için en iyi yapılandırmayı belirlemek amacıyla muhasebeciniz ile çalışmanızı öneririz.

| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | P/F | İzle | Açıklama |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-----|--------|-------------|
| Satın alma fiyat farkı | 510310 | Satın alma fiyat farkı | Gider | İkisinden biri | No. | C | Uygulanamaz | Satınalma fiyatıyla satın alma siparişindeki standart maliyet arasında bir fark olduğunda bu hesap kullanılır. |
| Stok maliyeti yeniden değerlemesi | 510330 | Stok maliyeti yeniden değerlemesi | Gider | İkisinden biri | No. | C | Uygulanamaz | Bu hesap, eldeki stoğu yeniden değerlemek amacıyla standart maliyet maddesi için yeni bir maliyetlendirme sürümü etkinleştirildiğinde kullanılır. |
| Maliyet değişim farkı | 510320 | Maliyet değişim farkı | Gider | İkisinden biri | No. | C | Uygulanamaz | Bu hesap, tesisler arasında standart maliyetlerde fark olduğunda veya bir madde iade edildiğinde ve ürünün orijinal standart maliyeti ile geçerli standart maliyeti arasında değişiklik olduğunda kullanılır. |
| Üretim lot boyutu farkı | 510370 | Üretim lot boyutu farkı | Gider | İkisinden biri | No. | C | Uygulanamaz | Bu hesap, ürün reçetesi (BOM) hesaplama esası ile üretim emri maliyet hesaplaması için fiili miktar arasında farklılıklar olduğunda kullanılır. |
| Üretim fiyat farkı | 510340 | Üretim fiyat farkı | Gider | İkisinden biri | No. | C | Uygulanamaz | Bu hesap, bir üretim emri için tahmini maliyet ile fiili maliyet arasında fiyat farklılıkları olduğunda kullanılır. |
| Üretim miktar farkı | 510350 | Üretim miktar farkı | Gider | İkisinden biri | No. | C | Uygulanamaz | Bu hesap, bir üretim emri için tahmini maliyet ile fiili maliyetler arasında miktar farklılıkları olduğunda kullanılır. |
| Üretim yedekleme farkı | 510360 | Üretim yedekleme farkı | Gider | İkisinden biri | No. | C | Uygulanamaz | Bu hesap, üretim emrinde beklenmeyen bir tüketim olduğunda kullanılır. |
| Yuvarlama farkı | 618160 | Yuvarlama farkı | Gider | İkisinden biri | No. | C | Uygulanamaz | Bu hesap, üretim maliyetleri standart maliyetten hesaplanırken yuvarlama farkı olduğunda kullanılır. |
