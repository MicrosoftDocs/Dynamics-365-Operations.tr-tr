---
title: 'Maliyet nesneleri oluşturma  '
description: Bu yordam maliyet merkezi mali boyutunu bir veri bağlayıcı aracılığıyla Maliyet muhasebesine aktararak maliyet nesneleri oluşturmayı gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed020348e50158362fda7b6b36dcdb17c48b4532
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142329"
---
# <a name="create-cost-objects"></a><span data-ttu-id="9dcd1-103">Maliyet nesneleri oluşturma  </span><span class="sxs-lookup"><span data-stu-id="9dcd1-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9dcd1-104">Bu yordam maliyet merkezi mali boyutunu bir veri bağlayıcı aracılığıyla Maliyet muhasebesine aktararak maliyet nesneleri oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="9dcd1-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="9dcd1-105">Bu yordamı oluşturmak için USMF demo şirketi kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="9dcd1-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="9dcd1-106">Yeni maliyet nesneleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="9dcd1-106">Create new cost objects</span></span>
1. <span data-ttu-id="9dcd1-107">Maliyet muhasebesi > Boyutlar > Maliyet nesnesi boyutları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="9dcd1-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="9dcd1-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9dcd1-108">Click New.</span></span>
3. <span data-ttu-id="9dcd1-109">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9dcd1-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9dcd1-110">Boyut üyeleri için veri bağlayıcı alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9dcd1-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="9dcd1-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9dcd1-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="9dcd1-112">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9dcd1-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="9dcd1-113">Veri bağlayıcıyı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9dcd1-113">Configure the data connector</span></span>
1. <span data-ttu-id="9dcd1-114">Boyut üyesi sağlayıcısını yapılandır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9dcd1-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="9dcd1-115">CostCenter boyutunu Maliyet muhasebesine aktarmak için CostCenter öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9dcd1-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="9dcd1-116">Boyut adı alanında, Maliyet merkezi öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9dcd1-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="9dcd1-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9dcd1-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="9dcd1-118">Maliyet merkezlerini içe aktarma</span><span class="sxs-lookup"><span data-stu-id="9dcd1-118">Import cost centers</span></span>
1. <span data-ttu-id="9dcd1-119">Boyut üyelerini içe aktar öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9dcd1-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="9dcd1-120">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9dcd1-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="9dcd1-121">İçe aktarılan maliyet merkezlerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="9dcd1-121">View the imported cost centers</span></span>
1. <span data-ttu-id="9dcd1-122">Boyut üyelerini görüntüle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9dcd1-122">Click View dimension members.</span></span>

