--- 
title: "Yalın planlama gruplarını tanımlama"
description: "Yalın planlama grupları, ürünleri kanban planlamada gruplamak ve ayırt etmek için tanımlanır."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a5bc20c0a9e2396365caebeb3751d2090e4575a4
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="efb66-103">Yalın planlama gruplarını tanımlama</span><span class="sxs-lookup"><span data-stu-id="efb66-103">Define lean schedule groups</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="efb66-104">Yalın planlama grupları, ürünleri kanban planlamada gruplamak ve ayırt etmek için tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="efb66-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="efb66-105">Gruplandırma, şirket başına genel bir ilişkilendirmeyle veya belirli bir iş hücresine özgü olarak yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="efb66-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="efb66-106">Kanban planlama liste sayfasında görsel bir gösterge olması amacıyla her grup için atanmış bir renk kodu vardır.</span><span class="sxs-lookup"><span data-stu-id="efb66-106">Each group has a color code assigned for visual indication in the kanban scheduling listpage.</span></span> <span data-ttu-id="efb66-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="efb66-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="efb66-108">Yalın planlama grubunu tanımlama</span><span class="sxs-lookup"><span data-stu-id="efb66-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="efb66-109">Ürün bilgileri yönetimi > Yalın imalat > Kanban planlama kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="efb66-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="efb66-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="efb66-110">Click New.</span></span>
3. <span data-ttu-id="efb66-111">Zamanlama grubu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="efb66-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="efb66-112">Zamanlama grubu, genel grup olarak veya belirli bir iş hücresine özgü şekilde tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="efb66-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="efb66-113">Bu basit örnekte, genel bir grup tanımlanmıştır ve iş hücresi boş tutulur.</span><span class="sxs-lookup"><span data-stu-id="efb66-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="efb66-114">Bu grubun ayarları, belirli zamanlama grupları olmayan tüm iş hücreleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="efb66-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="efb66-115">Renk seçiminden bir renk seçin.</span><span class="sxs-lookup"><span data-stu-id="efb66-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="efb66-116">Renkler, kanban zamanlama listesi sayfasındaki veya kanban işlem panosundaki işleri vurgulamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="efb66-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="efb66-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="efb66-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="efb66-118">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="efb66-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="efb66-119">Ürün ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="efb66-119">Associate product</span></span>
1. <span data-ttu-id="efb66-120">Belirli bir ürünle ilişkilendirme yapma</span><span class="sxs-lookup"><span data-stu-id="efb66-120">Associate a specific product</span></span>
    * <span data-ttu-id="efb66-121">Yalın planlama gruplarıyla, belirli bir ürün (Ürün ilişkisi türü = Ürün) ya da bir ürün tahsisat anahtarının parçası olarak (Ürün ilişkisi türü = grup) ürün ilişkilendirmek için iki yol vardır.</span><span class="sxs-lookup"><span data-stu-id="efb66-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="efb66-122">İlişki türü alanında Ürün öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="efb66-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="efb66-123">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="efb66-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="efb66-124">İş çıkarma yeteneği oranı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="efb66-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="efb66-125">Varsayılan İş çıkarma yeteneği oranı 1'dir ve bunun anlamı ilgili ürünlerin üretim akışlarının işlem faaliyetlerinde belirtilen tam kapasiteyi tüketeceğidir.</span><span class="sxs-lookup"><span data-stu-id="efb66-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activites of the production flows.</span></span> <span data-ttu-id="efb66-126">İş çıkarma yeteneği oranı > 1, daha yüksek kaynak tüketimi, İş çıkarma yeteneği oranı > 1 ise daha düşük bir kaynak tüketimi ifade edilir.</span><span class="sxs-lookup"><span data-stu-id="efb66-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="efb66-127">Oran, maliyet hesaplamasında ve kanban işi tüketiminin hesaplanmasında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="efb66-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="efb66-128">Ürün tahsisat anahtarını ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="efb66-128">Associate item allocation key</span></span>
1. <span data-ttu-id="efb66-129">Ürün tahsisat anahtarını ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="efb66-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="efb66-130">Ürün ilişki türü Grubu kullanarak bir ürün tahsisat anahtarına bir ilişki ekleyin.</span><span class="sxs-lookup"><span data-stu-id="efb66-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="efb66-131">Bu işlem için verilerinizde tanımlanan bir tahmini ürün tahsisatı anahtarı gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="efb66-131">Note that for this process, you need a forecast item alllocation key defined in your data.</span></span>  
2. <span data-ttu-id="efb66-132">İlişki türü alanında Grup öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="efb66-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="efb66-133">Ürün tahsisat anahtarı alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="efb66-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="efb66-134">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="efb66-134">In the list, click the link in the selected row.</span></span>


