--- 
title: "Sabit kıymetleri yeniden sınıflandırma"
description: "Sabit kıymeti yeniden sınıflandırmak için yeni bir sabit kıymet grubuna transfer etmeniz veya kıymete aynı grup içerisinde yeni bir sabit kıymet numarası atamanız gerekir."
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 02afc142187aed55e5186d83069c5419fc900106
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="2833e-103">Sabit kıymetleri yeniden sınıflandırma</span><span class="sxs-lookup"><span data-stu-id="2833e-103">Reclassify fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2833e-104">Sabit kıymeti yeniden sınıflandırmak için yeni bir sabit kıymet grubuna transfer etmeniz veya kıymete aynı grup içerisinde yeni bir sabit kıymet numarası atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2833e-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="2833e-105">Bir sabit kıymet yeniden sınıflandırıldığında:</span><span class="sxs-lookup"><span data-stu-id="2833e-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="2833e-106">• Varolan sabit kıymete yönelik tüm değer modelleri, yeni sabit kıymet için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2833e-106">• All value models for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="2833e-107">Özgün sabit kıymet için oluşturulan bilgiler yeni sabit kıymete kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2833e-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="2833e-108">Özgün sabit kıymete yönelik değer modellerinin durumu Kapalı'dır.</span><span class="sxs-lookup"><span data-stu-id="2833e-108">The status of the value models for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="2833e-109">• Yeni sabit kıymete yönelik yeni değer modelleri Alım tarihi alanındaki yeniden sınıflandırma tarihini içerir.</span><span class="sxs-lookup"><span data-stu-id="2833e-109">• The new value models of the new fixed asset contain the date of the reclassification in the Acquisition date field.</span></span> <span data-ttu-id="2833e-110">İlk amortisman göreceği tarih alanındaki tarih, özgün kıymet bilgilerinden kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2833e-110">The date in the Depreciation run date field is copied from the original asset information.</span></span> <span data-ttu-id="2833e-111">Amortisman önceden başlamışsa Amortismanın son çalıştırıldığı tarih alanında yeniden sınıflandırma tarihi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2833e-111">If the depreciation has already started, the Date when depreciation was last run field displays the date of the reclassification.</span></span> 

<span data-ttu-id="2833e-112">• Özgün sabit kıymetlere yönelik mevcut sabit kıymet hareketleri iptal edilir ve yeni sabit kıymet için yeniden oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2833e-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

1. <span data-ttu-id="2833e-113">Sabit kıymetler > Dönemsel görevler > Yeniden sınıflandırma öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="2833e-113">Go to Fixed assets > Periodic tasks > Reclassification.</span></span>
2. <span data-ttu-id="2833e-114">Sabit kıymet grubu alanında, yeniden sınıflandırılacak grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="2833e-114">In the Fixed asset group field, select the group to reclassify.</span></span>
3. <span data-ttu-id="2833e-115">Sabit kıymet numarası alanında, yeniden sınıflandırılacak sabit kıymeti seçin.</span><span class="sxs-lookup"><span data-stu-id="2833e-115">In the Fixed asset number field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="2833e-116">Yeni sabit kıymet grubu alanında, sabit kıymetin transfer edileceği grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="2833e-116">In the New fixed asset group field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="2833e-117">Yeni sabit kıymet grubu bir numara serisine eklenmişse Yeni sabit kıymet numarası alanı, yeni sabit kıymet grubu numara serisindeki numara ile güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2833e-117">If the new fixed asset group is attached to a number sequence, the New fixed asset number field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="2833e-118">Aksi takdirde, Yeni sabit kıymet numarası alanı Sabit kıymet parametreleri sayfasında ayarlanan numara serisindeki numara ile güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2833e-118">Otherwise, the New fixed asset number field is updated with the number from the number sequence that is set up in the Fixed asset parameters page.</span></span> <span data-ttu-id="2833e-119">Numara serisi Sabit kıymet parametreleri sayfasında ayarlanmadıysa Yeni sabit kıymet numarası alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="2833e-119">If a number sequence is not set up in the Fixed asset parameters page, enter a number in the New fixed asset number field.</span></span>  
5. <span data-ttu-id="2833e-120">Yeniden sınıflandırma tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="2833e-120">In the Reclassification date field, enter a date.</span></span>
6. <span data-ttu-id="2833e-121">Fiş serisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="2833e-121">In the Voucher series field, enter or select a value.</span></span>
7. <span data-ttu-id="2833e-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2833e-122">Click OK.</span></span>


