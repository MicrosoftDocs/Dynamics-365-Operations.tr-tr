---
title: Sabit kıymetleri yeniden sınıflandırma
description: Sabit kıymeti yeniden sınıflandırmak için yeni bir sabit kıymet grubuna transfer etmeniz veya kıymete aynı grup içerisinde yeni bir sabit kıymet numarası atamanız gerekir.
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbfb754459fad1f3b1509f4f9c65c20e0385b013
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944727"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="ff0f5-103">Sabit kıymetleri yeniden sınıflandırma</span><span class="sxs-lookup"><span data-stu-id="ff0f5-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff0f5-104">Sabit kıymeti yeniden sınıflandırmak için yeni bir sabit kıymet grubuna transfer etmeniz veya kıymete aynı grup içerisinde yeni bir sabit kıymet numarası atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="ff0f5-105">Bir sabit kıymet yeniden sınıflandırıldığında:</span><span class="sxs-lookup"><span data-stu-id="ff0f5-105">When a fixed asset is reclassified:</span></span>

- <span data-ttu-id="ff0f5-106">Varolan sabit kıymete yönelik tüm defterler, yeni sabit kıymet için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="ff0f5-107">Özgün sabit kıymet için oluşturulan bilgiler yeni sabit kıymete kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="ff0f5-108">Özgün sabit kıymete yönelik defterlerin durumu Kapalı'dır.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-108">The status of the books for the original fixed asset is Closed.</span></span> 

- <span data-ttu-id="ff0f5-109">Yeni sabit kıymete yönelik yeni defterler **Alım tarihi** alanındaki yeniden sınıflandırma tarihini içerir.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-109">The new books for the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="ff0f5-110">**İlk amortisman göreceği tarih** alanındaki tarih, özgün kıymet bilgilerinden kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="ff0f5-111">Amortisman önceden başlamışsa **Amortismanın son çalıştırıldığı tarih** alanında yeniden sınıflandırma tarihi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

- <span data-ttu-id="ff0f5-112">Özgün sabit kıymetlere yönelik mevcut sabit kıymet hareketleri iptal edilir ve yeni sabit kıymet için yeniden oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

- <span data-ttu-id="ff0f5-113">Transfer hareketi olan bir varlık yeniden sınıflandırıldığında sistem, bir transfer hareketinin yeniden sınıflandırma işlemi sırasında tamamlanmadığını belirtmek üzere **Eylem merkezi**'nde bir ileti görüntüler.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-113">When an asset that has a transfer transaction has been reclassified, the system will display a message in the **Action center** to indicate that a transfer transaction wasn't completed during the reclassification process.</span></span> <span data-ttu-id="ff0f5-114">Varolan yeniden sınıflandırma hareketlerini uygun mali boyutlara taşımak için bir transfer hareketini tamamlamak gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-114">It's necessary to complete a transfer transaction to move the existing reclassification transactions to the appropriate financial dimensions.</span></span> 

   <span data-ttu-id="ff0f5-115">Yeniden sınıflandırma işlemi sırasında, sistem varlık bakiyesini orijinal varlıktan yeni varlığa sınıflandırmak için aşağıdaki eylemleri çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-115">During the reclassification process, the system runs the following actions to reclassify the asset balance from the original asset to the new asset.</span></span> 
   
   - <span data-ttu-id="ff0f5-116">Yeniden sınıflama işlemi, verileri orijinal sabit varlık defterinden yeni sabit varlık defterine kopyalar.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-116">The reclassification process copies the data from the original fixed asset book to the new fixed asset book.</span></span>

   - <span data-ttu-id="ff0f5-117">Yeniden sınıflama hareketi, alım hareketine dahil edilen mali boyut bilgilerini içeren orijinal deftere nakledilen edinme bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-117">The reclassification transaction uses information from the original posted acquisition that includes financial dimension information that is included in the acquisition transaction.</span></span>  
   
   - <span data-ttu-id="ff0f5-118">Aynı zamanda, yeniden sınıflama işlemi, orijinal varlık alımı ve varlık transfer hareketini tersine çevirir.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-118">At the same time, the reclassification process reverses the original asset acquisition and asset transfer transaction.</span></span> 

<span data-ttu-id="ff0f5-119">Aşağıdaki diyagram ve prosedür, yeniden sınıflandırma işlemine bir örnek verir.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-119">The following diagram and procedure provide an example of the reclassification process.</span></span> 

<span data-ttu-id="ff0f5-120">[![Yeniden sınıflandırma işlemini gösteren diyagram](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span><span class="sxs-lookup"><span data-stu-id="ff0f5-120">[![Diagram showing the reclassicification process](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span></span>

<span data-ttu-id="ff0f5-121">Bir sabit kıymeti yeniden sınıflandırmak için şu adımları Izleyin:</span><span class="sxs-lookup"><span data-stu-id="ff0f5-121">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="ff0f5-122">**Sabit kıymetler > Dönemsel görevler > Yeniden sınıflandırma** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-122">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="ff0f5-123">**Sabit kıymet grubu** alanında, yeniden sınıflandırılacak grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-123">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="ff0f5-124">**Sabit kıymet numarası** alanında, yeniden sınıflandırılacak sabit kıymeti seçin.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-124">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="ff0f5-125">**Yeni sabit kıymet grubu** alanında, sabit kıymetin transfer edileceği grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-125">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="ff0f5-126">Yeni sabit kıymet grubu bir numara serisine eklenmişse **Yeni sabit kıymet numarası** alanı, yeni sabit kıymet grubu numara serisindeki numara ile güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-126">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="ff0f5-127">Aksi takdirde, **Yeni sabit kıymet numarası** alanı **Sabit kıymet parametreleri** sayfasında ayarlanan numara serisindeki numara ile güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-127">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="ff0f5-128">Numara serisi **Sabit kıymet parametreleri** sayfasında ayarlanmadıysa **Yeni sabit kıymet numarası** alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-128">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="ff0f5-129">**Yeniden sınıflandırma tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-129">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="ff0f5-130">**Fiş serisi** alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-130">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="ff0f5-131">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ff0f5-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
