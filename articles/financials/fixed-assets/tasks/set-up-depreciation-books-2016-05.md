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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3e2c3bfdde6fd06bfe9e22f215f691e0c92fa8ee
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-depreciation-books"></a><span data-ttu-id="10437-103">Amortisman defterleri ayarlama </span><span class="sxs-lookup"><span data-stu-id="10437-103">Set up depreciation books</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="10437-104">Bu görev kılavuzunda yeni bir amortisman defteri oluşturulup bir sabit kıymet grubuyla ilişkilendirilecek.</span><span class="sxs-lookup"><span data-stu-id="10437-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="10437-105">Kılavuzda Muhasebeci rolü ve USMF adlı tüzel kişilik için demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="10437-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="10437-106">Amortisman defteri oluşturun</span><span class="sxs-lookup"><span data-stu-id="10437-106">Create a depreciation book</span></span>
1. <span data-ttu-id="10437-107">Sabit kıymetler > Kurulum > Amortisman defterleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="10437-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="10437-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10437-108">Click New.</span></span>
3. <span data-ttu-id="10437-109">Amortisman defteri alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="10437-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="10437-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="10437-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="10437-111">Amortismanı hesapla onay kutusunu işaretleyin veya kutunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="10437-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="10437-112">Amortisman profili alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="10437-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="10437-113">Listede, istediğiniz amortisman profilini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="10437-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="10437-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10437-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="10437-115">Alternatif amortisman profili alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="10437-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="10437-116">Listede, istediğiniz amortisman profilini seçin.</span><span class="sxs-lookup"><span data-stu-id="10437-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="10437-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10437-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="10437-118">Olağandışı durumlarda bir kıymetin ek amortismanı için Olağandışı amortisman profili kullanılır.</span><span class="sxs-lookup"><span data-stu-id="10437-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="10437-119">Örneğin bunu doğal felaketlerden kaynaklanan amortismanı kaydetmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10437-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="10437-120">Temel düzeltmeler bulunan amortisman düzeltmeleri oluştur onay kutusunu işaretleyin veya kutunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="10437-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="10437-121">Takvim alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="10437-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="10437-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10437-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="10437-123">Amortisman defterini bir sabit kıymet grubuyla ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="10437-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="10437-124">Sabit kıymet grupları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10437-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="10437-125">Sabit kıymet grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="10437-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="10437-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="10437-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="10437-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10437-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="10437-128">Amortisman yöntemi alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="10437-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="10437-129">Servis ömrü alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="10437-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="10437-130">Amortisman dönemleri alanı değerinin Servis ömrü ayarlandıktan sonra hesaplandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="10437-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  


