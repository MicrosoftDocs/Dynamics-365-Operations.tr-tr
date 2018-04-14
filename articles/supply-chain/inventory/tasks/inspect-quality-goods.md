---
title: "Malların kalitesini denetleme"
description: ",Bu yordam, bir kalite emrinin nasıl işleneceğini gösterir."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ab536047340bdebecb7c8317e20208c87a4776f7
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="3abe0-103">Malların kalitesini denetleme</span><span class="sxs-lookup"><span data-stu-id="3abe0-103">Inspect the quality of goods</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3abe0-104">,Bu yordam, bir kalite emrinin nasıl işleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3abe0-104">This procedure shows you how to process a quality order.</span></span> <span data-ttu-id="3abe0-105">Bu kılavuzu USMF demo şirketinde çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3abe0-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="3abe0-106">Bu örnek işleme başlamadan önce "000016" satınalma siparişini onaylamanız ve ürün alış irsaliyesini deftere nakletmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3abe0-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="3abe0-107">Bu otomatik olarak bir kalite emri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3abe0-107">This will automatically create a quality order.</span></span> <span data-ttu-id="3abe0-108">Kalite incelemeleri genellikle bir kalite memuru tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3abe0-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="3abe0-109">Bir kalite emri seçin</span><span class="sxs-lookup"><span data-stu-id="3abe0-109">Select a quality order</span></span>
1. <span data-ttu-id="3abe0-110">Stok yönetimi > Periyodik görevler > Kalite yönetimi > Kalite emirleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="3abe0-110">Go to Inventory management > Periodic tasks > Quality management > Quality orders.</span></span>
2. <span data-ttu-id="3abe0-111">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3abe0-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3abe0-112">Bu yordamı başlatmadan önce oluşturulan kalite emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="3abe0-112">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="3abe0-113">Test sonuçlarını kaydetme</span><span class="sxs-lookup"><span data-stu-id="3abe0-113">Record test results</span></span>
1. <span data-ttu-id="3abe0-114">Sonuçlar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3abe0-114">Click Results.</span></span>
2. <span data-ttu-id="3abe0-115">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3abe0-115">Click Edit.</span></span>
3. <span data-ttu-id="3abe0-116">Sonuç miktarı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3abe0-116">In the Result quantity field, enter a number.</span></span>
4. <span data-ttu-id="3abe0-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3abe0-117">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="3abe0-118">Sonuç alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3abe0-118">In the Outcome field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3abe0-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3abe0-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3abe0-120">Bu örnekte sonuç, önceden tanımlanmış bir sonuca bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="3abe0-120">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="3abe0-121">Normalde, örneğin bir ebat veya başka bir boyut gibi, daha belirli bir test sonucu kaydedersiniz.</span><span class="sxs-lookup"><span data-stu-id="3abe0-121">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
7. <span data-ttu-id="3abe0-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3abe0-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="3abe0-123">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3abe0-123">Click Save.</span></span>
9. <span data-ttu-id="3abe0-124">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3abe0-124">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="3abe0-125">Kalite emrini doğrula</span><span class="sxs-lookup"><span data-stu-id="3abe0-125">Validate the quality order</span></span>
1. <span data-ttu-id="3abe0-126">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3abe0-126">Click Validate.</span></span>
2. <span data-ttu-id="3abe0-127">Tarafından alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3abe0-127">In the Validated by field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3abe0-128">Denetlemeyi gerçekleştirecek kullanıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="3abe0-128">Select the user performing the inspection.</span></span>  
3. <span data-ttu-id="3abe0-129">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3abe0-129">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3abe0-130">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3abe0-130">Click Select.</span></span>
5. <span data-ttu-id="3abe0-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3abe0-131">Click OK.</span></span>
6. <span data-ttu-id="3abe0-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3abe0-132">Close the page.</span></span>

