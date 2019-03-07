---
title: 'Maliyet öğeleri oluşturma  '
description: Maliyet muhasebesinde maliyet öğeleri oluşturmanın birkaç yolu vardır.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bbaf4f7533d51d554d838e8e9e2aa05ca451298a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "321720"
---
# <a name="create-cost-elements"></a><span data-ttu-id="5dd63-103">Maliyet öğeleri oluşturma  </span><span class="sxs-lookup"><span data-stu-id="5dd63-103">Create cost elements</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5dd63-104">Maliyet muhasebesinde maliyet öğeleri oluşturmanın birkaç yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="5dd63-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="5dd63-105">Bu yordam ana hesapları bir veri bağlayıcı aracılığıyla içe aktararak maliyet öğeleri oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="5dd63-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="5dd63-106">Bu yordamı oluşturmak için USMF demo şirketi kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="5dd63-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="5dd63-107">Bu yordam Dynamics 365 for Operations sürüm 1611 ile eklenen bir Maliyet muhasebesi özelliği içindir.</span><span class="sxs-lookup"><span data-stu-id="5dd63-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="5dd63-108">Yeni maliyet öğeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="5dd63-108">Create new cost elements</span></span>
1. <span data-ttu-id="5dd63-109">Maliyet muhasebesi > Boyutlar > Maliyet öğesi boyutları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="5dd63-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="5dd63-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dd63-110">Click New.</span></span>
3. <span data-ttu-id="5dd63-111">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="5dd63-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="5dd63-112">Boyut üyeleri için veri bağlayıcı alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="5dd63-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="5dd63-113">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="5dd63-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="5dd63-114">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dd63-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="5dd63-115">Veri bağlayıcıyı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5dd63-115">Configure the data connector</span></span>
1. <span data-ttu-id="5dd63-116">Boyut üyesi sağlayıcısını yapılandır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dd63-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="5dd63-117">Hesap planı alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="5dd63-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="5dd63-118">Paylaşılan hesap planını kullanmak için Paylaştırılmış öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5dd63-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="5dd63-119">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dd63-119">Click New.</span></span>
4. <span data-ttu-id="5dd63-120">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="5dd63-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5dd63-121">Hesaplara ölçütlerinizi karşılayacak filtreler uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5dd63-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="5dd63-122">Aba hesaptan alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="5dd63-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="5dd63-123">Ana hesaba alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="5dd63-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="5dd63-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dd63-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="5dd63-125">Ana hesapları içe aktar</span><span class="sxs-lookup"><span data-stu-id="5dd63-125">Import main accounts</span></span>
1. <span data-ttu-id="5dd63-126">Boyut üyelerini içe aktar öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dd63-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="5dd63-127">Ana hesapları Maliyet muhasebesine aktarılır ve maliyet öğesi olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5dd63-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="5dd63-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dd63-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="5dd63-129">İçe aktarılan hesapları maliyet öğesi olarak görüntüleme</span><span class="sxs-lookup"><span data-stu-id="5dd63-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="5dd63-130">Boyut üyelerini görüntüle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dd63-130">Click View dimension members.</span></span>
    * <span data-ttu-id="5dd63-131">Genel muhasebe hesaplarını işinizde maliyetlerin akış gerçekleştirebileceği maliyet öğeleri olarak görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="5dd63-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  

