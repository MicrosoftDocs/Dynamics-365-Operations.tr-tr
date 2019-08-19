---
title: RFQ'lar için talep türleri ve puanlama ölçütleri oluşturma
description: Bu kılavuzda bir talep türünün nasıl oluşturulacağı ve bunun puanlama yöntemi ile nasıl ilişkilendirileceği gösterilir.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1a3e0d00d674af913953d7fd01183b0289c20d3d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844132"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="7d16a-103">RFQ'lar için talep türleri ve puanlama ölçütleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="7d16a-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d16a-104">Bu kılavuzda bir talep türünün nasıl oluşturulacağı ve bunun puanlama yöntemi ile nasıl ilişkilendirileceği gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7d16a-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="7d16a-105">Ayrıca, sonrasında varsayılan puanlama yöntemini ayarlamak üzere talep türünün resmi teklif talebinde (RFQ) nasıl kullanılacağı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7d16a-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="7d16a-106">Bu görevler genellikle satınalma yöneticisi tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="7d16a-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="7d16a-107">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d16a-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="7d16a-108">Başlamadan önce kullanılabilir bir puanlama yöntemi gerekir.</span><span class="sxs-lookup"><span data-stu-id="7d16a-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="7d16a-109">Bir talep türü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7d16a-109">Create a solicitation type</span></span>
1. <span data-ttu-id="7d16a-110">Tedarik ve kaynak atama > Ayarlar > Teklif talebi > Talep türü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7d16a-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="7d16a-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d16a-111">Click New.</span></span>
3. <span data-ttu-id="7d16a-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="7d16a-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="7d16a-113">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7d16a-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7d16a-114">Puanlama yöntemi alanında, talep türü için kullanmak istediğiniz puanlama yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="7d16a-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="7d16a-115">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d16a-115">Click Save.</span></span>
7. <span data-ttu-id="7d16a-116">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7d16a-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="7d16a-117">Talep türünü kullanın</span><span class="sxs-lookup"><span data-stu-id="7d16a-117">Use the solicitation type</span></span>
1. <span data-ttu-id="7d16a-118">Tedarik ve kaynak atama > Teklif talepleri > Tüm teklif talepleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="7d16a-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="7d16a-119">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d16a-119">Click New.</span></span>
3. <span data-ttu-id="7d16a-120">Talep türü alanında yeni oluşturduğunuz talep türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="7d16a-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="7d16a-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d16a-121">Click OK.</span></span>
5. <span data-ttu-id="7d16a-122">Puanlama ölçütü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d16a-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="7d16a-123">Gösterilen puanlama ölçütü, talep türüyle ilişkili puanlama yönteminden olanlardır.</span><span class="sxs-lookup"><span data-stu-id="7d16a-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="7d16a-124">Bu sayfadan ölçüt ekleyebilir veya silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d16a-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="7d16a-125">Diğer puanlama yöntemlerinden kopyalayarak yeni ölçüt eklemek de mümkündür.</span><span class="sxs-lookup"><span data-stu-id="7d16a-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="7d16a-126">Ölçütü kopyala'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d16a-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="7d16a-127">Puanlama yöntemi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7d16a-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="7d16a-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d16a-128">Click OK.</span></span>
9. <span data-ttu-id="7d16a-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7d16a-129">Close the page.</span></span>

