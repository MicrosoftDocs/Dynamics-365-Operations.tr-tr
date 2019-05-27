---
title: Amortisman defterleri ayarlama (Mayıs 2016)
description: Bu görev kılavuzunda yeni bir amortisman defteri oluşturulup bir sabit kıymet grubuyla ilişkilendirilecek.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1fd53ea1dff9b116d19c525c5d6967ece0993b6f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566927"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="5b14c-103">Amortisman defterleri ayarlama (Mayıs 2016)</span><span class="sxs-lookup"><span data-stu-id="5b14c-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5b14c-104">Bu görev kılavuzunda yeni bir amortisman defteri oluşturulup bir sabit kıymet grubuyla ilişkilendirilecek.</span><span class="sxs-lookup"><span data-stu-id="5b14c-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="5b14c-105">Kılavuzda Muhasebeci rolü ve USMF adlı tüzel kişilik için demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5b14c-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="5b14c-106">Amortisman defteri oluşturun</span><span class="sxs-lookup"><span data-stu-id="5b14c-106">Create a depreciation book</span></span>
1. <span data-ttu-id="5b14c-107">Sabit kıymetler > Kurulum > Amortisman defterleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="5b14c-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="5b14c-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b14c-108">Click New.</span></span>
3. <span data-ttu-id="5b14c-109">Amortisman defteri alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="5b14c-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="5b14c-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="5b14c-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5b14c-111">Amortismanı hesapla onay kutusunu işaretleyin veya kutunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5b14c-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="5b14c-112">Amortisman profili alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="5b14c-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5b14c-113">Listede, istediğiniz amortisman profilini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5b14c-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="5b14c-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b14c-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5b14c-115">Alternatif amortisman profili alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="5b14c-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="5b14c-116">Listede, istediğiniz amortisman profilini seçin.</span><span class="sxs-lookup"><span data-stu-id="5b14c-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="5b14c-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b14c-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5b14c-118">Olağandışı durumlarda bir kıymetin ek amortismanı için Olağandışı amortisman profili kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5b14c-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="5b14c-119">Örneğin bunu doğal felaketlerden kaynaklanan amortismanı kaydetmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b14c-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="5b14c-120">Temel düzeltmeler bulunan amortisman düzeltmeleri oluştur onay kutusunu işaretleyin veya kutunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5b14c-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="5b14c-121">Takvim alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="5b14c-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="5b14c-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b14c-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="5b14c-123">Amortisman defterini bir sabit kıymet grubuyla ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="5b14c-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="5b14c-124">Sabit kıymet grupları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b14c-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="5b14c-125">Sabit kıymet grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="5b14c-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="5b14c-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5b14c-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="5b14c-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b14c-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="5b14c-128">Amortisman yöntemi alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="5b14c-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="5b14c-129">Servis ömrü alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="5b14c-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="5b14c-130">Amortisman dönemleri alanı değerinin Servis ömrü ayarlandıktan sonra hesaplandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="5b14c-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

