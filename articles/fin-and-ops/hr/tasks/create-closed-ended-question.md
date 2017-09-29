--- 
title: "Kapalı uçlu soru oluşturma"
description: "Kapalı uçlu sorular, yanıtlayan kişinin arasından seçim yapabileceği seçenekler sunmanızı sağlar."
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 59f1af68e4b1198894a7cdab291021de9f3cf8a9
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="22ec9-103">Kapalı uçlu soru oluşturma</span><span class="sxs-lookup"><span data-stu-id="22ec9-103">Create a closed ended question</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22ec9-104">Kapalı uçlu sorular, yanıtlayan kişinin arasından seçim yapabileceği seçenekler sunmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="22ec9-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="22ec9-105">İlk olarak, yanıt grubunu, yanıtları ile birlikte oluşturun, sonra da yanıt grubunu kullanacak soruyu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="22ec9-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="22ec9-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="22ec9-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="22ec9-107">Yanıt grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="22ec9-107">Create an answer group</span></span>
1. <span data-ttu-id="22ec9-108">Sırasıyla Anket > Tasarım > Yanıt grupları seçimlerini yapın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="22ec9-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-109">Click New.</span></span>
3. <span data-ttu-id="22ec9-110">Yanıt grubu alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="22ec9-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="22ec9-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="22ec9-112">Yanıt grubunun bir soru için her kullanılışında, yanıtların farklı bir düzende yerleştirilmesi için rastgele seç özelliğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="22ec9-113">Yanıtla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-113">Click Answer.</span></span>
6. <span data-ttu-id="22ec9-114">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-114">Click New.</span></span>
    * <span data-ttu-id="22ec9-115">Sıra numarası rastgele seç, yanıt grubu için seçili olmadıkça yanıtların görüntülenme sırasını denetler.</span><span class="sxs-lookup"><span data-stu-id="22ec9-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="22ec9-116">Soru formunu puanlamak için yanıtların puan vermesi sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="22ec9-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="22ec9-117">Puanlar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="22ec9-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="22ec9-118">Seçilen yanıtın doğru olduğunu belirtmek üzere işaretlenebilir.</span><span class="sxs-lookup"><span data-stu-id="22ec9-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="22ec9-119">Bu, soru formunu puanlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="22ec9-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="22ec9-120">Yanıt alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="22ec9-121">Yanıt grubu için yanıt seçim seçenekleri oluşturmaya devam edin.</span><span class="sxs-lookup"><span data-stu-id="22ec9-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="22ec9-122">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-122">Click New.</span></span>
10. <span data-ttu-id="22ec9-123">Puanlar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="22ec9-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="22ec9-124">Yanıt alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="22ec9-125">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-125">Click New.</span></span>
13. <span data-ttu-id="22ec9-126">Puanlar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="22ec9-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="22ec9-127">Yanıt alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="22ec9-128">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-128">Click New.</span></span>
16. <span data-ttu-id="22ec9-129">Puanlar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="22ec9-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="22ec9-130">Yanıt alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="22ec9-131">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-131">Click New.</span></span>
19. <span data-ttu-id="22ec9-132">Puanlar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="22ec9-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="22ec9-133">Yanıt alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="22ec9-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-134">Close the page.</span></span>
22. <span data-ttu-id="22ec9-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="22ec9-136">Soruyu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="22ec9-136">Create the question</span></span>
1. <span data-ttu-id="22ec9-137">Soru formu > Tasarım > Sorular'a gidin.</span><span class="sxs-lookup"><span data-stu-id="22ec9-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="22ec9-138">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-138">Click New.</span></span>
3. <span data-ttu-id="22ec9-139">Tür alanını ilgili soruları birlikte gruplandırmak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="22ec9-140">Kapalı uçlu sorular için onay kutusu, alternatif düğmesi veya birleşik giriş kutusu giriş türlerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="22ec9-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="22ec9-141">Giriş türü alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="22ec9-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="22ec9-142">Yanıt grubu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="22ec9-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="22ec9-143">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="22ec9-143">In the Text field, type a value.</span></span>


