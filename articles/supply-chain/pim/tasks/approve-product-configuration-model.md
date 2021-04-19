---
title: Ürün yapılandırma modelini onaylama
description: Bu yordamın çalıştırılması için kullanılabilir en az bir ürün yapılandırma modeli olması gerekir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4767d5dc3944d2595a5b2a74a6d5c7c0ea0c849a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809458"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="ffaa2-103">Ürün yapılandırma modelini onaylama</span><span class="sxs-lookup"><span data-stu-id="ffaa2-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ffaa2-104">Bu yordamın çalıştırılması için kullanılabilir en az bir ürün yapılandırma modeli olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="ffaa2-105">Bu yordam, USMF demo verisi şirketindeki son teknoloji hoparlör modelini kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="ffaa2-106">Bu modelin önceden onaylandığını unutmayın; yordam yine de tüm işlemi adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="ffaa2-107">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ffaa2-108">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="ffaa2-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ffaa2-110">Bu yordam için son teknoloji hoparlör modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="ffaa2-111">Sürümler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-111">Click Versions.</span></span>
5. <span data-ttu-id="ffaa2-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-112">Click New.</span></span>
6. <span data-ttu-id="ffaa2-113">Ürün numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="ffaa2-114">Bir ürüne verilen referans, ürün yapılandırma modelinin bir sürümünü temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="ffaa2-115">Yalnızca kısıtlama tabanlı yapılandırma teknolojisine sahip olan ana ürünler bu listede görünecektir.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="ffaa2-116">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="ffaa2-117">Ürün modeli sürümünün ne zaman kullanılabilir olacağını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="ffaa2-118">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="ffaa2-119">Bu ürün modeli sürümünün sona ereceği bitiş tarihini seçin veya Hiçbir zaman seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="ffaa2-120">İletişim kutusunu açmak için Onayla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="ffaa2-121">Onaylayan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="ffaa2-122">İşlemlerde kullanılacak ürün modellerinin onaylanmasından sorumlu kişiyi seçin.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="ffaa2-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-123">Click OK.</span></span>
12. <span data-ttu-id="ffaa2-124">Fiyatlandırma yöntemi alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="ffaa2-125">Ürün modeli versiyonunu etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-125">Activate the product model version.</span></span> <span data-ttu-id="ffaa2-126">Bir defada bir ürün modeli için yalnızca bir etkin ürün olması mümkündür.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="ffaa2-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ffaa2-127">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]