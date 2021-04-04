---
title: Özgün bir bütçe oluştur ve sonra kamu sektörü için ön bütçe girişlerini geri al
description: Bu konu, bütçe modelini ve ön bütçe tutarları içeren boyut değerlerini kullanarak orijinal bütçe girişinin nasıl oluşturulacağı ve tersine çevrileceği hakkında bilgi sağlar.
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
ms.openlocfilehash: 0b11aeb377caf50808f661de25fcbbf90429d475
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235077"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="6afc7-103">Özgün bir bütçe oluştur ve sonra kamu sektörü için ön bütçe girişlerini geri al</span><span class="sxs-lookup"><span data-stu-id="6afc7-103">Create an original budget and then reverse preliminary budget entries in the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6afc7-104">Özgün bir bütçe girişi oluşturduğunuzda ve ön bütçe tutarlarını bütçe modeli ve boyut değerlerini kullandığınızda, ön bütçe tutarları geri alınabilir.</span><span class="sxs-lookup"><span data-stu-id="6afc7-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="6afc7-105">Bu yöntem kamu sektörü bölümündeki PSUS demo şirketinin verileri kullanılarak yaratılmıştır.</span><span class="sxs-lookup"><span data-stu-id="6afc7-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="6afc7-106">Bütçeleme > Bütçe kayıt girişleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="6afc7-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="6afc7-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6afc7-107">Click New.</span></span>
3. <span data-ttu-id="6afc7-108">Bütçe modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6afc7-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6afc7-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6afc7-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="6afc7-110">Bütçe kodu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6afc7-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6afc7-111">Listede Orijinal bütçe seçeneğine tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6afc7-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="6afc7-112">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6afc7-112">Click Save.</span></span>
8. <span data-ttu-id="6afc7-113">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6afc7-113">Click Add line.</span></span>
9. <span data-ttu-id="6afc7-114">İsteğe bağlı: Başlıktaki tarihi değiştirmek istiyorsanız, yeni bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="6afc7-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="6afc7-115">Bu tarih, bütçenin kaydedileceği mali dönemi belirler.</span><span class="sxs-lookup"><span data-stu-id="6afc7-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="6afc7-116">Hesap yapısı alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6afc7-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="6afc7-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6afc7-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="6afc7-118">Boyut değerleri alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="6afc7-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="6afc7-119">Tutar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6afc7-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="6afc7-120">Para birimi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="6afc7-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="6afc7-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6afc7-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="6afc7-122">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6afc7-122">Click Save.</span></span>
17. <span data-ttu-id="6afc7-123">Bütçe bakiyelerini güncelleştir seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6afc7-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="6afc7-124">İsteğe bağlı: Ters Ön bütçe seçeneğini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6afc7-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="6afc7-125">Not: Tüm Ön bütçe girişlerini veya sadece belirlediğiniz bütçe koduna sahip olan Ön bütçe girişlerini geri alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6afc7-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="6afc7-126">İsteğe bağlı seçimler yapmak için sayfanın üstündeki Kilidi Aç simgesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6afc7-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="6afc7-127">Güncelleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6afc7-127">Click Update.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]