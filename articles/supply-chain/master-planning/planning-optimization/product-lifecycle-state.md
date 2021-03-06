---
title: Belirli ürün yaşam döngüsü durumlarına sahip ürünleri hariç tutma
description: Bu konuda, Planlama İyileştirmesi işlevi kullanılırken ürünlerin yaşam döngüsü durumlarına göre nasıl hariç tutulacağı açıklanmaktadır.
author: ChristianRytt
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7028a509aa884589958542f7ec627d69dffcfcec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839259"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a>Belirli ürün yaşam döngüsü durumlarına sahip ürünleri hariç tutma

[!include [banner](../../includes/banner.md)]

Serbest bırakılmış ürünler ve serbest bırakılmış ürün sürümleri bir **Ürün yaşam döngüsü durumu** alanı içerir. Bu alan, diğer işlemlerin yanı sıra master planlama sırasında dahil edilen ürünleri denetlemenize olanak tanır. **Ürün bilgileri yönetimi \> Kurulum \> Ürün yaşam döngüsü durumu**'na giderek yaşam döngüsü durumlarını gerektiği gibi ekleyebilir, kaldırabilir ve düzenleyebilirsiniz. Ürünlerin master planlama sırasında dahil edilmesi gerekiyorsa her ürün yaşam döngüsü durumu için **Planlama için etkin** seçeneğini *Evet* olarak ayarlayın. Seçenek *Hayır* olarak ayarlandığında, ilişkili ürünler ve varyantlar tüm master planlamalardan ve ürün reçetesi düzeyindeki tüm hesaplamalardan hariç tutulur.

**Ürün yaşam döngüsü durumu** alanının boş bırakıldığı serbest bırakılan ürünler ve varyantlar, **Planlama için etkin** seçeneği *Evet* olarak ayarlanmış bir ürün yaşam döngüsü durumuna sahipmiş gibi kabul edilir. Başka bir deyişle, master planlama sırasında dahil edilirler.

> [!NOTE]
> Gereksiz tedarik önerilerini önlemek için kullanım dışı bırakılmış tüm serbest bırakılan ürünleri ve varyantları **Planlama için etkin** seçeneğinin *Hayır* olarak ayarlandığı bir ürün yaşam döngüsü durumuyla ilişkilendirmenizi öneririz. Bu yaklaşım özellikle, yeniden kullanılabilir olmayan ürün yapılandırma varyantlarıyla çalışırken önemlidir çünkü atığı önlemeye yardımcı olur.

## <a name="related-resources"></a>İlgili kaynaklar

Ürün yaşam döngüsü durumları hakkında daha fazla bilgi edinmek için [Ürün yaşam döngüsü durumuna genel bakış](../../pim/product-lifecycle.md) başlıklı makaleye bakın.

Ürünleri master planlama ve ürün reçetesi düzeyinde hesaplamalar dışında tutmak amacıyla ürün yaşam döngüsü durumlarının nasıl kullanılacağı ile ilgili adımları içeren daha fazla bilgi edinmek için [Ürünleri Master planlama dışında tutmak için bir ürün yaşam döngüsü durumu oluşturma](../../pim/tasks/exclude-products-master-planning.md) konusuna bakın.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]