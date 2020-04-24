---
title: RFQ'lar için talep türleri ve puanlama ölçütleri oluşturma
description: Bu kılavuzda bir talep türünün nasıl oluşturulacağı ve bunun puanlama yöntemi ile nasıl ilişkilendirileceği gösterilir.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b3876238a191cbbacc4e8c435bb798232e6fd6f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204689"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="083d8-103">RFQ'lar için talep türleri ve puanlama ölçütleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="083d8-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="083d8-104">Bu kılavuzda bir talep türünün nasıl oluşturulacağı ve bunun puanlama yöntemi ile nasıl ilişkilendirileceği gösterilir.</span><span class="sxs-lookup"><span data-stu-id="083d8-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="083d8-105">Ayrıca, sonrasında varsayılan puanlama yöntemini ayarlamak üzere talep türünün resmi teklif talebinde (RFQ) nasıl kullanılacağı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="083d8-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="083d8-106">Bu görevler genellikle satınalma yöneticisi tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="083d8-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="083d8-107">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="083d8-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="083d8-108">Başlamadan önce kullanılabilir bir puanlama yöntemi gerekir.</span><span class="sxs-lookup"><span data-stu-id="083d8-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="083d8-109">Bir talep türü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="083d8-109">Create a solicitation type</span></span>
1. <span data-ttu-id="083d8-110">Tedarik ve kaynak atama > Ayarlar > Teklif talebi > Talep türü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="083d8-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="083d8-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="083d8-111">Click New.</span></span>
3. <span data-ttu-id="083d8-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="083d8-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="083d8-113">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="083d8-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="083d8-114">Puanlama yöntemi alanında, talep türü için kullanmak istediğiniz puanlama yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="083d8-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="083d8-115">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="083d8-115">Click Save.</span></span>
7. <span data-ttu-id="083d8-116">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="083d8-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="083d8-117">Talep türünü kullanın</span><span class="sxs-lookup"><span data-stu-id="083d8-117">Use the solicitation type</span></span>
1. <span data-ttu-id="083d8-118">Tedarik ve kaynak atama > Teklif talepleri > Tüm teklif talepleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="083d8-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="083d8-119">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="083d8-119">Click New.</span></span>
3. <span data-ttu-id="083d8-120">Talep türü alanında yeni oluşturduğunuz talep türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="083d8-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="083d8-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="083d8-121">Click OK.</span></span>
5. <span data-ttu-id="083d8-122">Puanlama ölçütü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="083d8-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="083d8-123">Gösterilen puanlama ölçütü, talep türüyle ilişkili puanlama yönteminden olanlardır.</span><span class="sxs-lookup"><span data-stu-id="083d8-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="083d8-124">Bu sayfadan ölçüt ekleyebilir veya silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="083d8-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="083d8-125">Diğer puanlama yöntemlerinden kopyalayarak yeni ölçüt eklemek de mümkündür.</span><span class="sxs-lookup"><span data-stu-id="083d8-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="083d8-126">Ölçütü kopyala'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="083d8-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="083d8-127">Puanlama yöntemi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="083d8-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="083d8-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="083d8-128">Click OK.</span></span>
9. <span data-ttu-id="083d8-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="083d8-129">Close the page.</span></span>

