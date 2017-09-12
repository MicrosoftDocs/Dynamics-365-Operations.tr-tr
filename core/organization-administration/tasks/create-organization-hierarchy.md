--- 
title: "Bir kuruluş hiyerarşisi oluşturma"
description: "Bir organizasyon hiyerarşisi oluşturmak için aşağıdaki prosedürü kullanın."
author: sericks007
manager: AnnBe
ms.date: 06/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: be64b137fc885747bcd9e3cf11013a18b7835d0e
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="af9a8-103">Bir kuruluş hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="af9a8-103">Create an organization hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af9a8-104">Bir organizasyon hiyerarşisi oluşturmak için aşağıdaki prosedürü kullanın.</span><span class="sxs-lookup"><span data-stu-id="af9a8-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="af9a8-105">İşlerinize farklı perspektiflerden bakmak ve raporlamak için organizasyonel hiyerarşileri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af9a8-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="af9a8-106">Örneğin, vergi, hukuki veya yasal raporlamaya yönelik bir hiyerarşi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af9a8-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="af9a8-107">Ardından, yasal olarak gerekmeyen ama dahili raporlama için kullanılan mali bilgileri raporlamak için başka bir hiyerarşi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af9a8-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 



<span data-ttu-id="af9a8-108">Bir kuruluş hiyerarşisi oluşturmadan önce kuruluşları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="af9a8-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="af9a8-109">Daha fazla bilgi için "Bir tüzel kişilik oluşturma" veya "Bir işletme birimi oluşturma" görevlerine bakın.</span><span class="sxs-lookup"><span data-stu-id="af9a8-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="af9a8-110">Ayrıca, departmanlar ve ekipler de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af9a8-110">You can also create departments and teams.</span></span> 



<span data-ttu-id="af9a8-111">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="af9a8-111">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-hierarchy"></a><span data-ttu-id="af9a8-112">Hiyerarşi oluştur</span><span class="sxs-lookup"><span data-stu-id="af9a8-112">Create a hierarchy</span></span>
1. <span data-ttu-id="af9a8-113">Organizasyon yönetimi > Kuruluşlar > Kuruluş hiyerarşileri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="af9a8-113">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="af9a8-114">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af9a8-114">Click New.</span></span>
3. <span data-ttu-id="af9a8-115">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="af9a8-115">In the Name field, type a value.</span></span>
4. <span data-ttu-id="af9a8-116">Amaç ata'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af9a8-116">Click Assign purpose.</span></span>
5. <span data-ttu-id="af9a8-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="af9a8-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="af9a8-118">Organizasyon hiyerarşinize atanacak bir amaç seçin.</span><span class="sxs-lookup"><span data-stu-id="af9a8-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="af9a8-119">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="af9a8-119">Click Add.</span></span>
7. <span data-ttu-id="af9a8-120">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="af9a8-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="af9a8-121">Yeni oluşturduğunuz hiyerarşiyi bulun.</span><span class="sxs-lookup"><span data-stu-id="af9a8-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="af9a8-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af9a8-122">Click OK.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="af9a8-123">Kuruluşları hiyerarşiye ekleme</span><span class="sxs-lookup"><span data-stu-id="af9a8-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="af9a8-124">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="af9a8-124">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="af9a8-125">Hiyerarşinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="af9a8-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="af9a8-126">Hiyerarşiyi görüntüle düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af9a8-126">Click View hierarchy.</span></span>
    * <span data-ttu-id="af9a8-127">Gerekirse kuruluşlar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="af9a8-127">Add organizations, as necessary.</span></span>  
    * <span data-ttu-id="af9a8-128">Bir kuruluş eklemek için Düzenle düğmesini ve ardından kuruluşu eklemek için Ekle düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af9a8-128">To add an organization, click Edit and then Insert to add the organization.</span></span>     <span data-ttu-id="af9a8-129">Değişiklikleri tamamladıktan sonra bir taslak kaydedebilir ve/veya değişiklikleri yayınlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af9a8-129">When you are done making changes you can save a draft and/or publish the changes.</span></span>  


