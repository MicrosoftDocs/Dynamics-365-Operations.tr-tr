---
title: Kamu sektörü için bir ön bütçe oluştur
description: Belirli bir bütçe modeli ve boyut değerleri için bütçe ön kayıt girişlerini oluşturabilirsiniz.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22538d58cc3499bd030848699d6c5831dfd8888a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975172"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="1b792-103">Kamu sektörü için bir ön bütçe oluştur</span><span class="sxs-lookup"><span data-stu-id="1b792-103">Create a preliminary budget for Public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1b792-104">Belirli bir bütçe modeli ve boyut değerleri için bütçe ön kayıt girişlerini oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1b792-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="1b792-105">Gerçek bütçe onaylandıktan sonra orijinal bütçe kayıt girişlerini oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1b792-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="1b792-106">Bu yöntem kamu sektörü bölümündeki PSUS demo şirketinin verileri kullanılarak yaratılmıştır.</span><span class="sxs-lookup"><span data-stu-id="1b792-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="1b792-107">Bütçeleme > Bütçe kayıt girişleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="1b792-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="1b792-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1b792-108">Click New.</span></span>
3. <span data-ttu-id="1b792-109">Bütçe modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1b792-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1b792-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1b792-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="1b792-111">Bütçe kodu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1b792-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="1b792-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1b792-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="1b792-113">Sebep kodu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1b792-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="1b792-114">Listede, istenen kayda tıklayın</span><span class="sxs-lookup"><span data-stu-id="1b792-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="1b792-115">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1b792-115">Click Save.</span></span>
10. <span data-ttu-id="1b792-116">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1b792-116">Click Add line.</span></span>
    * <span data-ttu-id="1b792-117">İsteğe bağlı: Başlıktaki tarihi değiştirmek istiyorsanız, yeni bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="1b792-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="1b792-118">Bu tarih, bütçenin kaydedileceği mali dönemi belirler.</span><span class="sxs-lookup"><span data-stu-id="1b792-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="1b792-119">Görev Kılavuzu görüntülerken diğer alanları doldurmak için sayfanın üstündeki Kilidi Aç'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1b792-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="1b792-120">Hesap yapısı alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1b792-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="1b792-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1b792-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="1b792-122">Boyut değerleri alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="1b792-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="1b792-123">Tutar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1b792-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="1b792-124">Aynı zamanda tutar türünü de girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1b792-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="1b792-125">Para birimi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="1b792-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="1b792-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1b792-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="1b792-127">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1b792-127">Click Save.</span></span>
18. <span data-ttu-id="1b792-128">Bütçe bakiyelerini güncelleştir seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1b792-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="1b792-129">Güncelleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1b792-129">Click Update.</span></span>
    * <span data-ttu-id="1b792-130">Güncellemenin sonuçlarını görmek için, mavi çubuktaki mesaj detaylarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1b792-130">To see the results of the update, click Message details on the blue bar.</span></span>  

