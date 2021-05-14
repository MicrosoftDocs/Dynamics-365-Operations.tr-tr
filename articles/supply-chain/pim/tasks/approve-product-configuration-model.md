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
ms.openlocfilehash: 2c945756997b0580ac7ffb19261f9184e53a1c10
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920519"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="35fbc-103">Ürün yapılandırma modelini onaylama</span><span class="sxs-lookup"><span data-stu-id="35fbc-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="35fbc-104">Bu yordamın çalıştırılması için kullanılabilir en az bir ürün yapılandırma modeli olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="35fbc-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="35fbc-105">Bu yordam, USMF demo verisi şirketindeki son teknoloji hoparlör modelini kullanılır.</span><span class="sxs-lookup"><span data-stu-id="35fbc-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="35fbc-106">Bu modelin önceden onaylandığını unutmayın; yordam yine de tüm işlemi adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="35fbc-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="35fbc-107">**Ürün bilgileri yönetimi \> Ürünler \> Ürün yapılandırma modelleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="35fbc-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="35fbc-109">Bu yordam için son teknoloji hoparlör modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-109">Select the High end speaker model for this procedure.</span></span>  
1. <span data-ttu-id="35fbc-110">**Sürümler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-110">Select **Versions**.</span></span>
1. <span data-ttu-id="35fbc-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-111">Select **New**.</span></span>
1. <span data-ttu-id="35fbc-112">**Ürün numarası** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-112">In the **Product number** field, enter or select a value.</span></span>
    * <span data-ttu-id="35fbc-113">Bir ürüne verilen referans, ürün yapılandırma modelinin bir sürümünü temsil eder.</span><span class="sxs-lookup"><span data-stu-id="35fbc-113">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="35fbc-114">Yalnızca kısıtlama tabanlı yapılandırma teknolojisine sahip olan ana ürünler bu listede görünecektir.</span><span class="sxs-lookup"><span data-stu-id="35fbc-114">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
1. <span data-ttu-id="35fbc-115">**Başlangıç tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-115">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="35fbc-116">Ürün modeli sürümünün ne zaman kullanılabilir olacağını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-116">Select when the product model version will be available.</span></span>  
1. <span data-ttu-id="35fbc-117">**Bitiş tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-117">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="35fbc-118">Bu ürün modeli sürümünün sona ereceği bitiş tarihini seçin veya Hiçbir zaman seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-118">Select an end date when this product model version will expire, or select Never.</span></span>  
1. <span data-ttu-id="35fbc-119">Açılır iletişim kutusunu açmak için **Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-119">Select **Approve** to open the drop dialog.</span></span>
1. <span data-ttu-id="35fbc-120">**Onaylayan** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-120">In the **Approved by** field, enter or select a value.</span></span>
    * <span data-ttu-id="35fbc-121">İşlemlerde kullanılacak ürün modellerinin onaylanmasından sorumlu kişiyi seçin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-121">Select the person who is responsible for approving product models for use in operations.</span></span>  
1. <span data-ttu-id="35fbc-122">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-122">Select **OK**.</span></span>
1. <span data-ttu-id="35fbc-123">**Fiyatlandırma yöntemi** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-123">In the **Pricing method** field, select an option.</span></span>
    * <span data-ttu-id="35fbc-124">Ürün modeli versiyonunu etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="35fbc-124">Activate the product model version.</span></span> <span data-ttu-id="35fbc-125">Bir defada bir ürün modeli için yalnızca bir etkin ürün olması mümkündür.</span><span class="sxs-lookup"><span data-stu-id="35fbc-125">It is only possible to have one product active for one product model at a time.</span></span>  
1. <span data-ttu-id="35fbc-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="35fbc-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]