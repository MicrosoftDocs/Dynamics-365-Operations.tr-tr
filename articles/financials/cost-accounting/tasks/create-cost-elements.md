--- 
title: "Maliyet öğeleri oluşturma  "
description: "Maliyet muhasebesinde maliyet öğeleri oluşturmanın birkaç yolu vardır."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1e665fc53455e457a2488f4ec28ebb5b715d90eb
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-cost-elements"></a><span data-ttu-id="9fc75-103">Maliyet öğeleri oluşturma  </span><span class="sxs-lookup"><span data-stu-id="9fc75-103">Create cost elements</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9fc75-104">Maliyet muhasebesinde maliyet öğeleri oluşturmanın birkaç yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="9fc75-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="9fc75-105">Bu yordam ana hesapları bir veri bağlayıcı aracılığıyla içe aktararak maliyet öğeleri oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fc75-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="9fc75-106">Bu yordamı oluşturmak için USMF demo şirketi kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="9fc75-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="9fc75-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir Maliyet muhasebesi özelliği içindir.</span><span class="sxs-lookup"><span data-stu-id="9fc75-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="9fc75-108">Yeni maliyet öğeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="9fc75-108">Create new cost elements</span></span>
1. <span data-ttu-id="9fc75-109">Maliyet muhasebesi > Boyutlar > Maliyet öğesi boyutları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="9fc75-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="9fc75-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9fc75-110">Click New.</span></span>
3. <span data-ttu-id="9fc75-111">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9fc75-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9fc75-112">Boyut üyeleri için veri bağlayıcı alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9fc75-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="9fc75-113">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9fc75-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="9fc75-114">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9fc75-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="9fc75-115">Veri bağlayıcıyı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9fc75-115">Configure the data connector</span></span>
1. <span data-ttu-id="9fc75-116">Boyut üyesi sağlayıcısını yapılandır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9fc75-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="9fc75-117">Hesap planı alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9fc75-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="9fc75-118">Paylaşılan hesap planını kullanmak için Paylaştırılmış öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9fc75-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="9fc75-119">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9fc75-119">Click New.</span></span>
4. <span data-ttu-id="9fc75-120">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="9fc75-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9fc75-121">Hesaplara ölçütlerinizi karşılayacak filtreler uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9fc75-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="9fc75-122">Aba hesaptan alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9fc75-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="9fc75-123">Ana hesaba alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9fc75-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="9fc75-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9fc75-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="9fc75-125">Ana hesapları içe aktar</span><span class="sxs-lookup"><span data-stu-id="9fc75-125">Import main accounts</span></span>
1. <span data-ttu-id="9fc75-126">Boyut üyelerini içe aktar öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9fc75-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="9fc75-127">Ana hesapları Maliyet muhasebesine aktarılır ve maliyet öğesi olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9fc75-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="9fc75-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9fc75-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="9fc75-129">İçe aktarılan hesapları maliyet öğesi olarak görüntüleme</span><span class="sxs-lookup"><span data-stu-id="9fc75-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="9fc75-130">Boyut üyelerini görüntüle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9fc75-130">Click View dimension members.</span></span>
    * <span data-ttu-id="9fc75-131">Genel muhasebe hesaplarını işinizde maliyetlerin akış gerçekleştirebileceği maliyet öğeleri olarak görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="9fc75-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  


