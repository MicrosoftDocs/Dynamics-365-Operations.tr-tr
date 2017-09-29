--- 
title: "Ürün yapılandırma modelini onaylama"
description: "Bu yordamın çalıştırılması için kullanılabilir en az bir ürün yapılandırma modeli olması gerekir."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fa4548d3017246cbe49e2613f8990df6ea1c368b
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="01191-103">Ürün yapılandırma modelini onaylama</span><span class="sxs-lookup"><span data-stu-id="01191-103">Approve a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="01191-104">Bu yordamın çalıştırılması için kullanılabilir en az bir ürün yapılandırma modeli olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="01191-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="01191-105">Bu yordam, USMF demo verisi şirketindeki son teknoloji hoparlör modelini kullanılır.</span><span class="sxs-lookup"><span data-stu-id="01191-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="01191-106">Bu modelin önceden onaylandığını unutmayın; yordam yine de tüm işlemi adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="01191-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="01191-107">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01191-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="01191-108">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01191-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="01191-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="01191-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="01191-110">Bu yordam için son teknoloji hoparlör modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="01191-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="01191-111">Sürümler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="01191-111">Click Versions.</span></span>
5. <span data-ttu-id="01191-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01191-112">Click New.</span></span>
6. <span data-ttu-id="01191-113">Ürün numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="01191-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="01191-114">Bir ürüne verilen referans, ürün yapılandırma modelinin bir sürümünü temsil eder.</span><span class="sxs-lookup"><span data-stu-id="01191-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="01191-115">Yalnızca kısıtlama tabanlı yapılandırma teknolojisine sahip olan ana ürünler bu listede görünecektir.</span><span class="sxs-lookup"><span data-stu-id="01191-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="01191-116">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="01191-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="01191-117">Ürün modeli sürümünün ne zaman kullanılabilir olacağını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="01191-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="01191-118">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="01191-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="01191-119">Bu ürün modeli sürümünün sona ereceği bitiş tarihini seçin veya Hiçbir zaman seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="01191-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="01191-120">İletişim kutusunu açmak için Onayla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="01191-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="01191-121">Onaylayan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="01191-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="01191-122">İşlemlerde kullanılacak ürün modellerinin onaylanmasından sorumlu kişiyi seçin.</span><span class="sxs-lookup"><span data-stu-id="01191-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="01191-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01191-123">Click OK.</span></span>
12. <span data-ttu-id="01191-124">Fiyatlandırma yöntemi alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="01191-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="01191-125">Ürün modeli versiyonunu etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="01191-125">Activate the product model version.</span></span> <span data-ttu-id="01191-126">Bir defada bir ürün modeli için yalnızca bir etkin ürün olması mümkündür.</span><span class="sxs-lookup"><span data-stu-id="01191-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="01191-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="01191-127">Close the page.</span></span>


