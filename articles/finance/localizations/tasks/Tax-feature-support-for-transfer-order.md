---
title: Transfer emirleri için vergi özelliği desteği
description: Bu konu, vergi hesaplama servisi kullanılarak transfer emirleri için yeni vergi özelliği desteğini açıklamaktadır.
author: kailiang
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 55597e4f0f40677e793b4c182e4b0ced01057751
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832573"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="765af-103">Transfer emirleri için vergi özelliği desteği</span><span class="sxs-lookup"><span data-stu-id="765af-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="765af-104">Bu konu, transfer emirlerinde vergi hesaplaması ve deftere nakil tümleştirmesi hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="765af-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="765af-105">Bu işlevsellik, stok transferleri için vergi hesaplamasını ayarlamanıza ve transfer emirlerine nakil yapmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="765af-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="765af-106">Avrupa Birliği (AB) katma değer vergisi (KDV) düzenlemeleri altında, stok transferleri topluluk içi tedarik ve topluluk içi alım olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="765af-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="765af-107">Bu işlevi yapılandırmak ve kullanmak için, üç ana adımı tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="765af-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="765af-108">**RCS'i ayarlama:** Regulatory Configuration Service, transfer emirlerinde vergi kodu belirleme için vergi özelliğini, vergi kodlarını ve vergi kodları uygulanabilirliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="765af-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="765af-109">**Finance'i ayarlama:** Microsoft Dynamics 365 Finance'te, **Transfer emrinde vergi** özelliğini açın, stok için vergi servis parametrelerini ayarlayın ve ana vergi parametrelerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="765af-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="765af-110">**Stok ayarlama:** Transfer emri hareketleri için stok yapılandırmasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="765af-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="765af-111">Vergi ve transfer emri işlemleri için RCS'yi ayarlama</span><span class="sxs-lookup"><span data-stu-id="765af-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="765af-112">Bir transfer emrine dahil olan vergiyi ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="765af-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="765af-113">Burada gösterilen örnekte, Transfer emri, Hollanda'dan Belçika'ya yapılır.</span><span class="sxs-lookup"><span data-stu-id="765af-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="765af-114">**Vergi özellikleri** sayfasında, **sürümler** sekmesinde, taslak özelliğinin sürümünü seçin ve sonra **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![Düzenle'yi seçme](../media/image1.png)

2. <span data-ttu-id="765af-116">**Vergi özelliklerini ayarlama** sayfasında, **Vergi kodları** sekmesinde, yeni vergi kodları oluşturmak için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="765af-117">Bu örnekte, üç vergi kodu oluşturulur: **NL-Exempt**, **BE-RC-21** ve **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="765af-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="765af-118">Bir transfer emri Hollanda'daki bir ambardan sevk edildiğinde, Hollanda KDV'den muaf vergi kodu (**NL-Exempt**) uygulanır.</span><span class="sxs-lookup"><span data-stu-id="765af-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="765af-119">**NL-Exempt** olarak oluşturun.</span><span class="sxs-lookup"><span data-stu-id="765af-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="765af-120">**Ekle**'yi seçin, **Vergi kodu** alanına **NL-Exempt** yazın.</span><span class="sxs-lookup"><span data-stu-id="765af-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="765af-121">**Vergi bileşeni** alanında **net tutara göre**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="765af-122">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-122">Select **Save**.</span></span>
        4. <span data-ttu-id="765af-123">**Ücret** sekmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="765af-124">**Genel** bölümünde **Muaf**'ı **Evet** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="765af-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![NL-Exempt vergi kodu](../media/image2.png)

    - <span data-ttu-id="765af-126">Belçika ambarında bir transfer emri alındığında, karşı ödeme mekanizması **BE-RC-21** ve **BE-RC+21** Vergi kodları kullanılarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="765af-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="765af-127">Vergi kodu **BE-RC-21**'i oluşturun.</span><span class="sxs-lookup"><span data-stu-id="765af-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="765af-128">**Ekle**'yi seçin, **Vergi kodu** alanına **BE-RC-21** yazın.</span><span class="sxs-lookup"><span data-stu-id="765af-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="765af-129">**Vergi bileşeni** alanında **net tutara göre**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="765af-130">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-130">Select **Save**.</span></span>
        4. <span data-ttu-id="765af-131">**Ücret** sekmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="765af-132">**Vergi oranı** alanına **-21** girin.</span><span class="sxs-lookup"><span data-stu-id="765af-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="765af-133">**Genel** bölümünde **Karşı Ödeme**'yi **Evet** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="765af-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="765af-134">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-134">Select **Save**.</span></span>

        ![Karşı ödeme için BE-RC-21 vergi kodu](../media/image3.png)
        
        <span data-ttu-id="765af-136">Vergi kodu **BE-RC+21**'i oluşturun.</span><span class="sxs-lookup"><span data-stu-id="765af-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="765af-137">**Ekle**'yi seçin, **Vergi kodu** alanına **BE-RC-21** yazın.</span><span class="sxs-lookup"><span data-stu-id="765af-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="765af-138">**Vergi bileşeni** alanında **net tutara göre**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="765af-139">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-139">Select **Save**.</span></span>
        4. <span data-ttu-id="765af-140">**Ücret** sekmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="765af-141">**Vergi oranı** alanına **21** girin.</span><span class="sxs-lookup"><span data-stu-id="765af-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="765af-142">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-142">Select **Save**.</span></span>

        ![Karşı ödeme için BE-RC+21 vergi kodu](../media/image4.png)

3. <span data-ttu-id="765af-144">Vergi kodlarının uygulanabilirliğini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="765af-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="765af-145">**Sütunları Yönet**'i seçin ve sonra uygulanabilirlik tablosunu oluşturmak için kullanılacak sütunları seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="765af-146">**İş süreci** ve **vergi yönleri** sütunlarını tabloya eklediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="765af-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="765af-147">Transfer emirlerinde vergi işlevi için her iki sütun da gereklidir.</span><span class="sxs-lookup"><span data-stu-id="765af-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="765af-148">Uygulanabilirlik kuralları ekleyin.</span><span class="sxs-lookup"><span data-stu-id="765af-148">Add applicability rules.</span></span> <span data-ttu-id="765af-149">**Vergi kodları**, **vergi grubu** ve **Madde vergi grubu** alanlarını boş bırakmayın.</span><span class="sxs-lookup"><span data-stu-id="765af-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="765af-150">Transfer emri sevkiyatı için yeni bir kural ekleyin.</span><span class="sxs-lookup"><span data-stu-id="765af-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="765af-151">**Uygulanabilirlik kuralları** sekmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="765af-152">**İş süreci** alanında, kuralı transfer emri için uygulanabilir hale getirmek üzere **Stok**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="765af-153">**Sevkiyatın yapıldığı ülke/bölge** alanına **NLD**'yi girin.</span><span class="sxs-lookup"><span data-stu-id="765af-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="765af-154">**Sevkiyatın varacağı ülke/bölge** alanına **BEL**'yi girin.</span><span class="sxs-lookup"><span data-stu-id="765af-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="765af-155">**Vergi yönü** alanında, kuralı transfer emri sevkiyatı için geçerli hale getirmek için **çıkış**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="765af-156">**Vergi kodları** alanında **NL-Exempt**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="765af-157">**Vergi grubu** alanına ve **Madde vergi grubu** kısmına, Finance sisteminizde tanımlanan ilgili satış vergisi grubunu ve madde satış vergisi grubunu girin.</span><span class="sxs-lookup"><span data-stu-id="765af-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="765af-158">Transfer emri girişi için başka bir kural ekleyin.</span><span class="sxs-lookup"><span data-stu-id="765af-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="765af-159">**Uygulanabilirlik kuralları** sekmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="765af-160">**İş süreci** alanında, kuralı transfer emri için uygulanabilir hale getirmek üzere **Stok**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="765af-161">**Sevkiyatın yapıldığı ülke/bölge** alanına **NLD**'yi girin.</span><span class="sxs-lookup"><span data-stu-id="765af-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="765af-162">**Sevkiyatın varacağı ülke/bölge** alanına **BEL**'yi girin.</span><span class="sxs-lookup"><span data-stu-id="765af-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="765af-163">**Vergi yönü** alanında, kuralı transfer emri girişi için geçerli hale getirmek için **Giriş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="765af-164">**Vergi kodları** alanında **BE-RC+21** ve **BE-RC-21**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="765af-165">**Vergi grubu** alanına ve **Madde vergi grubu** kısmına, Finance sisteminizde tanımlanan ilgili satış vergisi grubunu ve madde satış vergisi grubunu girin.</span><span class="sxs-lookup"><span data-stu-id="765af-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![Uygulanabilirlik kuralları](../media/image5.png)

4. <span data-ttu-id="765af-167">Yeni vergi özelliği sürümünü tamamlayın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="765af-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="765af-168">[![Yeni sürümün durumunu değiştirme](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="765af-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="765af-169">Transfer emri işlemleri için Finance'i ayarlama</span><span class="sxs-lookup"><span data-stu-id="765af-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="765af-170">Transfer emirleri için vergileri etkinleştirmek ve ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="765af-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="765af-171">Finance'te **Çalışma alanları** \> **Özellik yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="765af-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="765af-172">Listede, **transfer emrinde vergi** özelliğindeki vergiyi bulun ve seçin ve açmak için **şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="765af-173">**Transfer emrinde vergi** özelliği vergi servisine tamamıyla bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="765af-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="765af-174">Bu nedenle, yalnızca vergi Servisi yüklendikten sonra etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="765af-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![Transfer emrinde vergi özelliği](../media/image7.png)

3. <span data-ttu-id="765af-176">Vergi hizmetini etkinleştirin ve **Stok** iş sürecini seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="765af-177">Bu adımı, vergi servisinin ve transfer emirlerinde vergi işlevinin kullanılabilir olmasını istediğiniz her tüzel kişilik için tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="765af-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="765af-178">**Vergi** \> **Ayarlama** \> **Vergi yapılandırması** \> **Vergi servis ayarı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="765af-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="765af-179">**İş süreci** alanında **stok**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-179">In the **Business process** field, select **Inventory**.</span></span>

    ![İş süreci alanını ayarlama](../media/image8.png)

4. <span data-ttu-id="765af-181">Karşı ödeme mekanizmasının ayarlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="765af-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="765af-182">**Genel Kayıt defteri** \> **Ayarlama** \> **Parametreler**'e gidin ve **Karşı ödeme** sekmesinde **Karşı ödemeyi etkinleştir** seçeneğinin **Evet** olarak ayarlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="765af-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![Karşı ödeme seçeneğini etkinleştirme](../media/image9.png)

5. <span data-ttu-id="765af-184">İlgili vergi kodlarının, vergi gruplarının, madde vergi gruplarının ve KDV kayıt numaralarının vergi servis kılavuzuna göre Finance'te ayarlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="765af-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="765af-185">Bir geçiş transit hesabı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="765af-185">Set up an interim transit account.</span></span> <span data-ttu-id="765af-186">Bu adım yalnızca bir transfer emrine uygulanan vergi, vergi muafiyet veya karşı ödeme mekanizması için geçerli olmadığı durumlarda gereklidir.</span><span class="sxs-lookup"><span data-stu-id="765af-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="765af-187">**Vergi** \> **Ayarlama** \> **Satış vergisi** \> **Genel muhasebe deftere nakil grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="765af-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="765af-188">**Ara geçiş** alanında bir kayıt defteri hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![Bir geçiş transit hesabı seçme](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="765af-190">Transfer emri işlemleri için temel envanteri ayarlama</span><span class="sxs-lookup"><span data-stu-id="765af-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="765af-191">Transfer emri işlemlerini etkinleştirmek üzere temel envanteri ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="765af-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="765af-192">Farklı ülkelerde veya bölgelerde ambarlarınız için sevk çıkış yeri ve sevk gidiş yeri siteleri oluşturun ve her tesis için birincil adresi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="765af-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="765af-193">**Ambar yönetimi** \> **Kurulum** \> **Ambar** \> **Tesisler** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="765af-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="765af-194">Bir ambara daha sonra atayacağınız tesisi oluşturmak için **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="765af-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="765af-195">Oluşturmanız gereken tüm diğer tesisler için 2. adımı yineleyin.</span><span class="sxs-lookup"><span data-stu-id="765af-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="765af-196">Oluşturduğunuz sitelerden biri **geçiş** olarak adlandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="765af-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="765af-197">Bu yordamın sonraki adımlarında, bu tesisi transit ambarına atayacaksınız böylece vergi ile ilgili stok fişleri transfer emirleri için "sevk etme" ve "teslim alma" işlemlerine nakledilebilecek.</span><span class="sxs-lookup"><span data-stu-id="765af-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="765af-198">Transit tesisinin adresi vergi hesaplamasıyla ilgili değildir.</span><span class="sxs-lookup"><span data-stu-id="765af-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="765af-199">Bu nedenle boş bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="765af-199">Therefore, you can leave it blank.</span></span>

    ![Tesisleri ayarlama](../media/image11.png)

2. <span data-ttu-id="765af-201">Sevkiyat çıkış yeri, transit ve sevkiyat varış yeri ambarları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="765af-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="765af-202">Bir ambarda tutulan tüm adres bilgileri, vergi hesaplaması sırasında tesis adresini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="765af-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="765af-203">**Ambar yönetimi** \> **Ayarlama** \> **Ambar** \> **Ambarlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="765af-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="765af-204">Bir ambar oluşturmak için **Yeni**'yi seçin ve ilgili tesise atayın.</span><span class="sxs-lookup"><span data-stu-id="765af-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="765af-205">Gerektiğinde her tesis için bir ambar oluşturmak üzere 2. adımı yineleyin.</span><span class="sxs-lookup"><span data-stu-id="765af-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![Ambar ayarlama](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="765af-207">Sevkiyat çıkış yeri ambarı için, Transfer emri işlemleri için **transit ambarı** alanında bir transit ambarı seçilmelidir.</span><span class="sxs-lookup"><span data-stu-id="765af-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![Transit ambarı seçme](../media/image13.png)

3. <span data-ttu-id="765af-209">Transfer emri işlemleri için envanter deftere nakil yapılandırmasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="765af-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="765af-210">**Stok Yönetimi** \> **Ayarlama** \> **Deftere nakil** \> **Deftere nakil** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="765af-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="765af-211">**Stok** sekmesinde, bir kayıt defteri hesabının hem **stok sorunu** hem de **stok girişi** deftere nakli için ayarlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="765af-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![Stok sorunu ve stok girişi deftere naklini ayarlama](../media/image14.png)

    3. <span data-ttu-id="765af-213">Kayıt defteri hesabının, **birimler arası borç** deftere nakil için ayarlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="765af-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![Birimler arası borç deftere nakli ayarlama](../media/image15.png)

    4. <span data-ttu-id="765af-215">Kayıt defteri hesabının, **birimler arası alacak** deftere nakil için ayarlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="765af-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![Birimler arası alacak deftere nakli ayarlama](../media/image16.png)
