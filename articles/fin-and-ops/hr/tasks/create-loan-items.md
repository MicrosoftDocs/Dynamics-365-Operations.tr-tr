--- 
title: "Ödünç verme maddeleri oluştur"
description: "Ödünç verilen maddeler, telefonlar veya bilgisayarlar gibi şirketinizin çalışanlarına ödünç verdiği fiziksel öğeleri izlemek için yardımcı kayıtlardır."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cef1f9b2e3d202d7eea3a967fa8a6c371c6ac3a5
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-loan-items"></a><span data-ttu-id="b7fdb-103">Ödünç verme maddeleri oluştur</span><span class="sxs-lookup"><span data-stu-id="b7fdb-103">Create loan items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b7fdb-104">Ödünç verilen maddeler, telefonlar veya bilgisayarlar gibi şirketinizin çalışanlarına ödünç verdiği fiziksel öğeleri izlemek için yardımcı kayıtlardır.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="b7fdb-105">Her fiziksel öğeye karşılık gelen bir ödünç verilen madde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="b7fdb-106">Ödünç verilen her madde kaydı, neyin ödünç verildiği, ödünç verme işleminden kimin sorumlu olduğu ve maddenin ödünç verilebileceği gün sayısını açıklamalıdır.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="b7fdb-107">Aynı anda birden fazla ödünç verilen maddeler, anahtar, erişim kartı veya üniforma gibi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="b7fdb-108">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="b7fdb-109">Ödünç verme türleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="b7fdb-109">Create Loan types</span></span>
1. <span data-ttu-id="b7fdb-110">İnsan Kaynakları > Çalışanlar > Ödünç maddeler > Ödünç verme türleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="b7fdb-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-111">Click New.</span></span>
3. <span data-ttu-id="b7fdb-112">Ödünç verme türü alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="b7fdb-113">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b7fdb-114">Bu ödünç verme türüne atanan maddelerin süresinin geçebileceği gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="b7fdb-115">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-115">Click Save.</span></span>
7. <span data-ttu-id="b7fdb-116">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-116">Close the page.</span></span>
8. <span data-ttu-id="b7fdb-117">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="b7fdb-118">Ödünç verme maddeleri oluşturun</span><span class="sxs-lookup"><span data-stu-id="b7fdb-118">Create Loan items</span></span>
1. <span data-ttu-id="b7fdb-119">İnsan Kaynakları > Çalışanlar > Ödünç maddeler > Ödünç verilen maddeler seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="b7fdb-120">Ödünç verilen maddeler oluşturma'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-120">Click Create loan items.</span></span>
3. <span data-ttu-id="b7fdb-121">Miktar'da bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="b7fdb-122">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b7fdb-123">Ödünç verme türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b7fdb-124">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="b7fdb-125">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b7fdb-126">Maddenin ödünç verilebileceği gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="b7fdb-127">Ödünç verilen ekipman sayfasındaki Planlanan iade alanında bulunan varsayılan değer geçerli tarih ve bu sayı toplanarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="b7fdb-128">Sorumlu kişi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="b7fdb-129">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-129">Click Select.</span></span>
11. <span data-ttu-id="b7fdb-130">Başlangıç değeri alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="b7fdb-131">Aralık alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="b7fdb-132">Biçim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="b7fdb-133">Örneğin, ödünç verilen madde için başlangıç numarası 10 ise, Biçim alanında iki sayı sembolü girin.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="b7fdb-134">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-134">Click OK.</span></span>
15. <span data-ttu-id="b7fdb-135">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="b7fdb-135">Refresh the page.</span></span>


