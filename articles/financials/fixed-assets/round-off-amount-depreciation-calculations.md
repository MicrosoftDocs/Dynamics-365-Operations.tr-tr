---
title: "Amortisman hesaplamaları için yuvarlanan tutar"
description: "Bu makalede, Defter ayarları sayfalarında bulunan Yuvarlama amortismanı alanı ele alınmaktadır."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0ad57b076542c38d3c29dba4caacf830de6f7200
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="a7f4c-103">Amortisman hesaplamaları için yuvarlanan tutar</span><span class="sxs-lookup"><span data-stu-id="a7f4c-103">Round-off amount for depreciation calculations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a7f4c-104">Bu makalede, Defter ayarları sayfalarında bulunan Yuvarlama amortismanı alanı ele alınmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="a7f4c-105">Her defter için yuvarlanan amortisman tutarları ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="a7f4c-106">Yuvarlanan amortisman tutarları, gelecek amortismanı ve sabit kıymetin değerini gösteren sabit kıymet amortisman profilinde ve ayrıca amortisman tekliflerinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="a7f4c-107">Defter için izin verilen en düşük amortisman tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="a7f4c-108">Ayarlanan yuvarlamadan bağımsız olarak, son amortisman dönemindeki amortisman tutarı yuvarlanmaz.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="a7f4c-109">Son amortisman döneminin sonunda sabit kıymet değeri mutlaka 0 (sıfır) olmalı veya hurda değeri kullanılıyorsa hurda değerine eşit olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="a7f4c-110">Örnek</span><span class="sxs-lookup"><span data-stu-id="a7f4c-110">Example</span></span>

<span data-ttu-id="a7f4c-111">Amortisman, yuvarlama olmadan 2,444.44 olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="a7f4c-112">Aşağıdaki tabloda da gösterildiği gibi, önerilen tutarlar yuvarlamanın nasıl ayarlandığına bağlı olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="a7f4c-113">Yuvarlama yöntemi</span><span class="sxs-lookup"><span data-stu-id="a7f4c-113">Rounding method</span></span> | <span data-ttu-id="a7f4c-114">Amortisman tutarı</span><span class="sxs-lookup"><span data-stu-id="a7f4c-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="a7f4c-115">Yuvarlama 0,1</span><span class="sxs-lookup"><span data-stu-id="a7f4c-115">Rounding 0.1</span></span>    | <span data-ttu-id="a7f4c-116">2.444,40</span><span class="sxs-lookup"><span data-stu-id="a7f4c-116">2,444.40</span></span>            |
| <span data-ttu-id="a7f4c-117">Yuvarlama 1,00</span><span class="sxs-lookup"><span data-stu-id="a7f4c-117">Rounding 1.00</span></span>   | <span data-ttu-id="a7f4c-118">2,444.00</span><span class="sxs-lookup"><span data-stu-id="a7f4c-118">2,444.00</span></span>            |
| <span data-ttu-id="a7f4c-119">Yuvarlama 10,00</span><span class="sxs-lookup"><span data-stu-id="a7f4c-119">Rounding 10.00</span></span>  | <span data-ttu-id="a7f4c-120">2,440.00</span><span class="sxs-lookup"><span data-stu-id="a7f4c-120">2,440.00</span></span>            |
| <span data-ttu-id="a7f4c-121">Yuvarlama 100,00</span><span class="sxs-lookup"><span data-stu-id="a7f4c-121">Rounding 100.00</span></span> | <span data-ttu-id="a7f4c-122">2,400.00</span><span class="sxs-lookup"><span data-stu-id="a7f4c-122">2,400.00</span></span>            |






