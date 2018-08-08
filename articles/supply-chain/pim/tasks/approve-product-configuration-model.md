--- 
title: "Ürün yapılandırma modelini onaylama"
description: "Bu yordamın çalıştırılması için kullanılabilir en az bir ürün yapılandırma modeli olması gerekir."
author: ShylaThompson
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e0abc73543fef662e6070408324bac5d1f41f4d4
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="dbdc1-103">Ürün yapılandırma modelini onaylama</span><span class="sxs-lookup"><span data-stu-id="dbdc1-103">Approve a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dbdc1-104">Bu yordamın çalıştırılması için kullanılabilir en az bir ürün yapılandırma modeli olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="dbdc1-105">Bu yordam, USMF demo verisi şirketindeki son teknoloji hoparlör modelini kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="dbdc1-106">Bu modelin önceden onaylandığını unutmayın; yordam yine de tüm işlemi adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="dbdc1-107">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="dbdc1-108">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="dbdc1-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dbdc1-110">Bu yordam için son teknoloji hoparlör modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="dbdc1-111">Sürümler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-111">Click Versions.</span></span>
5. <span data-ttu-id="dbdc1-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-112">Click New.</span></span>
6. <span data-ttu-id="dbdc1-113">Ürün numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="dbdc1-114">Bir ürüne verilen referans, ürün yapılandırma modelinin bir sürümünü temsil eder.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="dbdc1-115">Yalnızca kısıtlama tabanlı yapılandırma teknolojisine sahip olan ana ürünler bu listede görünecektir.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="dbdc1-116">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="dbdc1-117">Ürün modeli sürümünün ne zaman kullanılabilir olacağını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="dbdc1-118">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="dbdc1-119">Bu ürün modeli sürümünün sona ereceği bitiş tarihini seçin veya Hiçbir zaman seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="dbdc1-120">İletişim kutusunu açmak için Onayla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="dbdc1-121">Onaylayan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="dbdc1-122">İşlemlerde kullanılacak ürün modellerinin onaylanmasından sorumlu kişiyi seçin.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="dbdc1-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-123">Click OK.</span></span>
12. <span data-ttu-id="dbdc1-124">Fiyatlandırma yöntemi alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="dbdc1-125">Ürün modeli versiyonunu etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-125">Activate the product model version.</span></span> <span data-ttu-id="dbdc1-126">Bir defada bir ürün modeli için yalnızca bir etkin ürün olması mümkündür.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="dbdc1-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="dbdc1-127">Close the page.</span></span>


