---
title: Satış vergisi kapatma dönemlerini ayarla
description: Satış vergisi kapatma dönemleri, satış vergisinin bildirilip ödenmesi gereken dönem aralıkları hakkında bilgiler içerir.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8304d9e8997a5d31740ee1203aa4bf0603014056
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863000"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="2ffa2-103">Satış vergisi kapatma dönemlerini ayarla</span><span class="sxs-lookup"><span data-stu-id="2ffa2-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2ffa2-104">Satış vergisi kapatma dönemleri, satış vergisinin bildirilip ödenmesi gereken dönem aralıkları hakkında bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="2ffa2-105">Belirli bir tarih aralığında bir kapatma dönemi için bir kapatma işlemi yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="2ffa2-106">Kapatma dönemiyle ilişkili tüm vergi kodları kapatılır.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="2ffa2-107">İlgili satış vergisi dairesinin ayarlarına bağlı olarak, vergi borcu ya bir satıcıya veya bir Genel muhasebe hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="2ffa2-108">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="2ffa2-109">Vergi > Dolaylı vergiler > Satış vergisi > Satış vergisi kapatma dönemleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="2ffa2-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-110">Click New.</span></span>
3. <span data-ttu-id="2ffa2-111">Kapatma dönemi alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="2ffa2-112">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2ffa2-113">Makam alanında kapatma dönemi için oluşturulan bildirimleri ve ödemeleri alan satış vergisi makamını seçin.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="2ffa2-114">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="2ffa2-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2ffa2-116">Ödeme şartları alanında açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2ffa2-117">İlgili Satış vergi dairesi, bir satıcı olarak kurulabilir ve Satış vergisi kapatma işlemi bir açık satıcı faturası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="2ffa2-118">Ödeme koşulları, açık satıcı faturası için Vade tarihi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="2ffa2-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="2ffa2-120">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="2ffa2-121">Kapatma dönemi aralıkları için tür seçin.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="2ffa2-122">Dönem başına dönem aralığı birim sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="2ffa2-123">Örneğin üç aylık dönemde 3 ay vardır.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="2ffa2-124">Satış vergisi kapatma için toplu işlem kullan onay kutusunu işaretleyin veya kutuda işaret varsa kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="2ffa2-125">Kapatma dönemi için kapatma işlemi arka planda toplu iş olarak sürdürülebilir.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="2ffa2-126">Bu bir dönem aralığında çok sayıda vergi hareketi olması durumunda önerilir.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="2ffa2-127">Şu anda bu Avusturya, Belçika, İspanya, İtalya, Japonya ve Hollanda'da desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-127">Currently this is not supported in Austria, Belgium, Spain, Italy, Japan, and the Netherlands.</span></span>
14. <span data-ttu-id="2ffa2-128">Mahsup vergi hareketleri oluşturmayı engelle onay kutusunu seçin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-128">Select or clear the Prevent generating offset tax transactions check box.</span></span>
    * <span data-ttu-id="2ffa2-129">Varsayılan olarak, sistem kapatma işlemi sırasında mahsup vergi hareketleri oluşturur; bu da bir dönem aralığında çok sayıda vergi hareketi varsa performans sorununa neden olur.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-129">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="2ffa2-130">Mahsup vergi hareketleri oluşturmayı engellemek için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-130">Select this check box to prevent generating offset tax transactions.</span></span>
15. <span data-ttu-id="2ffa2-131">Dönem aralıkları sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-131">Expand the Period intervals tab.</span></span>
16. <span data-ttu-id="2ffa2-132">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-132">Click Add.</span></span>
17. <span data-ttu-id="2ffa2-133">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-133">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="2ffa2-134">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-134">In the From date field, enter a date.</span></span>
19. <span data-ttu-id="2ffa2-135">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-135">In the To date field, enter a date.</span></span>
20. <span data-ttu-id="2ffa2-136">Yeni dönem aralığı'nı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-136">Click New period interval.</span></span>
    * <span data-ttu-id="2ffa2-137">İlk dönem aralığı girildikten sonra yeni dönemler otomatik olarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-137">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="2ffa2-138">Gerektiğinde geri dönüp yeni dönem aralıkları ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-138">You can come back and add new period intervals as required.</span></span>  
21. <span data-ttu-id="2ffa2-139">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2ffa2-139">Close the page.</span></span>

