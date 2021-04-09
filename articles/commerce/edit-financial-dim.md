---
title: Perakende hareketlerinin mali boyutlarını düzenleme
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta perakende hareketlerinin mali boyutların nasıl düzenleneceği açıklanmaktadır.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: ff16d8e2e75a877e5ca7de604c7915e908473da6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792717"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="7ba38-103">Perakende hareketlerinin mali boyutlarını düzenleme</span><span class="sxs-lookup"><span data-stu-id="7ba38-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ba38-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta perakende hareketlerinin mali boyutların nasıl düzenleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7ba38-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="7ba38-105">Mali boyutları düzenleme</span><span class="sxs-lookup"><span data-stu-id="7ba38-105">Edit financial dimensions</span></span>

<span data-ttu-id="7ba38-106">Commerce genel merkezindeki perakende hareketlerinin mali boyutlarını düzenlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7ba38-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="7ba38-107">**Uygulamaları tümleştirmek için mali boyut konfigürasyonu** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="7ba38-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="7ba38-108">Etkin **Varsayılan boyut tümleştirmesi** kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="7ba38-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="7ba38-109">**Mali boyutlar** hızlı sekmesinde, Excel çalışma sayfasındaki düzenlemek istediğiniz tüm boyutların **Seçili** listesinde bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="7ba38-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="7ba38-110">Daha fazla bilgi için bkz. [Veri varlıkları](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span><span class="sxs-lookup"><span data-stu-id="7ba38-110">For more information, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span></span>
1. <span data-ttu-id="7ba38-111">Excel dosyasını **Ekstreler** sayfasından, **Perakende hareketleri** sayfasından veya **Mağaza mali öğeleri** çalışma alanındaki **Hareket doğrulama hataları** kutucuğundan indirin ve açın.</span><span class="sxs-lookup"><span data-stu-id="7ba38-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="7ba38-112">Hareket mali boyutunu değiştirmek için **Tasarım**'ı seçin ve ardından **Hareket (denetlenebilir)** satırının yanındaki kalem simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ba38-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="7ba38-113">**FinancialDimensionDisplayValue** alanını bulup seçin, Excel çalışma sayfasının başlık bölümünde bir hücre seçin ve ardından **Etiket ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7ba38-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="7ba38-114">Önceki adımda seçtiğiniz hücrenin altında bir hücre seçin, **Değer Ekle**'yi ve ardından **Yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7ba38-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="7ba38-115">Mali boyutlar Excel çalışma sayfasına eklenir ve daha sonra düzenlenebilir ve yayımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="7ba38-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="7ba38-116">Hareket satırlarındaki boyutları değiştirmek için **Satış hareketleri (denetlenebilir)** satırını seçin, kalem simgesini seçin ve ardından 6. ve 7. adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="7ba38-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="7ba38-117">Ödeme satırlarındaki boyutları değiştirmek için **Ödeme hareketleri (denetlenebilir)** satırını seçin, kalem simgesini seçin ve ardından 6. ve 7. adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="7ba38-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7ba38-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7ba38-118">Additional resources</span></span>

[<span data-ttu-id="7ba38-119">Peşin ve nakit yönetimi hareketlerini düzenleme ve denetleme</span><span class="sxs-lookup"><span data-stu-id="7ba38-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="7ba38-120">Çevrimiçi siparişi ve zaman uyumsuz müşteri siparişi hareketlerini düzenleme ve denetleme</span><span class="sxs-lookup"><span data-stu-id="7ba38-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="7ba38-121">Perakende hareketlerini düzenlemek için bir Excel çalışma kitabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="7ba38-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="7ba38-122">Perakende hareketlerini düzenlemek için Excel çalışma kitabına alanlar ekleme</span><span class="sxs-lookup"><span data-stu-id="7ba38-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]