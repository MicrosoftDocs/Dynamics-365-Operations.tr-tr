---
title: Formül kopyalama
description: Bu yordam, varolan bir formülün, ancak küçük farklılıklar ile aynı maddeleri içeren bir formül oluşturma üzerinde odaklanır.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd87ded3bcc20b94fae723424d9cc6b94049a1a5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "312451"
---
# <a name="copy-a-formula"></a><span data-ttu-id="01988-103">Formül kopyalama</span><span class="sxs-lookup"><span data-stu-id="01988-103">Copy a formula</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="01988-104">Bu yordam, varolan bir formülün, ancak küçük farklılıklar ile aynı maddeleri içeren bir formül oluşturma üzerinde odaklanır.</span><span class="sxs-lookup"><span data-stu-id="01988-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="01988-105">Formül satırlarını oluşturmak için gereken malzemelerin çoğunu içeren varolan bir formülü kopyalamak için Kopyala işlevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01988-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="01988-106">Tek tek satırlara yeni sürümünde gerekli değişiklikleri daha sonra yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01988-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="01988-107">Kopyalama işlevini kullanarak, neredeyse aynı olan birden çok formül oluşturmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="01988-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="01988-108">Bu görevi oluşturmak için kullanılan demo verisi şirketi USP2'dir.</span><span class="sxs-lookup"><span data-stu-id="01988-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="01988-109">Formül oluşturma</span><span class="sxs-lookup"><span data-stu-id="01988-109">Create a formula</span></span>
1. <span data-ttu-id="01988-110">Ürün bilgi yönetimi > Ürün reçeteleri ve formülleri > Formüller seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="01988-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="01988-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01988-111">Click New.</span></span>
3. <span data-ttu-id="01988-112">Formül alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="01988-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="01988-113">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="01988-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="01988-114">Formül için anlamlı bir isim girin.</span><span class="sxs-lookup"><span data-stu-id="01988-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="01988-115">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01988-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="01988-116">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01988-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="01988-117">Madde modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01988-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="01988-118">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="01988-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="01988-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01988-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="01988-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01988-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="01988-121">Formül satırlarını kopyalayın</span><span class="sxs-lookup"><span data-stu-id="01988-121">Copy formula lines</span></span>
1. <span data-ttu-id="01988-122">Eylem Bölmesinde, Formül'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01988-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="01988-123">Kopyala'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="01988-123">Click Copy.</span></span>
3. <span data-ttu-id="01988-124">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="01988-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="01988-125">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01988-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="01988-126">Formül sürümü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01988-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="01988-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01988-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="01988-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01988-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="01988-129">Kopyalanan formül satırlarını ayarlayın</span><span class="sxs-lookup"><span data-stu-id="01988-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="01988-130">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="01988-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="01988-131">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="01988-131">Click Delete.</span></span>
3. <span data-ttu-id="01988-132">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="01988-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="01988-133">Formülü onayla</span><span class="sxs-lookup"><span data-stu-id="01988-133">Approve formula</span></span>
1. <span data-ttu-id="01988-134">Eylem Bölmesinde, Formül'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01988-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="01988-135">Formülü onayla’yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="01988-135">Click Approve formula.</span></span>
3. <span data-ttu-id="01988-136">Onaylayan alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="01988-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="01988-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01988-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="01988-138">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01988-138">Click Select.</span></span>
6. <span data-ttu-id="01988-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01988-139">Click OK.</span></span>

