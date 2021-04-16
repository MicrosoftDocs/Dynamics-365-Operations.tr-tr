---
title: Aralığa sahip faiz kodu oluşturma
description: Faiz kodları değer aralığına göre farklı faiz tutarlarını hesaplayacak şekilde ayarlanabilir.
author: ShivamPandey-msft
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c18269d277f64433da35e7dc1675cd3afda8e070
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835040"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="f0aef-103">Aralığa sahip faiz kodu oluşturma</span><span class="sxs-lookup"><span data-stu-id="f0aef-103">Create an interest code with a range</span></span>

[!include [banner](../../includes/banner.md)]
<span data-ttu-id="f0aef-104">Faiz kodları değer aralığına göre farklı faiz tutarlarını hesaplayacak şekilde ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="f0aef-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="f0aef-105">Bu yordam, bir faiz kodunun nasıl ekleneceğini ve ona nasıl bir aralık ekleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f0aef-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="f0aef-106">Alacak ve Tahsilatlar > Faiz > Faiz kodlarını ayarla'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="f0aef-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="f0aef-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f0aef-107">Click New.</span></span>
3. <span data-ttu-id="f0aef-108">Faiz kodu alanında, faiz kodunun adını girin.</span><span class="sxs-lookup"><span data-stu-id="f0aef-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="f0aef-109">Açıklama alanında faiz kodu için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="f0aef-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="f0aef-110">Ay'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f0aef-110">Select Month.</span></span>
6. <span data-ttu-id="f0aef-111">Kazançlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="f0aef-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="f0aef-112">Para birimine göre kazançlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="f0aef-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="f0aef-113">Genel muhasebe hesabı alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="f0aef-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="f0aef-114">Aralığa göre faiz alanında, 'Ay' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f0aef-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="f0aef-115">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f0aef-115">Click Add.</span></span>
11. <span data-ttu-id="f0aef-116">Açıklama alanında, bu para birimi ve aralık için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="f0aef-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="f0aef-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f0aef-117">Click Save.</span></span>
13. <span data-ttu-id="f0aef-118">Aralıklar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f0aef-118">Click Ranges.</span></span>
14. <span data-ttu-id="f0aef-119">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f0aef-119">Click New.</span></span>
15. <span data-ttu-id="f0aef-120">Başlangıç değeri olarak 0 girin ve ardından faizi hesaplamak için kullanılacak aylık faiz yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="f0aef-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="f0aef-121">Bizim örneğimizde değer 1,5'tir.</span><span class="sxs-lookup"><span data-stu-id="f0aef-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="f0aef-122">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f0aef-122">Click New.</span></span>
17. <span data-ttu-id="f0aef-123">Sonraki başlangıç değeri olarak, yeni faiz tutarının hesaplanacağı ilk ay için 4 değerini girin.</span><span class="sxs-lookup"><span data-stu-id="f0aef-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="f0aef-124">Faizin 4. ay içinde hesaplanmaya başlayacağı aylık faiz yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="f0aef-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="f0aef-125">Bu örnekte, değer 2,0'dır.</span><span class="sxs-lookup"><span data-stu-id="f0aef-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="f0aef-126">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f0aef-126">Click New.</span></span>
20. <span data-ttu-id="f0aef-127">Sonraki başlangıç değeri olarak, yeni faiz tutarının hesaplanacağı sonraki ay için 7 değerini girin.</span><span class="sxs-lookup"><span data-stu-id="f0aef-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="f0aef-128">Faizin 7. ay içinde hesaplanmaya başlayacağı aylık faiz yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="f0aef-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="f0aef-129">Bu örnekte, değer 2,5'dır.</span><span class="sxs-lookup"><span data-stu-id="f0aef-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="f0aef-130">Ayarları tamamlamak için Kapat'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f0aef-130">Click Close to complete the setup.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]