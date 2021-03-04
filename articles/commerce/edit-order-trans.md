---
title: Çevrimiçi siparişi ve zaman uyumsuz müşteri siparişi hareketlerini düzenleme ve denetleme
description: Bu konuda, Microsoft Dynamics 365 Commerce uygulamasında çevrimiçi siparişin ve zaman uyumsuz müşteri siparişi hareketlerinin nasıl düzenleneceği ve denetleneceği açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8fa6f7a71bae759e2b8feb3c5778200bb7bdbfe9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010163"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="eed4a-103">Çevrimiçi siparişi ve zaman uyumsuz müşteri siparişi hareketlerini düzenleme ve denetleme</span><span class="sxs-lookup"><span data-stu-id="eed4a-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eed4a-104">Bu konuda, Microsoft Dynamics 365 Commerce uygulamasında çevrimiçi siparişin ve zaman uyumsuz müşteri siparişi hareketlerinin nasıl düzenleneceği ve denetleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="eed4a-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="eed4a-105">Overview</span></span>

<span data-ttu-id="eed4a-106">Commerce 10.0.5 sürümünden 10.0.6 sürümüne geçiş sırasında peşin hareketleri (satışlar ve iadeler gibi) ve nakit yönetimi hareketlerini (kasa devri girişi ve ödeme kaldırma gibi) düzenlemek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="eed4a-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="eed4a-107">Commerce 10.0.7 sürümünde, çevrimiçi sipariş hareketlerini ve zaman uyumsuz müşteri siparişi hareketlerini düzenleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="eed4a-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="eed4a-108">Sipariş hareketlerini düzenleme ve denetleme</span><span class="sxs-lookup"><span data-stu-id="eed4a-108">Edit and audit order transactions</span></span>

<span data-ttu-id="eed4a-109">Commerce genel merkezinde sipariş hareketlerini düzenlemek ve denetlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="eed4a-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="eed4a-110">[Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview)'ni yükleyin.</span><span class="sxs-lookup"><span data-stu-id="eed4a-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="eed4a-111">**Perakende parametreleri** sayfasında, **Müşteri siparişleri** sekmesindeki **Sipariş** hızlı sekmesinde, **Sipariş eşitleme hataları için tutma kodu** için bir tutma kodu belirtin.</span><span class="sxs-lookup"><span data-stu-id="eed4a-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="eed4a-112">**Mağaza mali öğeleri** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="eed4a-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="eed4a-113">**Çevrimiçi sipariş eşitleme hataları** ve **Müşteri siparişi eşitleme hataları** kutucukları, perakende hareketi sayfasının önceden filtrelenmiş bir görünümünü sağlar.</span><span class="sxs-lookup"><span data-stu-id="eed4a-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="eed4a-114">Her biri, karşılık gelen sipariş türü için eşitlemenin başarısız olduğu hareket kayıtlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eed4a-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="eed4a-115">**Çevrimiçi sipariş eşitleme hataları** sayfasını veya **Müşteri siparişi eşitleme hataları** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="eed4a-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="eed4a-116">Eşitleme hatasının ayrıntılarını görüntülemek için bir kayıt seçin.</span><span class="sxs-lookup"><span data-stu-id="eed4a-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="eed4a-117">**Eşitleme durumu** hızlı sekmesinde aşağıdaki hata ayrıntıları sağlanır:</span><span class="sxs-lookup"><span data-stu-id="eed4a-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="eed4a-118">Beklemedeki sipariş durumu</span><span class="sxs-lookup"><span data-stu-id="eed4a-118">Pending order status</span></span>
    - <span data-ttu-id="eed4a-119">Sipariş hatası ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="eed4a-119">Order error details</span></span>
    - <span data-ttu-id="eed4a-120">Değiştirilme tarihi ve saati</span><span class="sxs-lookup"><span data-stu-id="eed4a-120">Modified date and time</span></span>
    - <span data-ttu-id="eed4a-121">Yeniden deneme sayısı</span><span class="sxs-lookup"><span data-stu-id="eed4a-121">Retry count</span></span>

1. <span data-ttu-id="eed4a-122">Hata ayrıntılarında kaydın düzeltilmesi gerektiği belirtiliyorsa **Office Eklentisi**'ni ve ardından **Seçili hareketi düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="eed4a-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="eed4a-123">Seçilen hareketin ayrıntılarını gösteren bir Excel dosyası açılır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="eed4a-124">Düzenlenmekte olan hareket bir çevrimiçi sipariş hareketiyse Excel dosyası aşağıdaki çalışma sayfalarını içerir:</span><span class="sxs-lookup"><span data-stu-id="eed4a-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="eed4a-125">**Hareket**: Bu çalışma sayfasında harekete ilişkin başlık ayrıntıları yer alır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="eed4a-126">**Satış hareketi**: Bu çalışma sayfasında harekete ilişkin satır ayrıntıları yer alır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="eed4a-127">**Ödeme hareketleri**: Bu çalışma sayfasında harekete ilişkin ödeme satırlarının ayrıntıları yer alır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="eed4a-128">**İskonto hareketleri**: Bu çalışma sayfasında harekete ilişkin iskontoyla ilgili ayrıntılar yer alır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="eed4a-129">**Vergi hareketleri**: Bu çalışma sayfasında harekete ilişkin vergiyle ilgili ayrıntılar yer alır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="eed4a-130">**Masraf hareketleri**: Bu çalışma sayfasında harekete ilişkin masraflarla ilgili veriler yer alır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="eed4a-131">Düzenlenmekte olan hareket bir zaman uyumsuz müşteri siparişi hareketiyse Excel dosyası aşağıdaki çalışma sayfalarını içerir:</span><span class="sxs-lookup"><span data-stu-id="eed4a-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="eed4a-132">**Satırlar**: Bu çalışma sayfasında hareket için başlık ve satır ayrıntıları yer alır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="eed4a-133">**Ödemeler**: Bu çalışma sayfasında harekete ilişkin ödeme satırlarının ayrıntıları yer alır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="eed4a-134">**İskontolar**: Bu çalışma sayfasında harekete ilişkin iskontoyla ilgili ayrıntılar yer alır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="eed4a-135">**Vergiler**: Bu çalışma sayfasında harekete ilişkin vergiyle ilgili ayrıntılar yer alır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="eed4a-136">**Masraflar**: Bu çalışma sayfasında harekete ilişkin masraflarla ilgili veriler yer alır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="eed4a-137">Excel dosyasında, **Beklemedeki sipariş durumu** alanına **Düzenleme** yazın ve ardından değişikliği yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="eed4a-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="eed4a-138">Bu şekilde, toplu iş modunda çalışan **Siparişi eşitle** işinin işlem sırasında bu kaydı atlamasını engellersiniz.</span><span class="sxs-lookup"><span data-stu-id="eed4a-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="eed4a-139">Excel dosyasında, uygun alanları değiştirin ve ardından Dynamics Excel Eklentisi'nin yayımlama işlevini kullanarak verileri Commerce genel merkezine geri yükleyin.</span><span class="sxs-lookup"><span data-stu-id="eed4a-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="eed4a-140">Veriler yayımlandıktan sonra değişiklikler sisteme yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="eed4a-141">Yayımlama sırasında, kullanıcıların yaptığı değişiklikler için doğrulama yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="eed4a-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="eed4a-142">Başlık düzeyindeki değişiklikler için **Perakende hareketi** başlığındaki **Denetim kaydını görüntüle**'yi seçip uygun hareket sayfasındaki ilgili bölümü veya kaydı seçerek değişikliklerle ilgili eksiksiz bir denetim kaydı görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eed4a-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="eed4a-143">Örneğin, satış satırlarıyla ilgili tüm değişiklikler **Satış hareketleri** sayfasında ve ödemelerle ilgili tüm değişiklikler de **Ödeme hareketleri** sayfasında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="eed4a-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="eed4a-144">Değişiklikler için aşağıdaki denetim ayrıntıları korunur:</span><span class="sxs-lookup"><span data-stu-id="eed4a-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="eed4a-145">Değiştirilme tarihi ve saati</span><span class="sxs-lookup"><span data-stu-id="eed4a-145">Modified date and time</span></span>
    - <span data-ttu-id="eed4a-146">Alan</span><span class="sxs-lookup"><span data-stu-id="eed4a-146">Field</span></span>
    - <span data-ttu-id="eed4a-147">Eski değer</span><span class="sxs-lookup"><span data-stu-id="eed4a-147">Old value</span></span>
    - <span data-ttu-id="eed4a-148">Yeni değer</span><span class="sxs-lookup"><span data-stu-id="eed4a-148">New value</span></span>
    - <span data-ttu-id="eed4a-149">Değiştiren</span><span class="sxs-lookup"><span data-stu-id="eed4a-149">Modified by</span></span>

1. <span data-ttu-id="eed4a-150">Değişikliklerinizi yapıp yayımladıktan sonra eşitleme sürecini hemen başlatmak için **Siparişi eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="eed4a-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="eed4a-151">Alternatif olarak, toplu işlem modunda çalışan eşitleme işleminin hareketi işlemesini bekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eed4a-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="eed4a-152">Varsayılan olarak, siparişler başarıyla eşitlendikten sonra Commerce parametrelerinde tanımlanan tutma koduna göre bir tutma durumuna alınır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="eed4a-153">Siparişlerin karşılanması veya diğer işlemler için daha fazla işlenebilmesi için siparişler üzerindeki tutma kaldırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="eed4a-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eed4a-154">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="eed4a-154">Additional resources</span></span>

[<span data-ttu-id="eed4a-155">Peşin ve nakit yönetimi hareketlerini düzenleme ve denetleme</span><span class="sxs-lookup"><span data-stu-id="eed4a-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="eed4a-156">Perakende hareketlerinin mali boyutlarını düzenleme</span><span class="sxs-lookup"><span data-stu-id="eed4a-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="eed4a-157">Perakende hareketlerini düzenlemek için bir Excel çalışma kitabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="eed4a-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="eed4a-158">Perakende hareketlerini düzenlemek için Excel çalışma kitabına alanlar ekleme</span><span class="sxs-lookup"><span data-stu-id="eed4a-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
