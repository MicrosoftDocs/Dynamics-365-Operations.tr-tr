---
title: Yapılandırma kuralları oluşturma
description: Bu yordam, çeşitli ürün reçetesi satırlarının oluşmasını engellemek veya zorlamak için boyut tabanlı yapılandırmada kullanılmak üzere konfigürasyon kurallarını oluşturur.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a315ddecd2e10f508b86ac8ea18a36df71616963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "314751"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="98b8b-103">Yapılandırma kuralları oluşturma</span><span class="sxs-lookup"><span data-stu-id="98b8b-103">Create configuration rules</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="98b8b-104">Bu yordam, çeşitli ürün reçetesi satırlarının oluşmasını engellemek veya zorlamak için boyut tabanlı yapılandırmada kullanılmak üzere konfigürasyon kurallarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98b8b-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="98b8b-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="98b8b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="98b8b-106">Boyut tabanlı yapılandırma birleşimlerini nasıl oluşturulacağını açıklayan sekiz prosedür arasındaki yedinci budur.</span><span class="sxs-lookup"><span data-stu-id="98b8b-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="98b8b-107">Ürün bilgi yönetimi > Ürün reçeteleri, malzemeler ve formülleri > Ürün reçetesi seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="98b8b-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="98b8b-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="98b8b-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="98b8b-109">Boyut tabanlı yapılandırma için ürün reçetesini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="98b8b-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="98b8b-110">Eylem Bölmesinde, Seçenekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98b8b-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="98b8b-111">Görünümü değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98b8b-111">Click Change view.</span></span>
5. <span data-ttu-id="98b8b-112">Başlık görünümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98b8b-112">Click Header view.</span></span>
    * <span data-ttu-id="98b8b-113">Konfigürasyon rotası hızlı sekmesine erişim için üstbilgi görünümünü açın.</span><span class="sxs-lookup"><span data-stu-id="98b8b-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="98b8b-114">Yapılandırma yolu bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="98b8b-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="98b8b-115">Konfigürasyon rotası hızlı sekmesinin genişletilmiş modda olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="98b8b-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="98b8b-116">Konfigürasyon kuralları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98b8b-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="98b8b-117">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98b8b-117">Click New.</span></span>
9. <span data-ttu-id="98b8b-118">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="98b8b-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="98b8b-119">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="98b8b-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="98b8b-120">Geçerli konfigürasyon grubu içindeki öğeler görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="98b8b-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="98b8b-121">Kuraldaki koşulu temsil eden birini seçin.</span><span class="sxs-lookup"><span data-stu-id="98b8b-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="98b8b-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98b8b-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="98b8b-123">Yöntem alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="98b8b-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="98b8b-124">Başka bir konfigürasyon grubundaki bir maddenin seçilmesi veya seçiminin kaldırılmasını zorlamak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="98b8b-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="98b8b-125">Türetilen grup alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98b8b-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="98b8b-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="98b8b-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="98b8b-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98b8b-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="98b8b-128">İstenen konfigürasyon grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="98b8b-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="98b8b-129">Türetilen madde numarası alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98b8b-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="98b8b-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98b8b-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="98b8b-131">Tercih edilen yönteme göre seçilecek veya seçimi kaldırılacak madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="98b8b-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="98b8b-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="98b8b-132">Close the page.</span></span>

