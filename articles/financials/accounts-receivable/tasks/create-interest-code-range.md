---
title: Aralığa sahip faiz kodu oluşturma
description: Faiz kodları değer aralığına göre farklı faiz tutarlarını hesaplayacak şekilde ayarlanabilir.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d76ae320ee43a473b64afe311876cc94b953b20
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "367651"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="9f292-103">Aralığa sahip faiz kodu oluşturma</span><span class="sxs-lookup"><span data-stu-id="9f292-103">Create an interest code with a range</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f292-104">Faiz kodları değer aralığına göre farklı faiz tutarlarını hesaplayacak şekilde ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="9f292-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="9f292-105">Bu yordam, bir faiz kodunun nasıl ekleneceğini ve ona nasıl bir aralık ekleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9f292-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="9f292-106">Alacak ve Tahsilatlar > Faiz > Faiz kodlarını ayarla'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="9f292-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="9f292-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9f292-107">Click New.</span></span>
3. <span data-ttu-id="9f292-108">Faiz kodu alanında, faiz kodunun adını girin.</span><span class="sxs-lookup"><span data-stu-id="9f292-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="9f292-109">Açıklama alanında faiz kodu için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="9f292-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="9f292-110">Ay'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9f292-110">Select Month.</span></span>
6. <span data-ttu-id="9f292-111">Kazançlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="9f292-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="9f292-112">Para birimine göre kazançlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="9f292-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="9f292-113">Genel muhasebe hesabı alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="9f292-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="9f292-114">Aralığa göre faiz alanında, 'Ay' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9f292-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="9f292-115">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9f292-115">Click Add.</span></span>
11. <span data-ttu-id="9f292-116">Açıklama alanında, bu para birimi ve aralık için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="9f292-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="9f292-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9f292-117">Click Save.</span></span>
13. <span data-ttu-id="9f292-118">Aralıklar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9f292-118">Click Ranges.</span></span>
14. <span data-ttu-id="9f292-119">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9f292-119">Click New.</span></span>
15. <span data-ttu-id="9f292-120">Başlangıç değeri olarak 0 girin ve ardından faizi hesaplamak için kullanılacak aylık faiz yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="9f292-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="9f292-121">Bizim örneğimizde değer 1,5'tir.</span><span class="sxs-lookup"><span data-stu-id="9f292-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="9f292-122">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9f292-122">Click New.</span></span>
17. <span data-ttu-id="9f292-123">Sonraki başlangıç değeri olarak, yeni faiz tutarının hesaplanacağı ilk ay için 4 değerini girin.</span><span class="sxs-lookup"><span data-stu-id="9f292-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="9f292-124">Faizin 4. ay içinde hesaplanmaya başlayacağı aylık faiz yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="9f292-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="9f292-125">Bu örnekte, değer 2,0'dır.</span><span class="sxs-lookup"><span data-stu-id="9f292-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="9f292-126">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9f292-126">Click New.</span></span>
20. <span data-ttu-id="9f292-127">Sonraki başlangıç değeri olarak, yeni faiz tutarının hesaplanacağı sonraki ay için 7 değerini girin.</span><span class="sxs-lookup"><span data-stu-id="9f292-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="9f292-128">Faizin 7. ay içinde hesaplanmaya başlayacağı aylık faiz yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="9f292-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="9f292-129">Bu örnekte, değer 2,5'dır.</span><span class="sxs-lookup"><span data-stu-id="9f292-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="9f292-130">Ayarları tamamlamak için Kapat'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9f292-130">Click Close to complete the setup.</span></span>

