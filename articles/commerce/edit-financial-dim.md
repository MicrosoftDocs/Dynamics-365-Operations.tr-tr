---
title: Perakende hareketlerinin mali boyutlarını düzenleme
description: Bu konuda, Microsoft Dynamics 365 Commerce uygulamasında Perakende hareketlerinin mali boyutların nasıl düzenleneceği açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 5a5a82adbad16d8fea2ccf60ae0dbfbd2fd9f3c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010187"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="f883f-103">Perakende hareketlerinin mali boyutlarını düzenleme</span><span class="sxs-lookup"><span data-stu-id="f883f-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f883f-104">Bu konuda, Microsoft Dynamics 365 Commerce uygulamasında Perakende hareketlerinin mali boyutların nasıl düzenleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f883f-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="f883f-105">Mali boyutları düzenleme</span><span class="sxs-lookup"><span data-stu-id="f883f-105">Edit financial dimensions</span></span>

<span data-ttu-id="f883f-106">Commerce genel merkezindeki Perakende hareketlerinin mali boyutlarını düzenlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f883f-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f883f-107">**Uygulamaları tümleştirmek için mali boyut konfigürasyonu** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="f883f-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="f883f-108">Etkin **Varsayılan boyut tümleştirmesi** kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="f883f-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="f883f-109">**Mali boyutlar** hızlı sekmesinde, Excel çalışma sayfasındaki düzenlemek istediğiniz tüm boyutların **Seçili** listesinde bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="f883f-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="f883f-110">Daha fazla bilgi için bkz. [Veri varlıkları](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span><span class="sxs-lookup"><span data-stu-id="f883f-110">For more information, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span></span>
1. <span data-ttu-id="f883f-111">Excel dosyasını **Ekstreler** sayfasından, **Perakende hareketleri** sayfasından veya **Mağaza mali öğeleri** çalışma alanındaki **Hareket doğrulama hataları** kutucuğundan indirin ve açın.</span><span class="sxs-lookup"><span data-stu-id="f883f-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="f883f-112">Hareket mali boyutunu değiştirmek için **Tasarım**'ı seçin ve ardından **Hareket (denetlenebilir)** satırının yanındaki kalem simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f883f-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="f883f-113">**FinancialDimensionDisplayValue** alanını bulup seçin, Excel çalışma sayfasının başlık bölümünde bir hücre seçin ve ardından **Etiket ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f883f-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="f883f-114">Önceki adımda seçtiğiniz hücrenin altında bir hücre seçin, **Değer Ekle**'yi ve ardından **Yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f883f-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="f883f-115">Mali boyutlar Excel çalışma sayfasına eklenir ve daha sonra düzenlenebilir ve yayımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="f883f-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="f883f-116">Hareket satırlarındaki boyutları değiştirmek için **Satış hareketleri (denetlenebilir)** satırını seçin, kalem simgesini seçin ve ardından 6. ve 7. adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="f883f-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="f883f-117">Ödeme satırlarındaki boyutları değiştirmek için **Ödeme hareketleri (denetlenebilir)** satırını seçin, kalem simgesini seçin ve ardından 6. ve 7. adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="f883f-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f883f-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f883f-118">Additional resources</span></span>

[<span data-ttu-id="f883f-119">Peşin ve nakit yönetimi hareketlerini düzenleme ve denetleme</span><span class="sxs-lookup"><span data-stu-id="f883f-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="f883f-120">Çevrimiçi siparişi ve zaman uyumsuz müşteri siparişi hareketlerini düzenleme ve denetleme</span><span class="sxs-lookup"><span data-stu-id="f883f-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="f883f-121">Perakende hareketlerini düzenlemek için bir Excel çalışma kitabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="f883f-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="f883f-122">Perakende hareketlerini düzenlemek için Excel çalışma kitabına alanlar ekleme</span><span class="sxs-lookup"><span data-stu-id="f883f-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
