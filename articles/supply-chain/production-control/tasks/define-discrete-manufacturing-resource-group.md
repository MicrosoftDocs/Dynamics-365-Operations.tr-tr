--- 
title: "Kesikli üretim kaynak grubunu tanımlama"
description: "Kaynak grubu, genellikle üretim atölyesinde sarı satırlarla tanımlanan fiziki iş hücreleri düzenine karşılık gelen operasyon kaynakları grubudur."
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 50733e34bbf14ae2cade6822105da4d8c2120d7d
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="ab681-103">Kesikli üretim kaynak grubunu tanımlama</span><span class="sxs-lookup"><span data-stu-id="ab681-103">Define discrete manufacturing resource group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ab681-104">Kaynak grubu, genellikle üretim atölyesinde sarı satırlarla tanımlanan fiziki iş hücreleri düzenine karşılık gelen operasyon kaynakları grubudur.</span><span class="sxs-lookup"><span data-stu-id="ab681-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="ab681-105">Bu yordam, kesikli üretimde kullanmak üzere bir kaynak grubu tanımlama hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="ab681-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="ab681-106">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab681-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="ab681-107">Kaynak grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ab681-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="ab681-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab681-108">Click New.</span></span>
3. <span data-ttu-id="ab681-109">Kaynak grubu alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ab681-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="ab681-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ab681-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ab681-111">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab681-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="ab681-112">Üretim birimi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab681-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="ab681-113">Varsayılan operasyon parametrelerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="ab681-113">Define default operational parameters</span></span>
1. <span data-ttu-id="ab681-114">Operasyon bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="ab681-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="ab681-115">Hurda yüzdesi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ab681-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="ab681-116">Kurulum kategorisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="ab681-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="ab681-117">Çalışma süresi kategorisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab681-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="ab681-118">Operasyon planlama yüzdesi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ab681-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="ab681-119">Çalışma saatlerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="ab681-119">Define operating hours</span></span>
1. <span data-ttu-id="ab681-120">Takvimler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="ab681-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="ab681-121">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ab681-121">Click Add.</span></span>
3. <span data-ttu-id="ab681-122">Takvim alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab681-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="ab681-123">Operasyon kaynakları ekleme</span><span class="sxs-lookup"><span data-stu-id="ab681-123">Add operations resources</span></span>
1. <span data-ttu-id="ab681-124">Kaynaklar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="ab681-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="ab681-125">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ab681-125">Click Add.</span></span>
3. <span data-ttu-id="ab681-126">Kaynaklar alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab681-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="ab681-127">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ab681-127">Click Add.</span></span>
5. <span data-ttu-id="ab681-128">Kaynaklar alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab681-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="ab681-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ab681-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ab681-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab681-130">In the list, click the link in the selected row.</span></span>


