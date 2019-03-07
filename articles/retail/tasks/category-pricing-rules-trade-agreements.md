---
title: Ticari sözleşmeler oluşturmak için kategori fiyatlandırma kuralları
description: Bu yordam, kategori fiyatlandırma kuralı kullanarak satış fiyatı ticaret anlaşmalarının nasıl oluşturulacağını göstermektedir.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPricingDiscountCategoryPriceRule, RetailCategoryPriceRule, EcoResCategorySingleLookup, RetailCategoryPriceWizard, PriceDiscAdm, PriceDiscAdmTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d252982cf1e4fa2f06646d0909e6f82d16f4cfc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "355530"
---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="cf69e-103">Ticari sözleşmeler oluşturmak için kategori fiyatlandırma kuralları</span><span class="sxs-lookup"><span data-stu-id="cf69e-103">Category pricing rules to create trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="cf69e-104">Bu yordam, kategori fiyatlandırma kuralı kullanarak satış fiyatı ticaret anlaşmalarının nasıl oluşturulacağını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="cf69e-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="cf69e-105">Bu görevi oluşturmak için kullanılan demo verisi şirketi USRT'dir.</span><span class="sxs-lookup"><span data-stu-id="cf69e-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="cf69e-106">Bu görev, perakende ticaret yöneticisi rolü için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="cf69e-106">This task is intended for the Retail merchandising manager role.</span></span>

1. <span data-ttu-id="cf69e-107">Fiyatlandırma ve iskonto yönetimi öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cf69e-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="cf69e-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cf69e-108">Click New.</span></span>
3. <span data-ttu-id="cf69e-109">Kategori fiyatı kuralına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cf69e-109">Click Category price rule.</span></span>
4. <span data-ttu-id="cf69e-110">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="cf69e-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="cf69e-111">Hesap kodu alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="cf69e-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="cf69e-112">"Grup" türü hesap kodu, belirli Kanallar, bağlılık programları, kataloglar ve ilişkiler için satış fiyatlı ticari anlaşmaları ayarlamakta kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cf69e-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="cf69e-113">Hesap seçim alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="cf69e-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="cf69e-114">Kategori alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="cf69e-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="cf69e-115">Tutar/Yüzde alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="cf69e-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="cf69e-116">Yuvarlama sürümü alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="cf69e-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="cf69e-117">Ticari sözleşmeler oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cf69e-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="cf69e-118">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cf69e-118">Click Next.</span></span>
12. <span data-ttu-id="cf69e-119">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="cf69e-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="cf69e-120">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="cf69e-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="cf69e-121">Sonrakini bul alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cf69e-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="cf69e-122">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cf69e-122">Click Next.</span></span>
16. <span data-ttu-id="cf69e-123">Son düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cf69e-123">Click Finish.</span></span>
    * <span data-ttu-id="cf69e-124">Bu bir ticari sözleşme günlüğü oluşturur ve gözden geçirmeniz için açar.</span><span class="sxs-lookup"><span data-stu-id="cf69e-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="cf69e-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cf69e-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cf69e-126">Kategori fiyatlandırma kurallarından oluşturulan ticari sözleşme günlükleri kayıt edilmez.</span><span class="sxs-lookup"><span data-stu-id="cf69e-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="cf69e-127">Fiyatları deftere nakletmeden önce gözden geçirin ve fiyatlarını düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="cf69e-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="cf69e-128">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cf69e-128">Click Edit.</span></span>
19. <span data-ttu-id="cf69e-129">Para birimi miktarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="cf69e-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="cf69e-130">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cf69e-130">Click Post.</span></span>
21. <span data-ttu-id="cf69e-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cf69e-131">Click OK.</span></span>
22. <span data-ttu-id="cf69e-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="cf69e-132">Close the page.</span></span>
23. <span data-ttu-id="cf69e-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="cf69e-133">Close the page.</span></span>
24. <span data-ttu-id="cf69e-134">Kategori fiyatı kuralları sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cf69e-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="cf69e-135">Kanal için belirli kategori fiyatlandırma kuralları bu listede gösterilir.</span><span class="sxs-lookup"><span data-stu-id="cf69e-135">Channel specific Category pricing rules will show in this list.</span></span>  

