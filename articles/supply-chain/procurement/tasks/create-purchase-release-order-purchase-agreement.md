---
title: Satınalma sözleşmesinden satınalma sevk emri oluşturma
description: Bu yordam, bir satınalma siparişi oluşturduğunuzda bir satın alma sözleşmesini kullanmayı gösterir.
author: RichardLuan
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c095eaf1a93d6f1a803c6c9618c930fb2eda2d2
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021076"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a><span data-ttu-id="b46cf-103">Satınalma sözleşmesinden satınalma sevk emri oluşturma</span><span class="sxs-lookup"><span data-stu-id="b46cf-103">Create a purchase release order from a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b46cf-104">Bu yordam, bir satınalma siparişi oluşturduğunuzda bir satın alma sözleşmesini kullanmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="b46cf-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="b46cf-105">Satınalma siparişi başlığına kopyalanacak genel terimler olduğundan, satınalma siparişi oluşturduğunuzda satın alma sözleşmesinin uygulanması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b46cf-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="b46cf-106">Genellikle bu görev bir satınalma aracısı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b46cf-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="b46cf-107">Bu kılavuz için bir önkoşul olarak bir satıcı ve öğeler için bir ürün miktarı taahüdüne sahip etkili satınalma anlaşmanızın olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b46cf-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="b46cf-108">Aynı yordam, diğer tür taahhütleri içeren bir satın alma sözleşmeniz varsa da kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b46cf-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="b46cf-109">Bu kılavuzu USMF demo şirketinde çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b46cf-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="b46cf-110">USMF kullanıyorsanız, bu kılavuzu ayarlamak için gerekli önkoşulları sağlamak için "satın alma sözleşmesi oluştur" kılavuzunu çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b46cf-110">If you're using USMF, you can run the "Create a purchase agreement" guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="b46cf-111">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b46cf-111">Create a purchase order</span></span>
1. <span data-ttu-id="b46cf-112">**Gezinti bölmesi**'nde, **Çalışma alanları > Satınalma siparişi hazırlığı**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b46cf-112">In the **Navigation pane**, go to **Workspaces > Purchase order preparation**.</span></span> 
2. <span data-ttu-id="b46cf-113">**Yeni satınalma siparişi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-113">Click **New purchase order**.</span></span>
3. <span data-ttu-id="b46cf-114">**Satıcı hesabı** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-114">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b46cf-115">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b46cf-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b46cf-116">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b46cf-117">**Genel** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="b46cf-117">Expand the **General** fastTab.</span></span>
7. <span data-ttu-id="b46cf-118">**Satınalma sözleşmesi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-118">In the **Purchase agreement** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="b46cf-119">Satıcı için kullanılabilir tüm sözleşmeler burada listelenir.</span><span class="sxs-lookup"><span data-stu-id="b46cf-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="b46cf-120">Kullanmak istediğiniz etkin sözleşmeyi bulun.</span><span class="sxs-lookup"><span data-stu-id="b46cf-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="b46cf-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b46cf-122">**Evet** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-122">Click **Yes**.</span></span>
10. <span data-ttu-id="b46cf-123">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-123">Click **OK**.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="b46cf-124">Bir satır ekleyin</span><span class="sxs-lookup"><span data-stu-id="b46cf-124">Add a line</span></span>
1. <span data-ttu-id="b46cf-125">**Madde numarası** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b46cf-125">In the **Item number** field, type a value.</span></span> <span data-ttu-id="b46cf-126">Taahhüt üzerinde belirli stok ve konum boyutları mevcutsa, sözleşmeden faydalanabilmeniz için satınalma siparişi satırında aynı değeri girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b46cf-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="b46cf-127">**Site** alanında, aramayı açmak için aşağı açılır düğmeyi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-127">In the **Site** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="b46cf-128">Siparişte veya satıcıda varsayılan olarak bulunan değer halihazırda tesis için girilmiş olabilir.</span><span class="sxs-lookup"><span data-stu-id="b46cf-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="b46cf-129">Bu durumda, bu adımı atlayın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="b46cf-130">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b46cf-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="b46cf-131">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b46cf-132">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="b46cf-132">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="b46cf-133">Fiyatın taahhütten kopyalandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="b46cf-134">Taahhüdü bulun</span><span class="sxs-lookup"><span data-stu-id="b46cf-134">Look up the commitment</span></span>
1. <span data-ttu-id="b46cf-135">**Satırı güncelleştir** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-135">Click **Update line**.</span></span>
2. <span data-ttu-id="b46cf-136">**İlişik** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-136">Click **Attached**.</span></span> <span data-ttu-id="b46cf-137">Burada satın alma sözleşmesinin ayrıntılarını alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b46cf-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="b46cf-138">Örneğin, fiyatı ve fiyatın ve iskontonun sabit olup olmadığını görebilirsiniz, bu da satınalma siparişi üzerindeki fiyatınızı ya da iskontonuzu taahhüdün üzerinde bulunandan değiştirirseniz, sistemin bağlantıyı kaldırarak satınalma siparişi satırının taahhüdü yerine getirmesinin önüne geçer.</span><span class="sxs-lookup"><span data-stu-id="b46cf-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="b46cf-139">Ayrıca, taahhüdün üzerindeki miktarın, taahhüdü yerine getiren tüm siparişlerin toplamını geçemeyeceği anlamına gelen, Maksimum uygulanır kuralının seçili olup olmadığını da görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="b46cf-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="b46cf-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="b46cf-141">Satınalma sözleşmesi'ni bulun</span><span class="sxs-lookup"><span data-stu-id="b46cf-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="b46cf-142">**Eylem Bölmesi**'nde, **Genel** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-142">On the **Action Pane**, click **General**.</span></span>
2. <span data-ttu-id="b46cf-143">**Satınalma sözleşmesi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-143">Click **Purchase agreement**.</span></span>
3. <span data-ttu-id="b46cf-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-144">Close the page.</span></span>
4. <span data-ttu-id="b46cf-145">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b46cf-145">Close the page.</span></span>

