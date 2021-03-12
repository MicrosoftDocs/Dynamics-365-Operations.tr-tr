---
title: Sabit kıymete bir ek girme
description: Bu prosedür, mevcut bir sabit kıymeti eklemenin nasıl yapılacağını gösterir.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: baac842660b6231529349ec97bcdbcdb971a0ac0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975978"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="51f0f-103">Sabit kıymete bir ek girme</span><span class="sxs-lookup"><span data-stu-id="51f0f-103">Enter an addition to a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51f0f-104">Bu prosedür, mevcut bir sabit kıymeti eklemenin nasıl yapılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="51f0f-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="51f0f-105">Sabit kıymet eklerinin amacı, yalnızca, bir kıymetin madde eklemelerini, bakımını veya iyileştirmelerini izleme ve bilgi amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="51f0f-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="51f0f-106">Sabit kıymet değerindeki veya servis ömründeki değişikliklerin ayrı ayrı yapılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="51f0f-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   

<span data-ttu-id="51f0f-107">Prosedürde Muhasebeci rolü ve USMF adlı tüzel kişilik için demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="51f0f-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="51f0f-108">Gezinti bölmesinde **Modüller > Sabit kıymetler > Sabit kıymetler > Sabit kıymetler günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="51f0f-108">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="51f0f-109">Listede, eklemede kullanılacak sabit kıymeti bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="51f0f-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="51f0f-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="51f0f-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="51f0f-111">Eylem Bölmesinde, **Sabit kıymet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="51f0f-111">On the Action Pane, click **Fixed asset**.</span></span>
5. <span data-ttu-id="51f0f-112">**Sabit kıymet ekleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="51f0f-112">Click **Fixed asset additions**.</span></span>
6. <span data-ttu-id="51f0f-113">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="51f0f-113">Click **New**.</span></span>
7. <span data-ttu-id="51f0f-114">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="51f0f-114">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="51f0f-115">**Alım tarihi** alanında, ek satınalma veya servisin tarihini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="51f0f-115">In the **Acquisition date** field, set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="51f0f-116">**Birim maliyeti** alanına madde bakım veya diğer geliştirmelerin maliyetini girin.</span><span class="sxs-lookup"><span data-stu-id="51f0f-116">In the **Unit cost** field, enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="51f0f-117">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="51f0f-117">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="51f0f-118">Toplam maliyetin sabit kıymet değeri üzerinde hiçbir etkisi yoktur; yalnızca izleme ve bilgi amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="51f0f-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="51f0f-119">Maliyet büyük harfle yazılırsa, ayrıca bir değer artırma düzeltmesi hareketinin nakledilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="51f0f-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="51f0f-120">**Genel** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="51f0f-120">Click the **General** tab.</span></span>

    * <span data-ttu-id="51f0f-121">Ekleme kıymetin servis ömrünü artırıyorsa, **Servis ömrünü artırır**'ı **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="51f0f-121">Set **Increases service life** to **Yes** if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="51f0f-122">Bu alan yalnızca bilgi amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="51f0f-122">This field is informational only.</span></span> <span data-ttu-id="51f0f-123">Servis ömrünü uzatmak için, kıymetin Değer modellerindeki ve/veya Amortisman defterlerindeki Servis ömrünü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="51f0f-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  

