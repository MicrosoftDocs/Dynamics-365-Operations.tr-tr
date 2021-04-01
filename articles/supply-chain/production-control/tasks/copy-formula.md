---
title: Formül kopyalama
description: Bu yordam, varolan bir formülün, ancak küçük farklılıklar ile aynı maddeleri içeren bir formül oluşturma üzerinde odaklanır.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdeeb760ab6bb00cefc6b358e53996dd652e5bc6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255337"
---
# <a name="copy-a-formula"></a><span data-ttu-id="9756d-103">Formül kopyalama</span><span class="sxs-lookup"><span data-stu-id="9756d-103">Copy a formula</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9756d-104">Bu yordam, varolan bir formülün, ancak küçük farklılıklar ile aynı maddeleri içeren bir formül oluşturma üzerinde odaklanır.</span><span class="sxs-lookup"><span data-stu-id="9756d-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="9756d-105">Formül satırlarını oluşturmak için gereken malzemelerin çoğunu içeren varolan bir formülü kopyalamak için Kopyala işlevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9756d-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="9756d-106">Tek tek satırlara yeni sürümünde gerekli değişiklikleri daha sonra yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9756d-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="9756d-107">Kopyalama işlevini kullanarak, neredeyse aynı olan birden çok formül oluşturmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="9756d-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="9756d-108">Bu görevi oluşturmak için kullanılan demo verisi şirketi USP2'dir.</span><span class="sxs-lookup"><span data-stu-id="9756d-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="9756d-109">Formül oluşturma</span><span class="sxs-lookup"><span data-stu-id="9756d-109">Create a formula</span></span>
1. <span data-ttu-id="9756d-110">Ürün bilgi yönetimi > Ürün reçeteleri ve formülleri > Formüller seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="9756d-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="9756d-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9756d-111">Click New.</span></span>
3. <span data-ttu-id="9756d-112">Formül alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9756d-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="9756d-113">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9756d-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="9756d-114">Formül için anlamlı bir isim girin.</span><span class="sxs-lookup"><span data-stu-id="9756d-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="9756d-115">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9756d-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9756d-116">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9756d-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="9756d-117">Madde modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9756d-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="9756d-118">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9756d-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="9756d-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9756d-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="9756d-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9756d-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="9756d-121">Formül satırlarını kopyalayın</span><span class="sxs-lookup"><span data-stu-id="9756d-121">Copy formula lines</span></span>
1. <span data-ttu-id="9756d-122">Eylem Bölmesinde, Formül'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9756d-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="9756d-123">Kopyala'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9756d-123">Click Copy.</span></span>
3. <span data-ttu-id="9756d-124">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="9756d-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9756d-125">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9756d-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9756d-126">Formül sürümü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9756d-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9756d-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9756d-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="9756d-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9756d-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="9756d-129">Kopyalanan formül satırlarını ayarlayın</span><span class="sxs-lookup"><span data-stu-id="9756d-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="9756d-130">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="9756d-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="9756d-131">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9756d-131">Click Delete.</span></span>
3. <span data-ttu-id="9756d-132">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9756d-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="9756d-133">Formülü onayla</span><span class="sxs-lookup"><span data-stu-id="9756d-133">Approve formula</span></span>
1. <span data-ttu-id="9756d-134">Eylem Bölmesinde, Formül'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9756d-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="9756d-135">Formülü onayla’yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9756d-135">Click Approve formula.</span></span>
3. <span data-ttu-id="9756d-136">Onaylayan alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="9756d-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9756d-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9756d-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9756d-138">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9756d-138">Click Select.</span></span>
6. <span data-ttu-id="9756d-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9756d-139">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]