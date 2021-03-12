---
title: Perakende ürünler için iskontoları engelleme seçenekleri
description: Satıcıların bazı ürünlerin ister bir promosyon isterse de POS'taki satış sırasında indirime girmesini engellemeleri için çeşitli sebepler olabilir.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7c408068ece94d47c0f41e286a2ce0ae7efd23dd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972516"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="4411a-103">Perakende ürünler için iskontoları engelleme seçenekleri</span><span class="sxs-lookup"><span data-stu-id="4411a-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4411a-104">Satıcıların bazı ürünlerin ister bir promosyon isterse de POS'taki satış sırasında indirime girmesini engellemeleri için çeşitli sebepler olabilir.</span><span class="sxs-lookup"><span data-stu-id="4411a-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="4411a-105">Yayımlanan ürünlerin **Commerce** sekmesinde bulunabilen aşağıdaki seçenekler, ürünün tüm veya el ile indirimlerini engellemek üzere yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="4411a-105">The following options, which can be found on the **Commerce** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="4411a-106">Ayarlar ayrıca kategori hiyerarşisinden kategori düzeyinde de belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="4411a-106">The settings can also be specified at the category level from the category hierarchy.</span></span>

- <span data-ttu-id="4411a-107">**Tüm indirimleri engelle** – Bu seçeneği, tüm indirimlerin bu ürüne uygulanmasını engellemek için seçin.</span><span class="sxs-lookup"><span data-stu-id="4411a-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="4411a-108">Bu karıştırma ve eşleştirme, miktar ve eşik indirimleri dahil tüm promosyonları ve bir POS kullanıcısı tarafından uygulanan el ile satır ve hareket indirimlerini kapsar.</span><span class="sxs-lookup"><span data-stu-id="4411a-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="4411a-109">**El ile indirimleri engelle** – Bu seçeneği yalnızca bir satış sırasında bir POS kullanıcısı tarafından uygulanan el ile satır ve hareket indirimlerini engellemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="4411a-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="4411a-110">Bu seçeneğin işaretli olduğu ürünler, karıştır ve eşleştir ve miktar ve eşik indirimleri gibi promosyonlar için kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4411a-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="4411a-111">Bu ayarlar fiyat geçersiz kılma işlemini kısıtlamaz çünkü bu, taban fiyatı belirler ve bir indirim olarak görülmez.</span><span class="sxs-lookup"><span data-stu-id="4411a-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="4411a-112">[![İndirim alanlarını engelle](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="4411a-112">[![Prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>
