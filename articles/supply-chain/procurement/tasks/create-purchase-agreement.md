--- 
title: "Satınalma sözleşmesi oluşturma"
description: "Bu yordam bir satın alma sözleşmesi oluşturma aşamasında size yol gösterir."
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c547f825c567848b06b84ac1baaa5ae3bc6c2860
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="049f5-103">Satınalma sözleşmesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="049f5-103">Create a purchase agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="049f5-104">Bu yordam bir satın alma sözleşmesi oluşturma aşamasında size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="049f5-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="049f5-105">Bu genellikle bir satın alma yöneticisi tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="049f5-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="049f5-106">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="049f5-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="049f5-107">Başlamadan önce satınalma sözleşmesi sınıflandırmaları ayarlamış olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="049f5-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="049f5-108">Bir anlaşma oluşturduğunuzda bunu bir satınalma siparişi oluşturmak için kullanabilirsiniz ve bu satınalma sözleşmesinin koşulları, başlığa ve sözleşme tarafından etkilenen tüm sipariş satırlarına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="049f5-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="049f5-109">Yeni bir satınalma sözleşmesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="049f5-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="049f5-110">Tedarik ve kaynak Hizmeti > Satın alma anlaşmaları > Satın alma anlaşmaları seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="049f5-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="049f5-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-111">Click New.</span></span>
3. <span data-ttu-id="049f5-112">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="049f5-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="049f5-113">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="049f5-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="049f5-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="049f5-115">Satın alma sözleşmeleri sınıflandırması alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="049f5-116">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="049f5-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="049f5-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="049f5-118">Genel bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="049f5-118">Expand the General section.</span></span>
10. <span data-ttu-id="049f5-119">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="049f5-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="049f5-120">Bu bitiş tarihi tüm taahhüt satırları için varsayılan olacaktır ve her bir taahhüdün ne kadar süreceğini belirleyecektir.</span><span class="sxs-lookup"><span data-stu-id="049f5-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="049f5-121">Belge başlığı alanına satınalma sözleşmeniz için ad yazın.</span><span class="sxs-lookup"><span data-stu-id="049f5-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="049f5-122">Varsayılan taahhüt alanını Ürün miktarı taahhüdü olarak bırakın (veya bunun için ayarlanmamış ise buna çevirin).</span><span class="sxs-lookup"><span data-stu-id="049f5-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="049f5-123">Varsayılan taahhüt değeri, sözleşme satırlarındaki seçeneklerinizi belirler.</span><span class="sxs-lookup"><span data-stu-id="049f5-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="049f5-124">Sözleşme satırlarını oluştururken yeni bir taahhüt türüne ihtiyaç duyarsanız, başlıktaki varsayılan taahhütü değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="049f5-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="049f5-125">4 tür taahhüt vardır. Ürün miktarı taahhüdü, belirli bir miktar ürün için. Ürün değeri taahhüdü, bir ürünün belirli bir para birimi tutarı için. Ürün kategori değeri taahhüdü: Bir tedarik kategorisindeki para birimi miktarı için, miktarın katalogda mevcut olan veya olmayan bir madde için. Değer taahhüdü, belirli bir para birimi miktarı için herhangi bir ürün veya herhangi bir tedarik kategorisi kullanılarak yerine getirilebilmek üzere.</span><span class="sxs-lookup"><span data-stu-id="049f5-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="049f5-126">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="049f5-127">Taahhüt ekleyin</span><span class="sxs-lookup"><span data-stu-id="049f5-127">Add a commitment</span></span>
1. <span data-ttu-id="049f5-128">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-128">Click Add line.</span></span>
2. <span data-ttu-id="049f5-129">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="049f5-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="049f5-130">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="049f5-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="049f5-131">Bir taahhüt eklemek istediğiniz ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="049f5-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="049f5-132">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="049f5-133">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="049f5-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="049f5-134">Bu, satıcınızdan satın almak üzere anlaştığınız toplam miktarıdır.</span><span class="sxs-lookup"><span data-stu-id="049f5-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="049f5-135">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="049f5-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="049f5-136">Satır ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="049f5-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="049f5-137">Maksimum uygulanır seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="049f5-138">Maksimum zorlanan seçeneği, taahhüdün kullanımını sınırlar.</span><span class="sxs-lookup"><span data-stu-id="049f5-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="049f5-139">Yalnızca satır için miktar alanında belirttiğiniz miktar kadar satın alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="049f5-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="049f5-140">Satır ayrıntıları bölümü daraltın.</span><span class="sxs-lookup"><span data-stu-id="049f5-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="049f5-141">Başlık koşulları ekleyin</span><span class="sxs-lookup"><span data-stu-id="049f5-141">Add header conditions</span></span>
1. <span data-ttu-id="049f5-142">Eylem Bölmesinde, Seçenekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="049f5-143">Görünümü değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-143">Click Change view.</span></span>
3. <span data-ttu-id="049f5-144">Başlık görünümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-144">Click Header view.</span></span>
4. <span data-ttu-id="049f5-145">Koşullar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="049f5-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="049f5-146">Ödeme yöntemi alanında açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="049f5-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="049f5-147">Satıcı hesabının ödeme koşulları burada varsayılan olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="049f5-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="049f5-148">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="049f5-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="049f5-149">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="049f5-150">Teslimat şekli alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="049f5-151">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="049f5-152">Teslimat koşulları alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="049f5-153">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="049f5-154">Sözleşmeyi onaylayın ve etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="049f5-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="049f5-155">Eylem Bölmesinde, Satınalma sözleşmesi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="049f5-156">Onay'a tıklayın</span><span class="sxs-lookup"><span data-stu-id="049f5-156">Click Confirmation.</span></span>
    * <span data-ttu-id="049f5-157">Anlaşmayı etkin olarak işaretle seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="049f5-158">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="049f5-158">Click OK.</span></span>
4. <span data-ttu-id="049f5-159">Eylem Bölmesinde, Satınalma sözleşmesi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="049f5-160">Satınalma sözleşmesi onayları'nı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049f5-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="049f5-161">Önizleme/yazdırma seçeneği, bir belge yazdırmak veya satıcıya göndermek için bir satınalma anlaşması oluşturmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="049f5-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="049f5-162">Daha sonra anlaşmayı günceller veya yeniden onaylarsanız, her iki sürüm de burada gösterilir.</span><span class="sxs-lookup"><span data-stu-id="049f5-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="049f5-163">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="049f5-163">Close the page.</span></span>


