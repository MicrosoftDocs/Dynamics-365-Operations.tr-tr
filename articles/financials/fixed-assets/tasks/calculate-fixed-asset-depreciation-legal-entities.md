--- 
title: "Tüzel kişilikler arasında sabit kıymet amortismanı hesaplama"
description: "Bu yordam, birden fazla tüzel kişilik için amortisman işlemini nasıl ayarlayacağınızı ve çalıştıracağınızı gösterir."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 4221acf200f41ca39803bcd56c1b05e0d87bd948
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="a918e-103">Tüzel kişilikler arasında sabit kıymet amortismanı hesaplama</span><span class="sxs-lookup"><span data-stu-id="a918e-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a918e-104">Sabit kıymet amortismanı tüzel kişilikler arasında tek bir adımda çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="a918e-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="a918e-105">Bu yordam, birden fazla tüzel kişilik için işlemi nasıl ayarlayacağınızı ve çalıştıracağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="a918e-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="a918e-106">Muhasebeci rolünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="a918e-106">It uses the accountant role.</span></span>  

<span data-ttu-id="a918e-107">Bu kayıtta USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a918e-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="a918e-108">Adımlar (16) Alt görev: Şirketler arası amortisman çalıştırma günlüklerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a918e-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="a918e-109">İlk olarak, her tüzel kişilikte şirketler arası amortisman çalıştırmada kullanılacak günlükleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a918e-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="a918e-110">Sabit kıymetler > Kurulum > Sabit kıymet parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a918e-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="a918e-111">Sabit kıymet teklifleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a918e-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="a918e-112">Tüzel kişilikteki her deftere nakil katmanı için kullanılacak günlük adıyla bir kayıt oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a918e-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="a918e-113">Defterler genel muhasebeye nakledilmezse, ilişkilendirilen günlükle Hiçbiri deftere nakil katmanının seçilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a918e-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="a918e-114">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a918e-114">Click Add.</span></span> 
4. <span data-ttu-id="a918e-115">Deftere nakil katmanı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a918e-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="a918e-116">Günlük adı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="a918e-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="a918e-117">Her tüzel kişilik için Sabit kıymet parametreleri sayfasında günlük kurulumunu yineleyin.</span><span class="sxs-lookup"><span data-stu-id="a918e-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="a918e-118">Alt görev: Amortismanı hesaplama</span><span class="sxs-lookup"><span data-stu-id="a918e-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="a918e-119">Tüzel kişilikler arasında amortisman çalıştırmayı başlatmak için Amortisman teklifi oluştur sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="a918e-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="a918e-120">Sabit kıymetler > Günlük girişleri > Amortisman tekifi oluştur'a gidin.</span><span class="sxs-lookup"><span data-stu-id="a918e-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="a918e-121">Deftere nakil katmanı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a918e-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="a918e-122">Günlük adı varsayılan olarak Sabit kıymet parametrelerinden alınacaktır.</span><span class="sxs-lookup"><span data-stu-id="a918e-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="a918e-123">Burada geçerli tüzel kişilik için değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="a918e-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="a918e-124">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="a918e-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="a918e-125">Amortisman çalıştırmaya dahil edilecek tüzel kişilikleri seçin.</span><span class="sxs-lookup"><span data-stu-id="a918e-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="a918e-126">Yalnızca Sabit kıymet parametreleri sayfasında Sabit kıymet teklifleri için ayarlanan günlükleri bulunan tüzel kişilikler listede görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a918e-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="a918e-127">Etkinleştirildiğinde, Günlükleri deftere naklet seçeneği amortisman günlüklerini oluşturuldukları zaman otomatik olarak nakleder.</span><span class="sxs-lookup"><span data-stu-id="a918e-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="a918e-128">Seçili değilse, günlükler oluşturulur ancak deftere nakledilmez, böylece deftere nakletmeden önce ayrıntıları inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a918e-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="a918e-129">Günlükleri deftere naklet alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a918e-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="a918e-130">Filtreleme alanları, bu amortisman çalıştırma için seçilen tüzel kişiliklerle ilgili tüm sabit kıymetleri, grupları ve defterleri içerir.</span><span class="sxs-lookup"><span data-stu-id="a918e-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="a918e-131">Toplu işleme seçeneği varsayılan olarak etkindir.</span><span class="sxs-lookup"><span data-stu-id="a918e-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="a918e-132">Bu seçenek etkinleştirildiğinde, amortisman günlüğü oluşturma ve deftere nakletme arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="a918e-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="a918e-133">Günlük oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a918e-133">Click Create journal.</span></span> 
10. <span data-ttu-id="a918e-134">İlgili tüzel kişiliklerde oluşturulan amortisman günlüklerini görüntülemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a918e-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="a918e-135">Sabit kıymetler > Günlük girişler > Sabit kıymetler günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a918e-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

