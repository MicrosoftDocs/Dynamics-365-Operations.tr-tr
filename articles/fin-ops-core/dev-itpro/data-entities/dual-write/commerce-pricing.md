---
title: Dynamics 365 Commerce fiyatlandırma altyapısını Dynamics 365 Sales ile kullanma
description: Bu konu başlığında, Dynamics 365 Sales'da satış teklifleri oluşturmak için Microsoft Dynamics 365 Commerce fiyatlandırma altyapısının nasıl kullanılacağı açıklanmaktadır.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fad5c21d75db62b85efe803f1667dd3f9164a5fc
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594930"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Dynamics 365 Commerce fiyatlandırma altyapısını Dynamics 365 Sales ile kullanma

[!include [banner](../../includes/banner.md)]

Bu konu başlığında, Dynamics 365 Sales'da satış teklifleri oluşturmak için Microsoft Dynamics 365 Commerce fiyatlandırma altyapısının nasıl kullanılacağı açıklanmaktadır.

Dynamics 365 Commerce fiyatlandırma altyapısı, mağaza düzeyinde fiyatlandırma, ilişki tabanlı ve bağlılık programı tabanlı fiyatlandırma, karıştırma ve eşleme iskontoları, miktar iskontoları ve eşik iskontoları gibi işletme-müşteri (B2C) fiyatlandırma senaryolarının çoğunu destekler. Fiyatlandırma motoru, belirli bir teklif veya sipariş için en iyi fiyatı belirlemek amacıyla karmaşık kurallar kullanır.

[Çift yazma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) özelliğini kullandığınızda, fiyatlandırma gereksinimleriniz için üç seçenek sunulur. Dynamics 365 Sales'daki fiyat listesinden gelen statik fiyatlandırmayı, Dynamics 365 Supply Chain Management'taki fiyatlandırma altyapısını veya Dynamics 365 Commerce'teki fiyatlandırma altyapısını kullanabilirsiniz. Bu seçenekler arasında Commerce fiyatlandırma altyapısı, B2C senaryolarına en uygun yöntemdir.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>Sales'da Commerce fiyatlandırma altyapısını kullanma

> [!NOTE]
> Şu anda, Commerce fiyatlandırma altyapısı Salesa yalnızca teklif oluşturmak için kullanılabilir. Commerce fiyatlandırma altyapısıyla satış siparişi tümleştirmesi henüz kullanılabilir değildir.

Kullanıcılar Sales'da bir teklif başlattıklarında çift yazma çerçevesi teklif ayrıntılarını Commerce'e kopyalar. Sales'daki mevcut teklif satırlarında yapılan değişiklikler veya yeni eklenen teklif satırları Commerce'e kopyalanır. Kullanıcılar teklife fiyat verme için Commerce fiyatlandırma altyapısını kullanmak istediklerinde, teklifin fiyatını Commerce fiyatlandırma altyapısına göre güncelleştirmek için **Fiyat teklifi**'ni seçebilir. Bu işlemin ardından fiyatlar hem Sales'da hem de Commerce'te güncelleştirilir.

## <a name="prerequisites"></a>Önkoşullar

- Commerce fiyatlandırma altyapısını Sales'da kullanabilmek için [Çift yazmada aday müşteriden nakde](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/) konusundaki adımları uygulamanız gerekir.
- Aşağıdaki adımları izleyerek, el ile giriş için ticari sözleşme değerlendirmesini kapatmanız gerekir:

    1. Commerce ortamınızda **Alacak hesapları\>Kurulum \>Alacak hesapları parametreleri**'ne gidin.
    1. **Fiyatlar** sekmesindeki **Ticari sözleşme değerlendirmesi** hızlı sekmesi altında **El ile giriş onay** kutusunun işaretini kaldırın.

## <a name="additional-resources"></a>Ek kaynaklar

[Çift yazmada aday müşteriden nakde](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]