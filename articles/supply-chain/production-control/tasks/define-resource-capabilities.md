---
title: Kaynak yeteneklerini tanımlama
description: Kaynak yetenekleri, kaynağın hangi işlemleri yapabileceğini açıklar.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bd3f2b1efc1e6a883ad2a25d127e74a8925de8f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146802"
---
# <a name="define-resource-capabilities"></a><span data-ttu-id="ca5e5-103">Kaynak yeteneklerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="ca5e5-103">Define resource capabilities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca5e5-104">Kaynak yetenekleri, kaynağın hangi işlemleri yapabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="ca5e5-105">Planlama sırasında, her iş ve operasyonun gereklilikleri kullanılabilir kaynakların yetenekleriyle eşleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="ca5e5-106">Bu görev kılavuzu, bir kaynak yeteneği oluşturup bunu bir kaynağa atamanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="ca5e5-107">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="ca5e5-108">Kaynak yeteneği oluşturma</span><span class="sxs-lookup"><span data-stu-id="ca5e5-108">Create a resource capability</span></span>
1. <span data-ttu-id="ca5e5-109">Kaynak yetenekleri'ne gidin</span><span class="sxs-lookup"><span data-stu-id="ca5e5-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="ca5e5-110">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-110">Click New.</span></span>
3. <span data-ttu-id="ca5e5-111">Yetenek alanına, kaynak yeteneği kodunu yazın.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="ca5e5-112">Belirli bir işlem için, kaynakların operasyonu gerçekleştirmek üzere sahip olması gereken yeteneği belirtmek için yetenek kodunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="ca5e5-113">Açıklama alanına yetenek açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="ca5e5-114">Bir kaynağa yetenek atama</span><span class="sxs-lookup"><span data-stu-id="ca5e5-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="ca5e5-115">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-115">Click Add.</span></span>
2. <span data-ttu-id="ca5e5-116">Kaynak alanına, kaynak kodunu yazın.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="ca5e5-117">Kaynak yeteneği bir veya daha fazla kaynağa atanabilir.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="ca5e5-118">Bitiş alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="ca5e5-119">Bu alanı, bir kaynağın yeteneğe sınırlı süre sahip olduğunu belirtmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="ca5e5-120">Öncelik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="ca5e5-121">İşleri ve operasyonları planlarken, kaynakların öncelik sırasına göre seçilip seçilmeyeceğini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="ca5e5-122">Bunu yapmayı seçtiğinizde, istenen tarih için işi veya operasyonu gerçekleştirebilecek birden fazla kaynak varsa, istenen yetenekle ilgili en düşük önceliğe sahip kaynak seçilir.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="ca5e5-123">Düzey alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="ca5e5-124">Bir iş veya operasyonun belirli bir yetenek gerektirdiğini belirttiğinizde, gerekli olan en düşük düzeyi de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="ca5e5-125">Aynı işi farklı hızda, güçte ve boyutta yapabilecek kaynakları birbirinden ayırmak için yetenek düzeyini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ca5e5-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  

