---
title: Satış siparişi durumu sütunları için eşlemeyi ayarlama
description: Bu konu, çift yazma için satış siparişi durumu sütunlarının nasıl ayarlanacağını açıklar.
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 9afa64df73aa17e7a15a0ee4f4529ac74bcd3c67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750726"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="436a5-103">Satış siparişi durumu sütunları için eşlemeyi ayarlama</span><span class="sxs-lookup"><span data-stu-id="436a5-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="436a5-104">Satış siparişi durumunu gösteren sütunlar, Microsoft Dynamics 365 Supply Chain Management ve Dynamics 365 Sales uygulamalarında farklı sabit numaralandırma değerlerine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="436a5-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="436a5-105">Bu sütunları çift-yazılır olarak eşlemek için ek kurulum gerekir.</span><span class="sxs-lookup"><span data-stu-id="436a5-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="436a5-106">Supply Chain Management'ta sütunlar</span><span class="sxs-lookup"><span data-stu-id="436a5-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="436a5-107">Supply Chain Management'ta, iki sütun satış siparişinin durumunu yansıtır.</span><span class="sxs-lookup"><span data-stu-id="436a5-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="436a5-108">Eşlemeniz gereken sütunlar **Durum** ve **Belge Durumu** sütunlarıdır.</span><span class="sxs-lookup"><span data-stu-id="436a5-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="436a5-109">**Durum** numaralandırma alanı siparişin genel durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="436a5-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="436a5-110">Bu durum sipariş başlığında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="436a5-110">This status is shown on the order header.</span></span>

<span data-ttu-id="436a5-111">**Durum** numaralandırma alanında aşağıdaki değerler bulunur:</span><span class="sxs-lookup"><span data-stu-id="436a5-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="436a5-112">Açık Sipariş</span><span class="sxs-lookup"><span data-stu-id="436a5-112">Open Order</span></span>
- <span data-ttu-id="436a5-113">Teslim edildi</span><span class="sxs-lookup"><span data-stu-id="436a5-113">Delivered</span></span>
- <span data-ttu-id="436a5-114">Faturalanan</span><span class="sxs-lookup"><span data-stu-id="436a5-114">Invoiced</span></span>
- <span data-ttu-id="436a5-115">İptal edildi</span><span class="sxs-lookup"><span data-stu-id="436a5-115">Cancelled</span></span>

<span data-ttu-id="436a5-116">**Belge Durumu** numaralandırma alanı sipariş için oluşturulan en son belgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="436a5-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="436a5-117">Örneğin, sipariş onaylandığında bu belge bir satış siparişi onayıdır.</span><span class="sxs-lookup"><span data-stu-id="436a5-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="436a5-118">Bir satış siparişi kısmen faturalanmışsa ve kalan satır onaylandıysa, belge durumu **Fatura** olarak kalır, çünkü fatura bu işlem içinde daha sonra oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="436a5-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="436a5-119">**Belge Durumu** numaralandırma alanında aşağıdaki değerler bulunur:</span><span class="sxs-lookup"><span data-stu-id="436a5-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="436a5-120">Onay</span><span class="sxs-lookup"><span data-stu-id="436a5-120">Confirmation</span></span>
- <span data-ttu-id="436a5-121">Malzeme Çekme Listesi</span><span class="sxs-lookup"><span data-stu-id="436a5-121">Picking List</span></span>
- <span data-ttu-id="436a5-122">Sevk İrsaliyesi</span><span class="sxs-lookup"><span data-stu-id="436a5-122">Packing Slip</span></span>
- <span data-ttu-id="436a5-123">Fatura</span><span class="sxs-lookup"><span data-stu-id="436a5-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="436a5-124">Sales'da sütunlar</span><span class="sxs-lookup"><span data-stu-id="436a5-124">columns in Sales</span></span>

<span data-ttu-id="436a5-125">Sales'da, iki sütun siparişin durumunu yansıtır.</span><span class="sxs-lookup"><span data-stu-id="436a5-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="436a5-126">Eşlemeniz gereken sütunlar **Durum** ve **İşleme Durumu** sütunlarıdır.</span><span class="sxs-lookup"><span data-stu-id="436a5-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="436a5-127">**Durum** numaralandırma alanı siparişin genel durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="436a5-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="436a5-128">Aşağıdaki değerlere sahiptir:</span><span class="sxs-lookup"><span data-stu-id="436a5-128">It has the following values:</span></span>

- <span data-ttu-id="436a5-129">Active</span><span class="sxs-lookup"><span data-stu-id="436a5-129">Active</span></span>
- <span data-ttu-id="436a5-130">Gönderildi</span><span class="sxs-lookup"><span data-stu-id="436a5-130">Submitted</span></span>
- <span data-ttu-id="436a5-131">Yerine getirildi</span><span class="sxs-lookup"><span data-stu-id="436a5-131">Fulfilled</span></span>
- <span data-ttu-id="436a5-132">Faturalanan</span><span class="sxs-lookup"><span data-stu-id="436a5-132">Invoiced</span></span>
- <span data-ttu-id="436a5-133">İptal edildi</span><span class="sxs-lookup"><span data-stu-id="436a5-133">Cancelled</span></span>

<span data-ttu-id="436a5-134">**İşlem Durumu** numaralandırma alanı, Supply Chain Management ile daha doğru şekilde eşleştirilebilecek şekilde kullanılmaya başlandı.</span><span class="sxs-lookup"><span data-stu-id="436a5-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="436a5-135">Aşağıdaki tablo, Supply Chain Management uygulamasında **İşleme Durumu** alanlarının eşlemesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="436a5-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="436a5-136">İşlem Durumu</span><span class="sxs-lookup"><span data-stu-id="436a5-136">Processing Status</span></span>   | <span data-ttu-id="436a5-137">Supply Chain Management'ta durum</span><span class="sxs-lookup"><span data-stu-id="436a5-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="436a5-138">Supply Chain Management'ta Belge Durumu</span><span class="sxs-lookup"><span data-stu-id="436a5-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="436a5-139">Active</span><span class="sxs-lookup"><span data-stu-id="436a5-139">Active</span></span>              | <span data-ttu-id="436a5-140">Açık Sipariş</span><span class="sxs-lookup"><span data-stu-id="436a5-140">Open Order</span></span>                        | <span data-ttu-id="436a5-141">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="436a5-141">None</span></span>                                       |
| <span data-ttu-id="436a5-142">Onaylı</span><span class="sxs-lookup"><span data-stu-id="436a5-142">Confirmed</span></span>           | <span data-ttu-id="436a5-143">Açık Sipariş</span><span class="sxs-lookup"><span data-stu-id="436a5-143">Open Order</span></span>                        | <span data-ttu-id="436a5-144">Onay</span><span class="sxs-lookup"><span data-stu-id="436a5-144">Confirmation</span></span>                               |
| <span data-ttu-id="436a5-145">Çekildi</span><span class="sxs-lookup"><span data-stu-id="436a5-145">Picked</span></span>              | <span data-ttu-id="436a5-146">Açık Sipariş</span><span class="sxs-lookup"><span data-stu-id="436a5-146">Open Order</span></span>                        | <span data-ttu-id="436a5-147">Malzeme Çekme Listesi</span><span class="sxs-lookup"><span data-stu-id="436a5-147">Picking List</span></span>                               |
| <span data-ttu-id="436a5-148">Kısmen Teslim Edildi</span><span class="sxs-lookup"><span data-stu-id="436a5-148">Partially Delivered</span></span> | <span data-ttu-id="436a5-149">Açık Sipariş</span><span class="sxs-lookup"><span data-stu-id="436a5-149">Open Order</span></span>                        | <span data-ttu-id="436a5-150">Sevk İrsaliyesi</span><span class="sxs-lookup"><span data-stu-id="436a5-150">Packing Slip</span></span>                               |
| <span data-ttu-id="436a5-151">Teslim edildi</span><span class="sxs-lookup"><span data-stu-id="436a5-151">Delivered</span></span>           | <span data-ttu-id="436a5-152">Teslim edildi</span><span class="sxs-lookup"><span data-stu-id="436a5-152">Delivered</span></span>                         | <span data-ttu-id="436a5-153">Sevk İrsaliyesi</span><span class="sxs-lookup"><span data-stu-id="436a5-153">Packing Slip</span></span>                               |
| <span data-ttu-id="436a5-154">Kısmen Faturalandı</span><span class="sxs-lookup"><span data-stu-id="436a5-154">Partially Invoiced</span></span>  | <span data-ttu-id="436a5-155">Teslim edildi</span><span class="sxs-lookup"><span data-stu-id="436a5-155">Delivered</span></span>                         | <span data-ttu-id="436a5-156">Fatura</span><span class="sxs-lookup"><span data-stu-id="436a5-156">Invoice</span></span>                                    |
| <span data-ttu-id="436a5-157">Faturalanan</span><span class="sxs-lookup"><span data-stu-id="436a5-157">Invoiced</span></span>            | <span data-ttu-id="436a5-158">Faturalanan</span><span class="sxs-lookup"><span data-stu-id="436a5-158">Invoiced</span></span>                          | <span data-ttu-id="436a5-159">Fatura</span><span class="sxs-lookup"><span data-stu-id="436a5-159">Invoice</span></span>                                    |
| <span data-ttu-id="436a5-160">İptal edildi</span><span class="sxs-lookup"><span data-stu-id="436a5-160">Cancelled</span></span>           | <span data-ttu-id="436a5-161">İptal edildi</span><span class="sxs-lookup"><span data-stu-id="436a5-161">Cancelled</span></span>                         | <span data-ttu-id="436a5-162">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="436a5-162">Not applicable</span></span>                             |

<span data-ttu-id="436a5-163">Aşağıdaki tablo, Sales ile Supply Chain Management uygulamaları arasında **İşleme Durumu** alanlarının eşlemesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="436a5-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="436a5-164">İşlem Durumu</span><span class="sxs-lookup"><span data-stu-id="436a5-164">Processing Status</span></span>   | <span data-ttu-id="436a5-165">Sales'ta Durum</span><span class="sxs-lookup"><span data-stu-id="436a5-165">Status in Sales</span></span> | <span data-ttu-id="436a5-166">Supply Chain Management'ta durum</span><span class="sxs-lookup"><span data-stu-id="436a5-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="436a5-167">Active</span><span class="sxs-lookup"><span data-stu-id="436a5-167">Active</span></span>              | <span data-ttu-id="436a5-168">Active</span><span class="sxs-lookup"><span data-stu-id="436a5-168">Active</span></span>          | <span data-ttu-id="436a5-169">Açık Sipariş</span><span class="sxs-lookup"><span data-stu-id="436a5-169">Open Order</span></span>                        |
| <span data-ttu-id="436a5-170">Onaylı</span><span class="sxs-lookup"><span data-stu-id="436a5-170">Confirmed</span></span>           | <span data-ttu-id="436a5-171">Gönderildi</span><span class="sxs-lookup"><span data-stu-id="436a5-171">Submitted</span></span>       | <span data-ttu-id="436a5-172">Açık Sipariş</span><span class="sxs-lookup"><span data-stu-id="436a5-172">Open Order</span></span>                        |
| <span data-ttu-id="436a5-173">Çekildi</span><span class="sxs-lookup"><span data-stu-id="436a5-173">Picked</span></span>              | <span data-ttu-id="436a5-174">Gönderildi</span><span class="sxs-lookup"><span data-stu-id="436a5-174">Submitted</span></span>       | <span data-ttu-id="436a5-175">Açık Sipariş</span><span class="sxs-lookup"><span data-stu-id="436a5-175">Open Order</span></span>                        |
| <span data-ttu-id="436a5-176">Kısmen Teslim Edildi</span><span class="sxs-lookup"><span data-stu-id="436a5-176">Partially Delivered</span></span> | <span data-ttu-id="436a5-177">Active</span><span class="sxs-lookup"><span data-stu-id="436a5-177">Active</span></span>          | <span data-ttu-id="436a5-178">Açık Sipariş</span><span class="sxs-lookup"><span data-stu-id="436a5-178">Open Order</span></span>                        |
| <span data-ttu-id="436a5-179">Kısmen Faturalandı</span><span class="sxs-lookup"><span data-stu-id="436a5-179">Partially Invoiced</span></span>  | <span data-ttu-id="436a5-180">Active</span><span class="sxs-lookup"><span data-stu-id="436a5-180">Active</span></span>          | <span data-ttu-id="436a5-181">Açık Sipariş</span><span class="sxs-lookup"><span data-stu-id="436a5-181">Open Order</span></span>                        |
| <span data-ttu-id="436a5-182">Kısmen Faturalandı</span><span class="sxs-lookup"><span data-stu-id="436a5-182">Partially Invoiced</span></span>  | <span data-ttu-id="436a5-183">Yerine getirildi</span><span class="sxs-lookup"><span data-stu-id="436a5-183">Fulfilled</span></span>       | <span data-ttu-id="436a5-184">Teslim edildi</span><span class="sxs-lookup"><span data-stu-id="436a5-184">Delivered</span></span>                         |
| <span data-ttu-id="436a5-185">Faturalanan</span><span class="sxs-lookup"><span data-stu-id="436a5-185">Invoiced</span></span>            | <span data-ttu-id="436a5-186">Faturalanan</span><span class="sxs-lookup"><span data-stu-id="436a5-186">Invoiced</span></span>        | <span data-ttu-id="436a5-187">Faturalanan</span><span class="sxs-lookup"><span data-stu-id="436a5-187">Invoiced</span></span>                          |
| <span data-ttu-id="436a5-188">İptal edildi</span><span class="sxs-lookup"><span data-stu-id="436a5-188">Cancelled</span></span>           | <span data-ttu-id="436a5-189">İptal edildi</span><span class="sxs-lookup"><span data-stu-id="436a5-189">Cancelled</span></span>       | <span data-ttu-id="436a5-190">İptal edildi</span><span class="sxs-lookup"><span data-stu-id="436a5-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="436a5-191">Ayar</span><span class="sxs-lookup"><span data-stu-id="436a5-191">Setup</span></span>

<span data-ttu-id="436a5-192">Satış siparişi durumu sütunlarıyla ilgili eşlemeyi ayarlamak için **IsSOPIntegrationEnabled** ve **isIntegrationUser** özniteliklerini etkinleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="436a5-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="436a5-193">**IsSOPIntegrationEnabled** özniteliğini etkinleştirmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="436a5-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="436a5-194">Web tarayıcısında `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations` adresine gidin.</span><span class="sxs-lookup"><span data-stu-id="436a5-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="436a5-195">**\<test-name\>** değerini şirketinizin Sales bağlantısı ile değiştirin.</span><span class="sxs-lookup"><span data-stu-id="436a5-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="436a5-196">Açılan sayfada, **organizationId** değerini bulun ve değeri not alın.</span><span class="sxs-lookup"><span data-stu-id="436a5-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![organizationId bulma](media/sales-map-orgid.png)

3. <span data-ttu-id="436a5-198">Sales'ta, tarayıcı konsolunu açın ve aşağıdaki kodu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="436a5-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="436a5-199">2. adımdaki **organizationId** değerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="436a5-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![Tarayıcı konsolundaki JavaScript kodu](media/sales-map-script.png)

4. <span data-ttu-id="436a5-201">**IsSOPIntegrationEnabled** değerinin **TRUE** olarak ayarlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="436a5-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="436a5-202">Değeri kontrol etmek için 1. adımdaki URL'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="436a5-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled değerinin TRUE olarak ayarlanmış](media/sales-map-integration-enabled.png)

<span data-ttu-id="436a5-204">**isIntegrationUser** özniteliğini etkinleştirmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="436a5-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="436a5-205">Sales'da, **Ayarlar \> Özelleştirme \> Sistemi Özelleştirme** sayfasına gidin, **Kullanıcı tablosu** ögesini seçin ve sonra **Form \> Kullanıcısı** ögesini açın.</span><span class="sxs-lookup"><span data-stu-id="436a5-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![Kullanıcı formunu açma](media/sales-map-user.png)

2. <span data-ttu-id="436a5-207">Alan Gezgini'nde, **Tümleştirme kullanıcısı modunu** bulun ve forma eklemek için çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="436a5-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="436a5-208">Değişikliğinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="436a5-208">Save your change.</span></span>

    ![Tümleştirme kullanıcısı modu sütununu forma ekleme](media/sales-map-field-explorer.png)

3. <span data-ttu-id="436a5-210">Sales'ta, **Ayarlar \> Güvenlik \> Kullanıcılar** sayfasına gidin ve görünümü **Etkin Kullanıcılar** ayarından **Uygulama kullanıcıları** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="436a5-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Görünümü Etkin Kullanıcılardan Uygulama Kullanıcıları olarak değiştirme](media/sales-map-enabled-users.png)

4. <span data-ttu-id="436a5-212">**DualWrite IntegrationUser** için iki giriş seçin.</span><span class="sxs-lookup"><span data-stu-id="436a5-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Uygulama kullanıcıları listesi](media/sales-map-user-mode.png)

5. <span data-ttu-id="436a5-214">**Tümleştirme kullanıcısı modu** sütununun değerini **Evet** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="436a5-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![Tümleştirme kullanıcısı modu sütununun değerini Evet olarak değiştirme](media/sales-map-user-mode-yes.png)

<span data-ttu-id="436a5-216">Satış siparişleriniz artık eşlendi.</span><span class="sxs-lookup"><span data-stu-id="436a5-216">Your sales orders are now mapped.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]