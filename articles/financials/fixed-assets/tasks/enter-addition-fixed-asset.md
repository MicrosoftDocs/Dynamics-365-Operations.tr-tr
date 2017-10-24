--- 
title: "Sabit kıymete bir ek girme"
description: "Bu prosedür, mevcut bir sabit kıymeti eklemenin nasıl yapılacağını gösterir."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 3579148033023f648e1a78a3dd009018f153fdad
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="c7e1a-103">Sabit kıymete bir ek girme</span><span class="sxs-lookup"><span data-stu-id="c7e1a-103">Enter an addition to a fixed asset</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c7e1a-104">Bu prosedür, mevcut bir sabit kıymeti eklemenin nasıl yapılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="c7e1a-105">Sabit kıymet eklerinin amacı, yalnızca, bir kıymetin madde eklemelerini, bakımını veya iyileştirmelerini izleme ve bilgi amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="c7e1a-106">Sabit kıymet değerindeki veya servis ömründeki değişikliklerin ayrı ayrı yapılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   



<span data-ttu-id="c7e1a-107">Prosedürde Muhasebeci rolü ve USMF adlı tüzel kişilik için demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="c7e1a-108">Sabit kıymetler > Sabit kıymetler > Sabit kıymetler menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="c7e1a-109">Listede, eklemede kullanılacak sabit kıymeti bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="c7e1a-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c7e1a-111">Eylem Bölmesinde, Sabit kıymet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-111">On the Action Pane, click Fixed asset.</span></span>
5. <span data-ttu-id="c7e1a-112">Sabit kıymet ekleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-112">Click Fixed asset additions.</span></span>
6. <span data-ttu-id="c7e1a-113">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-113">Click New.</span></span>
7. <span data-ttu-id="c7e1a-114">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="c7e1a-115">Ek satınalma veya servis tarihini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-115">Set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="c7e1a-116">Kıymete ait madde, bakım veya diğer geliştirmelerin maliyetini girin.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-116">Enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="c7e1a-117">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-117">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="c7e1a-118">Toplam maliyetin sabit kıymet değeri üzerinde hiçbir etkisi yoktur; yalnızca izleme ve bilgi amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="c7e1a-119">Maliyet büyük harfle yazılırsa, ayrıca bir değer artırma düzeltmesi hareketinin nakledilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="c7e1a-120">Genel sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-120">Click the General tab.</span></span>
    * <span data-ttu-id="c7e1a-121">Ekleme kıymetin servis ömrünü artırıyorsa, Servis ömrünü artırır'ı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-121">Set Increases service life if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="c7e1a-122">Bu alan yalnızca bilgi amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-122">This field is informational only.</span></span> <span data-ttu-id="c7e1a-123">Servis ömrünü uzatmak için, kıymetin Değer modellerindeki ve/veya Amortisman defterlerindeki Servis ömrünü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  


