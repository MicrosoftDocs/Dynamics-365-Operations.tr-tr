---
title: Ek amortisman ayarlama
description: Bu yordam, özel amortisman payının nasıl oluşturulacağını ve bir sabit kıymet defteriyle nasıl ilişkilendirileceğini gösterir.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bbd6b78d05fcc9d95f6e6409db2619a210ad760
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "339223"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="0c936-103">Ek amortisman ayarlama</span><span class="sxs-lookup"><span data-stu-id="0c936-103">Set up bonus depreciation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c936-104">Bu yordam, özel amortisman payının nasıl oluşturulacağını ve bir sabit kıymet defteriyle nasıl ilişkilendirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c936-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="0c936-105">Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="0c936-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="0c936-106">Özel amortisman payı oluşturun</span><span class="sxs-lookup"><span data-stu-id="0c936-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="0c936-107">Sabit kıymetler > Kurulum > Özel amortisman payı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="0c936-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="0c936-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c936-108">Click New.</span></span>
3. <span data-ttu-id="0c936-109">Özel amortisman payı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="0c936-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="0c936-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="0c936-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0c936-111">Yüzde alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0c936-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="0c936-112">Yüzde gösterilmediyse bir tutar ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0c936-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="0c936-113">Özel amortisman payını bir sabit kıymet grubu defteriyle ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="0c936-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="0c936-114">Sabit kıymetler > Kurulum > Sabit kıymet grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="0c936-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="0c936-115">Listede, özel amortisman payıyla ilişkili sabit kıymet grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="0c936-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="0c936-116">Defterler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c936-116">Click Books.</span></span>
4. <span data-ttu-id="0c936-117">Listede, özel amortisman payıyla ilişkili defteri seçin.</span><span class="sxs-lookup"><span data-stu-id="0c936-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="0c936-118">Özel amortisman payı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c936-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="0c936-119">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c936-119">Click New.</span></span>
7. <span data-ttu-id="0c936-120">Özel amortisman payı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="0c936-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="0c936-121">Yüzde veya Tutar için varsayılan değer, özel amortisman payı kurulumundan alınır.</span><span class="sxs-lookup"><span data-stu-id="0c936-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="0c936-122">Öncelik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0c936-122">In the Priority field, enter a number.</span></span>

