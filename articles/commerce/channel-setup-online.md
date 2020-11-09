---
title: Çevrimiçi kanal ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir çevrimiçi kanalın nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 07225d97af76ea665fa28362cc205c6e8dc4fdf4
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107242"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="6a2eb-103">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="6a2eb-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6a2eb-104">Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir çevrimiçi kanalın nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6a2eb-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="6a2eb-105">Overview</span></span>

<span data-ttu-id="6a2eb-106">Dynamics 365 Commerce birden fazla perakende kanalı destekler.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="6a2eb-107">Bu perakende kanalları çevrimiçi mağazaları, çağrı merkezlerini ve perakende mağazalarını (tuğla dibek mağazalar olarak da bilinir) içerir.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="6a2eb-108">Çevrimiçi mağazalar müşterilere perakendecinin perakende mağazalarının yanı sıra çevrimiçi mağazasından da ürün satın alma seçeneği verir.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="6a2eb-109">Commerce'te bir çevrimiçi mağaza oluşturmak için önce bir çevrimiçi kanal oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-109">To create an online store in Commerce, you must first create an online channel.</span></span> <span data-ttu-id="6a2eb-110">Yeni bir çevrimiçi kanal oluşturmadan önce [Kanal kurulumu önkoşullarını](channels-prerequisites.md) tamamladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

<span data-ttu-id="6a2eb-111">Yeni bir site oluşturabilmeniz için, Commerce'te en az bir çevrimiçi mağazanın oluşturulması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-111">Before you can create a new site, at least one online store must be created in Commerce.</span></span> <span data-ttu-id="6a2eb-112">Daha fazla bilgi için, bkz [e-ticaret sitesi oluşturma](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="6a2eb-112">For more information, see [Create an e-Commerce site](create-ecommerce-site.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="6a2eb-113">Yeni bir çevrimiçi kanal oluşturma ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6a2eb-113">Create and configure a new online channel</span></span>

<span data-ttu-id="6a2eb-114">Yeni bir çevrimiçi kanal oluşturmak ve yapılandırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-114">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="6a2eb-115">Gezinti bölmesinde **Modüller \> Kanallar \> Çevrimiçi Mağazalar** 'a gidin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-115">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="6a2eb-116">Eylem bölmesinde **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-116">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6a2eb-117">**Ad** alanına yeni kanal için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-117">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="6a2eb-118">**Tüzel kişilik** açılır listesinde, uygun tüzel kişiliği girin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-118">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="6a2eb-119">**Ambar** açılır listesinde, ilgili ambarı girin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-119">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="6a2eb-120">**Mağaza saati dilimi** alanında, ilgili saat dilimini seçin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-120">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="6a2eb-121">**Para birimi** alanında uygun para birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="6a2eb-122">**Varsayılan müşteri** alanında, geçerli bir varsayılan müşteri girin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="6a2eb-123">**Müşteri adres defteri** alanında, geçerli bir adres defteri girin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-123">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="6a2eb-124">**İşlevsellik profili** alanında, varsa bir işlevsellik profili seçin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="6a2eb-125">**E-posta bildirimi profili** alanında, geçerli bir e-posta bildirimi profili girin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="6a2eb-126">Eylem bölmesinde, **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6a2eb-127">Aşağıdaki resimde yeni bir çevrimiçi kanalın oluşturulması gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-127">The following image shows the creation of a new online channel.</span></span>

![Yeni çevrimiçi kanal](media/channel-setup-online-1.png)

<span data-ttu-id="6a2eb-129">Aşağıdaki resimde örnek bir çevrimiçi kanal gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-129">The following image shows an example online channel.</span></span>

![Örnek çevrimiçi kanal](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="6a2eb-131">Dilleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="6a2eb-131">Set up languages</span></span>

<span data-ttu-id="6a2eb-132">E-ticaret siteniz birden çok dili destekleyecekse **Diller** bölümünü genişletin ve gereken dilleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-132">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="6a2eb-133">Ödeme hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6a2eb-133">Set up payment account</span></span>

<span data-ttu-id="6a2eb-134">**Ödeme hesabı** bölümünün içinden, üçüncü taraf ödeme sağlayıcı ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-134">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="6a2eb-135">Adyen ödeme bağlayıcısı ayarlama hakkında bilgi için bkz. [Adyen için Dynamics 365 Ödeme Bağlayıcı](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="6a2eb-135">For information on setting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-setup"></a><span data-ttu-id="6a2eb-136">Ek kanal ayarları</span><span class="sxs-lookup"><span data-stu-id="6a2eb-136">Additional channel setup</span></span>

<span data-ttu-id="6a2eb-137">Çevrimiçi kanal kurulumu için gereken ek görevler ödeme yöntemleri, teslimat şekilleri ve karşılama grubu ataması ayarlamayı içerir.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-137">Additional tasks that are required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="6a2eb-138">Aşağıdaki resimde, **Ayarla** sekmesindeki **Teslimat şekilleri** , **Ödeme yöntemleri** ve **Karşılama grubu ataması** ayarlama seçenekleri gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-138">The following image shows **Modes of delivery** , **Payment methods** , and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Ek çevrimiçi kanal kurulumu eylemleri](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="6a2eb-140">Ödeme yöntemlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="6a2eb-140">Set up payment methods</span></span>

<span data-ttu-id="6a2eb-141">Ödeme yöntemlerini ayarlamak için, bu kanalda desteklenen her ödeme türü için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="6a2eb-142">Eylem bölmesinde, **Ayarla** sekmesini ve ardından **Ödeme yöntemleri** 'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="6a2eb-143">Eylem bölmesinde **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6a2eb-144">Gezinti bölmesinde, istediğiniz bir ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="6a2eb-145">**Genel** bölümünde bir **İşlem adı** belirtin ve istediğiniz diğer ayarları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="6a2eb-146">Ödeme türü için gereken ek ayarları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="6a2eb-147">Eylem bölmesinde, **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6a2eb-148">Aşağıdaki resimde bir nakit ödeme yöntemi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-148">The following image shows an example of a cash payment method.</span></span>

![Örnek ödeme yöntemleri](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="6a2eb-150">Teslimat şekillerini ayarla</span><span class="sxs-lookup"><span data-stu-id="6a2eb-150">Set up modes of delivery</span></span>

<span data-ttu-id="6a2eb-151">Yapılandırılan teslimat şekillerini, **Eylem bölmesindeki** **Ayarla** sekmesinden **Teslimat şekilleri** 'ni seçerek görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-151">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="6a2eb-152">Bir teslimat şekli eklemek veya değiştirmek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-152">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="6a2eb-153">Gezinti bölmesinde **Modüller \> Stok yönetimi \> Teslimat şekilleri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-153">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="6a2eb-154">Eylem bölmesinde, yeni bir teslimat şekli oluşturmak için **Yeni** 'yi seçin veya varolan bir şekli seçin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-154">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="6a2eb-155">**Perakende kanalları** bölümünde, kanalı eklemek için **Satır ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-155">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="6a2eb-156">Kanalları tek tek eklemek yerine kuruluş düğümleri kullanarak eklemek, kanal eklemeyi kolaylaştırabilir.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-156">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="6a2eb-157">Aşağıdaki resimde bir teslimat şekli örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-157">The following image shows an example of a mode of delivery.</span></span>

![Teslimat şekillerini ayarla](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="6a2eb-159">Karşılama grubu atamasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6a2eb-159">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="6a2eb-160">Bir karşılama grubu ataması ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-160">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="6a2eb-161">Eylem bölmesinde, **Ayarla** sekmesini ve ardından **Karşılama grubu ataması** 'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-161">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="6a2eb-162">Eylem bölmesinde **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-162">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6a2eb-163">**Karşılama grubu** açılır listesinde bir karşılama grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-163">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="6a2eb-164">**Açıklama** açılır listesinde bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-164">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="6a2eb-165">Eylem bölmesinde, **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-165">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6a2eb-166">Aşağıdaki resimde, bir karşılama grubu ataması kurulum örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-166">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Karşılama grubu atamasını ayarlama](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="6a2eb-168">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6a2eb-168">Additional resources</span></span>

[<span data-ttu-id="6a2eb-169">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="6a2eb-169">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="6a2eb-170">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="6a2eb-170">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="6a2eb-171">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6a2eb-171">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="6a2eb-172">Çağrı merkezi kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6a2eb-172">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="6a2eb-173">Adyen için Dynamics 365 Ödeme Bağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="6a2eb-173">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
