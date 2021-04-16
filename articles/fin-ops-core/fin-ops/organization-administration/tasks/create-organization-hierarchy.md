---
title: Bir kuruluş hiyerarşisi oluşturma
description: Bir organizasyon hiyerarşisi oluşturmak için aşağıdaki prosedürü kullanın.
author: sericks007
ms.date: 12/15/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d27bec86302f3e6cef8318a0d846f31d2d9c6a5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747405"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="3e0c7-103">Bir kuruluş hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="3e0c7-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e0c7-104">Bir organizasyon hiyerarşisi oluşturmak için aşağıdaki prosedürü kullanın.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="3e0c7-105">İşlerinize farklı perspektiflerden bakmak ve raporlamak için organizasyonel hiyerarşileri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="3e0c7-106">Örneğin, vergi, hukuki veya yasal raporlamaya yönelik bir hiyerarşi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="3e0c7-107">Ardından, yasal olarak gerekmeyen ama dahili raporlama için kullanılan mali bilgileri raporlamak için başka bir hiyerarşi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="3e0c7-108">Bir kuruluş hiyerarşisi oluşturmadan önce kuruluşları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="3e0c7-109">Daha fazla bilgi için "Bir tüzel kişilik oluşturma" veya "Bir işletme birimi oluşturma" görevlerine bakın.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="3e0c7-110">Ayrıca, departmanlar ve ekipler de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="3e0c7-111">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="3e0c7-112">Hiyerarşi oluştur</span><span class="sxs-lookup"><span data-stu-id="3e0c7-112">Create a hierarchy</span></span>
1. <span data-ttu-id="3e0c7-113">**Gezinti bölmesi > Modüller > Kuruluş Yönetimi > Kuruluşlar > Kuruluş hiyerarşileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="3e0c7-114">**Eylem bölmesinde** **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="3e0c7-115">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="3e0c7-116">**Amaç** bölümünde, **Amaç ata**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="3e0c7-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="3e0c7-118">Organizasyon hiyerarşinize atanacak bir amaç seçin.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="3e0c7-119">**Atanan hiyerarşiler** bölümünde **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-119">In the **Assigned hierarchies** section, click **Add**.</span></span>
7. <span data-ttu-id="3e0c7-120">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-120">In the list, mark the selected row.</span></span> <span data-ttu-id="3e0c7-121">Yeni oluşturduğunuz hiyerarşiyi bulun.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="3e0c7-122">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="3e0c7-123">Kuruluşları hiyerarşiye ekleme</span><span class="sxs-lookup"><span data-stu-id="3e0c7-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="3e0c7-124">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="3e0c7-125">Hiyerarşinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="3e0c7-126">**Atanan hiyerarşiler** bölümünde **Hiyerarşiyi görüntüle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="3e0c7-127">Gerekirse kuruluşlar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="3e0c7-128">Bir kuruluş eklemek için **Düzenle** düğmesine ve ardından kuruluşu eklemek için **Ekle** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="3e0c7-129">Değişiklikleri tamamladıktan sonra bir taslak **Kaydedebilir** ve/veya değişiklikleri **Yayınlayabilirsiniz**.</span><span class="sxs-lookup"><span data-stu-id="3e0c7-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]