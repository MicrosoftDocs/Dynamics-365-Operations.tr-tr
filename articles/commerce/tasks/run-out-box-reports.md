---
title: Hazır raporlar oluştur ve çalıştır
description: Farklı çalışma alanlarından merkezdeki hazır raporları ve Ticaret altında bulunan Sorgular ve Satış raporlarını çalıştırmak için bu görev kılavuzunu kullanın.
author: ashishmsft
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db75b09f1ae1f83a88a5e5eaef0c8c1b8eab5901
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804149"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="60218-103">Hazır raporlar oluştur ve çalıştır</span><span class="sxs-lookup"><span data-stu-id="60218-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60218-104">Farklı çalışma alanlarından merkezdeki hazır raporları ve Ticaret altında bulunan Sorgular ve Satış raporlarını çalıştırmak için bu görev kılavuzunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="60218-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="60218-105">Bu kaydı oluşturmak için kullanılan demo verisi şirketi USRT'dir.</span><span class="sxs-lookup"><span data-stu-id="60218-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="60218-106">Bu kayıt Sistem Yöneticisi rolüne yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="60218-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="60218-107">Raporları çalışma alanlarından başlatma</span><span class="sxs-lookup"><span data-stu-id="60218-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="60218-108">Perakende ve ticaret > Ürünler ve kategoriler > Kategori ve ürün yönetimi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="60218-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="60218-109">Raporlar bölümünü genişletmek veya daraltmak için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60218-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="60218-110">En çok satılan ürünler raporu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60218-110">Click Top products report.</span></span>
4. <span data-ttu-id="60218-111">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="60218-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="60218-112">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="60218-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="60218-113">Kanal alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60218-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="60218-114">Ağaçta 'Contoso Retail\Contoso Retail USA\Central\Houston' seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="60218-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="60218-115">Bu, Commerce raporlama için varsayılan kuruluş hiyerarşisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="60218-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="60218-116">Kuruluş yönetimi > Kuruluşlar > Kuruluş hiyerarşisi amaçları'na gidin, Commerce raporlama seçeneğini belirleyin ve Atanan hiyerarşiler altından Varsayılan sütununun işaretlendiği hiyerarşi adını işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="60218-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="60218-117">Demo verilerin (bu görev kaydı için kullanılan) bir parçası olarak, raporlama amacı için varsayılan kuruluş hiyerarşisi Bölgeye göre Mağazaları'dır.</span><span class="sxs-lookup"><span data-stu-id="60218-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="60218-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60218-118">Click OK.</span></span>
9. <span data-ttu-id="60218-119">Görünüm alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="60218-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="60218-120">Ölçüt alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="60218-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="60218-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60218-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="60218-122">Sorgular ve satış raporlarındaki raporları Başlat</span><span class="sxs-lookup"><span data-stu-id="60218-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="60218-123">Perakende ve ticaret > Sorgular ve raporlar > Satış raporları > Kategori satış raporu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60218-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="60218-124">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="60218-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="60218-125">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="60218-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="60218-126">Kanal alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60218-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="60218-127">Ağaçta 'Contoso Retail\Contoso Retail USA\West\Seattle' seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="60218-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="60218-128">Bu, Commerce raporlama için varsayılan kuruluş hiyerarşisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="60218-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="60218-129">Kuruluş yönetimi > Kuruluşlar > Kuruluş hiyerarşisi amaçları'na gidin, Commerce raporlama seçeneğini belirleyin ve Atanan hiyerarşiler altından Varsayılan sütununun işaretlendiği hiyerarşi adını işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="60218-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="60218-130">Demo verilerin (bu görev kaydı için kullanılan) bir parçası olarak, raporlama amacı için varsayılan kuruluş hiyerarşisi Bölgeye göre Mağazaları'dır.</span><span class="sxs-lookup"><span data-stu-id="60218-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="60218-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60218-131">Click OK.</span></span>
7. <span data-ttu-id="60218-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60218-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="60218-133">HQ raporlarını dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="60218-133">Export an HQ reports</span></span>
1. <span data-ttu-id="60218-134">Perakende ve ticaret > Sorgular ve raporlar > Satış raporları > Kuruluş satış raporu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60218-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="60218-135">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="60218-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="60218-136">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="60218-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="60218-137">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60218-137">Click OK.</span></span>
5. <span data-ttu-id="60218-138">Dışa Aktar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60218-138">Click Export.</span></span>
6. <span data-ttu-id="60218-139">PDF'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60218-139">Click PDF.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]