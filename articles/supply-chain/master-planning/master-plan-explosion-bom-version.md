---
title: Bir ürün reçetesi versiyonu açılımı
description: Bu makalede ürün reçetesi (BOM) sürümü açılımı içeren bir master planlama senaryosu açıklanmaktadır.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 119b77b695ff065c8e45693e1cf7cf15360d441e
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468650"
---
# <a name="explosion-of-a-bom-version"></a>Bir ürün reçetesi versiyonu açılımı

[!include [banner](../includes/banner.md)]

Bu makalede ürün reçetesi (BOM) sürümü açılımı içeren bir master planlama senaryosu açıklanmaktadır.

Bir ürün reçetesi sürümünün talep açılımı, belirli bir tesisteki ve muhtemelen belirli bir ambardaki her ürün satırı maddesine yönelik bir talep oluşturur. Bir tesise özel ürün reçetesinde, her ürün reçetesi satırı için belirli bir ambar tanımlanabilir. Ek olarak, her ürün reçetesi satırı için maddenin boyut ayarları ambarın gerekli olup olmadığını belirlemektedir. Her ürün reçetesi satırı maddesi için sonuçta elde edilen talep, ardından ilave talep açılımının başlangıç noktasını oluşturmaktadır. Bu master planlama senaryosu aşağıdaki koşulları kapsar:

-   Tesis boyutları zorunludur ve talep hareketinde girilmesi gerekmektedir.
-   Tesis boyutu tutarlıdır. Bu nedenle, daha düşük düzeydeki talep için tasarlanmış tesis başlangıçtaki talep hareketindeki tesisle aynıdır.

Aşağıdaki resimde, master planlama talep açılımının ne şekilde ilerlediği gösterilmiştir. ![Ürün reçetesi versiyonu kullanılarak talep açılımı.](./media/multisitedemandexplosionscenariousingbomversion.gif)

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün reçetesi sürümünü belirleme](master-plan-bom-version-determined.md)

[Master planlama ve birden çok tesis işlevine genel bakış](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]