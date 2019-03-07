---
title: Hazır raporlar oluştur ve çalıştır
description: Farklı çalışma alanlarından merkezdeki hazır raporları ve Perakende ve Ticaret altında bulunan Sorgular ve Satış raporlarını çalıştırmak için bu görev kılavuzunu kullanın.
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
ms.openlocfilehash: b42f86fc243312d18654b1a048f9dffb29afd187
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "365259"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="957bf-103">Hazır raporlar oluştur ve çalıştır</span><span class="sxs-lookup"><span data-stu-id="957bf-103">Generate and run out of box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="957bf-104">Farklı çalışma alanlarından merkezdeki hazır raporları ve Perakende ve Ticaret altında bulunan Sorgular ve Satış raporlarını çalıştırmak için bu görev kılavuzunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="957bf-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="957bf-105">Bu kaydı oluşturmak için kullanılan demo verisi şirketi USRT'dir.</span><span class="sxs-lookup"><span data-stu-id="957bf-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="957bf-106">Bu kayıt Sistem Yöneticisi rolüne yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="957bf-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="957bf-107">Raporları çalışma alanlarından başlatma</span><span class="sxs-lookup"><span data-stu-id="957bf-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="957bf-108">Perakende ve ticaret > Ürünler ve kategoriler > Kategori ve ürün yönetimi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="957bf-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="957bf-109">Raporlar bölümünü genişletmek veya daraltmak için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="957bf-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="957bf-110">En çok satılan ürünler raporu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="957bf-110">Click Top products report.</span></span>
4. <span data-ttu-id="957bf-111">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="957bf-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="957bf-112">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="957bf-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="957bf-113">Kanal alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="957bf-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="957bf-114">Ağaçta 'Contoso Retail\Contoso Retail USA\Central\Houston' seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="957bf-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="957bf-115">Bu, Perakende raporlama için varsayılan perakende kuruluş hiyerarşisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="957bf-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="957bf-116">Kuruluş yönetimi > Kuruluşlar > Kuruluş hiyerarşisi amaçları'na gidin, Perakende raporlama seçeneğini seçin ve Atanan hiyerarşiler altından Varsayılan sütununun işaretlendiği hiyerarşi adını işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="957bf-116">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="957bf-117">Demo verilerin (bu görev kaydı için kullanılan) bir parçası olarak, Perakende raporlama amacı için varsayılan kuruluş hiyerarşisi Bölgeye göre Perakende Mağazaları'dır.</span><span class="sxs-lookup"><span data-stu-id="957bf-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="957bf-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="957bf-118">Click OK.</span></span>
9. <span data-ttu-id="957bf-119">Görünüm alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="957bf-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="957bf-120">Ölçüt alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="957bf-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="957bf-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="957bf-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="957bf-122">Perakende ve Ticaret uygulaması bağlantısı altında bulunan satış raporları ve sorgulardan raporları başlatın.</span><span class="sxs-lookup"><span data-stu-id="957bf-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="957bf-123">Perakende ve ticaret > Sorgular ve raporlar > Satış raporları > Kategori satış raporu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="957bf-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="957bf-124">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="957bf-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="957bf-125">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="957bf-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="957bf-126">Kanal alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="957bf-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="957bf-127">Ağaçta 'Contoso Retail\Contoso Retail USA\West\Seattle' seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="957bf-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="957bf-128">Bu, Perakende raporlama için varsayılan perakende kuruluş hiyerarşisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="957bf-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="957bf-129">Kuruluş yönetimi > Kuruluşlar > Kuruluş hiyerarşisi amaçları'na gidin, Perakende raporlama seçeneğini seçin ve Atanan hiyerarşiler altından Varsayılan sütununun işaretlendiği hiyerarşi adını işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="957bf-129">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="957bf-130">Demo verilerin (bu görev kaydı için kullanılan) bir parçası olarak, Perakende raporlama amacı için varsayılan kuruluş hiyerarşisi Bölgeye göre Perakende Mağazaları'dır.</span><span class="sxs-lookup"><span data-stu-id="957bf-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="957bf-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="957bf-131">Click OK.</span></span>
7. <span data-ttu-id="957bf-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="957bf-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="957bf-133">HQ raporlarını dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="957bf-133">Export an HQ reports</span></span>
1. <span data-ttu-id="957bf-134">Perakende ve ticaret > Sorgular ve raporlar > Satış raporları > Kuruluş satış raporu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="957bf-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="957bf-135">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="957bf-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="957bf-136">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="957bf-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="957bf-137">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="957bf-137">Click OK.</span></span>
5. <span data-ttu-id="957bf-138">Dışa Aktar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="957bf-138">Click Export.</span></span>
6. <span data-ttu-id="957bf-139">PDF'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="957bf-139">Click PDF.</span></span>

