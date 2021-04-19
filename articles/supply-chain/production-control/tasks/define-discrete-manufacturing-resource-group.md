---
title: Kesikli üretim kaynak grubunu tanımlama
description: Kaynak grubu, genellikle üretim atölyesinde sarı satırlarla tanımlanan fiziki iş hücreleri düzenine karşılık gelen operasyon kaynakları grubudur.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95a8e1c6daa78250118a8a16010ef4cc1b1ae693
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811546"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="8e022-103">Kesikli üretim kaynak grubunu tanımlama</span><span class="sxs-lookup"><span data-stu-id="8e022-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e022-104">Kaynak grubu, genellikle üretim atölyesinde sarı satırlarla tanımlanan fiziki iş hücreleri düzenine karşılık gelen operasyon kaynakları grubudur.</span><span class="sxs-lookup"><span data-stu-id="8e022-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="8e022-105">Bu yordam, kesikli üretimde kullanmak üzere bir kaynak grubu tanımlama hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="8e022-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="8e022-106">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e022-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="8e022-107">Kaynak grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8e022-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="8e022-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e022-108">Click New.</span></span>
3. <span data-ttu-id="8e022-109">Kaynak grubu alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8e022-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="8e022-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8e022-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8e022-111">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8e022-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="8e022-112">Üretim birimi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8e022-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="8e022-113">Varsayılan operasyon parametrelerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="8e022-113">Define default operational parameters</span></span>
1. <span data-ttu-id="8e022-114">Operasyon bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="8e022-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="8e022-115">Hurda yüzdesi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="8e022-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="8e022-116">Kurulum kategorisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="8e022-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="8e022-117">Çalışma süresi kategorisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8e022-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="8e022-118">Operasyon planlama yüzdesi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="8e022-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="8e022-119">Çalışma saatlerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="8e022-119">Define operating hours</span></span>
1. <span data-ttu-id="8e022-120">Takvimler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="8e022-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="8e022-121">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8e022-121">Click Add.</span></span>
3. <span data-ttu-id="8e022-122">Takvim alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8e022-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="8e022-123">Operasyon kaynakları ekleme</span><span class="sxs-lookup"><span data-stu-id="8e022-123">Add operations resources</span></span>
1. <span data-ttu-id="8e022-124">Kaynaklar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="8e022-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="8e022-125">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8e022-125">Click Add.</span></span>
3. <span data-ttu-id="8e022-126">Kaynaklar alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8e022-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="8e022-127">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8e022-127">Click Add.</span></span>
5. <span data-ttu-id="8e022-128">Kaynaklar alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8e022-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="8e022-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8e022-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="8e022-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e022-130">In the list, click the link in the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]