---
title: Hazır raporlar oluştur ve çalıştır
description: Farklı çalışma alanlarından merkezdeki hazır raporları ve Ticaret altında bulunan Sorgular ve Satış raporlarını çalıştırmak için bu görev kılavuzunu kullanın.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f9931a39e4ca2141ed5b43086226c7fcc7cbd7c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024303"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="78830-103">Hazır raporlar oluştur ve çalıştır</span><span class="sxs-lookup"><span data-stu-id="78830-103">Generate and run out of box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="78830-104">Farklı çalışma alanlarından merkezdeki hazır raporları ve Ticaret altında bulunan Sorgular ve Satış raporlarını çalıştırmak için bu görev kılavuzunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="78830-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="78830-105">Bu kaydı oluşturmak için kullanılan demo verisi şirketi USRT'dir.</span><span class="sxs-lookup"><span data-stu-id="78830-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="78830-106">Bu kayıt Sistem Yöneticisi rolüne yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="78830-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="78830-107">Raporları çalışma alanlarından başlatma</span><span class="sxs-lookup"><span data-stu-id="78830-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="78830-108">Perakende ve ticaret > Ürünler ve kategoriler > Kategori ve ürün yönetimi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="78830-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="78830-109">Raporlar bölümünü genişletmek veya daraltmak için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78830-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="78830-110">En çok satılan ürünler raporu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78830-110">Click Top products report.</span></span>
4. <span data-ttu-id="78830-111">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="78830-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="78830-112">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="78830-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="78830-113">Kanal alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78830-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="78830-114">Ağaçta 'Contoso Retail\Contoso Retail USA\Central\Houston' seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="78830-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="78830-115">Bu, Commerce raporlama için varsayılan kuruluş hiyerarşisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="78830-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="78830-116">Kuruluş yönetimi > Kuruluşlar > Kuruluş hiyerarşisi amaçları'na gidin, Commerce raporlama seçeneğini belirleyin ve Atanan hiyerarşiler altından Varsayılan sütununun işaretlendiği hiyerarşi adını işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="78830-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="78830-117">Demo verilerin (bu görev kaydı için kullanılan) bir parçası olarak, raporlama amacı için varsayılan kuruluş hiyerarşisi Bölgeye göre Mağazaları'dır.</span><span class="sxs-lookup"><span data-stu-id="78830-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="78830-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78830-118">Click OK.</span></span>
9. <span data-ttu-id="78830-119">Görünüm alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="78830-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="78830-120">Ölçüt alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="78830-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="78830-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78830-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="78830-122">Sorgular ve satış raporlarındaki raporları Başlat</span><span class="sxs-lookup"><span data-stu-id="78830-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="78830-123">Perakende ve ticaret > Sorgular ve raporlar > Satış raporları > Kategori satış raporu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78830-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="78830-124">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="78830-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="78830-125">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="78830-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="78830-126">Kanal alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78830-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="78830-127">Ağaçta 'Contoso Retail\Contoso Retail USA\West\Seattle' seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="78830-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="78830-128">Bu, Commerce raporlama için varsayılan kuruluş hiyerarşisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="78830-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="78830-129">Kuruluş yönetimi > Kuruluşlar > Kuruluş hiyerarşisi amaçları'na gidin, Commerce raporlama seçeneğini belirleyin ve Atanan hiyerarşiler altından Varsayılan sütununun işaretlendiği hiyerarşi adını işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="78830-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="78830-130">Demo verilerin (bu görev kaydı için kullanılan) bir parçası olarak, raporlama amacı için varsayılan kuruluş hiyerarşisi Bölgeye göre Mağazaları'dır.</span><span class="sxs-lookup"><span data-stu-id="78830-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="78830-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78830-131">Click OK.</span></span>
7. <span data-ttu-id="78830-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78830-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="78830-133">HQ raporlarını dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="78830-133">Export an HQ reports</span></span>
1. <span data-ttu-id="78830-134">Perakende ve ticaret > Sorgular ve raporlar > Satış raporları > Kuruluş satış raporu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78830-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="78830-135">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="78830-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="78830-136">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="78830-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="78830-137">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78830-137">Click OK.</span></span>
5. <span data-ttu-id="78830-138">Dışa Aktar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78830-138">Click Export.</span></span>
6. <span data-ttu-id="78830-139">PDF'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78830-139">Click PDF.</span></span>

