---
title: Bakım bütçelerini güncelleştirme
description: Bu konuda Varlık Yönetimi'nde bakım bütçesini güncelleştirme işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f3b771319eeb602a371500fdc69c68f88afe341
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571749"
---
# <a name="update-maintenance-budgets"></a>Bakım bütçelerini güncelleştirme

[!include [banner](../../includes/banner.md)]

 

**Bakım bütçesi satırları** sayfası, **Bakım bütçeleri** sayfasında seçilen bütçe için oluşturulan tüm bütçe satırlarını gösterir. (Daha fazla bilgi için bkz. [Bakım bütçeleri oluşturma](create-maintenance-budget.md).) Bakım bütçesi onaylanana kadar bakım bütçesi satırlarını yeniden hesaplayabilir ve ayarlayabilirsiniz. Bütçe dönemi geçtikten ve maliyetler Varlık Yönetimine nakledildikten sonra bütçe satırlarını fiili maliyetlerle de güncelleştirebilirsiniz.

## <a name="recalculate-a-maintenance-budget"></a>Bakım bütçesini yeniden hesaplama

Bakım bütçesini **Bakım bütçesi satırları** sayfasında yeniden hesaplayabilirsiniz. Bakım bütçesini yeniden hesapladığınızda mevcut bütçe satırları silinir ve yeni bir hesaplama yapılır.

1. **Bakım bütçesi satırları** sayfasında, **Yeniden hesapla**'yı seçin.
2. **Bütçeyi yeniden hesapla** iletişim kutusunda, yeni hesaplama için gerekli değişiklikleri yapın ve **Tamam**'ı seçin.

Yeni bütçe satırları, ayarladığınız değerlere göre oluşturulur.

## <a name="adjust-budget-lines"></a>Bütçe satırlarını ayarlama

Tüm bakım bütçesini yeniden hesaplamak yerine bütçe maliyetleriyle ilgili seçili satırları ayarlayabilirsiniz.

1. **Bakım bütçesi satırları** sayfasında, bütçe maliyetinin güncelleştirileceği satırları seçin.
2. **Ayarla**'yı seçin.
3. Seçili satırlara bir miktar eklemek için **Maliyet ekle** onay kutusunu seçin ve ardından **Değer ekle** alanına değer girin.
4. Seçilen bütçe satırlarında bütçe maliyetini bir katsayıyla çarpmak için **Maliyeti çarp** onay kutusunu seçin ve ardından **Değeri çarp** alanına katsayıyı girin.

    Örneğin, **Değeri çarp** alanına **1,2** girerseniz seçili satırlardaki bütçe maliyetini yüzde 20 oranında artırırsınız. **0,7** girerseniz seçili satırlardaki bütçe maliyetini yüzde 30 oranında azaltırsınız.

5. **Tamam**'ı seçin.

Seçili bütçe satırları, adım 3 veya 4'te ayarladığınız değerlere göre güncelleştirilir.

## <a name="update-actual-costs"></a>Fiili maliyetleri güncelleştirme

Bütçe satırlarındaki tarihler geçtikten ve fiili maliyetler Varlık Yönetimine nakledildikten sonra bakım bütçesindeki fiili maliyetleri güncelleştirebilirsiniz.

1. **Bakım bütçesi satırları** sayfasında, **Maliyeti güncelleştir**'i seçin.
2. **Fiili maliyeti hesapla** iletişim kutusunda, **Tamam**'ı seçin.

Fiili maliyetler nakledilmişse bütçe satırlarındaki **Fiili maliyet** alanları güncelleştirilir. Bütçeyi oluşturduktan sonra yeni varlık türleri oluşturulmuşsa ve bu varlık türleri, iş emirlerinin oluşturulduğu ve ilgili maliyetlerin nakledildiği varlıklarda kullanılmışsa yeni bütçe satırları oluşturulabilir. Yeni bütçe satırları bunlar için bütçe maliyetleri hesaplanmadığından yalnızca fiili maliyetleri gösterir.

> [!NOTE]
> Önleyici, düzeltici ve yatırım maliyetlerine bölünmüş fiili maliyetlere genel bakışı görmek için **Varlık maliyeti denetimi** sayfasında aynı dönem için bir hesaplama yapabilirsiniz. 

## <a name="manually-add-budget-lines"></a>Bütçe satırlarını el ile ekleme

**Bakım bütçesi satırları** sayfasında, **Yeni**'yi seçerek ve satır üzerinde seçimler yaparak el ile yeni bir bütçe satırı ekleyebilirsiniz. Bu yaklaşımın yararlı olabileceği durumlara yönelik birkaç örnek aşağıda gösterilmiştir:

- Bazı varlıkların yenilenmesinin şu anda planlama aşamasında olduğunu biliyorsunuz ancak ilgili işler henüz Varlık Yönetiminde oluşturulmadı. Ancak bu işlerin bütçe maliyetlerinin bakım bütçesine dahil edilmesini istiyorsunuz.
- Bakım bütçesi yaptığınız tarihten itibaren yeni varlıklar veya varlık türleri oluşturuldu ancak bakım planları henüz bu varlıklar veya varlık türlerinde ayarlanmadı. Ancak bu varlık türlerinin bütçe maliyetlerinin bakım bütçesine dahil edilmesini istiyorsunuz.
