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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 800b7009f023bd2a0d8437b81d82c0e9de770841
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174386"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="20c17-103">Kamu sektörü için bir ön bütçe oluştur</span><span class="sxs-lookup"><span data-stu-id="20c17-103">Create a preliminary budget for Public sector</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="20c17-104">Belirli bir bütçe modeli ve boyut değerleri için bütçe ön kayıt girişlerini oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="20c17-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="20c17-105">Gerçek bütçe onaylandıktan sonra orijinal bütçe kayıt girişlerini oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="20c17-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="20c17-106">Bu yöntem kamu sektörü bölümündeki PSUS demo şirketinin verileri kullanılarak yaratılmıştır.</span><span class="sxs-lookup"><span data-stu-id="20c17-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="20c17-107">Bütçeleme > Bütçe kayıt girişleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="20c17-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="20c17-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="20c17-108">Click New.</span></span>
3. <span data-ttu-id="20c17-109">Bütçe modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="20c17-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="20c17-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="20c17-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="20c17-111">Bütçe kodu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="20c17-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="20c17-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="20c17-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="20c17-113">Sebep kodu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="20c17-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="20c17-114">Listede, istenen kayda tıklayın</span><span class="sxs-lookup"><span data-stu-id="20c17-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="20c17-115">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="20c17-115">Click Save.</span></span>
10. <span data-ttu-id="20c17-116">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="20c17-116">Click Add line.</span></span>
    * <span data-ttu-id="20c17-117">İsteğe bağlı: Başlıktaki tarihi değiştirmek istiyorsanız, yeni bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="20c17-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="20c17-118">Bu tarih, bütçenin kaydedileceği mali dönemi belirler.</span><span class="sxs-lookup"><span data-stu-id="20c17-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="20c17-119">Görev Kılavuzu görüntülerken diğer alanları doldurmak için sayfanın üstündeki Kilidi Aç'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="20c17-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="20c17-120">Hesap yapısı alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="20c17-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="20c17-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="20c17-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="20c17-122">Boyut değerleri alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="20c17-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="20c17-123">Tutar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="20c17-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="20c17-124">Aynı zamanda tutar türünü de girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="20c17-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="20c17-125">Para birimi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="20c17-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="20c17-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="20c17-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="20c17-127">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="20c17-127">Click Save.</span></span>
18. <span data-ttu-id="20c17-128">Bütçe bakiyelerini güncelleştir seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="20c17-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="20c17-129">Güncelleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="20c17-129">Click Update.</span></span>
    * <span data-ttu-id="20c17-130">Güncellemenin sonuçlarını görmek için, mavi çubuktaki mesaj detaylarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="20c17-130">To see the results of the update, click Message details on the blue bar.</span></span>  

