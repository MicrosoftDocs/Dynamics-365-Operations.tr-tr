---
title: Dynamics 365 Commerce fiyatlandırma altyapısını Dynamics 365 Sales ile kullanma
description: Bu konu başlığında, Dynamics 365 Sales'da satış teklifleri oluşturmak için Microsoft Dynamics 365 Commerce fiyatlandırma altyapısının nasıl kullanılacağı açıklanmaktadır.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: fa93b1262049d80148ff23b3d7223ec0f6c2fe68
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941178"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="567d0-103">Dynamics 365 Commerce fiyatlandırma altyapısını Dynamics 365 Sales ile kullanma</span><span class="sxs-lookup"><span data-stu-id="567d0-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="567d0-104">Bu konu başlığında, Dynamics 365 Sales'da satış teklifleri oluşturmak için Microsoft Dynamics 365 Commerce fiyatlandırma altyapısının nasıl kullanılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="567d0-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="567d0-105">Dynamics 365 Commerce fiyatlandırma altyapısı, mağaza düzeyinde fiyatlandırma, ilişki tabanlı ve bağlılık programı tabanlı fiyatlandırma, karıştırma ve eşleme iskontoları, miktar iskontoları ve eşik iskontoları gibi işletme-müşteri (B2C) fiyatlandırma senaryolarının çoğunu destekler.</span><span class="sxs-lookup"><span data-stu-id="567d0-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="567d0-106">Fiyatlandırma motoru, belirli bir teklif veya sipariş için en iyi fiyatı belirlemek amacıyla karmaşık kurallar kullanır.</span><span class="sxs-lookup"><span data-stu-id="567d0-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="567d0-107">[Çift yazma](./dual-write-overview.md) özelliğini kullandığınızda, fiyatlandırma gereksinimleriniz için üç seçenek sunulur.</span><span class="sxs-lookup"><span data-stu-id="567d0-107">When you use [dual-write](./dual-write-overview.md), you have three options for your pricing needs.</span></span> <span data-ttu-id="567d0-108">Dynamics 365 Sales'daki fiyat listesinden gelen statik fiyatlandırmayı, Dynamics 365 Supply Chain Management'taki fiyatlandırma altyapısını veya Dynamics 365 Commerce'teki fiyatlandırma altyapısını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="567d0-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="567d0-109">Bu seçenekler arasında Commerce fiyatlandırma altyapısı, B2C senaryolarına en uygun yöntemdir.</span><span class="sxs-lookup"><span data-stu-id="567d0-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="567d0-110">Sales'da Commerce fiyatlandırma altyapısını kullanma</span><span class="sxs-lookup"><span data-stu-id="567d0-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="567d0-111">Şu anda, Commerce fiyatlandırma altyapısı Salesa yalnızca teklif oluşturmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="567d0-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="567d0-112">Commerce fiyatlandırma altyapısıyla satış siparişi tümleştirmesi henüz kullanılabilir değildir.</span><span class="sxs-lookup"><span data-stu-id="567d0-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="567d0-113">Kullanıcılar Sales'da bir teklif başlattıklarında çift yazma çerçevesi teklif ayrıntılarını Commerce'e kopyalar.</span><span class="sxs-lookup"><span data-stu-id="567d0-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="567d0-114">Sales'daki mevcut teklif satırlarında yapılan değişiklikler veya yeni eklenen teklif satırları Commerce'e kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="567d0-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="567d0-115">Kullanıcılar teklife fiyat verme için Commerce fiyatlandırma altyapısını kullanmak istediklerinde, teklifin fiyatını Commerce fiyatlandırma altyapısına göre güncelleştirmek için **Fiyat teklifi**'ni seçebilir.</span><span class="sxs-lookup"><span data-stu-id="567d0-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="567d0-116">Bu işlemin ardından fiyatlar hem Sales'da hem de Commerce'te güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="567d0-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="567d0-117">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="567d0-117">Prerequisites</span></span>

- <span data-ttu-id="567d0-118">Commerce fiyatlandırma altyapısını Sales'da kullanabilmek için [Çift yazmada aday müşteriden nakde](./dual-write-prospect-to-cash.md) konusundaki adımları uygulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="567d0-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](./dual-write-prospect-to-cash.md).</span></span>
- <span data-ttu-id="567d0-119">Aşağıdaki adımları izleyerek, el ile giriş için ticari sözleşme değerlendirmesini kapatmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="567d0-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="567d0-120">Commerce ortamınızda **Alacak hesapları\>Kurulum \>Alacak hesapları parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="567d0-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="567d0-121">**Fiyatlar** sekmesindeki **Ticari sözleşme değerlendirmesi** hızlı sekmesi altında **El ile giriş onay** kutusunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="567d0-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="567d0-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="567d0-122">Additional resources</span></span>

[<span data-ttu-id="567d0-123">Çift yazmada aday müşteriden nakde</span><span class="sxs-lookup"><span data-stu-id="567d0-123">Prospect-to-cash in dual-write</span></span>](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]