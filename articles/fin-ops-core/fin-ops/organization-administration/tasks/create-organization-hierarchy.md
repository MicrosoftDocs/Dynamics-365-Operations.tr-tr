---
title: Bir kuruluş hiyerarşisi oluşturma
description: Bir organizasyon hiyerarşisi oluşturmak için aşağıdaki prosedürü kullanın.
author: sericks007
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dde06f758be57fb646696c861218565476abcadc
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140571"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="c15ea-103">Bir kuruluş hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c15ea-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c15ea-104">Bir organizasyon hiyerarşisi oluşturmak için aşağıdaki prosedürü kullanın.</span><span class="sxs-lookup"><span data-stu-id="c15ea-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="c15ea-105">İşlerinize farklı perspektiflerden bakmak ve raporlamak için organizasyonel hiyerarşileri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c15ea-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="c15ea-106">Örneğin, vergi, hukuki veya yasal raporlamaya yönelik bir hiyerarşi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c15ea-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="c15ea-107">Ardından, yasal olarak gerekmeyen ama dahili raporlama için kullanılan mali bilgileri raporlamak için başka bir hiyerarşi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c15ea-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="c15ea-108">Bir kuruluş hiyerarşisi oluşturmadan önce kuruluşları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c15ea-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="c15ea-109">Daha fazla bilgi için "Bir tüzel kişilik oluşturma" veya "Bir işletme birimi oluşturma" görevlerine bakın.</span><span class="sxs-lookup"><span data-stu-id="c15ea-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="c15ea-110">Ayrıca, departmanlar ve ekipler de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c15ea-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="c15ea-111">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="c15ea-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="c15ea-112">Hiyerarşi oluştur</span><span class="sxs-lookup"><span data-stu-id="c15ea-112">Create a hierarchy</span></span>
1. <span data-ttu-id="c15ea-113">**Gezinti bölmesi > Modüller > Kuruluş Yönetimi > Kuruluşlar > Kuruluş hiyerarşileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c15ea-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="c15ea-114">**Eylem bölmesinde** **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c15ea-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="c15ea-115">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="c15ea-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="c15ea-116">**Amaç** bölümünde, **Amaç ata**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c15ea-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="c15ea-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c15ea-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="c15ea-118">Organizasyon hiyerarşinize atanacak bir amaç seçin.</span><span class="sxs-lookup"><span data-stu-id="c15ea-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="c15ea-119">**Atanan hiyerarşiler** bölümünde **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c15ea-119">In the **Assigned hierarchies** sectiom, click **Add**.</span></span>
7. <span data-ttu-id="c15ea-120">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c15ea-120">In the list, mark the selected row.</span></span> <span data-ttu-id="c15ea-121">Yeni oluşturduğunuz hiyerarşiyi bulun.</span><span class="sxs-lookup"><span data-stu-id="c15ea-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="c15ea-122">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c15ea-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="c15ea-123">Kuruluşları hiyerarşiye ekleme</span><span class="sxs-lookup"><span data-stu-id="c15ea-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="c15ea-124">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c15ea-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="c15ea-125">Hiyerarşinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="c15ea-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="c15ea-126">**Atanan hiyerarşiler** bölümünde **Hiyerarşiyi görüntüle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c15ea-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="c15ea-127">Gerekirse kuruluşlar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c15ea-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="c15ea-128">Bir kuruluş eklemek için **Düzenle** düğmesine ve ardından kuruluşu eklemek için **Ekle** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c15ea-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="c15ea-129">Değişiklikleri tamamladıktan sonra bir taslak **Kaydedebilir** ve/veya değişiklikleri **Yayınlayabilirsiniz**.</span><span class="sxs-lookup"><span data-stu-id="c15ea-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  

