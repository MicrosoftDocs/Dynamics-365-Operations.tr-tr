---
title: Satınalma sözleşmesinden satınalma sevk emri oluşturma
description: Bu yordam, bir satınalma siparişi oluşturduğunuzda bir satın alma sözleşmesini kullanmayı gösterir.
author: mkirknel
manager: AnnBe
ms.date: 12/04/2015
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c45db4ac01be831c0c75f888d313d61d934fc33f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "328896"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a><span data-ttu-id="e60c8-103">Satınalma sözleşmesinden satınalma sevk emri oluşturma</span><span class="sxs-lookup"><span data-stu-id="e60c8-103">Create a purchase release order from a purchase agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e60c8-104">Bu yordam, bir satınalma siparişi oluşturduğunuzda bir satın alma sözleşmesini kullanmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="e60c8-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="e60c8-105">Satınalma siparişi başlığına kopyalanacak genel terimler olduğundan, satınalma siparişi oluşturduğunuzda satın alma sözleşmesinin uygulanması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e60c8-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="e60c8-106">Genellikle bu görev bir satınalma aracısı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e60c8-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="e60c8-107">Bu kılavuz için bir önkoşul olarak bir satıcı ve öğeler için bir ürün miktarı taahüdüne sahip etkili satınalma anlaşmanızın olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e60c8-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="e60c8-108">Aynı yordam, diğer tür taahhütleri içeren bir satın alma sözleşmeniz varsa da kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e60c8-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="e60c8-109">Bu kılavuzu USMF demo şirketinde çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e60c8-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="e60c8-110">USMF kullanıyorsanız, bu kılavuzu ayarlamak için gerekli önkoşulları sağlamak için "satın alma sözleşmesi oluştur" kılavuzunu çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e60c8-110">If you’re using USMF, you can run the “Create a purchase agreement” guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="e60c8-111">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e60c8-111">Create a purchase order</span></span>
1. <span data-ttu-id="e60c8-112">Satınalma siparişi hazırlama çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-112">Open the purchase order preparation workspace.</span></span>
2. <span data-ttu-id="e60c8-113">Yeni satınalma siparişi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-113">Click New purchase order.</span></span>
3. <span data-ttu-id="e60c8-114">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e60c8-115">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e60c8-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e60c8-116">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e60c8-117">Genel bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="e60c8-117">Toggle the expansion of the General section.</span></span>
7. <span data-ttu-id="e60c8-118">Satınalma sözleşmesi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-118">In the Purchase agreement field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e60c8-119">Satıcı için kullanılabilir tüm sözleşmeler burada listelenir.</span><span class="sxs-lookup"><span data-stu-id="e60c8-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="e60c8-120">Kullanmak istediğiniz etkin sözleşmeyi bulun.</span><span class="sxs-lookup"><span data-stu-id="e60c8-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="e60c8-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e60c8-122">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-122">Click Yes.</span></span>
10. <span data-ttu-id="e60c8-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-123">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="e60c8-124">Bir satır ekleyin</span><span class="sxs-lookup"><span data-stu-id="e60c8-124">Add a line</span></span>
1. <span data-ttu-id="e60c8-125">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e60c8-125">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="e60c8-126">Taahhüt üzerinde belirli stok ve konum boyutları mevcutsa, sözleşmeden faydalanabilmeniz için satınalma siparişi satırında aynı değeri girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e60c8-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="e60c8-127">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-127">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e60c8-128">Siparişte veya satıcıda varsayılan olarak bulunan değer halihazırda tesis için girilmiş olabilir.</span><span class="sxs-lookup"><span data-stu-id="e60c8-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="e60c8-129">Bu durumda, bu adımı atlayın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="e60c8-130">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e60c8-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="e60c8-131">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e60c8-132">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e60c8-132">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="e60c8-133">Fiyatın taahhütten kopyalandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="e60c8-134">Taahhüdü bulun</span><span class="sxs-lookup"><span data-stu-id="e60c8-134">Look up the commitment</span></span>
1. <span data-ttu-id="e60c8-135">Satırı güncelleştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-135">Click Update line.</span></span>
2. <span data-ttu-id="e60c8-136">İlişik öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-136">Click Attached.</span></span>
    * <span data-ttu-id="e60c8-137">Burada satın alma sözleşmesinin ayrıntılarını alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e60c8-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="e60c8-138">Örneğin, fiyatı ve fiyatın ve iskontonun sabit olup olmadığını görebilirsiniz, bu da satınalma siparişi üzerindeki fiyatınızı ya da iskontonuzu taahhüdün üzerinde bulunandan değiştirirseniz, sistemin bağlantıyı kaldırarak satınalma siparişi satırının taahhüdü yerine getirmesinin önüne geçer.</span><span class="sxs-lookup"><span data-stu-id="e60c8-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="e60c8-139">Ayrıca, taahhüdün üzerindeki miktarın, taahhüdü yerine getiren tüm siparişlerin toplamını geçemeyeceği anlamına gelen, Maksimum uygulanır kuralının seçili olup olmadığını da görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="e60c8-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="e60c8-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="e60c8-141">Satınalma sözleşmesi'ni bulun</span><span class="sxs-lookup"><span data-stu-id="e60c8-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="e60c8-142">Eylem Bölmesinde, Genel öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-142">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="e60c8-143">Satınalma sözleşmesi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-143">Click Purchase agreement.</span></span>
3. <span data-ttu-id="e60c8-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-144">Close the page.</span></span>
4. <span data-ttu-id="e60c8-145">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e60c8-145">Close the page.</span></span>

