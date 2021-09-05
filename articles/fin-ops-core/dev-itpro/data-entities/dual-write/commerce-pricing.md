---
title: Dynamics 365 Commerce fiyatlandırma altyapısını Dynamics 365 Sales ile kullanma
description: Bu konu başlığında, Dynamics 365 Sales'da satış teklifleri oluşturmak için Microsoft Dynamics 365 Commerce fiyatlandırma altyapısının nasıl kullanılacağı açıklanmaktadır.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c3f1527e5f37bebba57661ca86b1a3aae7e62da0
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416767"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Dynamics 365 Commerce fiyatlandırma altyapısını Dynamics 365 Sales ile kullanma

[!include [banner](../../includes/banner.md)]

Bu konu başlığında, Dynamics 365 Sales'da satış teklifleri oluşturmak için Microsoft Dynamics 365 Commerce fiyatlandırma altyapısının nasıl kullanılacağı açıklanmaktadır.

Dynamics 365 Commerce fiyatlandırma altyapısı, mağaza düzeyinde fiyatlandırma, ilişki tabanlı ve bağlılık programı tabanlı fiyatlandırma, karıştırma ve eşleme iskontoları, miktar iskontoları ve eşik iskontoları gibi işletme-müşteri (B2C) fiyatlandırma senaryolarının çoğunu destekler. Fiyatlandırma motoru, belirli bir teklif veya sipariş için en iyi fiyatı belirlemek amacıyla karmaşık kurallar kullanır.

[Çift yazma](./dual-write-overview.md) özelliğini kullandığınızda, fiyatlandırma gereksinimleriniz için üç seçenek sunulur. Dynamics 365 Sales'daki fiyat listesinden gelen statik fiyatlandırmayı, Dynamics 365 Supply Chain Management'taki fiyatlandırma altyapısını veya Dynamics 365 Commerce'teki fiyatlandırma altyapısını kullanabilirsiniz. Bu seçenekler arasında Commerce fiyatlandırma altyapısı, B2C senaryolarına en uygun yöntemdir.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>Sales'da Commerce fiyatlandırma altyapısını kullanma

> [!NOTE]
> Şu anda, Commerce fiyatlandırma altyapısı Salesa yalnızca teklif oluşturmak için kullanılabilir. Commerce fiyatlandırma altyapısıyla satış siparişi tümleştirmesi henüz kullanılabilir değildir.

Kullanıcılar Sales'da bir teklif başlattıklarında çift yazma çerçevesi teklif ayrıntılarını Commerce'e kopyalar. Sales'daki mevcut teklif satırlarında yapılan değişiklikler veya yeni eklenen teklif satırları Commerce'e kopyalanır. Kullanıcılar teklife fiyat verme için Commerce fiyatlandırma altyapısını kullanmak istediklerinde, teklifin fiyatını Commerce fiyatlandırma altyapısına göre güncelleştirmek için **Fiyat teklifi**'ni seçebilir. Bu işlemin ardından fiyatlar hem Sales'da hem de Commerce'te güncelleştirilir.

## <a name="prerequisites"></a>Önkoşullar

- Commerce fiyatlandırma altyapısını Sales'da kullanabilmek için [Çift yazmada aday müşteriden nakde](./dual-write-prospect-to-cash.md) konusundaki adımları uygulamanız gerekir.
- Aşağıdaki adımları izleyerek, el ile giriş için ticari sözleşme değerlendirmesini kapatmanız gerekir:

    1. Commerce ortamınızda **Alacak hesapları\>Kurulum \>Alacak hesapları parametreleri**'ne gidin.
    1. **Fiyatlar** sekmesindeki **Ticari sözleşme değerlendirmesi** hızlı sekmesi altında **El ile giriş onay** kutusunun işaretini kaldırın.

## <a name="additional-resources"></a>Ek kaynaklar

[Çift yazmada aday müşteriden nakde](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]