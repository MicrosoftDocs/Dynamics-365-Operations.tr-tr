--- 
title: 'Amortisman defterleri ayarlama '
description: "Bu görev kılavuzunda yeni bir amortisman defteri oluşturulup bir sabit kıymet grubuyla ilişkilendirilecek."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d2001da7b3487a07a91abd406f74558916ac9f23
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="d6f92-103">Amortisman defterleri ayarlama </span><span class="sxs-lookup"><span data-stu-id="d6f92-103">Set up depreciation books</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d6f92-104">Bu görev kılavuzunda yeni bir amortisman defteri oluşturulup bir sabit kıymet grubuyla ilişkilendirilecek.</span><span class="sxs-lookup"><span data-stu-id="d6f92-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="d6f92-105">Kılavuzda Muhasebeci rolü ve USMF adlı tüzel kişilik için demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d6f92-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="d6f92-106">Amortisman defteri oluşturun</span><span class="sxs-lookup"><span data-stu-id="d6f92-106">Create a depreciation book</span></span>
1. <span data-ttu-id="d6f92-107">Sabit kıymetler > Kurulum > Amortisman defterleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d6f92-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="d6f92-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6f92-108">Click New.</span></span>
3. <span data-ttu-id="d6f92-109">Amortisman defteri alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d6f92-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="d6f92-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d6f92-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d6f92-111">Amortismanı hesapla onay kutusunu işaretleyin veya kutunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="d6f92-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="d6f92-112">Amortisman profili alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="d6f92-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d6f92-113">Listede, istediğiniz amortisman profilini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d6f92-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="d6f92-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6f92-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d6f92-115">Alternatif amortisman profili alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="d6f92-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="d6f92-116">Listede, istediğiniz amortisman profilini seçin.</span><span class="sxs-lookup"><span data-stu-id="d6f92-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="d6f92-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6f92-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d6f92-118">Olağandışı durumlarda bir kıymetin ek amortismanı için Olağandışı amortisman profili kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d6f92-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="d6f92-119">Örneğin bunu doğal felaketlerden kaynaklanan amortismanı kaydetmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6f92-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="d6f92-120">Temel düzeltmeler bulunan amortisman düzeltmeleri oluştur onay kutusunu işaretleyin veya kutunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="d6f92-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="d6f92-121">Takvim alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="d6f92-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="d6f92-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6f92-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="d6f92-123">Amortisman defterini bir sabit kıymet grubuyla ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="d6f92-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="d6f92-124">Sabit kıymet grupları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6f92-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="d6f92-125">Sabit kıymet grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="d6f92-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d6f92-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d6f92-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="d6f92-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6f92-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d6f92-128">Amortisman yöntemi alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="d6f92-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="d6f92-129">Servis ömrü alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d6f92-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="d6f92-130">Amortisman dönemleri alanı değerinin Servis ömrü ayarlandıktan sonra hesaplandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="d6f92-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  


