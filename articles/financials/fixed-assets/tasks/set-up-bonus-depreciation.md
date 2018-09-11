--- 
title: Ek amortisman ayarlama
description: "Bu yordam, özel amortisman payının nasıl oluşturulacağını ve bir sabit kıymet defteriyle nasıl ilişkilendirileceğini gösterir."
author: saraschi2
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 03b5e6c71ebe5070cce88c01daa5e7f2c4a9d036
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="74437-103">Ek amortisman ayarlama</span><span class="sxs-lookup"><span data-stu-id="74437-103">Set up bonus depreciation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="74437-104">Bu yordam, özel amortisman payının nasıl oluşturulacağını ve bir sabit kıymet defteriyle nasıl ilişkilendirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="74437-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="74437-105">Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="74437-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="74437-106">Özel amortisman payı oluşturun</span><span class="sxs-lookup"><span data-stu-id="74437-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="74437-107">Sabit kıymetler > Kurulum > Özel amortisman payı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="74437-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="74437-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74437-108">Click New.</span></span>
3. <span data-ttu-id="74437-109">Özel amortisman payı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="74437-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="74437-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="74437-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="74437-111">Yüzde alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="74437-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="74437-112">Yüzde gösterilmediyse bir tutar ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="74437-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="74437-113">Özel amortisman payını bir sabit kıymet grubu defteriyle ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="74437-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="74437-114">Sabit kıymetler > Kurulum > Sabit kıymet grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="74437-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="74437-115">Listede, özel amortisman payıyla ilişkili sabit kıymet grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="74437-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="74437-116">Defterler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74437-116">Click Books.</span></span>
4. <span data-ttu-id="74437-117">Listede, özel amortisman payıyla ilişkili defteri seçin.</span><span class="sxs-lookup"><span data-stu-id="74437-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="74437-118">Özel amortisman payı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74437-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="74437-119">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74437-119">Click New.</span></span>
7. <span data-ttu-id="74437-120">Özel amortisman payı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="74437-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="74437-121">Yüzde veya Tutar için varsayılan değer, özel amortisman payı kurulumundan alınır.</span><span class="sxs-lookup"><span data-stu-id="74437-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="74437-122">Öncelik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="74437-122">In the Priority field, enter a number.</span></span>


