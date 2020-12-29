---
title: Amortisman defterleri ayarlama
description: Bu yordamda, yeni amortisman defteri oluşturma ve bunu sabit kıymet grubuyla ilişkilendirme süreci boyunca izlenecek yol.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03f915fa91e0eeff2f26ab9a60bbd5118317e853
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448886"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="be4fa-103">Amortisman defterleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="be4fa-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be4fa-104">Bu yordamda, yeni amortisman defteri oluşturma ve bunu sabit kıymet grubuyla ilişkilendirme süreci boyunca izlenecek yol.</span><span class="sxs-lookup"><span data-stu-id="be4fa-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="be4fa-105">Amortisman defteri oluşturun</span><span class="sxs-lookup"><span data-stu-id="be4fa-105">Create a depreciation book</span></span>
1. <span data-ttu-id="be4fa-106">Sabit kıymetler > Kurulum > Amortisman defterleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="be4fa-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="be4fa-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be4fa-107">Click New.</span></span>
3. <span data-ttu-id="be4fa-108">Amortisman defteri alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="be4fa-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="be4fa-109">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="be4fa-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="be4fa-110">Amortismanı hesapla onay kutusunu işaretleyin veya kutunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="be4fa-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="be4fa-111">Amortisman profili alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="be4fa-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="be4fa-112">Listede, istediğiniz amortisman profilini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="be4fa-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="be4fa-113">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be4fa-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="be4fa-114">Alternatif amortisman profili alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="be4fa-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="be4fa-115">Listede, istediğiniz amortisman profilini seçin.</span><span class="sxs-lookup"><span data-stu-id="be4fa-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="be4fa-116">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be4fa-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="be4fa-117">Olağandışı durumlarda bir kıymetin ek amortismanı için Olağandışı amortisman profili kullanılır.</span><span class="sxs-lookup"><span data-stu-id="be4fa-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="be4fa-118">Örneğin bunu doğal felaketlerden kaynaklanan amortismanı kaydetmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="be4fa-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="be4fa-119">Temel düzeltmeler bulunan amortisman düzeltmeleri oluştur onay kutusunu işaretleyin veya kutunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="be4fa-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="be4fa-120">Takvim alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="be4fa-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="be4fa-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be4fa-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="be4fa-122">Amortisman defterini bir sabit kıymet grubuyla ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="be4fa-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="be4fa-123">Sabit kıymet grupları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be4fa-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="be4fa-124">Sabit kıymet grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="be4fa-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="be4fa-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="be4fa-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="be4fa-126">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be4fa-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="be4fa-127">Amortisman yöntemi alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="be4fa-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="be4fa-128">Servis ömrü alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="be4fa-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="be4fa-129">Amortisman dönemleri alanı değerinin Servis ömrü ayarlandıktan sonra hesaplandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="be4fa-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

