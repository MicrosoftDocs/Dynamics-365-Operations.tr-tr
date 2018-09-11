--- 
title: "Maliyet nesneleri oluşturma  "
description: "Bu yordam , Microsoft Dynamics 365 for Finance and Operations, Enterprise edition maliyet merkezi mali boyutunu bir veri bağlayıcı aracılığıyla Maliyet muhasebesine içe aktararak maliyet nesneleri oluşturmayı gösterir."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 52b5fe092048cd7efe7b0a697cd7061ee0f65103
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="5b8df-103">Maliyet nesneleri oluşturma  </span><span class="sxs-lookup"><span data-stu-id="5b8df-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5b8df-104">Bu yordam , Microsoft Dynamics 365 for Finance and Operations, Enterprise edition maliyet merkezi mali boyutunu bir veri bağlayıcı aracılığıyla Maliyet muhasebesine içe aktararak maliyet nesneleri oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b8df-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="5b8df-105">Bu yordamı oluşturmak için USMF demo şirketi kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="5b8df-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="5b8df-106">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir Maliyet muhasebesi özelliği içindir.</span><span class="sxs-lookup"><span data-stu-id="5b8df-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="5b8df-107">Yeni maliyet nesneleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="5b8df-107">Create new cost objects</span></span>
1. <span data-ttu-id="5b8df-108">Maliyet muhasebesi > Boyutlar > Maliyet nesnesi boyutları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="5b8df-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="5b8df-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b8df-109">Click New.</span></span>
3. <span data-ttu-id="5b8df-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="5b8df-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="5b8df-111">Boyut üyeleri için veri bağlayıcı alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="5b8df-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="5b8df-112">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="5b8df-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="5b8df-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b8df-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="5b8df-114">Veri bağlayıcıyı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5b8df-114">Configure the data connector</span></span>
1. <span data-ttu-id="5b8df-115">Boyut üyesi sağlayıcısını yapılandır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b8df-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="5b8df-116">CostCenter boyutunu Maliyet muhasebesine aktarmak için CostCenter öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5b8df-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="5b8df-117">Boyut adı alanında, Maliyet merkezi öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5b8df-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="5b8df-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b8df-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="5b8df-119">Maliyet merkezlerini içe aktarma</span><span class="sxs-lookup"><span data-stu-id="5b8df-119">Import cost centers</span></span>
1. <span data-ttu-id="5b8df-120">Boyut üyelerini içe aktar öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b8df-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="5b8df-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b8df-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="5b8df-122">İçe aktarılan maliyet merkezlerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="5b8df-122">View the imported cost centers</span></span>
1. <span data-ttu-id="5b8df-123">Boyut üyelerini görüntüle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b8df-123">Click View dimension members.</span></span>


