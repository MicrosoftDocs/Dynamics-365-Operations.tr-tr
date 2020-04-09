---
title: Satınalma sözleşmesi oluşturma
description: Bu konu bir satın alma sözleşmesi oluşturma aşamasında size yol gösterir.
author: mkirknel
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81b0e33d8f721cfcfd437e34b42a909798a6514b
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147469"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="0b2db-103">Satınalma sözleşmesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b2db-103">Create a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b2db-104">Bu konu bir satın alma sözleşmesi oluşturma aşamasında size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b2db-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="0b2db-105">Bu genellikle bir satın alma yöneticisi tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="0b2db-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="0b2db-106">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b2db-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="0b2db-107">Başlamadan önce satınalma sözleşmesi sınıflandırmaları ayarlamış olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0b2db-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="0b2db-108">Bir anlaşma oluşturduğunuzda bunu bir satınalma siparişi oluşturmak için kullanabilirsiniz ve bu satınalma sözleşmesinin koşulları, başlığa ve sözleşme tarafından etkilenen tüm sipariş satırlarına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="0b2db-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="0b2db-109">Yeni bir satınalma sözleşmesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0b2db-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="0b2db-110">**Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Satınalma sözleşmeleri > Satınalma sözleşmeleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="0b2db-111">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b2db-111">Click **New**.</span></span>
3. <span data-ttu-id="0b2db-112">**Satıcı hesabı** alanında, açılan menüyü seçin ve istediğiniz kaydın satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="0b2db-113">**Satınalma sözleşmesi sınıflandırması** alanında, açılan menüyü seçin ve istediğiniz kaydın satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="0b2db-114">**Genel** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="0b2db-115">**Bitiş tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="0b2db-116">Bu bitiş tarihi tüm taahhüt satırları için varsayılan olacaktır ve her bir taahhüdün ne kadar süreceğini belirleyecektir.</span><span class="sxs-lookup"><span data-stu-id="0b2db-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="0b2db-117">**Belge başlığı** alanına satınalma sözleşmeniz için ad yazın.</span><span class="sxs-lookup"><span data-stu-id="0b2db-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="0b2db-118">**Varsayılan taahhüt** alanını **Ürün miktarı taahhüdü** olarak bırakın (veya bunun için ayarlanmamış ise buna çevirin).</span><span class="sxs-lookup"><span data-stu-id="0b2db-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it's not set to this).</span></span>  
    - <span data-ttu-id="0b2db-119">Varsayılan taahhüt değeri, sözleşme satırlarındaki seçeneklerinizi belirler.</span><span class="sxs-lookup"><span data-stu-id="0b2db-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="0b2db-120">Sözleşme satırlarını oluştururken yeni bir taahhüt türüne ihtiyaç duyarsanız, başlıktaki varsayılan taahhütü değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0b2db-120">If you need a new commitment type when you're creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="0b2db-121">4 tür taahhüt vardır. **Ürün miktarı taahhüdü**, belirli bir miktar ürün için. **Ürün değeri taahhüdü**, bir ürünün belirli bir para birimi tutarı için. **Ürün kategori değeri taahhüdü**: Bir tedarik kategorisindeki para birimi miktarı için, miktarın katalogda mevcut olan veya olmayan bir madde için. **Değer taahhüdü**, belirli bir para birimi miktarı için herhangi bir ürün veya herhangi bir tedarik kategorisi kullanılarak yerine getirilebilmek üzere.</span><span class="sxs-lookup"><span data-stu-id="0b2db-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="0b2db-122">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="0b2db-123">Taahhüt ekleyin</span><span class="sxs-lookup"><span data-stu-id="0b2db-123">Add a commitment</span></span>
1. <span data-ttu-id="0b2db-124">**Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-124">Select **Add line**.</span></span>
2. <span data-ttu-id="0b2db-125">**Madde numarası** alanında, açılır menüden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="0b2db-126">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="0b2db-127">Bu, satıcınızdan satın almak üzere anlaştığınız toplam miktarıdır.</span><span class="sxs-lookup"><span data-stu-id="0b2db-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="0b2db-128">**Birim fiyatı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="0b2db-129">**Satır ayrıntıları** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="0b2db-130">**Maksimum uygulanır** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0b2db-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="0b2db-131">**Maksimum uygulanır** seçeneği, taahhüdün kullanımını sınırlar.</span><span class="sxs-lookup"><span data-stu-id="0b2db-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="0b2db-132">Yalnızca satır için **Miktar** alanında belirttiğiniz miktar kadar satın alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b2db-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="0b2db-133">Başlık koşulları ekleyin</span><span class="sxs-lookup"><span data-stu-id="0b2db-133">Add header conditions</span></span>
1. <span data-ttu-id="0b2db-134">Eylem Bölmesinde, **Seçenekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="0b2db-135">**Görünümü değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-135">Select **Change view**.</span></span>
3. <span data-ttu-id="0b2db-136">**Başlık görünümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-136">Select **Header view**.</span></span>
4. <span data-ttu-id="0b2db-137">**Koşullar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="0b2db-138">**Ödeme yöntemi** alanında, açılır menüden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="0b2db-139">Satıcı hesabının ödeme koşulları burada varsayılan olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="0b2db-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="0b2db-140">**Teslimat şekli** alanında, açılır menüden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="0b2db-141">**Teslimat koşulları** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="0b2db-142">Sözleşmeyi onaylayın ve etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="0b2db-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="0b2db-143">Eylem Bölmesinde, **Satınalma sözleşmesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="0b2db-144">**Onay**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-144">Select **Confirmation**.</span></span> <span data-ttu-id="0b2db-145">**Anlaşmayı etkin olarak işaretle** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0b2db-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="0b2db-146">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-146">Select **OK**.</span></span>
4. <span data-ttu-id="0b2db-147">Eylem Bölmesinde, **Satınalma sözleşmesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="0b2db-148">**Satınalma sözleşmesi onayları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0b2db-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="0b2db-149">**Önizleme/yazdırma** seçeneği, bir belge yazdırmak veya satıcıya göndermek için bir satınalma anlaşması oluşturmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="0b2db-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="0b2db-150">Daha sonra anlaşmayı günceller veya yeniden onaylarsanız, her iki sürüm de burada gösterilir.</span><span class="sxs-lookup"><span data-stu-id="0b2db-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="0b2db-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0b2db-151">Close the page.</span></span>

